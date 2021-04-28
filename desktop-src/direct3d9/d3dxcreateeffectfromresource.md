---
description: Функция D3DXCreateEffectFromResource — создание результата из описания ASCII-или двоичного воздействия.
ms.assetid: 8385512c-e93d-4c07-b353-87717eb58bcd
title: Функция D3DXCreateEffectFromResource (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f2a84d2da1f3ca88a117c0150e7b27485838c300
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107692"
---
# <a name="d3dxcreateeffectfromresource-function"></a>Функция D3DXCreateEffectFromResource

Создание результата из описания ASCII или двоичного действия.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateEffectFromResource(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на устройство.

</dd> <dt>

*хсркмодуле* \[ окне\]
</dt> <dd>

Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**

Обработчик для модуля, содержащего описание результата. Если этот параметр имеет **значение NULL**, будет использоваться текущий модуль.

</dd> <dt>

*псркресаурце* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Указатель на ресурс. Этот параметр поддерживает строки в Юникоде и ANSI. См. заметки.

</dd> <dt>

*пдефинес* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***

Необязательный завершающий **нуль** массив структур [**D3DXMACRO**](d3dxmacro.md) , описывающих определения препроцессора. Это значение может быть **равно NULL**.

</dd> <dt>

*пинклуде* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include. Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Если *хсркмодуле* содержит текстовый результат, флаги могут быть сочетанием флагов [D3DXSHADER](d3dxshader-flags.md) и [D3DXFX](d3dxfx.md) . в противном случае *хсркмодуле* содержит двоичный результат, а только соблюдаются флаги D3DXFX. Компилятор Direct3D 10 HLSL теперь является значением по умолчанию. Дополнительные сведения см. в разделе [средство компилятора Effect](../direct3dtools/fxc.md) .

</dd> <dt>

*ппул* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**

Указатель на объект [**ID3DXEffectPool**](id3dxeffectpool.md) , используемый для общих параметров. Если это значение равно **null**, общий доступ к параметрам не предоставляется.

</dd> <dt>

*ппеффект* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Возвращает буфер, содержащий скомпилированный результат.

</dd> <dt>

*ппкомпилатионеррорс* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Возвращает буфер, содержащий список ошибок компиляции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае тип данных LPCTSTR разрешается в LPCSTR.

Параметр компилятора также определяет версию функции. Если определен Юникод, вызов функции разрешается в D3DXCreateEffectFromResourceW. В противном случае вызов функции разрешается в D3DXCreateEffectFromResourceA, так как используются строки ANSI.

D3DXCreateEffectFromResource загружает данные из ресурса типа RT \_ RCDATA. Дополнительные сведения о ресурсах Windows см. на сайте MSDN.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции эффектов](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCompileShader**](d3dxcompileshader.md)
</dt> <dt>

[**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
