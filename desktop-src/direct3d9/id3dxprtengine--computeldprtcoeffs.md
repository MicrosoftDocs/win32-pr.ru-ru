---
description: Выполняет вычисление локально-определяемых предварительно вычисляемых радианценых перенаправлений (ЛДПРТ), относящихся к образцу обычных векторов, чтобы избежать ошибок с наименьшими квадратами по отношению к входным ID3DXPRTBuffer данным.
ms.assetid: 302c20cd-d495-4a23-9692-7456355471eb
title: 'Метод ID3DXPRTEngine:: Компутелдпрткоеффс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeLDPRTCoeffs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 351ecb8022e06b1a5a24abad8fa8541798d13ba0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714030"
---
# <a name="id3dxprtenginecomputeldprtcoeffs-method"></a>Метод ID3DXPRTEngine:: Компутелдпрткоеффс

Выполняет вычисление локально-определяемых предварительно вычисляемых радианценых перенаправлений (ЛДПРТ), относящихся к образцу обычных векторов, чтобы избежать ошибок с наименьшими квадратами по отношению к входным [**ID3DXPRTBuffer**](id3dxprtbuffer.md) данным. Эти коэффициенты можно использовать с обложками или преобразованными векторами, чтобы моделировать глобальные эффекты для динамических объектов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ComputeLDPRTCoeffs(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      UINT            Order,
  [in, out] D3DXVECTOR3     *pNormOut,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на входный объект данных радианце (PRT), который является [**ID3DXPRTBufferным**](id3dxprtbuffer.md) (SH).

</dd> <dt>

*Порядок следования* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Порядок вычисления SH. Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно. При оценке создается коэффициент порядка ². Степень оценки — Order-1.

</dd> <dt>

*пнормаут* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Необязательный Векторный массив, который должен быть заполнен с помощью оптимальных векторов нормали, для которых оптимизированы коэффициенты ЛДПРТ. Этот массив должен иметь тот же размер, что и число выборок в pData. Если **значение равно NULL**, используются векторы нормали Surface.

</dd> <dt>

*pData* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , содержащий количество коэффициентов гармониой зональныеа для каждого цветового канала на выборку.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

При необходимости можно получить решения для заливки обычных векторов с помощью этого метода. Эти обычные векторы, вместе с коэффициентами ЛДПРТ, могут точнее представлять сигнал PRT. В этом случае коэффициенты представляют гармонические зональные, ориентированные на нормальное направление.

Этот метод не может использоваться с результатами из [**ID3DXPRTEngine:: компутесурфсамплесбаунце**](id3dxprtengine--computesurfsamplesbounce.md) или [**ID3DXPRTEngine:: компутесурфсамплесдиректш**](id3dxprtengine--computesurfsamplesdirectsh.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
