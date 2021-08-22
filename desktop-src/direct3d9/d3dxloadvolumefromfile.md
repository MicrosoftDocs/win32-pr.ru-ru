---
description: Загружает том из файла.
ms.assetid: ea0fc588-094e-4488-bd82-54507ee0fc91
title: Функция D3DXLoadVolumeFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b83a7e1e4dddfb4222c5d37a417500332f6c0d3cecf366729188b4dd040f459
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495244"
---
# <a name="d3dxloadvolumefromfile-function"></a>Функция D3DXLoadVolumeFromFile

Загружает том из файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXLoadVolumeFromFile(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCTSTR           pSrcFile,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдестволуме* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Указатель на интерфейс [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) . Указывает целевой том.

</dd> <dt>

*пдестпалетте* \[ окне\]
</dt> <dd>

Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , целевую палитру 256 цветов или **значение NULL**.

</dd> <dt>

*пдестбокс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DBOX**](d3dbox.md) \***

Указатель на структуру [**D3DBOX**](d3dbox.md) . Задает поле назначения. Присвойте этому параметру **значение NULL** , чтобы указать весь том.

</dd> <dt>

*псркфиле* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Указатель на строку, указывающую имя файла. Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае строковый тип данных разрешается в LPCSTR. См. заметки.

</dd> <dt>

*псркбокс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DBOX**](d3dbox.md) \***

Указатель на структуру [**D3DBOX**](d3dbox.md) . Указывает поле источника. Присвойте этому параметру **значение NULL** , чтобы указать весь том.

</dd> <dt>

*Фильтр* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md), контролирующих фильтрацию изображения. Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.

</dd> <dt>

*ColorKey* \[ окне\]
</dt> <dd>

Тип: **[ **D3DCOLOR**](d3dcolor.md)**

Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey. Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения. Значение альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей. Таким образом, для непрозрачного черного значение будет равно 0xFF000000.

</dd> <dt>

*псрЦинфо* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***

Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) для заполнения описанием данных в исходном файле изображения или **значением NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Remarks

Параметр компилятора также определяет версию функции. Если определен Юникод, вызов функции разрешается в D3DXLoadVolumeFromFileW. В противном случае вызов функции разрешается в D3DXLoadVolumeFromFileA, так как используются строки ANSI.

Эта функция обрабатывает преобразование в форматы и из сжатых текстур и поддерживает следующие форматы файлов: .bmp, DDS, DIB, HDR, .jpg,. ПФМ, .png,. ppm и. tga. См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Запись на поверхность текстуры, не равную нулю, не приведет к обновлению «грязного» прямоугольника. Если вызывается **D3DXLoadVolumeFromFile** и текстура еще не была изменена (это маловероятно в нормальных сценариях использования), приложению необходимо явным образом вызвать [**IDirect3DVolumeTexture9:: адддиртибокс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) в текстуре тома.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[**D3DXLoadVolumeFromFileInMemory**](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[**D3DXLoadVolumeFromMemory**](d3dxloadvolumefrommemory.md)
</dt> <dt>

[**D3DXLoadVolumeFromResource**](d3dxloadvolumefromresource.md)
</dt> <dt>

[**D3DXLoadVolumeFromVolume**](d3dxloadvolumefromvolume.md)
</dt> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
