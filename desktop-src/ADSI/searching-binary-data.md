---
title: Поиск двоичных данных
description: Хотя функция поиска в ADSI поддерживает только поиск строковых данных, можно выполнять поиск двоичных данных.
ms.assetid: 52b75ae0-dbf1-4310-8b6b-a176de9f1b7d
ms.tgt_platform: multiple
keywords:
- Поиск в ADSI двоичных данных
- Двоичные данные ADSI
- Двоичные данные ADSI, поиск в двоичных данных
- ADSI ADSI, пример кода C/C++, Поиск двоичных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0973ff7a769d68abf85e6557fef2e1d434ba3ff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067317"
---
# <a name="searching-binary-data"></a><span data-ttu-id="3d963-107">Поиск двоичных данных</span><span class="sxs-lookup"><span data-stu-id="3d963-107">Searching Binary Data</span></span>

<span data-ttu-id="3d963-108">Хотя функция поиска в ADSI поддерживает только поиск строковых данных, можно выполнять поиск двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="3d963-108">Even though the ADSI search feature only supports searching for string data, it is possible to search for binary data.</span></span> <span data-ttu-id="3d963-109">Для этого используйте функцию [**адсенкодебинаридата**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) для преобразования двоичных данных в строку, которую можно использовать с методами поиска.</span><span class="sxs-lookup"><span data-stu-id="3d963-109">To do this, use the [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) function to convert the binary data into a string that can be used with the search methods.</span></span> <span data-ttu-id="3d963-110">Поиск двоичных данных особенно полезен при поиске идентификатора GUID или идентификатора безопасности, поскольку эти типы данных хранятся в виде двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="3d963-110">Searching for binary data is particularly useful when searching for a GUID or a SID because these data types are stored as binary data.</span></span>

<span data-ttu-id="3d963-111">При использовании функции [**адсенкодебинаридата**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) выделенная память должна быть освобождена с помощью функции [**фриадсмем**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .</span><span class="sxs-lookup"><span data-stu-id="3d963-111">When using the [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) function, the memory allocated must be freed using the [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) function.</span></span>

<span data-ttu-id="3d963-112">В следующем примере кода C++ показано, как создать строку запроса для поиска объекта с определенным значением **objectGUID** .</span><span class="sxs-lookup"><span data-stu-id="3d963-112">The following C++ code example shows how to build a query string to search for an object that has a particular **objectGUID** value.</span></span>


```C++
LPWSTR pwszGuid = NULL;
LPWSTR pwszFormat = L"(objectGUID=%s)";
LPWSTR pwszSearch = NULL;
hr = ADsEncodeBinaryData((LPBYTE)pguid, sizeof(GUID), &pwszGuid);
if(FAILED(hr))
{
    goto cleanup;
}

pwszSearch = new WCHAR[lstrlenW(pwszFormat) + lstrlenW(pwszGuid) + 1];
if(NULL == pwszSearch)
{
    goto cleanup;
}
    
swprintf_s(pwszSearch, pwszFormat, pwszGuid);

// Use pwszSearch to perform a query for the object.

cleanup:    
if(pwszGuid)
{
    FreeADsMem(pwszGuid);
}
if(pwszSearch)
{
    delete pwszSearch;
}

```



 

 




