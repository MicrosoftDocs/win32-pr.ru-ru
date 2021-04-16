---
description: Метод Жетрекуестид возвращает значение глобального уникального идентификатора (GUID) для запроса. GUID — это уникальное 128-разрядное число.
ms.assetid: c8df15cf-ab48-491f-ac18-1dad567bbc0b
ms.tgt_platform: multiple
title: 'Метод Ивбемкаусалитякцесс:: Жетрекуестид (Вбеминт. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.GetRequestId
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 075be627b26d99a8b4f03c5a4a962b41f153c8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683890"
---
# <a name="iwbemcausalityaccessgetrequestid-method"></a>Метод Ивбемкаусалитякцесс:: Жетрекуестид

Метод **жетрекуестид** возвращает значение глобального уникального идентификатора (GUID) для запроса. GUID — это уникальное 128-разрядное число.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetRequestId(
  [out] REQUESTID *pId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*идентификатор процесса* \[ заполняет\]
</dt> <dd>

Значение идентификатора GUID, уникально идентифицирующего запрос. Например, 5b2fc63a-8AF4-44cb-960c-aefdced908d6.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Вбеминт. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивбемкаусалитякцесс**](iwbemcausalityaccess.md)
</dt> </dl>

 

 




