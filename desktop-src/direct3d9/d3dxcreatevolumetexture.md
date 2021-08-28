---
description: Создает пустую текстуру тома, настраивая параметры вызова по мере необходимости.
ms.assetid: 8fc515cd-2fb3-40c7-8192-a41d93ac1e99
title: Функция D3DXCreateVolumeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fa3e7b701649b07a9a6da9c0faeed6e0594d1c0e145126c533f87e06249fb8c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119283"
---
# <a name="d3dxcreatevolumetexture-function"></a>Функция D3DXCreateVolumeTexture

Создает пустую текстуру тома, настраивая параметры вызова по мере необходимости.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateVolumeTexture(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  UINT                     Width,
  _In_  UINT                     Height,
  _In_  UINT                     Depth,
  _In_  UINT                     MipLevels,
  _In_  DWORD                    Usage,
  _In_  D3DFORMAT                Format,
  _In_  D3DPOOL                  Pool,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой тома.

</dd> <dt>

*Ширина* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Ширина в пикселях. Это значение должно быть ненулевым. Максимальное количество измерений, поддерживаемое драйвером (для ширины, высоты и глубины), можно найти в Максволумикстент в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

*Высота* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Высота в пикселях. Это значение должно быть ненулевым. Максимальное количество измерений, поддерживаемое драйвером (для ширины, высоты и глубины), можно найти в Максволумикстент в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

*Глубина* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Глубина в пикселях. Это значение должно быть ненулевым. Максимальное количество измерений, поддерживаемое драйвером (для ширины, высоты и глубины), можно найти в Максволумикстент в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

*Миплевелс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число запрошенных уровней MIP. Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap.

</dd> <dt>

*Использование* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

0 или D3DUSAGE \_ dynamic. Дополнительные сведения об использовании динамических текстур см. [в разделе Использование динамических текстур](performance-optimizations.md).

</dd> <dt>

*Формат* \[ окне\]
</dt> <dd>

Тип: **[D3DFORMAT](d3dformat.md)**

Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий запрошенный формат пикселей для текстуры тома. Возвращаемая текстура тома может иметь другой формат, заданный в формате. Приложения должны проверить формат полученной текстуры тома.

</dd> <dt>

*Пул* \[ окне\]
</dt> <dd>

Тип: **[ **D3DPOOL**](./d3dpool.md)**

Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура тома.

</dd> <dt>

*ппволуметекстуре* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***

Адрес указателя на интерфейс [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , представляющий созданный объект текстуры тома.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

На внутреннем уровне D3DXCreateVolumeTexture использует [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) для настройки параметров вызова. Таким образом, вызовы D3DXCreateVolumeTexture часто завершаются успешно, когда вызовы [**креатеволуметекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) завершатся сбоем.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
