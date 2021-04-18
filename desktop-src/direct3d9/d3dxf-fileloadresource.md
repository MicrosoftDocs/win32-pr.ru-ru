---
description: Определяет данные ресурса.
ms.assetid: f2ace2ad-228f-4f76-ab31-16e045e09331
title: Структура D3DXF_FILELOADRESOURCE (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: ee5dc27b551382a5fa5d1c7f4833c94b205e5521
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694155"
---
# <a name="d3dxf_fileloadresource-structure"></a>\_Структура ФИЛЕЛОАДРЕСАУРЦЕ D3DXF

Определяет данные ресурса.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXF_FILELOADRESOURCE {
  HMODULE hModule;
  LPCSTR  lpName;
  LPCSTR  lpType;
} D3DXF_FILELOADRESOURCE, *LPD3DXF_FILELOADRESOURCE;
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

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Указатель на строку, указывающую имя загружаемого ресурса. Например, если ресурс является сеткой, этот член должен указать имя файла сетки.

</dd> <dt>

**лптипе**
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Указатель на строку, указывающую определяемый пользователем тип, идентифицирующий ресурс.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта структура определяет ресурс для загрузки, когда приложение использует метод [**креатинумобжект**](id3dxfile--createenumobject.md) и задает флаг [D3DXF \_ филелоад \_ фромресаурце](d3dxf.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9xof. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры файлов D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
