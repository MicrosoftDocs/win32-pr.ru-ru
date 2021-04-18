---
title: Метод WSMan. Сессионфлагусекредссп (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлагусекредссп для использования в параметре flags метода WSMan. CreateSession.
ms.assetid: bb167445-91d6-4e06-a976-bf869320784a
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Сессионфлагусекредссп
- Служба удаленного управления Windows метода Сессионфлагусекредссп, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Сессионфлагусекредссп
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
ms.openlocfilehash: ed5dfbaba3e705f100cdd373e194174f4654a7d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490755"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                                                        |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                                                           |
| Распространяемые компоненты<br/>          | Windows Management Framework на Windows Server 2008 с пакетом обновления 2 (SP2), Windows Vista с пакетом обновления 1 и Windows Vista с пакетом обновления 2<br/> |
| Header<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>                                      |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl>                                    |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl>                                    |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>                                      |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ведущий**](wsman.md)
</dt> <dt>

[**Session**](session.md)
</dt> </dl>

 

 





