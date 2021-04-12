---
title: Структура BG_JOB_PROGRESS (Deliveryoptimization. h)
description: Структура BG_JOB_PROGRESS предоставляет сведения о ходе выполнения, связанные с заданиями, такие как число переданных байтов и файлов. Для заданий отправки это состояние применяется к файлу отправки, а не к файлу ответов.
ms.assetid: F07BBDDE-FD34-4779-9E17-3789A8098616
keywords:
- Структура BG_JOB_PROGRESS
topic_type:
- apiref
api_name:
- BG_JOB_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e45c4a2833f80644ff763fc85a6846f9858fb3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534934"
---
# <a name="bg_job_progress-structure"></a>Структура BG_JOB_PROGRESS

Структура **BG_JOB_PROGRESS** предоставляет сведения о ходе выполнения, связанные с заданиями, такие как число переданных байтов и файлов. Для заданий отправки это состояние применяется к файлу отправки, а не к файлу ответов.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _BG_JOB_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  ULONG  FilesTotal;
  ULONG  FilesTransferred;
} BG_JOB_PROGRESS;
```



## <a name="members"></a>Члены

<dl> <dt>

**BytesTotal**
</dt> <dd>

Общее число байтов для пересылки для всех файлов в задании. Если значение равно BG_SIZE_UNKNOWN, общий размер всех файлов в задании не определен. Не задавайте это значение, если не удается определить размер одного из файлов. Например, если указанный файл или сервер не существует, не удается определить размер файла.

При скачивании диапазонов из файла **битестотал** включает в себя общее число байтов, которое необходимо скачать из файла.

</dd> <dt>

**BytesTransferred**
</dt> <dd>

Число переданных байтов.

</dd> <dt>

**филестотал**
</dt> <dd>

Общее число переносимых файлов для этого задания.

</dd> <dt>

**филестрансферред**
</dt> <dd>

Число переданных файлов.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**BG_FILE_PROGRESS**](bg-file-progress.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: Progress**](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





