---
description: Включает или отключает оптимизацию ЦП.
ms.assetid: 6f73df12-f2fc-4651-b0f7-f7a55e534d3d
title: Функция D3DXCpuOptimizations (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCpuOptimizations
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a0ef276e6d3303acd77c9580b55a9aa49dbe2087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821292"
---
# <a name="d3dxcpuoptimizations-function"></a>Функция D3DXCpuOptimizations

Включает или отключает оптимизацию ЦП.

## <a name="syntax"></a>Синтаксис


```C++
D3DX_CPU_OPTIMIZATION D3DXCpuOptimizations(
  _In_ BOOL Enable
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Включить* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

**Значение true** , чтобы включить оптимизацию ЦП; в противном случае — **false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **\_ \_ Оптимизация ЦП D3DX**](d3dx-cpu-optimization.md)**

Возвращает тип обнаруженного ЦП, для которого существуют оптимизации (см. раздел [**\_ \_ Оптимизация ЦП D3DX**](d3dx-cpu-optimization.md)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
