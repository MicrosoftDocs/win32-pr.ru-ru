---
description: Определяет данные ресурса. Не рекомендуется.
ms.assetid: acb379c7-ac80-412f-8891-d5917b3f8da4
title: Структура ДКСФИЛЕЛОАДРЕСАУРЦЕ (Дксфиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 54d0072d7c87f6d26483faf8c591ea7651eff29b411643eb9848de11ff50d899
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803041"
---
# <a name="dxfileloadresource-structure"></a>Структура ДКСФИЛЕЛОАДРЕСАУРЦЕ

Определяет данные ресурса. Не рекомендуется.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct DXFILELOADRESOURCE {
  HMODULE hModule;
  LPCTSTR lpName;
  LPCTSTR lpType;
} DXFILELOADRESOURCE, *LPDXFILELOADRESOURCE;
```



## <a name="members"></a>Члены

<dl> <dt>

**хмодуле**
</dt> <dd>

Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**

</dd> <dd>

Маркер модуля, содержащего загружаемый ресурс. Если этот член имеет **значение NULL**, ресурс должен быть присоединен к исполняемому файлу, который будет его использовать.

</dd> <dt>

**лпнаме**
</dt> <dd>

Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Указатель на строку, указывающую имя загружаемого ресурса. Например, если ресурс является сеткой, этот член должен указать имя файла сетки.

</dd> <dt>

**лптипе**
</dt> <dd>

Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Указатель на строку, указывающую определяемый пользователем тип, идентифицирующий ресурс.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура определяет ресурс для загрузки, когда приложение использует метод [**креатинумобжект**](idirectxfile--createenumobject.md) и указывает дксфилелоад \_ фромресаурце.

## <a name="requirements"></a>Требования



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

 

 
