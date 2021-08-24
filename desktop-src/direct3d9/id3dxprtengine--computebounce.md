---
description: Выполняет вычисление исходного радианцеа, полученного на основе одного отскока с переходом. Этот метод можно использовать для любой освещенной сцены, включая модель предварительно вычисленных радианце (PRT) на основе сферического гармонического (SH).
ms.assetid: 91a6b503-acd2-459b-9d60-de68c879c61b
title: 'Метод ID3DXPRTEngine:: Компутебаунце (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cc4f362555c8cc86857733ecc3e75279dc68cc6b339f641f70c592f0e3576a96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847424"
---
# <a name="id3dxprtenginecomputebounce-method"></a>Метод ID3DXPRTEngine:: Компутебаунце

Выполняет вычисление исходного радианцеа, полученного на основе одного отскока с переходом. Этот метод можно использовать для любой освещенной сцены, включая модель предварительно вычисленных радианце (PRT) на основе сферического гармонического (SH).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ComputeBounce(
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

Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , моделирующий один элемент отскока на перенаправленном свете. Этот выходной буфер должен иметь правильное число цветовых каналов, выделенных для моделирования.

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

Используйте следующую последовательность вызова, чтобы смоделировать несколько световых отскоков с прямым освещением.


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;

ComputeDirectLightingSH( SHOrder, pDataA );
// The accumulation buffer, pDataC, needs to be 
// initialized to the direct lighting result.

pDataC->AddBuffer( pDataA );
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // first bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // second bounce
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // third bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // fourth bounce
```



Используйте следующую последовательность вызова, чтобы смоделировать несколько источников падения яркости с помощью геоточечной подповерхности.


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
ComputeDirectLightingSH( SHOrder, pDataA );

// *pDataC should be set to zero. The ComputeSS call will add together     
// the direct lighting results from pDataA for non-subsurface scattering 
// elements and subsurface scattering results for the subsurface scattering
// elements. Perform proper error handling for each call.
    
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // first bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // second bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
```



Выходные данные этого метода не включают албедо, и в симуляторе встроена только входящая лампочка. Не умножая албедо, вы можете моделировать албедо вариации на более точном масштабе, чем исходный радианце, тем самым обеспечивая более точные результаты сжатия.

Вызовите метод [**ID3DXPRTEngine:: мултиплялбедо**](id3dxprtengine--multiplyalbedo.md) , чтобы умножить каждый вектор PRT на албедо.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: COMPUTE**](id3dxprtengine--computess.md)
</dt> </dl>

 

 




