---
title: Ирдвтаскплугиннотифисинк ScheduleTask, метод
description: Вызывается агентом задачи для планирования задачи.
ms.assetid: 06793439-cf16-40ca-8a91-08acc22c73ed
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода ScheduleTask
- Службы удаленных рабочих столов метода ScheduleTask, интерфейс Ирдвтаскплугиннотифисинк
- Службы удаленных рабочих столов интерфейса Ирдвтаскплугиннотифисинк, метод ScheduleTask
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.ScheduleTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9bde92992eec9c4ab3d4151c59e6d687ec2f3fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892630"
---
# <a name="irdvtaskpluginnotifysinkscheduletask-method"></a>Метод Ирдвтаскплугиннотифисинк:: ScheduleTask

Вызывается агентом задачи для планирования задачи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ScheduleTask(
  [in] FILETIME        ftStartTime,
  [in] FILETIME        ftEndTime,
  [in] FILETIME        ftDeadline,
  [in] BSTR            bstrLabel,
  [in] BSTR            bstrIdentifier,
  [in] SAFEARRAY(BYTE) saContext
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фтстарттиме* \[ окне\]
</dt> <dd>

Тип: **[ **fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Самое раннее время запуска задачи в формате UTC.

</dd> <dt>

*фтендтиме* \[ окне\]
</dt> <dd>

Тип: **[ **fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Время окончания задачи в формате UTC. Передайте значение [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) , равное всем нулям, если время окончания не указано.

</dd> <dt>

*фтдеадлине* \[ окне\]
</dt> <dd>

Тип: **[ **fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Крайний срок задачи в формате UTC. Используется для задания приоритета для нескольких задач, находящихся в начальном окне. Если необходимо запустить более одной задачи, сначала начнется одна из них с самым ранним сроком.

</dd> <dt>

*бстрлабел* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Метка для задачи. Передается методу [**StartTask**](irdvtaskplugin-starttask.md) .

</dd> <dt>

*bstrIdentifier* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Идентификатор задачи. Передается методу [**StartTask**](irdvtaskplugin-starttask.md) .

</dd> <dt>

*саконтекст* \[ окне\]
</dt> <dd>

Тип: **SAFEARRAY (Byte)**

Необязательные данные для задачи. Передается методу [**StartTask**](irdvtaskplugin-starttask.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------|
| Минимальная версия клиента<br/> | Windows 7 Корпоративная<br/>   |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ирдвтаскплугиннотифисинк**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

