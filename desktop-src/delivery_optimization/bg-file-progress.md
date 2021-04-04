---
title: Структура BG_FILE_PROGRESS (Deliveryoptimization. h)
description: Структура BG_FILE_PROGRESS предоставляет сведения о ходе выполнения, связанные с файлами, например число переданных байтов.
ms.assetid: 49BDFEEE-D7BF-489A-8BC1-951549B06252
keywords:
- Структура BG_FILE_PROGRESS
topic_type:
- apiref
api_name:
- BG_FILE_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 93507b8aeefa9c0ea16f70f67e221ecc4218427f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803299"
---
# <a name="bg_file_progress-structure"></a>Структура BG_FILE_PROGRESS

Структура **BG_FILE_PROGRESS** предоставляет сведения о ходе выполнения, связанные с файлами, например число переданных байтов.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _BG_FILE_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  BOOL   Completed;
} BG_FILE_PROGRESS;
```



## <a name="members"></a>Члены

<dl> <dt>

**BytesTotal**
</dt> <dd>

Размер файла в байтах. Если не удается определить размер файла (например, если файл или сервер не существует), значение DO_UNKNOWN_FILE_SIZE.

Если вы скачиваете диапазоны из файла, **битестотал** отражает общее число байтов, которое необходимо скачать из файла.

</dd> <dt>

**BytesTransferred**
</dt> <dd>

Число переданных байтов.

</dd> <dt>

**Завершено**
</dt> <dd>

Для загрузки значение равно **true** , если файл доступен пользователю; в противном случае значение равно **false**. Файлы доступны пользователю после вызова метода [**использованием метода ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) . Если метод **Complete** создает временную ошибку, то эти файлы, обработанные до возникновения ошибки, становятся доступными для пользователя. другие — нет. Используйте **завершенный** член, чтобы определить, доступен ли файл пользователю при сбое **завершения** .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Чтобы определить, передавался ли файл, можно выполнить следующие действия.

-   Сравните **BytesTransferred** с **битестотал**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**BG_JOB_PROGRESS**](bg-job-progress.md)
</dt> <dt>

[**Ибаккграундкопифиле:: Progress**](ibackgroundcopyfile-getprogress-method.md)
</dt> </dl>

 

 





