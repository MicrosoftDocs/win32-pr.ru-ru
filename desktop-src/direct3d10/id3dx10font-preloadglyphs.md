---
description: Загрузка ряда глифов в видеопамять для повышения эффективности отрисовки на устройстве.
ms.assetid: 7d063d52-af2c-44a6-9019-3d546acfbd4a
title: 'ID3DX10Font: метод:P Релоадглифс (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadGlyphs
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 358523135db83f2ec7f973fce403a44d2f0ece82ab60cf9527cb612ccde61e49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540340"
---
# <a name="id3dx10fontpreloadglyphs-method"></a>ID3DX10Font: метод:P Релоадглифс

Загрузка ряда глифов в видеопамять для повышения эффективности отрисовки на устройстве.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Сначала* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор первого глифа, который будет загружен в видеопамять.

</dd> <dt>

*Последний раз* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор последнего глифа, который будет загружен в видеопамять.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Remarks

Этот метод создает текстуры, которые содержат глифы входных данных. Глифы рисуются в виде ряда треугольников.

Глифы не будут отображаться на устройстве; ID3DX10Font: для отрисовки глифов необходимо по-прежнему вызывать метод:D Равтекст. Однако предварительная загрузка глифов в видеопамять ID3DX10Font::D Равтекст будет использовать значительно меньше ресурсов ЦП.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
