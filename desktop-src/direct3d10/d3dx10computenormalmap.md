---
description: Преобразует карту высоты в обычную карту. Компоненты (x, y, z) каждой нормальной версии сопоставляются с каналами (r, g, b) выходной текстуры.
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: Функция D3DX10ComputeNormalMap (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ComputeNormalMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1d7318e6d00d921ba0d573eb6fb696eed6c6a58d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713761"
---
# <a name="d3dx10computenormalmap-function"></a>Функция D3DX10ComputeNormalMap

Преобразует карту высоты в обычную карту. Компоненты (x, y, z) каждой нормальной версии сопоставляются с каналами (r, g, b) выходной текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10ComputeNormalMap(
  _In_ ID3D10Texture2D *pSrcTexture,
  _In_ UINT            Flags,
  _In_ UINT            Channel,
  _In_ FLOAT           Amplitude,
  _In_ ID3D10Texture2D *pDestTexture
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псрктекстуре* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Указатель на интерфейс ID3D10Texture2D, представляющий текстуру исходной карты с высотой.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Один или несколько \_ флагов НОРМАЛМАП D3DX, управляющих созданием обычных карт.

</dd> <dt>

*Канал* \[ связи окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Один \_ флаг канала D3DX, указывающий источник сведений о высоте.

</dd> <dt>

*Амплитуда* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Коэффициент величины постоянного значения, увеличивающий (или уменьшающий) значения в нормальном сопоставлении. Более высокие значения обычно делают выпуклости более видимыми, а более низкие значения обычно делают невидимыми более выпуклости.

</dd> <dt>

*пдесттекстуре* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Указатель на интерфейс ID3D10Texture2D, представляющий текстуру назначения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может иметь следующее значение: D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Этот метод рассчитывает нормальную работу, используя Центральное различие с размером ядра 3X3. Каналы RGB в назначении содержат смещенные компоненты (x, y, z) нормали. Центральный разностный знаменатель жестко закодирован в 2,0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции текстуры в D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
