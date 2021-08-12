---
description: 'Выполняет вычисление исходного радианцеа, полученного из рассеивания подповерхности, с помощью свойств материала, заданных ID3DXPRTEngine:: Сетмешматериалс. Этот метод можно использовать только для материалов, определенных для вершины в объекте сетки.'
ms.assetid: cdf0d9c1-70e3-44d5-b97a-0521e6739daf
title: 'Метод ID3DXPRTEngine:: Compute (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSS
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b34561bf96983506cbb0f484f273de9a5e0f0b6138db2e1ddbb92b19c8bcd18f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294024"
---
# <a name="id3dxprtenginecomputess-method"></a>Метод ID3DXPRTEngine:: COMPUTE

Выполняет вычисление исходного радианцеа, полученного из рассеивания подповерхности, с помощью свойств материала, заданных [**ID3DXPRTEngine:: сетмешматериалс**](id3dxprtengine--setmeshmaterials.md). Этот метод можно использовать только для материалов, определенных для вершины в объекте сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ComputeSS(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на входной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , представляющий трехмерный объект из предыдущего освещения. Этот входной буфер должен иметь правильное число цветовых каналов, выделенных для моделирования.

</dd> <dt>

*pData* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , моделирующий один элемент отскока точечной светлой поверхности. Этот выходной буфер должен иметь правильное число цветовых каналов, выделенных для моделирования.

</dd> <dt>

*пдататотал* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на необязательный объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , который является выполняющейся суммой всех предыдущих выходов pData. Может иметь **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Чтобы смоделировать подложку, вызывайте этот метод для каждого освещения после вызова метода ID3DXPRTEngine:: Компутедиректлигхтинг.

Используйте следующую последовательность вызовов для моделирования рассеивания подповерхности.


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
    
hr = m_pPRTEngine->ComputeDirectLightingSH( SHOrder, pDataA );
    
// *pDataC should be set to zero. The ComputeSS call will add together the    
// direct lighting results from pDataA for non-subsurface scattering elements   
// and subsurface scattering results for the subsurface scattering elements.
    
hr = m_pPRTEngine->ComputeSS( pDataA, pDataB, pDataC );
if ( FAILED( hr ) ) goto Exit;
```



Выходные данные этого метода не включают албедо, и в симуляторе встроена только входящая лампочка. Не умножая албедо, вы можете моделировать албедо вариации на более точном масштабе, чем исходный радианце, тем самым обеспечивая более точные результаты сжатия.

Вызовите метод [**ID3DXPRTEngine:: мултиплялбедо**](id3dxprtengine--multiplyalbedo.md) , чтобы умножить каждый предварительно вычисленный вектор перемещения РАДИАНЦЕ (PRT) на албедо.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: Компутебаунце**](id3dxprtengine--computebounce.md)
</dt> </dl>

 

 




