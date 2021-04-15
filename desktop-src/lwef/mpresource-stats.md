---
title: Структура MPRESOURCE_STATS (Мпклиент. h)
description: Статистика, связанная с ресурсами.
ms.assetid: D1DC4BC9-911D-448C-A421-11D2F51F0A61
keywords:
- MPRESOURCE_STATS структуры устаревшие функции среды Windows
- Функции PMPRESOURCE_STATS указателя структур в устаревшей среде Windows
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
ms.openlocfilehash: afbe1ce6734aabd1093f7acd886af757c51ed83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491550"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





