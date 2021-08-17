---
description: Загружает том из памяти.
ms.assetid: 9f74fcc0-f935-4466-865b-e798711a1f2f
title: Функция D3DXLoadVolumeFromMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c473d5194a20a7de7e20d76fbde18d0a974ff8f314dc93822f57bfef2a4a6a5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122968"
---
# <a name="d3dxloadvolumefrommemory-function"></a>Функция D3DXLoadVolumeFromMemory

Загружает том из памяти.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXLoadVolumeFromMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcMemory,
  _In_       D3DFORMAT         SrcFormat,
  _In_       UINT              SrcRowPitch,
  _In_       UINT              SrcSlicePitch,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдестволуме* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Указатель на интерфейс [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) . Указывает целевой том, который получает образ.

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

*псркмемори* \[ окне\]
</dt> <dd>

Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**

Указатель на левый верхний угол исходного тома в памяти.

</dd> <dt>

*Сркформат* \[ окне\]
</dt> <dd>

Тип: **[D3DFORMAT](d3dformat.md)**

Член перечисляемого типа [D3DFORMAT](d3dformat.md) , являющийся форматом пикселей исходного тома.

</dd> <dt>

*Сркровпитч* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Шаг исходного изображения в байтах. Для форматов DXT (сжатых форматов текстур) это число должно представлять размер одной строки ячеек в байтах.

</dd> <dt>

*Сркслицепитч* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Шаг исходного изображения в байтах. Для форматов DXT (сжатых форматов текстур) это число должно представлять размер одного среза ячеек в байтах.

</dd> <dt>

*псркпалетте* \[ окне\]
</dt> <dd>

Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , исходную палитру 256 цветов или **значение NULL**.

</dd> <dt>

*псркбокс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DBOX**](d3dbox.md) \***

Указатель на структуру [**D3DBOX**](d3dbox.md) . Указывает поле источника. Значение **null** не является допустимым значением для этого параметра.

</dd> <dt>

*Фильтр* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией изображения. Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.

</dd> <dt>

*ColorKey* \[ окне\]
</dt> <dd>

Тип: **[ **D3DCOLOR**](d3dcolor.md)**

Значение [**D3DCOLOR**](d3dcolor.md) для замены на прозрачный черный или 0, чтобы отключить ColorKey. Это всегда 32-разрядный цвет ARGB, не зависящий от формата исходного изображения. Значение альфа имеет большое значение и обычно должно быть установлено в FF для непрозрачных цветовых ключей. Таким образом, для непрозрачного черного значение будет равно 0xFF000000.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Remarks

Запись на поверхность текстуры, не равную нулю, не приведет к обновлению «грязного» прямоугольника. Если вызывается **D3DXLoadVolumeFromMemory** и текстура еще не была изменена (это маловероятно в нормальных сценариях использования), приложению необходимо явным образом вызвать [**IDirect3DVolumeTexture9:: адддиртибокс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) в текстуре тома.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md)
</dt> <dt>

[**D3DXLoadVolumeFromResource**](d3dxloadvolumefromresource.md)
</dt> <dt>

[**D3DXLoadVolumeFromVolume**](d3dxloadvolumefromvolume.md)
</dt> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
