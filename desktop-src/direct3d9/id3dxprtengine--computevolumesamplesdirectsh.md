---
description: Выполняет проекцию неудаленного освещения на основе географических (SH) векторов, представляющих радианце инцидентов в указанных местах.
ms.assetid: 4d07b288-aec1-48eb-8d27-f3d7d8cfb69e
title: 'Метод ID3DXPRTEngine:: Компутеволумесамплесдиректш (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3aaa8f9332a80e35ffde43d145be1ed885caeaca6d61e4eb9190baba09b73ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747764"
---
# <a name="id3dxprtenginecomputevolumesamplesdirectsh-method"></a>Метод ID3DXPRTEngine:: Компутеволумесамплесдиректш

Выполняет проекцию неудаленного освещения на основе географических (SH) векторов, представляющих радианце инцидентов в указанных местах.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ComputeVolumeSamplesDirectSH(
  [in]            UINT            OrderIn,
  [in]            UINT            OrderOut,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Порядок* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Порядок представления SH с удаленным освещением. Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно. Степень оценки — Ordering-1.

</dd> <dt>

*Заказ* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Порядок представления SH для локального освещения. Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно. Степень оценки — Ordering-1.

</dd> <dt>

*NumVolSamples.xml* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число расположений выборки.

</dd> <dt>

*псамплелокс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Расположение для каждого образца.

</dd> <dt>

*pData* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , который проецирует удаленное освещение в векторы экземпляра sh. Этот буфер должен иметь правильное число цветовых каналов, выделенных для имитации. Этот метод создает упорядочение с сортировкой \* по убыванию на канал в каждом месте выборки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Этот метод выполняет вычисление того, как освещение от внешнего источника достигает каждой точки в пространстве, заданном параметром Псамплелокс. Коэффициенты SH представляют сопоставление (в каждой точке Псамплелокс) источника радианце с передачей радианце инцидента.

Чтобы успешно использовать этот метод, необходимо задать выборку для сферы с Усесфере = **true** и Усекосине = **false** в [**ID3DXPRTEngine:: сетсамплингинфо**](id3dxprtengine--setsamplinginfo.md); в противном случае этот метод возвратит ошибку с D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: Компутеволумесамплес**](id3dxprtengine--computevolumesamples.md)
</dt> </dl>

 

 
