---
title: Метод WSMan. Сессионфлагусенеготиате (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлагусенеготиате для использования в параметре flags метода WSMan. CreateSession.
ms.assetid: 86d8ed13-5eae-4a06-8ceb-b0ec067f4a4c
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода сессионфлагусенеготиате
- служба удаленного управления Windows метода сессионфлагусенеготиате, объект WSMan
- объект WSMan служба удаленного управления Windows, метод сессионфлагусенеготиате
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseNegotiate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d7a6af51cad3a1e0ea5c78aee92e9650af16d6b0d699d28a7d9d48cb51d0784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823276"
---
# <a name="wsmansessionflagusenegotiate-method"></a>Метод WSMan. Сессионфлагусенеготиате

Метод **WSMan. сессионфлагусенеготиате** возвращает значение флага проверки подлинности **всманфлагусенеготиате** для использования в параметре *flags* метода [**WSMan. CreateSession**](wsman-createsession.md) . Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение. Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).

**Всманфлагусенеготиате** — это константа в перечислении **\_ \_ всмансессионфлагс** . Дополнительные сведения см. в разделе [константы проверки подлинности](authentication-constants.md).

## <a name="syntax"></a>Синтаксис


```VB
WSMan.SessionFlagUseNegotiate( _
  ByRef flags _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* \[ заполняет\]
</dt> <dd>

Значение константы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ведущий**](wsman.md)
</dt> <dt>

[**Сеанс**](session.md)
</dt> </dl>

 

 





