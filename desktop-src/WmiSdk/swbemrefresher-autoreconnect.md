---
description: Свойство Аутореконнект объекта Свбемрефрешер является логическим значением, указывающим, будет ли Обновитель автоматически повторно подключаться к удаленному поставщику, если соединение разорвано.
ms.assetid: 3be24128-8a35-44b0-befd-8b8937eff1b7
ms.tgt_platform: multiple
title: Свойство Свбемрефрешер. Аутореконнект (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AutoReconnect
- ISWbemRefresher.AutoReconnect
- ISWbemRefresher.get_AutoReconnect
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b1ad11c4362276d5714e54ef3196b246a40de1e26bf8f311f41fb5b5834bab0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312816"
---
# <a name="swbemrefresherautoreconnect-property"></a>Свбемрефрешер. Аутореконнект, свойство

Свойство **аутореконнект** объекта [**свбемрефрешер**](swbemrefresher.md) является логическим значением, указывающим, будет ли Обновитель автоматически повторно подключаться к удаленному поставщику, если соединение разорвано.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
SWbemRefresher.AutoReconnect As Boolean
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Remarks

Изменение этого свойства влияет только на объекты в обновитель, которые поддерживаются высокопроизводительным поставщиком. Если поставщик не является высокопроизводительным, установка свойства **аутореконнект** в **значение true** не оказывает никакого влияния, так как объект [**свбемрефрешер**](swbemrefresher.md) никогда не будет повторно подключаться.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМРЕФРЕШЕР CLSID<br/>                                                        |
| IID<br/>                      | IID \_ исвбемрефрешер<br/>                                                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**свбемрефрешер**](swbemrefresher.md)
</dt> </dl>

 

 




