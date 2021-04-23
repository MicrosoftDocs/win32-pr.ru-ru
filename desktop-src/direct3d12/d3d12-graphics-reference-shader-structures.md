---
title: Структуры шейдеров (графика Direct3D 12)
description: d3d12shader. h объявляет следующие структуры, которые используются для создания и использования шейдеров.
ms.assetid: b8ece5c3-5065-4711-b12c-6cf7ea0e1ba0
keywords:
- структуры, шейдеры Direct3D 12
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 400d50c48b8b94fc9a59d8e48179aae43e14a4f5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105691734"
---
# <a name="shader-structures-direct3d-12-graphics"></a><span data-ttu-id="a8ad6-104">Структуры шейдеров (графика Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="a8ad6-104">Shader Structures (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="a8ad6-105">d3d12shader. h объявляет следующие структуры, которые используются для создания и использования шейдеров.</span><span class="sxs-lookup"><span data-stu-id="a8ad6-105">d3d12shader.h declares the following structures, which are used to create and use shaders.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a8ad6-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="a8ad6-106">In this section</span></span>



| <span data-ttu-id="a8ad6-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="a8ad6-107">Topic</span></span>                                                                                  | <span data-ttu-id="a8ad6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="a8ad6-108">Description</span></span>                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="a8ad6-109">**D3D12 \_ функция \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a8ad6-109">**D3D12\_FUNCTION\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_function_desc)<br/>                        | <span data-ttu-id="a8ad6-110">Описывает функцию.</span><span class="sxs-lookup"><span data-stu-id="a8ad6-110">Describes a function.</span></span> <br/>                                       |
| [<span data-ttu-id="a8ad6-111">**D3D12 \_ , \_ DESC, Библиотека**</span><span class="sxs-lookup"><span data-stu-id="a8ad6-111">**D3D12\_LIBRARY\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_library_desc)<br/>                          | <span data-ttu-id="a8ad6-112">Описывает библиотеку.</span><span class="sxs-lookup"><span data-stu-id="a8ad6-112">Describes a library.</span></span> <br/>                                        |
| [<span data-ttu-id="a8ad6-113">**\_DESC параметра \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="a8ad6-113">**D3D12\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_parameter_desc)<br/>                      | <span data-ttu-id="a8ad6-114">Описывает параметр функции.</span><span class="sxs-lookup"><span data-stu-id="a8ad6-114">Describes a function parameter.</span></span> <br/>                             |
| [<span data-ttu-id="a8ad6-115">**\_DESC буфера шейдеров D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8ad6-115">**D3D12\_SHADER\_BUFFER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_buffer_desc)<br/>             | <span data-ttu-id="a8ad6-116">Описывает константный буфер шейдера.</span><span class="sxs-lookup"><span data-stu-id="a8ad6-116">Describes a shader constant-buffer.</span></span> <br/>                         |
| [<span data-ttu-id="a8ad6-117">**Построитель текстуры D3D12, \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a8ad6-117">**D3D12\_SHADER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_desc)<br/>                            | <span data-ttu-id="a8ad6-118">Описывает шейдер.</span><span class="sxs-lookup"><span data-stu-id="a8ad6-118">Describes a shader.</span></span> <br/>                                         |
| [<span data-ttu-id="a8ad6-119">**\_ \_ \_ DESC входной привязки шейдера \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="a8ad6-119">**D3D12\_SHADER\_INPUT\_BIND\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_input_bind_desc)<br/>    | <span data-ttu-id="a8ad6-120">Описывает привязку ресурса шейдера к входным данным шейдера.</span><span class="sxs-lookup"><span data-stu-id="a8ad6-120">Describes how a shader resource is bound to a shader input.</span></span> <br/> |
| [<span data-ttu-id="a8ad6-121">**\_Тип D3D12 шейдера " \_ \_ DESC"**</span><span class="sxs-lookup"><span data-stu-id="a8ad6-121">**D3D12\_SHADER\_TYPE\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_type_desc)<br/>                 | <span data-ttu-id="a8ad6-122">Описывает тип переменной шейдера.</span><span class="sxs-lookup"><span data-stu-id="a8ad6-122">Describes a shader-variable type.</span></span> <br/>                           |
| [<span data-ttu-id="a8ad6-123">**D3D12ая \_ переменная шейдера \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8ad6-123">**D3D12\_SHADER\_VARIABLE\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_variable_desc)<br/>         | <span data-ttu-id="a8ad6-124">Описывает переменную шейдера.</span><span class="sxs-lookup"><span data-stu-id="a8ad6-124">Describes a shader variable.</span></span> <br/>                                |
| [<span data-ttu-id="a8ad6-125">**\_DESC параметра сигнатуры D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8ad6-125">**D3D12\_SIGNATURE\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_signature_parameter_desc)<br/> | <span data-ttu-id="a8ad6-126">Описывает сигнатуру шейдера.</span><span class="sxs-lookup"><span data-stu-id="a8ad6-126">Describes a shader signature.</span></span> <br/>                               |



 

## <a name="related-topics"></a><span data-ttu-id="a8ad6-127">См. также</span><span class="sxs-lookup"><span data-stu-id="a8ad6-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8ad6-128">Справочник по Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="a8ad6-128">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="a8ad6-129">Справочник по шейдерам</span><span class="sxs-lookup"><span data-stu-id="a8ad6-129">Shader Reference</span></span>](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 





