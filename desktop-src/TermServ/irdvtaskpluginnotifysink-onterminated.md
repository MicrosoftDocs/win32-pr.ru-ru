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
ms.openlocfilehash: 29ab2a3e8ddea5999b6d63322dbeb9fca07983e591e849f22a3e98e27c67609a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129136"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7 Корпоративная<br/>                                                    |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                  |
| Заголовок<br/>                   | <dl> <dt>Сбтсв. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ирдвтаскплугиннотифисинк**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





