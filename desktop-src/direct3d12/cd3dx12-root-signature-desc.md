---
title: Структура CD3DX12_ROOT_SIGNATURE_DESC (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ структуры D3D12 корневой \_ подписи \_ .
ms.assetid: A3B820C1-51E8-4E35-A67F-2C4BE82A6B7F
keywords:
- Структура CD3DX12_ROOT_SIGNATURE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f89f9cd0f5ad9be08af1fa9c2556ebfbd4fcff1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713967"
---
# <a name="cd3dx12_root_signature_desc-structure"></a>\_ \_ Структура описания корневой подписи CD3DX12 \_

Вспомогательная структура, позволяющая упростить инициализацию структуры [**D3D12 \_ корневой \_ подписи \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_ROOT_SIGNATURE_DESC  : public D3D12_ROOT_SIGNATURE_DESC{
       CD3DX12_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       CD3DX12_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init(D3D12_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a>Члены

<dl> <dt>

**CD3DX12 \_ корневая \_ сигнатура \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр CD3DX12 \_ корневой \_ подписи \_ .

</dd> <dt>

**явная CD3DX12 \_ корневая \_ подпись \_ DESC (const D3D12 \_ корневая \_ подпись \_ DESC &o)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ корневой \_ подписи \_ (desc), инициализируемый с помощью содержимого другой [**\_ корневой структуры \_ сигнатуры \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .

</dd> <dt>

**CD3DX12 \_ корневая \_ сигнатура \_ (uint НУМПАРАМЕТЕРС, const D3D12 \_ корневой \_ параметр \* \_ ппараметерс, uint нумстатиксамплерс = 0, const D3D12 статическая ВЫБОРка \_ \_ \_ DESC \* \_ пстатиксамплерс = null, D3D12 флаги флагов \_ корневой сигнатуры \_ \_ = D3D12 \_ корневая \_ подпись, \_ флаг \_ None)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ корневой \_ подписи \_ , инициализируя следующие параметры:

UINT Нумпараметерс

[**D3D12 \_ Корневой \_ параметр**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ ппараметерс

участие UINT Нумстатиксамплерс = 0

участие [**D3D12 \_ Статическая \_ проба \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null

участие [**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет

</dd> <dt>

**CD3DX12 \_ корневая \_ сигнатура \_ (CD3DX12 \_ по умолчанию)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ корневой \_ подписи \_ , инициализированный параметрами по умолчанию.

``` syntax
CD3DX12_ROOT_SIGNATURE_DESC(0,NULL,0,NULL,D3D12_ROOT_SIGNATURE_FLAG_NONE)
```

</dd> <dt>

**Inline init (UINT Нумпараметерс, const D3D12 \_ root, \_ параметр \* \_ ппараметерс, uint нумстатиксамплерс = 0, const D3D12 \_ статическая выборка \_ \_ DESC \* \_ пстатиксамплерс = null, флаги флагов \_ корневой \_ подписи \_ = D3D12 \_ корневой \_ подписи \_ \_ None)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

UINT Нумпараметерс

[**D3D12 \_ Корневой \_ параметр**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ ппараметерс

участие UINT Нумстатиксамплерс = 0

участие [**D3D12 \_ Статическая \_ проба \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null

участие [**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет

</dd> <dt>

**Статическая встроенная init (D3D12 \_ корневая \_ подпись \_ DESC &DESC, uint НУМПАРАМЕТЕРС, const D3D12 \_ корневой \_ параметр \* \_ ппараметерс, uint нумстатиксамплерс = 0, const D3D12 статическая ВЫБОРка \_ \_ \_ DESC \* \_ пстатиксамплерс = null, D3D12 флаги флагов \_ \_ \_ \_ корневой подписи = D3D12 корневая \_ подпись \_ \_ None)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ Корневая \_ сигнатура \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) &DESC

UINT Нумпараметерс

[**D3D12 \_ Корневой \_ параметр**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ ппараметерс

участие UINT Нумстатиксамплерс = 0

участие [**D3D12 \_ Статическая \_ проба \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null

участие [**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_DESC корневой \_ подписи D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





