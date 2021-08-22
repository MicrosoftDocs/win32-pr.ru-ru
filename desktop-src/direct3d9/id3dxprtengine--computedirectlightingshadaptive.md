---
description: Вычисление вклада прямого освещения в трехмерные объекты, в которых источник радианце представлен аппроксимацией (SH) с использованием адаптивной выборки.
ms.assetid: 792d8460-d608-4384-ac1c-556435074580
title: 'Метод ID3DXPRTEngine:: Компутедиректлигхтингшадаптиве (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 991337b31b10c39cccb622c2838bd53bcb25ad534ae8f896b6ec8f4842072de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801284"
---
# <a name="id3dxprtenginecomputedirectlightingshadaptive-method"></a>Метод ID3DXPRTEngine:: Компутедиректлигхтингшадаптиве

Вычисление вклада прямого освещения в трехмерные объекты, в которых источник радианце представлен аппроксимацией (SH) с использованием адаптивной выборки. Этот метод создает новые вершины и грани в сети для более точного приближения к предварительно вычисленному сигналу передачи радианце (PRT).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ComputeDirectLightingSHAdaptive(
  [in]      UINT            Order,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Порядок следования* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Порядок вычисления SH. Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно. При оценке создается коэффициент порядка ². Степень оценки — Order-1.

</dd> <dt>

*Адаптивесреш* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Пороговое значение для вектора PRT, используемого для подразделения вершин сетки и граней. Если значение параметра меньше 1E-6F, то указывается по умолчанию параметр 1E-6f.

</dd> <dt>

*Минеджеленгс* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Минимальная длина грани, которая будет создана при адаптивной выборки. Если метод определяет, что значение слишком мало, задается зависящее от модели значение. При нулевом значении указывается значение по умолчанию 4.

</dd> <dt>

*Макссубдив* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Максимальный уровень подраздела лица, который будет использоваться в адаптивной выборки.

</dd> <dt>

*pData* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) . Этот буфер должен иметь правильное число цветовых каналов, выделенных для имитации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: Робустмешрефине**](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
