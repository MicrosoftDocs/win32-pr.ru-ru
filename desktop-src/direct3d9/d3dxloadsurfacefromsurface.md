---
description: Загружает поверхность из другой поверхности с помощью преобразования цвета.
ms.assetid: eddb420d-fd32-4c09-afec-435887c4e905
title: Функция D3DXLoadSurfaceFromSurface (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28f239fb57ec0bccec120c5b2ea493a094e9cc6acc5b47fb19e9f7495ecde46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495314"
---
# <a name="d3dxloadsurfacefromsurface-function"></a>Функция D3DXLoadSurfaceFromSurface

Загружает поверхность из другой поверхности с помощью преобразования цвета.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXLoadSurfaceFromSurface(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPDIRECT3DSURFACE9 pSrcSurface,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдестсурфаце* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Указатель на интерфейс [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) . Задает поверхность назначения, которая получает изображение.

</dd> <dt>

*пдестпалетте* \[ окне\]
</dt> <dd>

Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , целевую палитру 256 цветов или **значение NULL**.

</dd> <dt>

*пдестрект* \[ окне\]
</dt> <dd>

Тип: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) . Задает прямоугольник назначения. Присвойте этому параметру **значение NULL** , чтобы указать всю поверхность.

</dd> <dt>

*псрксурфаце* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Указатель на интерфейс [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , представляющий поверхность источника.

</dd> <dt>

*псркпалетте* \[ окне\]
</dt> <dd>

Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , исходную палитру 256 цветов или **значение NULL**.

</dd> <dt>

*псркрект* \[ окне\]
</dt> <dd>

Тип: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) . Задает исходный прямоугольник. Присвойте этому параметру **значение NULL** , чтобы указать всю поверхность.

</dd> <dt>

*Фильтр* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md), управляющих фильтром изображения. Указание D3DX \_ по умолчанию для этого параметра является аналогом задания фильтра D3DX \_ \_ D3DX- \| \_ \_ дизеринга Filter.

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

Эта функция обрабатывает преобразование в форматы сжатой текстуры и из них.

Запись на поверхность без выравнивания не приведет к обновлению «грязного» прямоугольника. Если вызывается **D3DXLoadSurfaceFromSurface** и поверхность не была изменена (это маловероятно в нормальных сценариях использования), приложению необходимо явно вызвать [**адддиртирект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) на поверхности.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
