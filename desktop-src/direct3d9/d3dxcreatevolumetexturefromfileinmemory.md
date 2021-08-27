---
description: Создает текстуру тома из файла в памяти.
ms.assetid: 8ea22209-6110-4bef-a0d6-667f59017adc
title: Функция D3DXCreateVolumeTextureFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e7cfa39b689033d9675e3615fa1ab5d99291fa6058965cd47bf84c68c2abfe33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119275"
---
# <a name="d3dxcreatevolumetexturefromfileinmemory-function"></a>Функция D3DXCreateVolumeTextureFromFileInMemory

Создает текстуру тома из файла в памяти.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateVolumeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  LPCVOID                  pSrcFile,
  _In_  UINT                     SrcData,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 ppVolumeTexture
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой тома.

</dd> <dt>

*псркфиле* \[ окне\]
</dt> <dd>

Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**

Указатель на файл в памяти, из которого создается текстура тома.

</dd> <dt>

*SrcData* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Размер файла в памяти, в байтах.

</dd> <dt>

*ппволуметекстуре* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**

Адрес указателя на интерфейс [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , представляющий созданный объект текстуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Эта функция поддерживает следующие форматы файлов: .bmp, DDS, DIB, HDR, .jpg,. ПФМ, .png,. ppm и. tga. См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Функция эквивалентна D3DXCreateVolumeTextureFromFileInMemoryEx (Пдевице, Псркфиле, SrcData, D3DX \_ Default, D3DX \_ по умолчанию, D3DX \_ Default, D3DX \_ по умолчанию, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ по умолчанию, D3DX \_ по умолчанию, 0, **null**, **null**, ппволуметекстуре).

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

[**D3DXCreateVolumeTextureFromFileInMemoryEx**](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResourceEx**](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
