---
title: Метод Ирдвтаскплугиннотифисинк с преждевременным завершением (Сбтсв. h)
description: Вызывается агентом задачи для запроса завершения работы агента задачи.
ms.assetid: 163e0ce5-f4ee-4242-bdbb-977c5ede3451
ms.tgt_platform: multiple
keywords:
- Метод onTerminate службы удаленных рабочих столов
- Метод onTerminate службы удаленных рабочих столов, интерфейс Ирдвтаскплугиннотифисинк
- Интерфейс Ирдвтаскплугиннотифисинк службы удаленных рабочих столов, метод onTerminate
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTerminated
api_location:
- sbtsv.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b261437425b0b4dce4b2c2e17c52b6e24ea3e0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535321"
---
# <a name="irdvtaskpluginnotifysinkonterminated-method"></a>Метод Ирдвтаскплугиннотифисинк:: onTerminate

Вызывается агентом задачи для запроса завершения работы агента задачи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnTerminated(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HR* \[ окне\]
</dt> <dd>

Указывает, что завершение работы вызвано нормальным завершением работы или сбоем. Если завершение работы является нормальным, оно содержит **S \_ ОК**. В противном случае он содержит код ошибки **HRESULT** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7 Корпоративная<br/>                                                    |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                  |
| Header<br/>                   | <dl> <dt>Сбтсв. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ирдвтаскплугиннотифисинк**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





