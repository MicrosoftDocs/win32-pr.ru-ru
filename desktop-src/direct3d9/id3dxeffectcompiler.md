---
description: Интерфейс ID3DXEffectCompiler компилирует результат из функции или шейдера вершин.
ms.assetid: 2d1dbc63-1eb9-4736-a0b5-7f899c0638be
title: Интерфейс ID3DXEffectCompiler (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c7a16417528d1adbd9ba54f9bd7120057654d14e0ef4bddad829e8f232445069
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856744"
---
# <a name="id3dxeffectcompiler-interface"></a>Интерфейс ID3DXEffectCompiler

Интерфейс **ID3DXEffectCompiler** компилирует результат из функции или шейдера вершин.

## <a name="members"></a>Элементы

Интерфейс **ID3DXEffectCompiler** наследует от [**ID3DXBaseEffect**](id3dxbaseeffect.md). **ID3DXEffectCompiler** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXEffectCompiler** содержит следующие методы.



| Метод                                                      | Описание                                                                                                                                 |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**компилиффект**](id3dxeffectcompiler--compileeffect.md) | Компиляция результата.<br/>                                                                                                               |
| [**компилешадер**](id3dxeffectcompiler--compileshader.md) | Компилирует шейдер из действия, содержащего одну или несколько функций.<br/>                                                            |
| [**Знак ". Literal"**](id3dxeffectcompiler--getliteral.md)       | Возвращает состояние литерала параметра. Литеральный параметр имеет значение, которое не изменяется в течение времени существования действия.<br/>      |
| [**сетлитерал**](id3dxeffectcompiler--setliteral.md)       | Переключает состояние литерала для параметра. Литеральный параметр имеет значение, которое не изменяется в течение времени существования действия.<br/> |



 

## <a name="remarks"></a>Remarks

Интерфейс ID3DXEffectCompiler получается путем вызова [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md), [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)или [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md).

Тип LPD3DXEFFECTCOMPILER определяется как указатель на этот интерфейс.


```
typedef interface ID3DXEffectCompiler ID3DXEffectCompiler;
typedef interface ID3DXEffectCompiler *LPD3DXEFFECTCOMPILER;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID3DXBaseEffect**](id3dxbaseeffect.md)
</dt> <dt>

[Интерфейсы эффектов](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 




