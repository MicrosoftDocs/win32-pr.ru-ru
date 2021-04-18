---
description: Фильтрует mipmap уровни текстуры.
ms.assetid: bfeae9b0-9480-4a26-a225-4a34780546ce
title: Функция D3DXFilterTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFilterTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8a0d1c211b50379451c8b04830e9c97fe988137
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713691"
---
# <a name="d3dxfiltertexture-function"></a>Функция D3DXFilterTexture

Фильтрует mipmap уровни текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXFilterTexture(
  _In_        LPDIRECT3DBASETEXTURE9 pBaseTexture,
  _Out_ const PALETTEENTRY           *pPalette,
  _In_        UINT                   SrcLevel,
  _In_        DWORD                  MipFilter
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбасетекстуре* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Указатель на интерфейс [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) , представляющий объект текстуры для фильтрации.

</dd> <dt>

*ппалетте* \[ заполняет\]
</dt> <dd>

Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , которая представляет цветовую палитру 256 для заполнения, или **значение NULL** для форматов нонпалеттизед. Если палитра не указана, предоставляется палитра Direct3D по умолчанию (вся непрозрачная белая палитра). См. заметки.

</dd> <dt>

*Срклевел* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Уровень, изображение которого используется для создания последующих уровней. Указание D3DX \_ по умолчанию для этого параметра эквивалентно указанию значения 0.

</dd> <dt>

*Мипфилтер* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией mipmap. Указание D3DX \_ по умолчанию для этого параметра эквивалентно указанию \_ поля фильтра D3DX \_ , если размер текстуры является степенью числа 2, а \_ D3DX \_ поле \| фильтра \_ D3DX \_ — в противном случае.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Комментарии

Фильтр рекурсивно применяется к каждому уровню текстуры для создания следующего уровня текстуры.

Запись в текстуру без выравнивания на поверхности текстуры не приведет к обновлению «грязного» прямоугольника. Если вызывается **D3DXFilterTexture** и поверхность не была изменена (это маловероятно в нормальных сценариях использования), приложению необходимо явно вызвать [**адддиртирект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) для текстуры.

Текстуры, созданные в пуле по умолчанию (D3DPOOL \_ по умолчанию), нельзя использовать с **D3DXFilterTexture** (если только не создан с \_ динамическим D3DUSAGE), так как для объекта требуется операция блокировки. Обратите внимание, что блокировки в пуле по умолчанию запрещены для текстур (если они не являются динамическими).

Дополнительные сведения о [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)см. в разделе пакет SDK для платформы. Обратите внимание, что начиная с DirectX 8,0, член Пефлагс структуры **палеттинтри** не работает, как описано в пакете Platform SDK. Теперь элемент Пефлагс является альфа-каналом для 8 – разрядных форматов палеттизед.

Существует только одна функция фильтрации текстур, но два макроса, которые вызывают этот метод.


```
#define D3DXFilterCubeTexture D3DXFilterTexture
#define D3DXFilterVolumeTexture D3DXFilterTexture
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
