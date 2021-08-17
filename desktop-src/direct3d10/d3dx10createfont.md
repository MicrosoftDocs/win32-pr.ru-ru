---
description: Создает объект Font для устройства и шрифта. примечание. вместо использования этой функции рекомендуется использовать DirectWrite и библиотеку директкстк, класс спритефонт.
ms.assetid: a0dd02f1-c512-46d3-9e83-a785ac3ad7ee
title: Функция D3DX10CreateFont (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFont
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 396d0124d3edb79d6855c49f7d29f863fda6701a12678ab7712637b424bfbbc0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119370764"
---
# <a name="d3dx10createfont-function"></a>Функция D3DX10CreateFont

Создает объект Font для устройства и шрифта.

> [!Note]  
> вместо использования этой функции рекомендуется использовать [DirectWrite](../directwrite/direct-write-portal.md) и библиотеку [директкстк](https://github.com/Microsoft/DirectXTK) , класс **спритефонт** .

 

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10CreateFont(
  _In_  ID3D10Device *pDevice,
  _In_  INT          Height,
  _In_  UINT         Width,
  _In_  UINT         Weight,
  _In_  UINT         MipLevels,
  _In_  BOOL         Italic,
  _In_  UINT         CharSet,
  _In_  UINT         OutputPrecision,
  _In_  UINT         Quality,
  _In_  UINT         PitchAndFamily,
  _In_  LPCTSTR      pFaceName,
  _Out_ LPD3DX10FONT *ppFont
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Указатель на интерфейс ID3D10Device, устройство, связываемое с объектом Font.

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

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Кодировка шрифта.

</dd> <dt>

*АутпутпреЦисион* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

указывает, как Windows должны пытаться сопоставить желаемые размеры шрифта и характеристики с фактическими шрифтами. Используйте OUT \_ \_ только \_ преЦис для экземпляра, чтобы всегда получать шрифт TrueType.

</dd> <dt>

*Качество* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

указывает, как Windows должен соответствовать желаемому шрифту с реальным шрифтом. Он применяется только к растровым шрифтам и не должен влиять на шрифты TrueType.

</dd> <dt>

*Питчандфамили* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Индекс по высоте и семейству.

</dd> <dt>

*пфаценаме* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Строка, содержащая имя гарнитуры. Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае тип данных разрешается в LPCSTR. См. заметки.

</dd> <dt>

*ппфонт* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DX10FONT**](id3dx10font.md)\***

Возвращает указатель на интерфейс ID3DX10Font, представляющий созданный объект Font.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение S \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Параметр компилятора также определяет версию функции. Если определен Юникод, вызов функции разрешается в D3DXCreateFontW. В противном случае вызов функции разрешается в D3DXCreateFontA, так как используются строки ANSI.

Дополнительные сведения о параметрах шрифтов см. в разделе [логический шрифт](/previous-versions//ms533985(v=vs.85)).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции общего назначения](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
