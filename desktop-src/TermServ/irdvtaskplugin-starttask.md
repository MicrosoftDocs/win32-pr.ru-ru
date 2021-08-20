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
ms.openlocfilehash: 0e0bb9104ee1bbd3f0f6c2e8cc04b691205f2e40cb2221b79b5e9f251492a3a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129261"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------|
| Минимальная версия клиента<br/> | Windows 7 Корпоративная<br/>   |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ирдвтаскплугин**](irdvtaskplugin.md)
</dt> </dl>

 

 





