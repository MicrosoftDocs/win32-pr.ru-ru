---
title: Метод WSMan. Сессионфлаженаблеспнсерверпорт (Всмандисп. h)
description: Возвращает значение флага проверки подлинности Всманфлаженаблеспнсерверпорт для использования в параметре flags метода WSMan. CreateSession.
ms.assetid: a18a87e6-dcee-4e9f-8e8c-262fef36ab1a
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Сессионфлаженаблеспнсерверпорт
- Служба удаленного управления Windows метода Сессионфлаженаблеспнсерверпорт, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Сессионфлаженаблеспнсерверпорт
topic_type:
- apiref
api_name:
- WSMan.SessionFlagEnableSPNServerPort
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4153f088079b58b3b0e048f2cd8f38b3524754a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534523"
---
# <a name="wsmansessionflagenablespnserverport-method"></a>Метод WSMan. Сессионфлаженаблеспнсерверпорт

Метод **WSMan. сессионфлаженаблеспнсерверпорт** возвращает значение флага проверки подлинности **всманфлаженаблеспнсерверпорт** для использования в параметре *flags* метода [**WSMan. CreateSession**](wsman-createsession.md) . Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение. Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).

**Всманфлаженаблеспнсерверпорт** — это константа в перечислении **\_ \_ всмансессионфлагс** . Дополнительные сведения см. в разделе [**другие константы сеанса**](other-session-constants.md).

## <a name="syntax"></a>Синтаксис


```VB
WSMan.SessionFlagEnableSPNServerPort( _
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

 

 





