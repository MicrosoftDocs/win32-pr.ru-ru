---
description: 'Вычисление вектора перемещения, который сопоставляет источник радианце для выхода из радианце, полученного из рассеивания подповерхности, использование адаптивных свойств выборки и материала, заданных ID3DXPRTEngine:: Сетмешматериалс.'
ms.assetid: 34e42271-703b-4b67-8153-2eca3f8dde92
title: 'Метод ID3DXPRTEngine:: Компутессадаптиве (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSSAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a602566c4d0e5b3cb5c68b2f983b6c56a9d9f596ee673db97a72e6054837759b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847384"
---
# <a name="id3dxprtenginecomputessadaptive-method"></a>Метод ID3DXPRTEngine:: Компутессадаптиве

Вычисление вектора перемещения, который сопоставляет источник радианце для выхода из радианце, полученного из рассеивания подповерхности, использование адаптивных свойств выборки и материала, заданных [**ID3DXPRTEngine:: сетмешматериалс**](id3dxprtengine--setmeshmaterials.md). Метод создает новые вершины и грани в сети для более точного приближения к предварительно вычисленному сигналу передачи радианце (PRT). Этот метод можно использовать только для материалов, определенных для вершины в объекте сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ComputeSSAdaptive(
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

Минимальная длина грани, которая будет создана при адаптивной выборки. Если метод определяет, что значение слишком мало, задается зависящее от модели значение.

</dd> <dt>

*Макссубдив* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Максимальный уровень подраздела лица, который будет использоваться в адаптивной выборки. При нулевом значении указывается значение по умолчанию 4.

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

Чтобы смоделировать подложку, вызывайте этот метод для каждого освещения после вызова метода [**ID3DXPRTEngine:: компутедиректлигхтингшадаптиве**](id3dxprtengine--computedirectlightingshadaptive.md) .

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

[**ID3DXPRTEngine:: Компутебаунце**](id3dxprtengine--computebounce.md)
</dt> <dt>

[**ID3DXPRTEngine:: COMPUTE**](id3dxprtengine--computess.md)
</dt> </dl>

 

 
