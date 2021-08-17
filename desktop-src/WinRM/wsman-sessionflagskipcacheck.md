---
title: Метод WSMan. Сессионфлагскипкачекк (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлагскипкачекк для использования в параметре Flags WSMan. CreateSession.
ms.assetid: a67cadb3-c20a-4a58-a13b-5bbd23c547d1
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода сессионфлагскипкачекк
- служба удаленного управления Windows метода сессионфлагскипкачекк, объект WSMan
- объект WSMan служба удаленного управления Windows, метод сессионфлагскипкачекк
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCACheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe24e10ca7a568a6dc9b3af6efed6e31a3a9fde5acac70e2badab37d24373350
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742033"
---
# <a name="wsmansessionflagskipcacheck-method"></a>Метод WSMan. Сессионфлагскипкачекк

Метод **WSMan. сессионфлагскипкачекк** возвращает значение флага проверки подлинности **всманфлагскипкачекк** для использования в параметре *flags* [**WSMan. CreateSession**](wsman-createsession.md). Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение. Дополнительные сведения о том, как вызывать этот метод и примеры кода, см. в разделе [константы сеанса](session-constants.md).

**Всманфлагскипкачекк** — это константа в перечислении **\_ \_ всмансессионфлагс** . Дополнительные сведения см. в разделе [**константы проверки подлинности**](authentication-constants.md).

## <a name="syntax"></a>Синтаксис


```VB
WSMan.SessionFlagSkipCACheck( _
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

 

 





