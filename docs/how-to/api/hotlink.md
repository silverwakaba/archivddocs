---
sidebar_position: 1
---

# Hotlink

Hotlink is an activity where a user can enjoy the download process of files stored by ArchivD without visiting the download page on ArchivD's website. This process is also known as the bypass process.

Just like other file hosting sites, ArchivD also prohibits this kind of practice. The reason is because this practice is very detrimental to ArchivD who does not get traffic from this practice, but still has to pay storage and bandwidth costs.

However, even so, we feel that this hotlink process is needed by many people for various reasons. For example, to automate the download process from files stored on our end, which you can directly display on your site.

Therefore, we offer the best solution that allows you to still be able to hotlink on the ArchivD site legally. This hotlink process will later be carried out via paid API.

## Paid API

Like web services in general, the data exchange process can be done via our paid API service. That way the process can be carried out at any time and automatically, based on the user's needs.

Likewise with the hotlink process for ArchivD, you can and are permitted to do this as long as you meet the applicable requirements, which include:

- To start hotlinking you need a datacap.
- Datacap can be purchased according to your needs.
- Datacap is rollover and will not expire.
  - This means you can use all the remaining datacaps you buy without having to rush to spend them all.
  - Hotlink can also still be used even after your premium has expired.
- To hotlink you must have sufficient remaining datacap compared to the file.
  - Eg. To hotlink a file with a size of 1 GB, you must also have a datacap worth of 1 GB.
- The expiry time for hotlinked files is a maximum of 8 hours will be counted as one unit, but it can be extended up to 12 hours with an additional unit applied.
  - For an expiration period of 1 - 8 hours, a datacap of the size of the file will be used.
    - Eg. 1 GB hotlink will use a datacap of 1 GB.
  - For expiration periods of 9 hours and above, a datacap equal to the file size will be used, then multiplied by the additional expiration period as an additional unit.
    - Eg. 1 GB hotlink for expiration periods of 9 hours will use a datacap of 2 GB (1 unit from 1 - 8 hours period (1 GB) + 1 unit from extra 1 hours period (1 GB)).
    - Eg. 1 GB hotlink for expiration periods of 10 hours will use a datacap of 3 GB (1 unit from 1 - 8 hours period (1 GB) + 2 unit from extra 2 hours period (2 GB)).
    - Eg. 1 GB hotlink for expiration periods of 11 hours will use a datacap of 4 GB (1 unit from 1 - 8 hours period (1 GB) + 3 unit from extra 3 hours period (3 GB)).
    - Eg. 1 GB hotlink for expiration periods of 12 hours will use a datacap of 5 GB (1 unit from 1 - 8 hours  (1 GB)period + 4 unit from extra 4 hours period (4 GB)).
- Datacap is calculated based on API calls, which means if you save/cache the results of an API call and then reuse it again, you will not be charged.
  - This means that even if you don't download but only make an API call, your data cap will still be deducted.
- In order to maintain privacy, only files uploaded to your account can be hotlinked.

Other provisions can be added, changed or reduced at a later date.

### Getting Started

To be able to start using hotlink API, there are several parameters needed, namely API Key, file id and expiration time.

To get the API Key you must first have an account. If you don't have an account, please [register first](https://www.archivd.net/register). It's free.

After that, please please navigate to the [API Key menu](https://www.archivd.net/app/setting/apikey) to create a new API Key, which will later function as request authorization.

To create an API Key you just click the **"Create New"** button. After that, you will get a notification that the API Key was successfully created. Please note that currently one user can only create one API Key.

GAMBAR

After creating an API Key, you can also update it by clicking the **"Renew"** button. Later, the previous API Key will no longer be able to be used.

Or if you want to completely delete your API Key, you can click the **"Revoke"** button.

### Making a Request

Every hotlink API request can be made via the endpoint below:

```js title="Hotlink API Endpoint"
GET https://www.archivd.net/api/public/hotlink/v1
```

The available parameters include:

- API Key
- File ID
- Expiration Time

This means that if in an example my API Key is `07f300b5-7746-4d16-a464-88c0aa813be6`, the File ID that I want to hotlink is `01hase96940tgbjaeqxved504y` with an expiration date of `8 hours`, then the endpoint will be:

```js title="Hotlink API Endpoint with an Example"
GET https://www.archivd.net/api/public/hotlink/v1?fileid=01hase96940tgbjaeqxved504y&apikey=07f300b5-7746-4d16-a464-88c0aa813be6&expiration=8
```

From the API request above the results may vary. However, if the request is successful, the response will be similar to this.

```js title="An Example of Successful Hotlink API Request"
{
    "data": {
        "code": "200",
        "id": "01hase96940tgbjaeqxved504y",
        "name": "ArchivDummy.z01",
        "size": 524288000,
        "expiration": "8",
        // highlight-start
        "link": {
            "network": "Centralized EU",
            "originURL": null,
            "firstMirrorURLName": "BunnyCDN",
            "firstMirrorURL": "https://archivd-eu.static.silverspoon.me/01hase96940tgbjaeqxved504y/files?response-content-type=application%2Foctet-stream&response-content-disposition=attachment%3B%20filename%3DArchivDummy.z01&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=0037ab08f2835d60000000001%2F20230926%2Feu-central-003%2Fs3%2Faws4_request&X-Amz-Date=20230926T125607Z&X-Amz-SignedHeaders=host&X-Amz-Expires=0&X-Amz-Signature=2c04d29eb5ed4e3ccff478019252c8ef3a135e9fd00a4386ec7c2e15f58d8a04",
            "secondMirrorURLName": "Fastly",
            "secondMirrorURL": "https://archivd-eu.global.ssl.fastly.net/01hase96940tgbjaeqxved504y/files?response-content-type=application%2Foctet-stream&response-content-disposition=attachment%3B%20filename%3DArchivDummy.z01&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=0037ab08f2835d60000000001%2F20230926%2Feu-central-003%2Fs3%2Faws4_request&X-Amz-Date=20230926T125607Z&X-Amz-SignedHeaders=host&X-Amz-Expires=0&X-Amz-Signature=2c04d29eb5ed4e3ccff478019252c8ef3a135e9fd00a4386ec7c2e15f58d8a04"
        }
        // highlight-end
    }
}
```

I say similar because the link that appears may have a different format depending on the storage network. You can [read about storage networks](/docs/about/network-type) on the documentation page.