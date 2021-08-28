---
title: Структура MPRESOURCE_STATS (Мпклиент. h)
description: Статистика, связанная с ресурсами.
ms.assetid: D1DC4BC9-911D-448C-A421-11D2F51F0A61
keywords:
- MPRESOURCE_STATS структуры устаревшие функции среды Windows
- функции PMPRESOURCE_STATS Windows указателя структур в устаревшей среде
topic_type:
- apiref
api_name:
- MPRESOURCE_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72a21bf0ec020c1fc2cf5ba1394b4cd5ed04dc32721a4aac9f8349034907b49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848474"
---
# <a name="mpresource_stats-structure"></a>\_Структура статистики мпресаурце

Статистика, связанная с ресурсами.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPRESOURCE_STATS {
  DWORD  PPMProgress;
  UINT64 ProcessCount;
  UINT64 FileCount;
  UINT64 FileBytesCount;
  UINT64 RegKeyCount;
  UINT64 Reserved[4];
} MPRESOURCE_STATS, *PMPRESOURCE_STATS;
```



## <a name="members"></a>Члены

<dl> <dt>

**ппмпрогресс**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Приблизительный ход выполнения проверки в ppm (штук в миллион). Задайте значение **мппрогресс \_ недопустимо** , если сведения о ходе выполнения недоступны.

</dd> <dt>

**процесскаунт**
</dt> <dd>

Тип: **UINT64**

</dd> <dd>

Число проверенных процессов.

</dd> <dt>

**FileCount**
</dt> <dd>

Тип: **UINT64**

</dd> <dd>

Число проверенных файлов.

</dd> <dt>

**филебитескаунт**
</dt> <dd>

Тип: **UINT64**

</dd> <dd>

Число байтов, проверенных на наличие файлов.

</dd> <dt>

**регкэйкаунт**
</dt> <dd>

Тип: **UINT64**

</dd> <dd>

Число сканированных Регкэйс.

</dd> <dt>

**Reserved**
</dt> <dd>

Тип: **UINT64 \[ 4 \]**

</dd> <dd>

Поля, зарезервированные для будущего использования.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





