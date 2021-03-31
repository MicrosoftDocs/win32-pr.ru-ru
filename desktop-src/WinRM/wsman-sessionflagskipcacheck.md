---
title: Метод WSMan. Сессионфлагскипкачекк (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлагскипкачекк для использования в параметре Flags WSMan. CreateSession.
ms.assetid: a67cadb3-c20a-4a58-a13b-5bbd23c547d1
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Сессионфлагскипкачекк
- Служба удаленного управления Windows метода Сессионфлагскипкачекк, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Сессионфлагскипкачекк
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
ms.openlocfilehash: 7e536112b16ad8cbab3cebb2de582a2e0ea8aec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071132"
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

 

 





