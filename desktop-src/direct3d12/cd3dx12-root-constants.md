---
title: Структура CD3DX12_ROOT_CONSTANTS (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ структуры корневых \_ констант D3D12.
ms.assetid: 2F517DCE-BC0C-4678-9C25-D826036F99A8
keywords:
- Структура CD3DX12_ROOT_CONSTANTS
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_CONSTANTS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a1f81a429b083400adad60f316cc90c4ede1d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713510"
---
# <a name="cd3dx12_root_constants-structure"></a>\_Структура корневых \_ констант CD3DX12

Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ корневых \_ констант D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_ROOT_CONSTANTS  : public D3D12_ROOT_CONSTANTS{
       CD3DX12_ROOT_CONSTANTS();
       explicit CD3DX12_ROOT_CONSTANTS(const D3D12_ROOT_CONSTANTS &o);
       CD3DX12_ROOT_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_ \_ Константы CD3DX12 root ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ \_ константы CD3DX12 root.

</dd> <dt>

**явные \_ \_ константы CD3DX12 (const D3D12 \_ root \_ константы &o)**
</dt> <dd>

Создает новый экземпляр \_ \_ константы CD3DX12 root, который инициализируется содержимым другой структуры [**\_ \_ констант D3D12 root**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .

</dd> <dt>

**\_ \_ Константы CD3DX12 root (uint NUM32BITVALUES, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0)**
</dt> <dd>

Создает новый экземпляр \_ \_ константы CD3DX12 root, инициализируя следующие параметры:

UINT num32BitValues

UINT Шадеррегистер

участие UINT Регистерспаце = 0

</dd> <dt>

**Inline init (UINT num32BitValues, UINT Шадеррегистер, UINT Регистерспаце = 0)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

UINT num32BitValues

UINT Шадеррегистер

участие UINT Регистерспаце = 0

</dd> <dt>

**Статическая встроенная init (D3D12 \_ root- \_ константы &РУТКОНСТАНТС, uint NUM32BITVALUES, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ КОРНЕВые \_ константы**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &рутконстантс

UINT num32BitValues

UINT Шадеррегистер

участие UINT Регистерспаце = 0

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ Константы D3D12 root**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





