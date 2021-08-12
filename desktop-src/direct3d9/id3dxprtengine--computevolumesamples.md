---
description: Выдает проекцию прямого освещения, полученного от предыдущего света, в виде векторов, представляющих собой сферическую гармонию (SH), которые представляют радианце инцидентов в указанных местах.
ms.assetid: ccde7c59-cb82-4d61-822a-e1e9ecea0a28
title: 'Метод ID3DXPRTEngine:: Компутеволумесамплес (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamples
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edc13e8b6f0e5c725e957be22f1b297f825a4f3b622ced68adf19b34a0b64b5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293505"
---
# <a name="id3dxprtenginecomputevolumesamples-method"></a>Метод ID3DXPRTEngine:: Компутеволумесамплес

Выдает проекцию прямого освещения, полученного от предыдущего света, в виде векторов, представляющих собой сферическую гармонию (SH), которые представляют радианце инцидентов в указанных местах.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ComputeVolumeSamples(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            Order,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псурфдатаин* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на входной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , представляющий трехмерный объект из предыдущего освещения.

</dd> <dt>

*Порядок следования* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Порядок вычисления SH. Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно. При оценке создается коэффициент порядка ². Степень оценки — Order-1.

</dd> <dt>

*NumVolSamples.xml* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число расположений выборки.

</dd> <dt>

*псамплелокс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Расположение для каждого образца. Если Псамплелокс имеет **значение NULL**, компутеволумесамплес вычислит матрицы перемещения на каждой вершине сетки. Однако, если Псамплелокс не равен **null**, необходимо выделать выборку через сферу (Set Усесфере = **true** и Усекосине = **false** в [**ID3DXPRTEngine:: сетсамплингинфо**](id3dxprtengine--setsamplinginfo.md)); в противном случае Компутеволумесамплес вернет D3DERR \_ инвалидкалл.

</dd> <dt>

*pData* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , который проецирует прямое освещение от предыдущего света, в векторы на основе SH. Этот буфер должен иметь правильное число цветовых каналов, выделенных для имитации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Этот метод выполняет вычисление того, как освещение от исходной функции радианце отражается на поверхности, представляющей сцену (Псурфдатаин), и приходится на каждую точку в пространстве, указанную Псамплелокс. Коэффициенты SH представляют сопоставление (в каждой точке Псамплелокс) источника радианце с передачей радианце инцидента.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: Компутеволумесамплесдиректш**](id3dxprtengine--computevolumesamplesdirectsh.md)
</dt> </dl>

 

 
