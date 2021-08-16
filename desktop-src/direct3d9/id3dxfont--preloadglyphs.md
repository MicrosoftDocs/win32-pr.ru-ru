---
description: Загружает ряд глифов в видеопамять для повышения эффективности отрисовки на устройстве.
ms.assetid: df023359-bcb3-4c05-950b-19cdeba97c85
title: 'ID3DXFont: метод:P Релоадглифс (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadGlyphs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ea422a6e0b0ecfda6b4eb03a0636eb013d8c840c96cec6f1c482589de29f3c76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563934"
---
# <a name="id3dxfontpreloadglyphs-method"></a>ID3DXFont: метод:P Релоадглифс

Загружает ряд глифов в видеопамять для повышения эффективности отрисовки на устройстве.

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

Глифы не будут отображаться на устройстве; Для отрисовки глифов необходимо по-прежнему вызывать [**DrawText**](id3dxfont--drawtext.md) . Однако предварительная загрузка глифов в видеопамять **DrawText** будет использовать значительно меньше ресурсов ЦП.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
