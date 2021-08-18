---
title: Метод WSMan. SessionFlagUTF8 (Всмандисп. h)
description: Возвращает значение флага проверки подлинности WSManFlagUTF8 для использования в параметре Flags WSMan. CreateSession.
ms.assetid: a79e292a-364b-4bf3-ae66-6a15ad51524f
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода SessionFlagUTF8
- служба удаленного управления Windows метода SessionFlagUTF8, объект WSMan
- объект WSMan служба удаленного управления Windows, метод SessionFlagUTF8
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUTF8
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44fe6cc1b5f18fa316656d2b6974bd47c8209277ed24ef2798479227f9876e30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741922"
---
# <a name="wsmansessionflagutf8-method"></a>Метод WSMan. SessionFlagUTF8

Метод **WSMan. SessionFlagUTF8** возвращает значение флага проверки подлинности **WSManFlagUTF8** для использования в параметре *flags* [**WSMan. CreateSession**](wsman-createsession.md). Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение. Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).

**WSManFlagUTF8** — это константа в перечислении **\_ \_ всмансессионфлагс** . Дополнительные сведения см. в разделе [другие константы сеанса](other-session-constants.md).

## <a name="syntax"></a>Синтаксис


```VB
WSMan.SessionFlagUTF8( _
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
| Заголовок<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ведущий**](wsman.md)
</dt> <dt>

[**Сеанс**](session.md)
</dt> </dl>

 

 





