---
title: Метод WSMan. Сессионфлагусебасик (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлагусебасик для использования в параметре flags метода WSMan. CreateSession.
ms.assetid: 789ecef9-7871-43af-9d63-018f1d99bd09
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Сессионфлагусебасик
- Служба удаленного управления Windows метода Сессионфлагусебасик, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Сессионфлагусебасик
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
ms.openlocfilehash: 41641e0398791ab46c81f71f967f2d43700a2984
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071272"
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
| Header<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ведущий**](wsman.md)
</dt> <dt>

[**Session**](session.md)
</dt> </dl>

 

 





