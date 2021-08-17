---
title: Метод WSMan. Сессионфлагусебасик (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлагусебасик для использования в параметре flags метода WSMan. CreateSession.
ms.assetid: 789ecef9-7871-43af-9d63-018f1d99bd09
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода сессионфлагусебасик
- служба удаленного управления Windows метода сессионфлагусебасик, объект WSMan
- объект WSMan служба удаленного управления Windows, метод сессионфлагусебасик
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseBasic
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf908ad4cbe70f9480c23dbc26d5a0593212a285cd541ad70605e990e30792d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742006"
---
# <a name="wsmansessionflagusebasic-method"></a>Метод WSMan. Сессионфлагусебасик

Метод **WSMan. сессионфлагусебасик** возвращает значение флага проверки подлинности **всманфлагусебасик** для использования в параметре *flags* метода [**WSMan. CreateSession**](wsman-createsession.md) . Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение. Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).

**Всманфлагусебасик** — это константа в перечислении **\_ \_ всмансессионфлагс** . Дополнительные сведения см. в разделе [**константы проверки подлинности**](authentication-constants.md).

## <a name="syntax"></a>Синтаксис


```VB
WSMan.SessionFlagUseBasic( _
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

 

 





