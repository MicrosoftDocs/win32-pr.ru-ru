---
title: Структуры шейдеров (графика Direct3D 11)
description: Структуры используются для создания и использования шейдеров.
ms.assetid: 3b8ece5c-5065-4711-b12c-06cf7ea0e1ba
keywords:
- структуры, шейдеры Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14739e3db38c075e19e58a90b12bbf7d06b48a4e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800844"
---
# <a name="shader-structures-direct3d-11-graphics"></a><span data-ttu-id="249ed-104">Структуры шейдеров (графика Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="249ed-104">Shader Structures (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="249ed-105">Структуры используются для создания и использования шейдеров.</span><span class="sxs-lookup"><span data-stu-id="249ed-105">Structures are used to create and use shaders.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="249ed-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="249ed-106">In this section</span></span>



| <span data-ttu-id="249ed-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="249ed-107">Topic</span></span>                                                                                       | <span data-ttu-id="249ed-108">Описание</span><span class="sxs-lookup"><span data-stu-id="249ed-108">Description</span></span>                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="249ed-109">**\_Экземпляр класса D3D11, \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="249ed-109">**D3D11\_CLASS\_INSTANCE\_DESC**</span></span>](/windows/desktop/api/D3D11/ns-d3d11-d3d11_class_instance_desc)<br/>                | <span data-ttu-id="249ed-110">Описывает экземпляр класса HLSL.</span><span class="sxs-lookup"><span data-stu-id="249ed-110">Describes an HLSL class instance.</span></span><br/>                           |
| [<span data-ttu-id="249ed-111">**\_DESC D3D11 COMPUTE \_ Shader \_ Trace \_**</span><span class="sxs-lookup"><span data-stu-id="249ed-111">**D3D11\_COMPUTE\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_compute_shader_trace_desc)<br/>   | <span data-ttu-id="249ed-112">Описывает экземпляр шейдера вычислений для трассировки.</span><span class="sxs-lookup"><span data-stu-id="249ed-112">Describes an instance of a compute shader to trace.</span></span><br/>         |
| [<span data-ttu-id="249ed-113">**\_ \_ DESC трассировки шейдера \_ домена \_ D3D11**</span><span class="sxs-lookup"><span data-stu-id="249ed-113">**D3D11\_DOMAIN\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_domain_shader_trace_desc)<br/>     | <span data-ttu-id="249ed-114">Описывает экземпляр шейдера домена для трассировки.</span><span class="sxs-lookup"><span data-stu-id="249ed-114">Describes an instance of a domain shader to trace.</span></span><br/>          |
| [<span data-ttu-id="249ed-115">**D3D11 \_ функция \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="249ed-115">**D3D11\_FUNCTION\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_function_desc)<br/>                             | <span data-ttu-id="249ed-116">Описывает функцию.</span><span class="sxs-lookup"><span data-stu-id="249ed-116">Describes a function.</span></span><br/>                                       |
| [<span data-ttu-id="249ed-117">**\_DESC " \_ Трассировка шейдера D3D11 Geometry" \_ \_**</span><span class="sxs-lookup"><span data-stu-id="249ed-117">**D3D11\_GEOMETRY\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_geometry_shader_trace_desc)<br/> | <span data-ttu-id="249ed-118">Описывает экземпляр шейдера Geometry для трассировки.</span><span class="sxs-lookup"><span data-stu-id="249ed-118">Describes an instance of a geometry shader to trace.</span></span><br/>        |
| [<span data-ttu-id="249ed-119">**D3D11 \_ поверхности \_ Shader \_ Trace, \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="249ed-119">**D3D11\_HULL\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_hull_shader_trace_desc)<br/>         | <span data-ttu-id="249ed-120">Описывает экземпляр шейдера поверхности для трассировки.</span><span class="sxs-lookup"><span data-stu-id="249ed-120">Describes an instance of a hull shader to trace.</span></span><br/>            |
| [<span data-ttu-id="249ed-121">**D3D11 \_ , \_ DESC, Библиотека**</span><span class="sxs-lookup"><span data-stu-id="249ed-121">**D3D11\_LIBRARY\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_library_desc)<br/>                               | <span data-ttu-id="249ed-122">Описывает библиотеку.</span><span class="sxs-lookup"><span data-stu-id="249ed-122">Describes a library.</span></span><br/>                                        |
| [<span data-ttu-id="249ed-123">**\_DESC параметра \_ D3D11**</span><span class="sxs-lookup"><span data-stu-id="249ed-123">**D3D11\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_parameter_desc)<br/>                           | <span data-ttu-id="249ed-124">Описывает параметр функции.</span><span class="sxs-lookup"><span data-stu-id="249ed-124">Describes a function parameter.</span></span> <br/>                            |
| [<span data-ttu-id="249ed-125">**\_DESC D3D11 \_ построителя \_ текстуры \_**</span><span class="sxs-lookup"><span data-stu-id="249ed-125">**D3D11\_PIXEL\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_pixel_shader_trace_desc)<br/>       | <span data-ttu-id="249ed-126">Описывает экземпляр шейдера пикселей для трассировки.</span><span class="sxs-lookup"><span data-stu-id="249ed-126">Describes an instance of a pixel shader to trace.</span></span><br/>           |
| [<span data-ttu-id="249ed-127">**\_DESC буфера шейдеров D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="249ed-127">**D3D11\_SHADER\_BUFFER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_buffer_desc)<br/>                  | <span data-ttu-id="249ed-128">Описывает константный буфер шейдера.</span><span class="sxs-lookup"><span data-stu-id="249ed-128">Describes a shader constant-buffer.</span></span><br/>                         |
| [<span data-ttu-id="249ed-129">**Построитель текстуры D3D11, \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="249ed-129">**D3D11\_SHADER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_desc)<br/>                                 | <span data-ttu-id="249ed-130">Описывает шейдер.</span><span class="sxs-lookup"><span data-stu-id="249ed-130">Describes a shader.</span></span><br/>                                         |
| [<span data-ttu-id="249ed-131">**\_ \_ \_ DESC входной привязки шейдера \_ D3D11**</span><span class="sxs-lookup"><span data-stu-id="249ed-131">**D3D11\_SHADER\_INPUT\_BIND\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_input_bind_desc)<br/>         | <span data-ttu-id="249ed-132">Описывает привязку ресурса шейдера к входным данным шейдера.</span><span class="sxs-lookup"><span data-stu-id="249ed-132">Describes how a shader resource is bound to a shader input.</span></span><br/> |
| [<span data-ttu-id="249ed-133">**\_DESC шейдера \_ D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="249ed-133">**D3D11\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_shader_trace_desc)<br/>                    | <span data-ttu-id="249ed-134">Описывает объект трассировки шейдера.</span><span class="sxs-lookup"><span data-stu-id="249ed-134">Describes a shader-trace object.</span></span><br/>                            |
| [<span data-ttu-id="249ed-135">**\_Тип D3D11 шейдера " \_ \_ DESC"**</span><span class="sxs-lookup"><span data-stu-id="249ed-135">**D3D11\_SHADER\_TYPE\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_type_desc)<br/>                      | <span data-ttu-id="249ed-136">Описывает тип переменной шейдера.</span><span class="sxs-lookup"><span data-stu-id="249ed-136">Describes a shader-variable type.</span></span><br/>                           |
| [<span data-ttu-id="249ed-137">**D3D11ая \_ переменная шейдера \_ \_**</span><span class="sxs-lookup"><span data-stu-id="249ed-137">**D3D11\_SHADER\_VARIABLE\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_variable_desc)<br/>              | <span data-ttu-id="249ed-138">Описывает переменную шейдера.</span><span class="sxs-lookup"><span data-stu-id="249ed-138">Describes a shader variable.</span></span><br/>                                |
| [<span data-ttu-id="249ed-139">**\_DESC параметра сигнатуры D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="249ed-139">**D3D11\_SIGNATURE\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)<br/>      | <span data-ttu-id="249ed-140">Описывает сигнатуру шейдера.</span><span class="sxs-lookup"><span data-stu-id="249ed-140">Describes a shader signature.</span></span><br/>                               |
| [<span data-ttu-id="249ed-141">**\_Регистр трассировки \_ D3D11**</span><span class="sxs-lookup"><span data-stu-id="249ed-141">**D3D11\_TRACE\_REGISTER**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_register)<br/>                           | <span data-ttu-id="249ed-142">Описывает регистр трассировки.</span><span class="sxs-lookup"><span data-stu-id="249ed-142">Describes a trace register.</span></span><br/>                                 |
| [<span data-ttu-id="249ed-143">**\_Статистика трассировки \_ D3D11**</span><span class="sxs-lookup"><span data-stu-id="249ed-143">**D3D11\_TRACE\_STATS**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_stats)<br/>                                 | <span data-ttu-id="249ed-144">Указывает статистику трассировки.</span><span class="sxs-lookup"><span data-stu-id="249ed-144">Specifies statistics about a trace.</span></span><br/>                         |
| [<span data-ttu-id="249ed-145">**\_Шаг трассировки \_ D3D11**</span><span class="sxs-lookup"><span data-stu-id="249ed-145">**D3D11\_TRACE\_STEP**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_step)<br/>                                   | <span data-ttu-id="249ed-146">Описывает шаг трассировки, который является инструкцией.</span><span class="sxs-lookup"><span data-stu-id="249ed-146">Describes a trace step, which is an instruction.</span></span><br/>            |
| [<span data-ttu-id="249ed-147">**\_Значение трассировки \_ D3D11**</span><span class="sxs-lookup"><span data-stu-id="249ed-147">**D3D11\_TRACE\_VALUE**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_value)<br/>                                 | <span data-ttu-id="249ed-148">Описывает значение трассировки.</span><span class="sxs-lookup"><span data-stu-id="249ed-148">Describes a trace value.</span></span><br/>                                    |
| [<span data-ttu-id="249ed-149">**\_DESC D3D11 вершинного \_ шейдера \_ \_**</span><span class="sxs-lookup"><span data-stu-id="249ed-149">**D3D11\_VERTEX\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_vertex_shader_trace_desc)<br/>     | <span data-ttu-id="249ed-150">Описывает экземпляр шейдера вершин для трассировки.</span><span class="sxs-lookup"><span data-stu-id="249ed-150">Describes an instance of a vertex shader to trace.</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="249ed-151">См. также</span><span class="sxs-lookup"><span data-stu-id="249ed-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="249ed-152">Справочник по шейдерам</span><span class="sxs-lookup"><span data-stu-id="249ed-152">Shader Reference</span></span>](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

 





