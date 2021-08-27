---
description: Создает текстуру тома из ресурса.
ms.assetid: 82a0b7aa-69fa-450d-b0d2-769f05fd75ea
title: Функция D3DXCreateVolumeTextureFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: df0d54e4981b9dccf655978df8f08bb9154e41d1ec9918c9a6db0ee65b0be6de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119234"
---
# <a name="d3dxcreatevolumetexturefromresource-function"></a>Функция D3DXCreateVolumeTextureFromResource

Создает текстуру тома из ресурса.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateVolumeTextureFromResource(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
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

*хсркмодуле* \[ окне\]
</dt> <dd>

Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**

Указатель на модуль, в котором находится ресурс, или **значение NULL** для модуля, связанного с образом, операционной системой, используемой для создания текущего процесса.

</dd> <dt>

*псркресаурце* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Указатель на строку, указывающую имя ресурса. Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае строковый тип данных разрешается в LPCSTR. См. заметки.

</dd> <dt>

*ппволуметекстуре* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***

Адрес указателя на интерфейс [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , представляющий созданный объект текстуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Параметр компилятора также определяет версию функции. Если определен Юникод, вызов функции разрешается в D3DXCreateVolumeTextureFromResourceW. В противном случае вызов функции разрешается в D3DXCreateVolumeTextureFromResourceA, так как используются строки ANSI.

Функция эквивалентна D3DXCreateVolumeTextureFromResourceEx (Пдевице, Хсркмодуле, Псркресаурце, D3DX \_ Default, D3DX \_ по умолчанию, D3DX \_ Default, D3DX \_ по умолчанию, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ по умолчанию, D3DX \_ по умолчанию, 0, **null**, **null**, ппволуметекстуре).

Загружаемый ресурс должен быть ресурсом, определяемым приложением (RT \_ RCDATA).

Эта функция поддерживает следующие форматы файлов: .bmp, DDS, DIB, HDR, .jpg,. ПФМ, .png,. ppm и. tga. См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Обратите внимание, что ресурс, созданный с помощью этой функции при вызове из объекта IDirect3DDevice9, будет помещен в класс Memory, обозначенный D3DPOOL \_ Managed. При вызове этого метода из объекта IDirect3DDevice9Ex ресурс будет помещен в класс Memory, обозначенный параметром D3DPOOL \_ Default.

Фильтрация автоматически применяется к текстуре, созданной с помощью этого метода. Фильтрация эквивалентна D3DX фильтра \_ D3DX Filter \_ \| \_ \_ в [ \_ фильтре D3DX](d3dx-filter.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[**D3DXCreateVolumeTextureFromFile**](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileEx**](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileInMemoryEx**](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResourceEx**](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
