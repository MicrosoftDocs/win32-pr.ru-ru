---
title: Ирдвтаскплугин StartTask, метод
description: Вызывается для запуска задачи обновления на виртуальной машине.
ms.assetid: c1e9f18b-1e83-4a29-8646-8adde94e8c14
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода StartTask
- Службы удаленных рабочих столов метода StartTask, интерфейс Ирдвтаскплугин
- Службы удаленных рабочих столов интерфейса Ирдвтаскплугин, метод StartTask
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.StartTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 51c499549378700a90d8fc78d075bc07c1f874cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491319"
---
# <a name="irdvtaskpluginstarttask-method"></a>Метод Ирдвтаскплугин:: StartTask

Вызывается для запуска задачи обновления на виртуальной машине.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT StartTask(
  [in] BSTR            Label,
  [in] BSTR            Identifier,
  [in] SAFEARRAY(BYTE) *Context
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Метка* \[ окне\]
</dt> <dd>

Метка для задачи. Это метка, которая была передана агенту триггера в методе [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .

</dd> <dt>

*Идентификатор* \[ окне\]
</dt> <dd>

Идентификатор задачи. Это идентификатор, который был передан агенту триггера в методе [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .

</dd> <dt>

*Контекст* \[ окне\]
</dt> <dd>

Необязательные данные для задачи. Это данные, переданные в агент триггера в методе [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------|
| Минимальная версия клиента<br/> | Windows 7 Корпоративная<br/>   |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ирдвтаскплугин**](irdvtaskplugin.md)
</dt> </dl>

 

 





