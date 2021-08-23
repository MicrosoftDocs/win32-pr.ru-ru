---
title: Метод WSMan. Сессионфлагусекредссп (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлагусекредссп для использования в параметре flags метода WSMan. CreateSession.
ms.assetid: bb167445-91d6-4e06-a976-bf869320784a
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода сессионфлагусекредссп
- служба удаленного управления Windows метода сессионфлагусекредссп, объект WSMan
- объект WSMan служба удаленного управления Windows, метод сессионфлагусекредссп
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseCredSsp
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27eb96f1de72bbcceafd40c0ccbcfdd3b990ed2134739195bd29e130dbac5a64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642234"
---
# <a name="wsmansessionflagusecredssp-method"></a>Метод WSMan. Сессионфлагусекредссп

Возвращает значение флага проверки подлинности **всманфлагусекредссп** для использования в параметре *flags* метода [**WSMan. CreateSession**](wsman-createsession.md) . Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение. Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).

**Всманфлагусекредссп** — это константа в перечислении **\_ \_ всмансессионфлагс** . Дополнительные сведения см. в разделе [константы проверки подлинности](authentication-constants.md).

## <a name="syntax"></a>Синтаксис


```VB
WSMan.SessionFlagUseCredSsp( _
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                                                        |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                                                           |
| Распространяемые компоненты<br/>          | Windows Management Framework Windows Server 2008 с пакетом обновления 2 (sp2), Windows Vista с пакетом обновления 1 (SP1) и Windows Vista<br/> |
| Заголовок<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>                                      |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl>                                    |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl>                                    |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>                                      |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Ведущий**](wsman.md)
</dt> <dt>

[**Сеанс**](session.md)
</dt> </dl>

 

 





