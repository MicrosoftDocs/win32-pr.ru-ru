---
title: Структура CD3DX12_ROOT_DESCRIPTOR (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ \_ структуры дескриптора корня D3D12.
ms.assetid: DB05BAB7-DD30-4EC7-8D66-C0B2D8DD7BAC
keywords:
- Структура CD3DX12_ROOT_DESCRIPTOR
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710064436e0287b570700ff5812b728ca62be56d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713972"
---
# <a name="cd3dx12_root_descriptor-structure"></a>\_ \_ Структура дескриптора корня CD3DX12

Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ \_ дескриптора корня D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_ROOT_DESCRIPTOR  : public D3D12_ROOT_DESCRIPTOR{
       CD3DX12_ROOT_DESCRIPTOR();
       explicit CD3DX12_ROOT_DESCRIPTOR(const D3D12_ROOT_DESCRIPTOR &o);
       CD3DX12_ROOT_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Корневой \_ дескриптор CD3DX12 ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ \_ дескриптора CD3DX12 root.

</dd> <dt>

**явный CD3DX12 \_ корневого \_ дескриптора (const D3D12 \_ root \_ дескриптора &o)**
</dt> <dd>

Создает новый экземпляр \_ \_ дескриптора root CD3DX12, инициализированного с содержимым другой структуры [**\_ \_ дескриптора root D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .

</dd> <dt>

**\_Корневой \_ дескриптор CD3DX12 (uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0)**
</dt> <dd>

Создает новый экземпляр \_ корневого \_ дескриптора CD3DX12, инициализируя следующие параметры:

UINT Шадеррегистер

участие UINT Регистерспаце = 0

</dd> <dt>

**Inline init (UINT Шадеррегистер, UINT Регистерспаце = 0)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

UINT Шадеррегистер

участие UINT Регистерспаце = 0

</dd> <dt>

**static Inline init (D3D12 \_ root \_ дескриптора таблицы &, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ Таблица &КОРНЕВого \_ дескриптора**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)

UINT Шадеррегистер

участие UINT Регистерспаце = 0

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Дескриптор корня \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





