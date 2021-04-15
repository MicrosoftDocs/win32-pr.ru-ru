---
description: Создает текстуру из ресурса. Это более сложная функция, чем D3DXCreateTextureFromResource.
ms.assetid: 6015e2fa-9deb-4e6a-a401-f10fb05f40b7
title: Функция D3DXCreateTextureFromResourceEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 26298f8a63ccfde2171578c27e9208011c16dd28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547911"
---
# <a name="d3dxcreatetexturefromresourceex-function"></a>Функция D3DXCreateTextureFromResourceEx

Создает текстуру из ресурса. Это более сложная функция, чем [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    HMODULE            hSrcModule,
  _In_    LPCTSTR            pSrcResource,
  _In_    UINT               Width,
  _In_    UINT               Height,
  _In_    UINT               MipLevels,
  _In_    DWORD              Usage,
  _In_    D3DFORMAT          Format,
  _In_    D3DPOOL            Pool,
  _In_    DWORD              Filter,
  _In_    DWORD              MipFilter,
  _In_    D3DCOLOR           ColorKey,
  _Inout_ D3DXIMAGE_INFO     *pSrcInfo,
  _Out_   PALETTEENTRY       *pPalette,
  _Out_   LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой.

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

*Ширина* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Ширина в пикселях. Если это значение равно нулю или D3DX \_ по умолчанию, измерения берутся из файла.

</dd> <dt>

*Высота* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Высота в пикселях. Если это значение равно нулю или D3DX \_ по умолчанию, измерения берутся из файла.

</dd> <dt>

*Миплевелс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число запрошенных уровней MIP. Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap.

</dd> <dt>

*Использование* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

0, D3DUSAGE \_ рендертаржет или D3DUSAGE \_ dynamic. Установка этого флага в значение D3DUSAGE \_ рендертаржет указывает, что поверхность должна использоваться в качестве целевого объекта рендеринга. Затем ресурс можно передать в параметр *пневрендертаржет* метода [**сетрендертаржет**](/windows/desktop/api) . Если указано значение D3DUSAGE \_ рендертаржет или D3DUSAGE, для *пула* должно быть установлено значение D3DPOOL \_ по умолчанию, и приложение должно проверить, поддерживает ли устройство эту операцию, вызвав [**чеккдевицеформат**](/windows/desktop/api). D3DUSAGE \_ Dynamic указывает, что поверхность должна обрабатываться динамически. Дополнительные сведения об использовании динамических текстур см. в разделе [Оптимизация производительности (Direct3D 9)](performance-optimizations.md)с использованием динамических текстур.

</dd> <dt>

*Формат* \[ окне\]
</dt> <dd>

Тип: **[D3DFORMAT](d3dformat.md)**

Элемент перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий запрошенный формат пикселей для текстуры. Возвращаемая текстура может иметь другой формат, заданный в *формате*. Приложения должны проверять формат возвращенной текстуры. Если [D3DFMT \_ Unknown](other-d3dx-constants.md), то формат берется из файла. Если D3DFMT \_ из \_ файла, формат принимается точно так же, как в файле, и вызов завершается ошибкой, если это нарушает возможности устройства.

</dd> <dt>

*Пул* \[ окне\]
</dt> <dd>

Тип: **[ **D3DPOOL**](./d3dpool.md)**

Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура.

</dd> <dt>

*Фильтр* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения. Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.

</dd> <dt>

*Мипфилтер* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения. Указание D3DX \_ по умолчанию для этого параметра эквивалентно указанию \_ поля фильтра D3DX \_ .

</dd> <dt>

*ColorKey* \[ окне\]
</dt> <dd>

Тип: **[ **D3DCOLOR**](d3dcolor.md)**

Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey. Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения. Значение альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей. Таким образом, для непрозрачного черного значение будет равно 0xFF000000.

</dd> <dt>

*псрЦинфо* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***

Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) для заполнения описанием данных в исходном файле изображения или **значением NULL**.

</dd> <dt>

*ппалетте* \[ заполняет\]
</dt> <dd>

Тип: **[ **палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , представляющую 256-цветную палитру для заполнения или **null**.

</dd> <dt>

*пптекстуре* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Адрес указателя на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий созданный объект текстуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Параметр компилятора также определяет версию функции. Если определен Юникод, вызов функции разрешается в D3DXCreateTextureFromResourceExW. В противном случае вызов функции разрешается в D3DXCreateTextureFromResourceExA, так как используются строки ANSI.

Загружаемый ресурс должен иметь тип \_ Bitmap или "RT RCDATA" \_ . Тип ресурса RT \_ RCDATA используется для загрузки форматов, отличных от точечных рисунков (таких как. TGA,. jpg и. DDS).

Эта функция поддерживает следующие форматы файлов:. bmp,. DDS,. DIB,. HDR,. jpg,. ПФМ,. PNG,. ppm и. tga. См. раздел [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md)
</dt> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
