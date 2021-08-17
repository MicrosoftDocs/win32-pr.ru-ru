---
description: Выполняет вычисление исходного радианцеа, полученного на основе одного отскока с переходом на использование адаптивной выборки.
ms.assetid: 61f8cecd-d95a-4f02-929e-02f2bce5bde9
title: 'Метод ID3DXPRTEngine:: Компутебаунцеадаптиве (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounceAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: efe983a0160d46910e7b8d1e29d0042d801275ef70aef30f6050e0538b6f9927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729753"
---
# <a name="id3dxprtenginecomputebounceadaptive-method"></a>Метод ID3DXPRTEngine:: Компутебаунцеадаптиве

Выполняет вычисление исходного радианцеа, полученного на основе одного отскока с переходом на использование адаптивной выборки. Этот метод создает новые вершины и грани в сети для более точного приближения к предварительно вычисленному сигналу передачи радианце (PRT). Этот метод можно использовать для любой освещенной сцены, включая модель PRT на основе сферического гармонического (SH).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ComputeBounceAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
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

Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) . Этот выходной буфер должен иметь правильное число цветовых каналов, выделенных для моделирования.

</dd> <dt>

*пдататотал* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на необязательный объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , сохраняющий сумму pData с каждым светло-возвратным вычислением. Может иметь **значение NULL**.

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

 

 
