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
ms.openlocfilehash: 9f77ead11f4e2d02c6e7ef3e25975a7059c2c057dbc62f71e406bbda3e24c3b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005424"
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



 

 




