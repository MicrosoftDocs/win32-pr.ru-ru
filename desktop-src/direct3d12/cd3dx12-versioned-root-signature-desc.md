---
title: Структура CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию структуры D3D12 с \_ версией \_ корневой \_ подписи \_ .
ms.assetid: 4505C1CE-CAA5-4092-B990-75740A2B194C
keywords:
- Структура CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 695b60fef5aba124ce4e6f2ff729fdb9362c7b2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713496"
---
# <a name="cd3dx12_versioned_root_signature_desc-structure"></a>\_ \_ Структура CD3DX12 корневой \_ сигнатуры с управлением версиями \_

Вспомогательная структура, позволяющая упростить инициализацию структуры [**D3D12 с \_ версией \_ корневой \_ подписи \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC  : public D3D12_VERSIONED_ROOT_SIGNATURE_DESC{
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_VERSIONED_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC1 &o);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init_1_0(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_0(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void inline Init_1_1(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_1(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a>Члены

<dl> <dt>

**CD3DX12 \_ \_ корневая \_ сигнатура с версиями \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр CD3DX12 \_ \_ корневой подписи с версией \_ \_ .

</dd> <dt>

**явная CD3DX12 \_ версия \_ корневой \_ подписи \_ DESC (const D3D12 \_ \_ корневая \_ подпись \_ DESC &o)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ \_ корневой \_ подписи \_ с версией, инициализированной с содержимым структуры [**\_ \_ корневой \_ подписи \_ с версией D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

</dd> <dt>

**Explicit CD3DX12 \_ \_ корневая \_ подпись \_ DESC (const D3D12 \_ корневая \_ подпись \_ DESC &o)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ \_ корневой \_ подписи \_ с версией, инициализированной с содержимым структуры [**D3D12 \_ корневой \_ сигнатуры \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .

</dd> <dt>

**явная CD3DX12 \_ \_ корневая \_ подпись \_ DESC (const D3D12 \_ root \_ Signature \_ DESC1 &o)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ \_ корневой \_ подписи \_ с версией, инициализированной с содержимым [**D3D12 \_ корневой структуры \_ сигнатуры \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) .

</dd> <dt>

**CD3DX12 \_ версия \_ корневой \_ сигнатуры \_ DESC (uint нумпараметерс, const D3D12 \_ корневой \_ параметр \* \_ ППАРАМЕТЕРС, uint нумстатиксамплерс = 0, const D3D12 СТАТИЧЕСКАЯ выборка \_ \_ \_ DESC \* \_ пстатиксамплерс = null, D3D12 флаги флагов корневой сигнатуры \_ \_ \_ = D3D12 \_ корневая \_ подпись, \_ флаг \_ None)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ \_ корневой подписи с версией \_ \_ , инициализируя следующие параметры:

UINT Нумпараметерс

const [**D3D12 \_ \_ параметр root**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ ппараметерс

UINT Нумстатиксамплерс = 0

const [**D3D12 \_ static \_ образец \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null

[**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет

</dd> <dt>

**CD3DX12 \_ с версией \_ корневой \_ сигнатуры \_ DESC (uint нумпараметерс, const D3D12 \_ root \_ параметр1 \* \_ ППАРАМЕТЕРС, uint нумстатиксамплерс = 0, const D3D12 \_ static \_ образец DESC пстатиксамплерс = null, D3D12 флаги флагов корневой сигнатуры \_ \* \_ \_ \_ \_ = D3D12 \_ корневая \_ подпись, \_ флаг \_ None)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ \_ корневой подписи с версией \_ \_ , инициализируя следующие параметры:

UINT Нумпараметерс

const [**D3D12 \_ root \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ ппараметерс

UINT Нумстатиксамплерс = 0

const [**D3D12 \_ static \_ образец \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null

[**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет

</dd> <dt>

**CD3DX12 \_ \_ корневая \_ сигнатура с версиями \_ (CD3DX12 \_ по умолчанию)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ \_ корневой \_ подписи \_ с версией, инициализированной с параметрами по умолчанию:

UINT Нумпараметерс = 0

const [**D3D12 \_ root \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ ппараметерс = null

UINT Нумстатиксамплерс = 0

const [**D3D12 \_ static \_ образец \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null

[**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет

</dd> <dt>

**Встроенная инициализация \_ 1 \_ 0 (uint нумпараметерс, const D3D12 \_ root, \_ параметр \* \_ ппараметерс, uint нумстатиксамплерс = 0, const D3D12 СТАТИЧЕСКАЯ выборка DESC пстатиксамплерс = null, флаги флагов корневой \_ \_ \_ \* \_ \_ \_ сигнатуры \_ : D3D12 \_ флаг корневой \_ подписи \_ \_ None)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

UINT Нумпараметерс

const [**D3D12 \_ \_ параметр root**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ ппараметерс

UINT Нумстатиксамплерс = 0

const [**D3D12 \_ static \_ образец \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null

[**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет

</dd> <dt>

**Статическая встроенная инициализация \_ 1 \_ 0 (D3D12 \_ \_ с версией root \_ \_ , DESC &DESC, uint нумпараметерс, const D3D12 \_ корневой \_ параметр \* \_ ппараметерс, uint нумстатиксамплерс = 0, const D3D12 статическая выборка \_ \_ \_ DESC \* \_ пстатиксамплерс = null, D3D12 корневой метки флагов \_ \_ \_ = D3D12 \_ флаг корневой \_ подписи \_ \_ None)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ ВЕРСИЯ \_ корневой \_ сигнатуры \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &DESC

UINT Нумпараметерс

const [**D3D12 \_ \_ параметр root**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ ппараметерс

UINT Нумстатиксамплерс = 0

const [**D3D12 \_ static \_ образец \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null

[**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет

</dd> <dt>

**Встроенная инициализация \_ 1 \_ 1 (uint нумпараметерс, const D3D12 \_ root \_ параметр1 \* \_ ппараметерс, uint нумстатиксамплерс = 0, const D3D12 СТАТИЧЕСКАЯ выборка DESC пстатиксамплерс = null, флаги флагов корневой \_ \_ \_ \* \_ \_ \_ подписи \_ : D3D12 \_ флаг корневой \_ подписи \_ \_ None)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

UINT Нумпараметерс

const [**D3D12 \_ root \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ ппараметерс

UINT Нумстатиксамплерс = 0

const [**D3D12 \_ static \_ образец \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null

[**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет

</dd> <dt>

**Статическая встроенная инициализация \_ 1 \_ 1 (D3D12 \_ \_ с версией корневой \_ сигнатуры \_ DESC &DESC, uint нумпараметерс, const D3D12 \_ root \_ параметр1 \* \_ ппараметерс, uint нумстатиксамплерс = 0, const D3D12 \_ static \_ образец \_ DESC \* \_ пстатиксамплерс = null, D3D12 корневой подписи флаги \_ \_ \_ = D3D12 \_ флаг корневой \_ подписи \_ \_ None)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ ВЕРСИЯ \_ корневой \_ сигнатуры \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &DESC

UINT Нумпараметерс

const [**D3D12 \_ root \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ ппараметерс

UINT Нумстатиксамплерс = 0

const [**D3D12 \_ static \_ образец \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null

[**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**D3D12 \_ \_ корневая \_ сигнатура с \_ версией**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





