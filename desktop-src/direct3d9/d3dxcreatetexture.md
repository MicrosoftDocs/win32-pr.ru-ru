---
description: Создает пустую текстуру, настраивая параметры вызова по мере необходимости.
ms.assetid: ea028aa9-4f37-4625-9e07-9072ec1a61d0
title: Функция D3DXCreateTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6264be0712f5ac7f30a9882efde5c66e1e75404634e77d6b72d2313ba016fd6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299259"
---
# <a name="d3dxcreatetexture-function"></a>Функция D3DXCreateTexture

Создает пустую текстуру, настраивая параметры вызова по мере необходимости.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateTexture(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  UINT               Width,
  _In_  UINT               Height,
  _In_  UINT               MipLevels,
  _In_  DWORD              Usage,
  _In_  D3DFORMAT          Format,
  _In_  D3DPOOL            Pool,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой.

</dd> <dt>

*Ширина* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Ширина в пикселях. Если это значение равно 0, то используется значение 1. См. заметки.

</dd> <dt>

*Высота* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Высота в пикселях. Если это значение равно 0, то используется значение 1. См. заметки.

</dd> <dt>

*Миплевелс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число запрошенных уровней MIP. Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap.

</dd> <dt>

*Использование* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

0, [**D3DUSAGE \_ Рендертаржет**](d3dusage.md)или **D3DUSAGE \_ dynamic**. Установка этого флага в значение **D3DUSAGE \_ рендертаржет** указывает, что поверхность должна использоваться в качестве целевого объекта отрисовки путем вызова метода [**сетрендертаржет**](/windows/desktop/api) . Если указано значение **D3DUSAGE \_ Рендертаржет** или **D3DUSAGE \_ dynamic** , приложение должно проверить, поддерживает ли устройство эту операцию, вызвав [**чеккдевицеформат**](/windows/desktop/api). Дополнительные сведения об использовании динамических текстур см. [в разделе Использование динамических текстур](performance-optimizations.md).

</dd> <dt>

*Формат* \[ окне\]
</dt> <dd>

Тип: **[D3DFORMAT](d3dformat.md)**

Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий запрошенный формат пикселей для текстуры. Возвращаемая текстура может иметь другой формат из указанного, если устройство не поддерживает запрошенный формат. Приложения должны проверить формат возвращенной текстуры, чтобы узнать, соответствует ли он требуемому формату.

</dd> <dt>

*Пул* \[ окне\]
</dt> <dd>

Тип: **[ **D3DPOOL**](./d3dpool.md)**

Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура.

</dd> <dt>

*пптекстуре* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Адрес указателя на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий созданный объект текстуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ NOTAVAILABLE, D3DERR \_ аутофвидеомемори, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

На внутреннем уровне D3DXCreateTexture использует [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) для настройки параметров вызова. Таким образом, вызовы D3DXCreateTexture часто завершаются успешно, когда вызовы [**креатетекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) завершатся сбоем.

Если для высоты и ширины задано значение [D3DX \_ по умолчанию](other-d3dx-constants.md), для обоих параметров будет использоваться 256. Если для высоты или ширины задано значение D3DX \_ по умолчанию, а для другого параметра задано числовое значение, то текстура будет квадратной и высотой и шириной, равной числу значений.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
