---
description: Создает текстуру из файла.
ms.assetid: 247b0ee2-ee31-4090-b94c-41951b46675f
title: Функция D3DXCreateTextureFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b3ffce68a8044267e67d874412264d5a915c65b88ea5cc13b0cd8d2cd1400828
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732163"
---
# <a name="d3dxcreatetexturefromfile-function"></a>Функция D3DXCreateTextureFromFile

Создает текстуру из файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateTextureFromFile(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCTSTR            pSrcFile,
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

*псркфиле* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Указатель на строку, указывающую имя файла. Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае строковый тип данных разрешается в LPCSTR. См. заметки.

</dd> <dt>

*пптекстуре* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Адрес указателя на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий созданный объект текстуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Параметр компилятора также определяет версию функции. Если определен Юникод, вызов функции разрешается в D3DXCreateTextureFromFileW. В противном случае вызов функции разрешается в D3DXCreateTextureFromFileA, так как используются строки ANSI.

Эта функция поддерживает следующие форматы файлов: .bmp, DDS, DIB, HDR, .jpg,. ПФМ, .png,. ppm и. tga. См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Функция эквивалентна D3DXCreateTextureFromFileEx (Пдевице, Псркфиле, D3DX \_ Default, D3DX \_ по умолчанию, D3DX \_ по умолчанию, 0, D3DFMT \_ Unknown, D3DPOOL \_ управляемый, D3DX \_ Default, D3DX \_ по умолчанию, 0, **null**, **null**, пптекстуре).

Текстуры мипмаппед автоматически имеют каждый уровень, заполненный загруженной текстурой.

При загрузке изображений в текстуры мипмаппед некоторые устройства не могут подключиться к образу 1x1, и эта функция завершится ошибкой. Если это происходит, образы необходимо загружать вручную.

Обратите внимание, что ресурс, созданный с помощью этой функции, будет помещен в класс Memory, обозначенный D3DPOOL \_ Managed.

Фильтрация автоматически применяется к текстуре, созданной с помощью этого метода. Фильтрация эквивалентна D3DX фильтра \_ D3DX Filter \_ \| \_ \_ в [ \_ фильтре D3DX](d3dx-filter.md).

Для лучшей производительности при использовании **D3DXCreateTextureFromFile**:

1.  Масштабирование изображения и преобразование формата во время загрузки могут выполняться слишком долго. Храните изображения в формате и разрешении, которые они будут использовать. Если целевому оборудованию требуется мощность двух измерений, создайте и сохраните образы с помощью возможностей двух измерений.
2.  Рассмотрите возможность использования файлов поверхности DirectDraw (DDS). Так как файлы DDS могут использоваться для представления любого формата текстуры Direct3D 9, они очень просты в D3DX для чтения. Кроме того, они могут хранить MIP-карты, поэтому для создания образов можно использовать любые алгоритмы создания mipmap.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)
</dt> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
