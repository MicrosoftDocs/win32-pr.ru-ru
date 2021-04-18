---
title: Структура CD3DX12_ROOT_PARAMETER1 (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать структуру D3D12 \_ root \_ параметр1.
ms.assetid: CDE0C02E-0112-4FD9-A4A2-36E8C326715C
keywords:
- Структура CD3DX12_ROOT_PARAMETER1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d582016b26df0d57f7792afd30fc4fcbf3ba97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713968"
---
# <a name="cd3dx12_root_parameter1-structure"></a>\_Корневая \_ Структура параметр1 CD3DX12

Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12 \_ root \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_ROOT_PARAMETER1  : public D3D12_ROOT_PARAMETER1{
       CD3DX12_ROOT_PARAMETER1();
       explicit CD3DX12_ROOT_PARAMETER1(const D3D12_ROOT_PARAMETER1 &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Корневой элемент \_ параметр1 CD3DX12 ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр CD3DX12 \_ корневого элемента \_ параметр1.

</dd> <dt>

**явный CD3DX12 \_ root \_ параметр1 (const D3D12 \_ root \_ параметр1 &o)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ root \_ параметр1, инициализируемый с помощью содержимого другой [**\_ корневой структуры \_ параметр1 D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .

</dd> <dt>

**static Inline Инитасдескриптортабле (D3D12 \_ root \_ параметр1 &РУТПАРАМ, uint нумдескрипторранжес, const D3D12 \_ дескриптор \_ высокое \* пдескрипторранжес, D3D12 видимость \_ видимости шейдера \_ = D3D12 \_ видимость шейдера \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ КОРНЕВой элемент \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &рутпарам

UINT Нумдескрипторранжес

const [**D3D12 \_ дескриптор \_ высокое**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* пдескрипторранжес

[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> <dt>

**static Inline Инитасконстантс (D3D12 \_ root \_ параметр1 &РУТПАРАМ, uint NUM32BITVALUES, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0, D3D12 \_ ШЕЙДЕР видимости \_ = D3D12 \_ видимость шейдера \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ КОРНЕВой элемент \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &рутпарам

UINT num32BitValues

UINT Шадеррегистер

UINT Регистерспаце = 0

[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> <dt>

**static Inline Инитасконстантбуффервиев (D3D12 \_ root \_ параметр1 &РУТПАРАМ, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0, D3D12 флаги \_ flags root-дескриптора \_ \_ = D3D12 \_ корневого \_ дескриптора " \_ \_ нет", D3D12 видимость \_ видимости шейдеров \_ = D3D12 \_ видимость шейдеров \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ КОРНЕВой элемент \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &рутпарам

UINT Шадеррегистер

UINT Регистерспаце = 0

[**D3D12 \_ Флаги флагов КОРНЕВого \_ дескриптора \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ корневого \_ дескриптора \_ \_ None

[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> <dt>

**static Inline Инитасшадерресаурцевиев (D3D12 \_ root \_ параметр1 &РУТПАРАМ, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0, D3D12 флаги \_ flags root-дескриптора \_ \_ = D3D12 \_ корневого \_ дескриптора " \_ \_ нет", D3D12 видимость \_ видимости шейдеров \_ = D3D12 \_ видимость шейдеров \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ КОРНЕВой элемент \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &рутпарам

UINT Шадеррегистер

UINT Регистерспаце = 0

[**D3D12 \_ Флаги флагов КОРНЕВого \_ дескриптора \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ корневого \_ дескриптора \_ \_ None

[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> <dt>

**static Inline Инитасунордередакцессвиев (D3D12 \_ root \_ параметр1 &РУТПАРАМ, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0, D3D12 флаги \_ flags root-дескриптора \_ \_ = D3D12 \_ корневого \_ дескриптора " \_ \_ нет", D3D12 видимость \_ видимости шейдеров \_ = D3D12 \_ видимость шейдеров \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ КОРНЕВой элемент \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &рутпарам

UINT Шадеррегистер

UINT Регистерспаце = 0

[**D3D12 \_ Флаги флагов КОРНЕВого \_ дескриптора \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ корневого \_ дескриптора \_ \_ None

[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> <dt>

**Inline Инитасдескриптортабле (UINT Нумдескрипторранжес, const D3D12 \_ дескриптор \_ высокое \* пдескрипторранжес, D3D12 видимость \_ видимости шейдера \_ = D3D12 \_ видимость шейдера \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

UINT Нумдескрипторранжес

const [**D3D12 \_ дескриптор \_ высокое**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* пдескрипторранжес

[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> <dt>

**Inline Инитасконстантс (UINT num32BitValues, UINT Шадеррегистер, UINT Регистерспаце = 0, видимость D3D12 \_ шейдер видимости \_ = D3D12 \_ видимость шейдера \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

UINT num32BitValues

UINT Шадеррегистер

UINT Регистерспаце = 0

[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> <dt>

**Inline Инитасконстантбуффервиев (UINT Шадеррегистер, UINT Регистерспаце = 0, D3D12 флаги \_ flags в корневом \_ дескрипторе \_ = D3D12 \_ флаг корневого \_ дескриптора \_ \_ нет, D3D12 видимость \_ видимости шейдеров \_ = D3D12 \_ видимость шейдера \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

UINT Шадеррегистер

UINT Регистерспаце = 0

[**D3D12 \_ Флаги флагов КОРНЕВого \_ дескриптора \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ корневого \_ дескриптора \_ \_ None

[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> <dt>

**Inline Инитасшадерресаурцевиев (UINT Шадеррегистер, UINT Регистерспаце = 0, D3D12 флаги \_ flags в корневом \_ дескрипторе \_ = D3D12 \_ флаг корневого \_ дескриптора \_ \_ нет, D3D12 видимость \_ видимости шейдеров \_ = D3D12 \_ видимость шейдера \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

UINT Шадеррегистер

UINT Регистерспаце = 0

[**D3D12 \_ Флаги флагов КОРНЕВого \_ дескриптора \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ корневого \_ дескриптора \_ \_ None

[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> <dt>

**Inline Инитасунордередакцессвиев (UINT Шадеррегистер, UINT Регистерспаце = 0, D3D12 флаги \_ flags в корневом \_ дескрипторе \_ = D3D12 \_ флаг корневого \_ дескриптора \_ \_ нет, D3D12 видимость \_ видимости шейдеров \_ = D3D12 \_ видимость шейдера \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

UINT Шадеррегистер

UINT Регистерспаце = 0

[**D3D12 \_ Флаги флагов КОРНЕВого \_ дескриптора \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ корневого \_ дескриптора \_ \_ None

[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Корневой элемент \_ параметр1 D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





