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
# <a name="searching-binary-data"></a>Поиск двоичных данных

Хотя функция поиска в ADSI поддерживает только поиск строковых данных, можно выполнять поиск двоичных данных. Для этого используйте функцию [**адсенкодебинаридата**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) для преобразования двоичных данных в строку, которую можно использовать с методами поиска. Поиск двоичных данных особенно полезен при поиске идентификатора GUID или идентификатора безопасности, поскольку эти типы данных хранятся в виде двоичных данных.

При использовании функции [**адсенкодебинаридата**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) выделенная память должна быть освобождена с помощью функции [**фриадсмем**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .

В следующем примере кода C++ показано, как создать строку запроса для поиска объекта с определенным значением **objectGUID** .


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



 

 




