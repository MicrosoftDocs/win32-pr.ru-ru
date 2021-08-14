---
description: Определяет данные памяти. Не рекомендуется.
ms.assetid: fe791e13-d5de-425f-b68f-80db8b332cc6
title: Структура ДКСФИЛЕЛОАДМЕМОРИ (Дксфиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADMEMORY
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 3de6db80e12197f3ad61dd845519be7f532d320765c491cba7a8219ee701af05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119407464"
---
# <a name="dxfileloadmemory-structure"></a>Структура ДКСФИЛЕЛОАДМЕМОРИ

Определяет данные памяти. Не рекомендуется.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct DXFILELOADMEMORY {
  LPVOID lpMemory;
  DWORD  dSize;
} DXFILELOADMEMORY, *LPDXFILELOADMEMORY;
```



## <a name="members"></a>Члены

<dl> <dt>

**лпмемори**
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**

</dd> <dd>

Указатель на блок памяти для загрузки.

</dd> <dt>

**дсизе**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Размер блока памяти, который должен быть загружен, в байтах.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура определяет ресурс для загрузки, когда приложение использует метод [**креатинумобжект**](idirectxfile--createenumobject.md) и указывает дксфилелоад \_ фроммемори.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Дксфиле. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры файлов X](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[**креатинумобжект**](idirectxfile--createenumobject.md)
</dt> <dt>

[Константы ДКСФИЛЕ](dxfile.md)
</dt> </dl>

 

 
