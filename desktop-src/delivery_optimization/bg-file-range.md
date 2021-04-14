---
title: Структура BG_FILE_RANGE (Deliveryoptimization. h)
description: Структура BG_FILE_RANGE определяет диапазон байтов для загрузки из файла.
ms.assetid: 58993C51-E42E-4E44-9E8A-15E982B25413
keywords:
- Структура BG_FILE_RANGE
topic_type:
- apiref
api_name:
- BG_FILE_RANGE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cedabfb066a5905adb2ed8eac9996fd77c0e12be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415968"
---
# <a name="bg_file_range-structure"></a>Структура BG_FILE_RANGE

Структура **BG_FILE_RANGE** определяет диапазон байтов для загрузки из файла.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  UINT64 InitialOffset;
  UINT64 Length;
} BG_FILE_RANGE;
```



## <a name="members"></a>Члены

<dl> <dt>

**инитиалоффсет**
</dt> <dd>

Смещение от нуля до начала диапазона байтов для скачивания из файла.

</dd> <dt>

**Длина**
</dt> <dd>

Длина диапазона в байтах. Не указывайте нулевую длину байта. Чтобы указать, что диапазон расширяется до конца файла, укажите **BG_LENGTH_TO_EOF**.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Диапазон должен существовать в файле или выдает ошибку **DO_E_INVALID_RANGE** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IBackgroundCopyFile2:: Жетфилеранжес**](ibackgroundcopyfile2-getfileranges-method.md)
</dt> </dl>

 

 





