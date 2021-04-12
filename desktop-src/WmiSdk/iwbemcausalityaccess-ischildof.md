---
description: Метод Исчилдоф определяет, является ли запрос дочерним по отношению к указанному запросу (pId).
ms.assetid: 7be52496-7dcf-41c0-853a-859810a57d21
ms.tgt_platform: multiple
title: 'Метод Ивбемкаусалитякцесс:: Исчилдоф (Вбеминт. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.IsChildOf
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 6deec7521ceb58a76db3dbf8064ccc444019cb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265598"
---
# <a name="iwbemcausalityaccessischildof-method"></a>Метод Ивбемкаусалитякцесс:: Исчилдоф

Метод **исчилдоф** определяет, является ли запрос дочерним по отношению к указанному запросу (pId). Родительский запрос может иметь несколько дочерних запросов. Каждый запрос определяется глобальным уникальным идентификатором (GUID) и может иметь родительский запрос или может быть запросом Top. GUID — это уникальное 128-разрядное число.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsChildOf(
  [in] REQUESTID pId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*идентификатор процесса* \[ окне\]
</dt> <dd>

Значение идентификатора GUID, уникально идентифицирующего запрос. Например, 5b2fc63a-8AF4-44cb-960c-aefdced908d6.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение "успешно", если указанный запрос является дочерним по отношению к запросу, вызывающему метод **исчилдоф** .

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

 

 




