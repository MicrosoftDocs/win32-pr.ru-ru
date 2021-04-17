---
description: Использует графический процессор для расчета вклада прямого освещения в трехмерные объекты, в которых исходный радианце представлен аппроксимацией по негармоническому излучению (SH). Вычисление освещения в GPU обычно выполняется гораздо быстрее, чем в ЦП.
ms.assetid: ccea5a5e-23f1-4fdf-bce8-9bfc35d45257
title: 'Метод ID3DXPRTEngine:: Компутедиректлигхтингшгпу (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHGPU
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56dd807d28ba6952cd20c971b675b83687a3015
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674759"
---
# <a name="id3dxprtenginecomputedirectlightingshgpu-method"></a>Метод ID3DXPRTEngine:: Компутедиректлигхтингшгпу

Использует графический процессор для расчета вклада прямого освещения в трехмерные объекты, в которых исходный радианце представлен аппроксимацией по негармоническому излучению (SH). Вычисление освещения в GPU обычно выполняется гораздо быстрее, чем в ЦП.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ComputeDirectLightingSHGPU(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in]      UINT              Flags,
  [in]      UINT              Order,
  [in]      FLOAT             ZBias,
  [in]      FLOAT             ZAngleBias,
  [in, out] LPD3DXPRTBUFFER   pDataOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на объект устройства [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , используемый для моделирования GPU. Устройство должно поддерживать шейдеры [PS \_ 2 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) пикселей.

> [!Note]  
> Функции обратного вызова не должны использовать объект устройства [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , используемый симулятором GPU.

 

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Параметр моделирования GPU, определяющий разрешение теневого z-буфера. Необходимо задать одно из значений констант из [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md). Чтобы задать модель с более высокой точностью, \_ значение D3DXSHGPUSIMOPT хигхкуалити может быть объединено с одним из \_ значений D3DXSHGPUSIMOPT шадоврескскскс.

</dd> <dt>

*Порядок следования* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Порядок вычисления SH. Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно. При оценке создается коэффициент порядка ². Степень оценки — Order-1.

</dd> <dt>

*Збиас* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Смещение в нормальном направлении.

</dd> <dt>

*Занглебиас* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Сдвиг в нормальном направлении с масштабированием на один минус косинус угла с голубым лучом.

</dd> <dt>

*pData* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) . Этот буфер должен иметь правильное число цветовых каналов, выделенных для имитации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

В этом методе албедо не умножается на сигнал освещения, и в симуляторе встроена только входящая лампочка. Не умножая албедо, вы можете моделировать албедо вариации на более точном масштабе, чем исходный радианце, тем самым обеспечивая более точные результаты сжатия.

Вызовите [**мултиплялбедо**](id3dxprtengine--multiplyalbedo.md) , чтобы умножить каждый предварительно вычисленный вектор перемещения РАДИАНЦЕ (PRT) на албедо.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
