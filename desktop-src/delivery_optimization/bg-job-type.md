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
ms.openlocfilehash: f1f672bcf2d2538bfaa9b9573fa1dfa71ee7b9cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490065"
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
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Использованием метода ibackgroundcopyjob:: GetType**](ibackgroundcopyjob-gettype.md)
</dt> <dt>

[**Ибаккграундкопиманажер:: CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





