---
description: Проверяет параметры создания текстуры.
ms.assetid: 56ced947-1142-4d05-95e3-ca6a26b147d4
title: Функция D3DXCheckCubeTextureRequirements (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckCubeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f800617920c5d79361b5e6da291fd88b5b963b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821492"
---
# <a name="d3dxcheckcubetexturerequirements-function"></a>Функция D3DXCheckCubeTextureRequirements

Проверяет параметры создания текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCheckCubeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pSize,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой Куба.

</dd> <dt>

*псизе* \[ в, out\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Указатель на запрошенную ширину и высоту в пикселях или **значение NULL**. Возвращает исправленный размер.

</dd> <dt>

*пнуммиплевелс* \[ в, out\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Указатель на число запрошенных mipmap уровней или **значение NULL**. Возвращает исправленное число уровней mipmap.

</dd> <dt>

*Использование* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

0 или D3DUSAGE \_ рендертаржет. Установка этого флага в значение D3DUSAGE \_ рендертаржет указывает, что поверхность должна использоваться в качестве целевого объекта рендеринга. Затем ресурс можно передать в параметр Пневрендертаржет метода [**сетрендертаржет**](/windows/desktop/api) . Если указан параметр D3DUSAGE \_ рендертаржет, приложение должно проверить, поддерживает ли устройство эту операцию, вызвав [**чеккдевицеформат**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).

</dd> <dt>

*пформат* \[ в, out\]
</dt> <dd>

Тип: **[D3DFORMAT](d3dformat.md)\***

Указатель на член перечисляемого типа [D3DFORMAT](d3dformat.md) . Указывает требуемый формат пикселей или **значение NULL**. Возвращает исправленный формат.

</dd> <dt>

*Пул* \[ окне\]
</dt> <dd>

Тип: **[ **D3DPOOL**](./d3dpool.md)**

Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Если параметры для этой функции недопустимы, эта функция возвращает исправленные параметры.

Текстуры Куба отличаются от других поверхностей тем, что они являются коллекциями поверхностей. Чтобы вызвать [**сетрендертаржет**](/windows/desktop/api) с текстурой Куба, необходимо выбрать отдельное лицо с помощью [**жеткубемапсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) и передать полученную область в **сетрендертаржет**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
