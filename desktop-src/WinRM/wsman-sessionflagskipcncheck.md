---
title: Метод WSMan. Сессионфлагскипкнчекк (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлагскипкнчекк для использования в параметре Flags WSMan. CreateSession.
ms.assetid: 44884a9d-ec5f-4822-945d-2681d214a902
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Сессионфлагскипкнчекк
- Служба удаленного управления Windows метода Сессионфлагскипкнчекк, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Сессионфлагскипкнчекк
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCNCheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c98981ac166ea7b1b76f1ab322db6c48679a4bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988931"
---
# <a name="wsmansessionflagskipcncheck-method"></a>Метод WSMan. Сессионфлагскипкнчекк

Метод **WSMan. сессионфлагскипкнчекк** возвращает значение флага проверки подлинности **всманфлагскипкнчекк** для использования в параметре *flags* [**WSMan. CreateSession**](wsman-createsession.md). Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение. Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).

**Всманфлагскипкнчекк** — это константа в перечислении **\_ \_ всмансессионфлагс** . Дополнительные сведения см. в разделе [**константы проверки подлинности**](authentication-constants.md).

## <a name="syntax"></a>Синтаксис


```VB
WSMan.SessionFlagSkipCNCheck( _
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

 

 





