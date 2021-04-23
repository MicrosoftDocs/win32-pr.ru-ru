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
ms.openlocfilehash: 6d6b10749f7a56d928e0a4218d534cc2a8ec4fab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713501"
---
# <a name="cd3dx12_static_sampler_desc-structure"></a><span data-ttu-id="7529f-104">\_Статическая \_ Структура образцов \_ CD3DX12</span><span class="sxs-lookup"><span data-stu-id="7529f-104">CD3DX12\_STATIC\_SAMPLER\_DESC structure</span></span>

<span data-ttu-id="7529f-105">Вспомогательная структура, позволяющая упростить инициализацию структуры [**D3D12 со \_ статическими \_ образцами \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .</span><span class="sxs-lookup"><span data-stu-id="7529f-105">A helper structure to enable easy initialization of a [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7529f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7529f-106">Syntax</span></span>


```C++
struct CD3DX12_STATIC_SAMPLER_DESC  : public D3D12_STATIC_SAMPLER_DESC{
       CD3DX12_STATIC_SAMPLER_DESC();
       explicit CD3DX12_STATIC_SAMPLER_DESC(const D3D12_STATIC_SAMPLER_DESC &o);
       CD3DX12_STATIC_SAMPLER_DESC(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void static inline Init(D3D12_STATIC_SAMPLER_DESC &samplerDesc, UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="7529f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="7529f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7529f-108">**CD3DX12 \_ статическая выборка \_ \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="7529f-108">**CD3DX12\_STATIC\_SAMPLER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="7529f-109">Создает новый, неинициализированный экземпляр \_ статического \_ образца CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="7529f-109">Creates a new, uninitialized, instance of a CD3DX12\_STATIC\_SAMPLER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="7529f-110">**явная CD3DX12 статическая выборка, \_ \_ \_ DESC (const D3D12 \_ static \_ образец \_ DESC &o)**</span><span class="sxs-lookup"><span data-stu-id="7529f-110">**explicit CD3DX12\_STATIC\_SAMPLER\_DESC(const D3D12\_STATIC\_SAMPLER\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="7529f-111">Создает новый экземпляр CD3DX12 статической выборки \_ \_ \_ , инициализируемый с помощью содержимого другой [**D3D12 \_ статической \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) структуры выборки.</span><span class="sxs-lookup"><span data-stu-id="7529f-111">Creates a new instance of a CD3DX12\_STATIC\_SAMPLER\_DESC, initialized with the contents of another [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7529f-112">**CD3DX12 \_ статическая выборка \_ \_ , DESC (uint шадеррегистер, D3D12 \_ фильтра фильтра = D3D12 \_ Filter \_ анизотропный, D3D12 \_ текстурный \_ \_ режим адреса аддрессу = D3D12 \_ \_ режим адреса текстуры \_ \_ Перенос, D3D12 \_ \_ режим адреса текстуры \_ АДДРЕССВ = D3D12 \_ режим адреса текстуры \_ \_ \_ Перенос, D3D12ный \_ \_ режим адресации текстуры \_ аддрессв = D3D12 \_ \_ режим адресации текстуры \_ \_ , float МИПЛОДБИАС = 0, uint максанисотропи = 16, D3D12 \_ Сравнение Func, компарисонфунк \_ = D3D12 \_ Сравнение Func не \_ \_ \_ равно, D3D12 \_ статический \_ \_ Цвет границы Color = D3D12 \_ статический \_ \_ Цвет границы \_ непрозрачный \_ белый, float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ шейдер видимости shaderVisibility \_ = D3D12 \_ \_ видимость \_ , uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="7529f-112">**CD3DX12\_STATIC\_SAMPLER\_DESC(UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="7529f-113">Создает новый экземпляр CD3DX12 статической выборки \_ \_ \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="7529f-113">Creates a new instance of a CD3DX12\_STATIC\_SAMPLER\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="7529f-114">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="7529f-114">UINT shaderRegister</span></span>

<span data-ttu-id="7529f-115">участие [**D3D12 \_ Фильтр фильтра =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ Filter \_ анизотроп.</span><span class="sxs-lookup"><span data-stu-id="7529f-115">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="7529f-116">участие [**D3D12 \_ \_ \_ Режим адресации текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) аддрессу = \_ D3D12 \_ режим адресации текстуры \_ \_</span><span class="sxs-lookup"><span data-stu-id="7529f-116">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="7529f-117">участие [**D3D12 \_ \_ \_ Режим адресации текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) аддрессв = \_ D3D12 \_ режим адресации текстуры \_ \_</span><span class="sxs-lookup"><span data-stu-id="7529f-117">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="7529f-118">участие [**D3D12 \_ \_ \_ Режим адресации текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) аддрессв = \_ D3D12 \_ режим адресации текстуры \_ \_</span><span class="sxs-lookup"><span data-stu-id="7529f-118">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="7529f-119">участие FLOAT Миплодбиас = 0</span><span class="sxs-lookup"><span data-stu-id="7529f-119">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="7529f-120">участие UINT Максанисотропи = 16</span><span class="sxs-lookup"><span data-stu-id="7529f-120">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="7529f-121">участие [**D3D12 \_ Сравнение \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) КОМПАРИСОНФУНК = D3D12 \_ \_ \_ \_ Equals Func less</span><span class="sxs-lookup"><span data-stu-id="7529f-121">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="7529f-122">участие [**D3D12 \_ \_ \_ Цвет статического обрамления**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = \_ D3D12 \_ статический \_ Цвет границы \_ непрозрачный \_ белый</span><span class="sxs-lookup"><span data-stu-id="7529f-122">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="7529f-123">участие FLOAT Минлод = 0. f</span><span class="sxs-lookup"><span data-stu-id="7529f-123">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="7529f-124">участие FLOAT Макслод = D3D12 \_ FLOAT32 \_ Max</span><span class="sxs-lookup"><span data-stu-id="7529f-124">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="7529f-125">участие [**D3D12 \_ \_Видимость шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) ШАДЕРВИСИБИЛИТИ = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="7529f-125">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="7529f-126">участие UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="7529f-126">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="7529f-127">**Статическая встроенная init (D3D12 \_ static \_ образец \_ DESC &Самплердеск, uint шадеррегистер, D3D12 фильтр \_ фильтра = D3D12 \_ Filter \_ анизотропо, D3D12 \_ \_ режим адреса текстуры \_ АДДРЕССУ = D3D12 \_ \_ режим адреса текстуры \_ \_ — Перенос, \_ D3D12 \_ режим адреса текстуры \_ АДДРЕССВ = \_ D3D12 \_ режим адресации текстуры \_ \_ , D3D12ный \_ \_ режим адресации текстуры \_ аддрессв = D3D12 \_ \_ режим адресации текстуры \_ \_ , float МИПЛОДБИАС = 0, uint максанисотропи = 16, D3D12 \_ Сравнение Func, компарисонфунк \_ = D3D12 \_ Сравнение Func не \_ \_ \_ равно, D3D12 \_ статический \_ \_ Цвет границы Color = D3D12 \_ статический \_ \_ Цвет границы \_ непрозрачный \_ белый, float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ шейдер видимости shaderVisibility \_ = D3D12 \_ \_ видимость \_ , uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="7529f-127">**static inline Init(D3D12\_STATIC\_SAMPLER\_DESC &samplerDesc, UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="7529f-128">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="7529f-128">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="7529f-129">[**D3D12 \_ СТАТИЧЕСКИЙ \_ образец \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &самплердеск</span><span class="sxs-lookup"><span data-stu-id="7529f-129">[**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &samplerDesc</span></span>

<span data-ttu-id="7529f-130">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="7529f-130">UINT shaderRegister</span></span>

<span data-ttu-id="7529f-131">участие [**D3D12 \_ Фильтр фильтра =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ Filter \_ анизотроп.</span><span class="sxs-lookup"><span data-stu-id="7529f-131">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="7529f-132">участие [**D3D12 \_ \_ \_ Режим адресации текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) аддрессу = \_ D3D12 \_ режим адресации текстуры \_ \_</span><span class="sxs-lookup"><span data-stu-id="7529f-132">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="7529f-133">участие [**D3D12 \_ \_ \_ Режим адресации текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) аддрессв = \_ D3D12 \_ режим адресации текстуры \_ \_</span><span class="sxs-lookup"><span data-stu-id="7529f-133">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="7529f-134">участие [**D3D12 \_ \_ \_ Режим адресации текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) аддрессв = \_ D3D12 \_ режим адресации текстуры \_ \_</span><span class="sxs-lookup"><span data-stu-id="7529f-134">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="7529f-135">участие FLOAT Миплодбиас = 0</span><span class="sxs-lookup"><span data-stu-id="7529f-135">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="7529f-136">участие UINT Максанисотропи = 16</span><span class="sxs-lookup"><span data-stu-id="7529f-136">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="7529f-137">участие [**D3D12 \_ Сравнение \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) КОМПАРИСОНФУНК = D3D12 \_ \_ \_ \_ Equals Func less</span><span class="sxs-lookup"><span data-stu-id="7529f-137">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="7529f-138">участие [**D3D12 \_ \_ \_ Цвет статического обрамления**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = \_ D3D12 \_ статический \_ Цвет границы \_ непрозрачный \_ белый</span><span class="sxs-lookup"><span data-stu-id="7529f-138">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="7529f-139">участие FLOAT Минлод = 0. f</span><span class="sxs-lookup"><span data-stu-id="7529f-139">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="7529f-140">участие FLOAT Макслод = D3D12 \_ FLOAT32 \_ Max</span><span class="sxs-lookup"><span data-stu-id="7529f-140">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="7529f-141">участие [**D3D12 \_ \_Видимость шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) ШАДЕРВИСИБИЛИТИ = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="7529f-141">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="7529f-142">участие UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="7529f-142">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="7529f-143">**Inline init (UINT Шадеррегистер, фильтр фильтра D3D12 \_ = D3D12 \_ Filter \_ анизотроп, D3D12 \_ \_ режим адресации текстуры \_ аддрессу = D3D12 режим адресации \_ текстуры \_ \_ \_ , D3D12 \_ \_ режим адресации текстуры \_ аддрессв = D3D12 \_ \_ режим адресации текстуры \_ \_ , D3D12ный \_ \_ режим адресации текстуры \_ аддрессв = D3D12 \_ \_ режим адресации текстуры \_ \_ , float миплодбиас = 0, uint максанисотропи = 16, D3D12 \_ Сравнение Func, компарисонфунк \_ = D3D12 \_ Сравнение Func не \_ \_ \_ равно, D3D12 \_ статический \_ \_ Цвет границы Color = D3D12 \_ статический \_ \_ Цвет границы \_ непрозрачный \_ белый, float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ шейдер видимости shaderVisibility \_ = D3D12 \_ \_ видимость \_ , uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="7529f-143">**inline Init(UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="7529f-144">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="7529f-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="7529f-145">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="7529f-145">UINT shaderRegister</span></span>

<span data-ttu-id="7529f-146">участие [**D3D12 \_ Фильтр фильтра =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ Filter \_ анизотроп.</span><span class="sxs-lookup"><span data-stu-id="7529f-146">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="7529f-147">участие [**D3D12 \_ \_ \_ Режим адресации текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) аддрессу = \_ D3D12 \_ режим адресации текстуры \_ \_</span><span class="sxs-lookup"><span data-stu-id="7529f-147">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="7529f-148">участие [**D3D12 \_ \_ \_ Режим адресации текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) аддрессв = \_ D3D12 \_ режим адресации текстуры \_ \_</span><span class="sxs-lookup"><span data-stu-id="7529f-148">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="7529f-149">участие [**D3D12 \_ \_ \_ Режим адресации текстуры**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) аддрессв = \_ D3D12 \_ режим адресации текстуры \_ \_</span><span class="sxs-lookup"><span data-stu-id="7529f-149">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="7529f-150">участие FLOAT Миплодбиас = 0</span><span class="sxs-lookup"><span data-stu-id="7529f-150">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="7529f-151">участие UINT Максанисотропи = 16</span><span class="sxs-lookup"><span data-stu-id="7529f-151">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="7529f-152">участие [**D3D12 \_ Сравнение \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) КОМПАРИСОНФУНК = D3D12 \_ \_ \_ \_ Equals Func less</span><span class="sxs-lookup"><span data-stu-id="7529f-152">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="7529f-153">участие [**D3D12 \_ \_ \_ Цвет статического обрамления**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = \_ D3D12 \_ статический \_ Цвет границы \_ непрозрачный \_ белый</span><span class="sxs-lookup"><span data-stu-id="7529f-153">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="7529f-154">участие FLOAT Минлод = 0. f</span><span class="sxs-lookup"><span data-stu-id="7529f-154">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="7529f-155">участие FLOAT Макслод = D3D12 \_ FLOAT32 \_ Max</span><span class="sxs-lookup"><span data-stu-id="7529f-155">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="7529f-156">участие [**D3D12 \_ \_Видимость шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) ШАДЕРВИСИБИЛИТИ = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="7529f-156">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="7529f-157">участие UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="7529f-157">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7529f-158">Требования</span><span class="sxs-lookup"><span data-stu-id="7529f-158">Requirements</span></span>



| <span data-ttu-id="7529f-159">Требование</span><span class="sxs-lookup"><span data-stu-id="7529f-159">Requirement</span></span> | <span data-ttu-id="7529f-160">Значение</span><span class="sxs-lookup"><span data-stu-id="7529f-160">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7529f-161">Header</span><span class="sxs-lookup"><span data-stu-id="7529f-161">Header</span></span><br/> | <dl> <span data-ttu-id="7529f-162"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7529f-162"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7529f-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7529f-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7529f-164">**D3D12 \_ статическая выборка \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7529f-164">**D3D12\_STATIC\_SAMPLER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)
</dt> <dt>

[<span data-ttu-id="7529f-165">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="7529f-165">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





