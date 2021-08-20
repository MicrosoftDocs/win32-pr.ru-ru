---
title: Ирдвтаскплугиннотифисинк DeleteSchedule, метод
description: Вызывается агентом задачи для удаления запланированной задачи.
ms.assetid: 67a9493e-367a-48c9-8f94-276d696406b7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода DeleteSchedule
- Службы удаленных рабочих столов метода DeleteSchedule, интерфейс Ирдвтаскплугиннотифисинк
- Службы удаленных рабочих столов интерфейса Ирдвтаскплугиннотифисинк, метод DeleteSchedule
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.DeleteSchedule
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5674b3624edc102be6943e63b72444ec68f403fa1066e90a410f028008894d29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129146"
---
# <a name="irdvtaskpluginnotifysinkdeleteschedule-method"></a>Ирдвтаскплугиннотифисинк: метод:D Елетесчедуле

Вызывается агентом задачи для удаления запланированной задачи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DeleteSchedule(
  [in] BSTR bstrIdentifier
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*bstrIdentifier* \[ окне\]
</dt> <dd>

Идентификатор запланированной задачи.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------|
| Минимальная версия клиента<br/> | Windows 7 Корпоративная<br/>   |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ирдвтаскплугиннотифисинк**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





