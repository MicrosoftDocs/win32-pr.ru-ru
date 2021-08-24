---
title: Перечисление BG_JOB_TYPE (Deliveryoptimization. h)
description: Перечисление BG_JOB_TYPE определяет постоянные значения, указывающие тип задания перемещения, например download.
ms.assetid: 696A43C3-1FA2-436D-B34A-3544E7C9A66A
keywords:
- Перечисление BG_JOB_TYPE
topic_type:
- apiref
api_name:
- BG_JOB_TYPE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ae722871435af316e045b293f2cf439a07600af1823202b7bfda654bf01d771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755824"
---
# <a name="bg_job_type-enumeration"></a>Перечисление BG_JOB_TYPE

Перечисление **BG_JOB_TYPE** определяет постоянные значения, указывающие тип задания перемещения, например download.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  BG_JOB_TYPE_DOWNLOAD
} BG_JOB_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**
</dt> <dd>

Указывает, что задание загружает файлы на клиент.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                     |
| Заголовок<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Использованием метода ibackgroundcopyjob:: GetType**](ibackgroundcopyjob-gettype.md)
</dt> <dt>

[**Ибаккграундкопиманажер:: CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





