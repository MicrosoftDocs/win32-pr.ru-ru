---
description: Выполняет вычисление предварительно вычисленных радианце передач (PRT) для произвольной точки (и обычного вектора).
ms.assetid: 862a9067-5c5e-4428-86f4-ebef653411b9
title: 'Метод ID3DXPRTEngine:: Компутесурфсамплесбаунце (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 55cea3e87850273b6ea8d190422bd77afeb831f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356053"
---
# <a name="id3dxprtenginecomputesurfsamplesbounce-method"></a>Метод ID3DXPRTEngine:: Компутесурфсамплесбаунце

Выполняет вычисление предварительно вычисленных радианце передач (PRT) для произвольной точки (и обычного вектора).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ComputeSurfSamplesBounce(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut,
  [in, out]       LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псурфдатаин* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на входной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , представляющий исходный радианце трехмерного объекта. Этот входной буфер должен иметь правильное число цветовых каналов, выделенных для моделирования.

</dd> <dt>

*Нумсамплес* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число расположений выборки.

</dd> <dt>

*псамплелокс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Расположение для каждого образца.

</dd> <dt>

*псампленормс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Стандартный вектор для каждого расположения выборки.

</dd> <dt>

*pData* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , моделирующий прямое освещение в точке, с использованием аппроксимации «сферический гармонией» (SH).

</dd> <dt>

*пдататотал* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на необязательный объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , который является выполняющейся суммой всех предыдущих выходов pData. Может иметь **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: Компутесурфсамплесдиректш**](id3dxprtengine--computesurfsamplesdirectsh.md)
</dt> </dl>

 

 
