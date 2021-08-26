---
title: Структура CD3DX12_STATIC_SAMPLER_DESC (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию структуры D3D12 со \_ статическими \_ образцами \_ .
ms.assetid: C402415D-7BD5-4E23-82C9-B29B0B5669B8
keywords:
- Структура CD3DX12_STATIC_SAMPLER_DESC
topic_type:
- apiref
api_name:
- CD3DX12_STATIC_SAMPLER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdd2e64a98a8dd11b62154bb3239934fd8da29eb6f8bf2919ef88452d280de6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069764"
---
# <a name="cd3dx12_static_sampler_desc-structure"></a>\_Статическая \_ Структура образцов \_ CD3DX12

Вспомогательная структура, позволяющая упростить инициализацию структуры [**D3D12 со \_ статическими \_ образцами \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_STATIC_SAMPLER_DESC  : public D3D12_STATIC_SAMPLER_DESC{
       CD3DX12_STATIC_SAMPLER_DESC();
       explicit CD3DX12_STATIC_SAMPLER_DESC(const D3D12_STATIC_SAMPLER_DESC &o);
       CD3DX12_STATIC_SAMPLER_DESC(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void static inline Init(D3D12_STATIC_SAMPLER_DESC &samplerDesc, UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
};
```



## <a name="members"></a>Члены

<dl> <dt>

**CD3DX12 \_ статическая выборка \_ \_ DESC ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ статического \_ образца CD3DX12 \_ .

</dd> <dt>

**явная CD3DX12 статическая выборка, \_ \_ \_ DESC (const D3D12 \_ static \_ образец \_ DESC &o)**
</dt> <dd>

Создает новый экземпляр CD3DX12 статической выборки \_ \_ \_ , инициализируемый с помощью содержимого другой [**D3D12 \_ статической \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) структуры выборки.

</dd> <dt>

**CD3DX12 \_ статическая выборка \_ \_ , DESC (uint шадеррегистер, D3D12 \_ фильтра фильтра = D3D12 \_ Filter \_ анизотропный, D3D12 \_ текстурный \_ \_ режим адреса аддрессу = D3D12 \_ \_ режим адреса текстуры \_ \_ Перенос, D3D12 \_ \_ режим адреса текстуры \_ АДДРЕССВ = D3D12 \_ режим адреса текстуры \_ \_ \_ Перенос, D3D12ный \_ \_ режим адресации текстуры \_ аддрессв = D3D12 \_ \_ режим адресации текстуры \_ \_ , float МИПЛОДБИАС = 0, uint максанисотропи = 16, D3D12 \_ Сравнение Func, компарисонфунк \_ = D3D12 \_ Сравнение Func не \_ \_ \_ равно, D3D12 \_ статический \_ \_ Цвет границы Color = D3D12 \_ статический \_ \_ Цвет границы \_ непрозрачный \_ белый, float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ шейдер видимости shaderVisibility \_ = D3D12 \_ \_ видимость \_ , uint registerSpace = 0)**
</dt> <dd>

Создает новый экземпляр CD3DX12 статической выборки \_ \_ \_ , инициализируя следующие параметры:

UINT Шадеррегистер

участие [**D3D12 \_ Фильтр фильтра =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ Filter \_ анизотроп.

участие [**D3D12 \_ \_ \_ Режим адресации текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) аддрессу = \_ D3D12 \_ режим адресации текстуры \_ \_

участие [**D3D12 \_ \_ \_ Режим адресации текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) аддрессв = \_ D3D12 \_ режим адресации текстуры \_ \_

участие [**D3D12 \_ \_ \_ Режим адресации текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) аддрессв = \_ D3D12 \_ режим адресации текстуры \_ \_

участие FLOAT Миплодбиас = 0

участие UINT Максанисотропи = 16

участие [**D3D12 \_ Сравнение \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) КОМПАРИСОНФУНК = D3D12 \_ \_ \_ \_ Equals Func less

участие [**D3D12 \_ \_ \_ Цвет статического обрамления**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = \_ D3D12 \_ статический \_ Цвет границы \_ непрозрачный \_ белый

участие FLOAT Минлод = 0. f

участие FLOAT Макслод = D3D12 \_ FLOAT32 \_ Max

участие [**D3D12 \_ \_Видимость шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) ШАДЕРВИСИБИЛИТИ = D3D12 \_ \_ видимость шейдера \_

участие UINT Регистерспаце = 0

</dd> <dt>

**Статическая встроенная init (D3D12 \_ static \_ образец \_ DESC &Самплердеск, uint шадеррегистер, D3D12 фильтр \_ фильтра = D3D12 \_ Filter \_ анизотропо, D3D12 \_ \_ режим адреса текстуры \_ АДДРЕССУ = D3D12 \_ \_ режим адреса текстуры \_ \_ — Перенос, \_ D3D12 \_ режим адреса текстуры \_ АДДРЕССВ = \_ D3D12 \_ режим адресации текстуры \_ \_ , D3D12ный \_ \_ режим адресации текстуры \_ аддрессв = D3D12 \_ \_ режим адресации текстуры \_ \_ , float МИПЛОДБИАС = 0, uint максанисотропи = 16, D3D12 \_ Сравнение Func, компарисонфунк \_ = D3D12 \_ Сравнение Func не \_ \_ \_ равно, D3D12 \_ статический \_ \_ Цвет границы Color = D3D12 \_ статический \_ \_ Цвет границы \_ непрозрачный \_ белый, float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ шейдер видимости shaderVisibility \_ = D3D12 \_ \_ видимость \_ , uint registerSpace = 0)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ СТАТИЧЕСКИЙ \_ образец \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &самплердеск

UINT Шадеррегистер

участие [**D3D12 \_ Фильтр фильтра =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ Filter \_ анизотроп.

участие [**D3D12 \_ \_ \_ Режим адресации текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) аддрессу = \_ D3D12 \_ режим адресации текстуры \_ \_

участие [**D3D12 \_ \_ \_ Режим адресации текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) аддрессв = \_ D3D12 \_ режим адресации текстуры \_ \_

участие [**D3D12 \_ \_ \_ Режим адресации текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) аддрессв = \_ D3D12 \_ режим адресации текстуры \_ \_

участие FLOAT Миплодбиас = 0

участие UINT Максанисотропи = 16

участие [**D3D12 \_ Сравнение \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) КОМПАРИСОНФУНК = D3D12 \_ \_ \_ \_ Equals Func less

участие [**D3D12 \_ \_ \_ Цвет статического обрамления**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = \_ D3D12 \_ статический \_ Цвет границы \_ непрозрачный \_ белый

участие FLOAT Минлод = 0. f

участие FLOAT Макслод = D3D12 \_ FLOAT32 \_ Max

участие [**D3D12 \_ \_Видимость шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) ШАДЕРВИСИБИЛИТИ = D3D12 \_ \_ видимость шейдера \_

участие UINT Регистерспаце = 0

</dd> <dt>

**Inline init (UINT Шадеррегистер, фильтр фильтра D3D12 \_ = D3D12 \_ Filter \_ анизотроп, D3D12 \_ \_ режим адресации текстуры \_ аддрессу = D3D12 режим адресации \_ текстуры \_ \_ \_ , D3D12 \_ \_ режим адресации текстуры \_ аддрессв = D3D12 \_ \_ режим адресации текстуры \_ \_ , D3D12ный \_ \_ режим адресации текстуры \_ аддрессв = D3D12 \_ \_ режим адресации текстуры \_ \_ , float миплодбиас = 0, uint максанисотропи = 16, D3D12 \_ Сравнение Func, компарисонфунк \_ = D3D12 \_ Сравнение Func не \_ \_ \_ равно, D3D12 \_ статический \_ \_ Цвет границы Color = D3D12 \_ статический \_ \_ Цвет границы \_ непрозрачный \_ белый, float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ шейдер видимости shaderVisibility \_ = D3D12 \_ \_ видимость \_ , uint registerSpace = 0)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

UINT Шадеррегистер

участие [**D3D12 \_ Фильтр фильтра =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ Filter \_ анизотроп.

участие [**D3D12 \_ \_ \_ Режим адресации текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) аддрессу = \_ D3D12 \_ режим адресации текстуры \_ \_

участие [**D3D12 \_ \_ \_ Режим адресации текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) аддрессв = \_ D3D12 \_ режим адресации текстуры \_ \_

участие [**D3D12 \_ \_ \_ Режим адресации текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) аддрессв = \_ D3D12 \_ режим адресации текстуры \_ \_

участие FLOAT Миплодбиас = 0

участие UINT Максанисотропи = 16

участие [**D3D12 \_ Сравнение \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) КОМПАРИСОНФУНК = D3D12 \_ \_ \_ \_ Equals Func less

участие [**D3D12 \_ \_ \_ Цвет статического обрамления**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = \_ D3D12 \_ статический \_ Цвет границы \_ непрозрачный \_ белый

участие FLOAT Минлод = 0. f

участие FLOAT Макслод = D3D12 \_ FLOAT32 \_ Max

участие [**D3D12 \_ \_Видимость шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) ШАДЕРВИСИБИЛИТИ = D3D12 \_ \_ видимость шейдера \_

участие UINT Регистерспаце = 0

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**D3D12 \_ статическая выборка \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





