---
title: Структура CD3DX12_RESOURCE_BARRIER (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ \_ структуру барьера ресурсов D3D12.
ms.assetid: 89E0F38C-8802-46E6-9583-95C5D853CD99
keywords:
- Структура CD3DX12_RESOURCE_BARRIER
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_BARRIER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eaa9b19a8bc7dcebba5982313bb362dbcee6157
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713978"
---
# <a name="cd3dx12_resource_barrier-structure"></a>\_ \_ Структура барьера ресурсов CD3DX12

Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ барьера ресурсов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_RESOURCE_BARRIER  : public D3D12_RESOURCE_BARRIER{
                           CD3DX12_RESOURCE_BARRIER();
                           explicit CD3DX12_RESOURCE_BARRIER(const D3D12_RESOURCE_BARRIER &o);
  CD3DX12_RESOURCE_BARRIER static inline Transition(ID3D12Resource* pResource, D3D12_RESOURCE_STATES stateBefore, D3D12_RESOURCE_STATES stateAfter, UINT subresource = D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES, D3D12_RESOURCE_BARRIER_FLAGS flags = D3D12_RESOURCE_BARRIER_FLAG_NONE);
  CD3DX12_RESOURCE_BARRIER static inline Aliasing(ID3D12Resource* pResourceBefore, ID3D12Resource* pResourceAfter);
  CD3DX12_RESOURCE_BARRIER static inline UAV(ID3D12Resource* pResource);
                           operator const D3D12_RESOURCE_BARRIER&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Барьер ресурсов CD3DX12 \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ \_ барьера ресурсов CD3DX12.

</dd> <dt>

**явное CD3DX12 \_ Resource \_ барьер (const D3D12 \_ Resource \_ барьер &o)**
</dt> <dd>

Создает новый экземпляр \_ \_ барьера ресурсов CD3DX12, инициализированного с содержимым другого [**\_ \_ барьера ресурсов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier).

</dd> <dt>

**статический встроенный переход (ID3D12Resource \* , D3D12, \_ состояния ресурсов, \_ статебефоре, D3D12 \_ состояний ресурсов \_ статеафтер, uint Resources = D3D12 \_ Resource \_ барьер \_ все \_ подресурсы, D3D12 флаги \_ \_ \_ flags барьера = D3D12 \_ Resource барьер Flag \_ \_ \_ None)**
</dt> <dd>

Переходы между состояниями ресурсов с использованием следующих параметров:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* исходный код

[**D3D12 \_ Статебефоре \_ состояния ресурсов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)

[**D3D12 \_ Статеафтер \_ состояния ресурсов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)

участие Подресурс UINT = [ **D3D12 \_ Resource \_ барьер \_ все \_ подресурсы**](constants.md)

участие [**D3D12 \_ Флаги \_ \_ флагов Resource барьера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) = D3D12 \_ Resource \_ барьер \_ \_ None

</dd> <dt>

**статическое встроенное Присвоение псевдонимов (ID3D12Resource \* пресаурцебефоре, ID3D12Resource \* пресаурцеафтер)**
</dt> <dd>

Создает псевдонимы для ресурса до и после перехода барьера. Параметры

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* пресаурцебефоре

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* пресаурцеафтер

</dd> <dt>

**static Inline UAV ( \* Исходный код ID3D12Resource)**
</dt> <dd>

Создает неупорядоченный доступ к представлению (UAV) для ресурса. Параметры

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* исходный код

</dd> <dt>

**Константа D3D12 \_ Resource \_ барьера для оператора const& () const**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Барьер ресурсов \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





