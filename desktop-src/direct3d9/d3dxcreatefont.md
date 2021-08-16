---
description: Создает объект Font для устройства и шрифта.
ms.assetid: 3e65dfdc-9608-420c-9672-c38289d13ab1
title: Функция D3DXCreateFont (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFont
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d9bac71e89657f4df176a1ee15e2dca0cda6e4a25b8c47560adc5cf26c982383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526158"
---
# <a name="d3dxcreatefont-function"></a>Функция D3DXCreateFont

Создает объект Font для устройства и шрифта.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateFont(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  INT               Height,
  _In_  UINT              Width,
  _In_  UINT              Weight,
  _In_  UINT              MipLevels,
  _In_  BOOL              Italic,
  _In_  DWORD             CharSet,
  _In_  DWORD             OutputPrecision,
  _In_  DWORD             Quality,
  _In_  DWORD             PitchAndFamily,
  _In_  LPCTSTR           pFacename,
  _Out_ LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , устройство, связываемое с объектом Font.

</dd> <dt>

*Высота* \[ окне\]
</dt> <dd>

Тип: **[ **int**](../winprog/windows-data-types.md)**

Высота символов в логических единицах.

</dd> <dt>

*Ширина* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Ширина символов в логических единицах.

</dd> <dt>

*Вес* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Толщина гарнитуры. Одним из примеров является полужирный.

</dd> <dt>

*Миплевелс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число уровней mipmap.

</dd> <dt>

*Курсив* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

True для курсивного шрифта; в противном случае — false.

</dd> <dt>

*CharSet* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Кодировка шрифта.

</dd> <dt>

*АутпутпреЦисион* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

указывает, как Windows должны пытаться сопоставить желаемые размеры шрифта и характеристики с фактическими шрифтами. Используйте OUT \_ \_ только \_ преЦис для экземпляра, чтобы всегда получать шрифт TrueType.

</dd> <dt>

*Качество* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

указывает, как Windows должен соответствовать желаемому шрифту с реальным шрифтом. Он применяется только к растровым шрифтам и не должен влиять на шрифты TrueType.

</dd> <dt>

*Питчандфамили* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Индекс по высоте и семейству.

</dd> <dt>

*пфаценаме* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Строка, содержащая имя гарнитуры. Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае строковый тип данных разрешается в LPCSTR. См. заметки.

</dd> <dt>

*ппфонт* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXFONT**](id3dxfont.md)\***

Возвращает указатель на интерфейс [**ID3DXFont**](id3dxfont.md) , представляющий созданный объект Font.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение S \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Для создания объекта ID3DXFont требуется, чтобы устройство поддерживало 32-разрядный цвет.

Параметр компилятора также определяет версию функции. Если определен Юникод, вызов функции разрешается в D3DXCreateFontW. В противном случае вызов функции разрешается в D3DXCreateFontA, так как используются строки ANSI.

Дополнительные сведения о параметрах шрифтов см. в разделе [логический шрифт](../gdi/creating-a-logical-font.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции общего назначения](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
