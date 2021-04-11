---
description: 'В этом разделе содержатся сведения о следующих структурах шейдеров:'
ms.assetid: b36309e0-1c44-42d9-adcf-33acd753438c
title: Структуры шейдеров (графика Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0d84096e743b15e0d5f85635dab4caf72c7e93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262696"
---
# <a name="shader-structures-direct3d-10-graphics"></a><span data-ttu-id="89f1e-103">Структуры шейдеров (графика Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="89f1e-103">Shader Structures (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="89f1e-104">В этом разделе содержатся сведения о следующих структурах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="89f1e-104">This section contains information about the following shader structures:</span></span>



| <span data-ttu-id="89f1e-105">Структуры</span><span class="sxs-lookup"><span data-stu-id="89f1e-105">Structures</span></span>                                                                         | <span data-ttu-id="89f1e-106">Описание</span><span class="sxs-lookup"><span data-stu-id="89f1e-106">Description</span></span>                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="89f1e-107">**\_DESC буфера шейдеров D3D10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="89f1e-107">**D3D10\_SHADER\_BUFFER\_DESC**</span></span>](/windows/win32/api/D3D10Shader/ns-d3d10shader-d3d10_shader_buffer_desc)                    | <span data-ttu-id="89f1e-108">Описывает буфер шейдера или буфер текстуры шейдера.</span><span class="sxs-lookup"><span data-stu-id="89f1e-108">Describes a shader-constant buffer or a shader-texture buffer.</span></span>                        |
| [<span data-ttu-id="89f1e-109">**Построитель текстуры D3D10, \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="89f1e-109">**D3D10\_SHADER\_DESC**</span></span>](/windows/win32/api/D3D10Shader/ns-d3d10shader-d3d10_shader_desc)                                   | <span data-ttu-id="89f1e-110">Описывает шейдер.</span><span class="sxs-lookup"><span data-stu-id="89f1e-110">Describes a shader.</span></span>                                                                   |
| [<span data-ttu-id="89f1e-111">**\_ \_ \_ Сведения о файле отладки шейдера D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="89f1e-111">**D3D10\_SHADER\_DEBUG\_FILE\_INFO**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_file_info)           | <span data-ttu-id="89f1e-112">Описывает файлы, включаемые шейдером.</span><span class="sxs-lookup"><span data-stu-id="89f1e-112">Describes files included by a shader.</span></span>                                                 |
| [<span data-ttu-id="89f1e-113">**\_ \_ Сведения об отладке ШЕЙДЕРов D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="89f1e-113">**D3D10\_SHADER\_DEBUG\_INFO**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_info)                      | <span data-ttu-id="89f1e-114">Описывает формат интерфейса ID3D10Blob, возвращаемого методом D3D10GetShaderDebugInfo.</span><span class="sxs-lookup"><span data-stu-id="89f1e-114">Describes the format of the ID3D10Blob Interface returned by D3D10GetShaderDebugInfo.</span></span> |
| [<span data-ttu-id="89f1e-115">**\_ \_ \_ Сведения о входных данных отладки шейдера D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="89f1e-115">**D3D10\_SHADER\_DEBUG\_INPUT\_INFO**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_input_info)         | <span data-ttu-id="89f1e-116">Описывает входные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="89f1e-116">Describes a shader input.</span></span>                                                             |
| [<span data-ttu-id="89f1e-117">**\_ \_ \_ Сведения о inst отладки шейдеров D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="89f1e-117">**D3D10\_SHADER\_DEBUG\_INST\_INFO**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_inst_info)           | <span data-ttu-id="89f1e-118">Содержит данные инструкции.</span><span class="sxs-lookup"><span data-stu-id="89f1e-118">Contains instruction data.</span></span>                                                            |
| [<span data-ttu-id="89f1e-119">**\_ \_ \_ Сведения о аутпутрег отладки шейдеров D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="89f1e-119">**D3D10\_SHADER\_DEBUG\_OUTPUTREG\_INFO**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_outputreg_info) | <span data-ttu-id="89f1e-120">Описывает выходной регистр шейдера.</span><span class="sxs-lookup"><span data-stu-id="89f1e-120">Describes a shader output register.</span></span>                                                   |
| [<span data-ttu-id="89f1e-121">**\_Аутпутвар отладки шейдера D3D10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="89f1e-121">**D3D10\_SHADER\_DEBUG\_OUTPUTVAR**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_outputvar)            | <span data-ttu-id="89f1e-122">Описывает выходную переменную шейдера.</span><span class="sxs-lookup"><span data-stu-id="89f1e-122">Describes a shader output variable.</span></span>                                                   |
| [<span data-ttu-id="89f1e-123">**\_ \_ \_ Сведения о области отладки шейдера D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="89f1e-123">**D3D10\_SHADER\_DEBUG\_SCOPE\_INFO**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_scope_info)         | <span data-ttu-id="89f1e-124">Содержит данные области, которые сопоставляют имена переменных с переменными отладки.</span><span class="sxs-lookup"><span data-stu-id="89f1e-124">Contains scope data that maps variable names to debug variables.</span></span>                      |
| [<span data-ttu-id="89f1e-125">**\_ \_ \_ Сведения о скопевар отладки шейдеров D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="89f1e-125">**D3D10\_SHADER\_DEBUG\_SCOPEVAR\_INFO**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_scopevar_info)   | <span data-ttu-id="89f1e-126">Описывает переменную области.</span><span class="sxs-lookup"><span data-stu-id="89f1e-126">Describes a scope variable.</span></span>                                                           |
| [<span data-ttu-id="89f1e-127">**\_ \_ \_ Сведения о маркере отладки шейдера D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="89f1e-127">**D3D10\_SHADER\_DEBUG\_TOKEN\_INFO**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_token_info)         | <span data-ttu-id="89f1e-128">Возвращает исходное расположение для элемента шейдера.</span><span class="sxs-lookup"><span data-stu-id="89f1e-128">Gives the source location for a shader element.</span></span>                                       |
| [<span data-ttu-id="89f1e-129">**\_ \_ Отладочный VarType D3D10 шейдера \_**</span><span class="sxs-lookup"><span data-stu-id="89f1e-129">**D3D10\_SHADER\_DEBUG\_VARTYPE**</span></span>](/windows/win32/api/d3d10_1shader/ne-d3d10_1shader-d3d10_shader_debug_vartype)                | <span data-ttu-id="89f1e-130">Отличает переменные от функций в области.</span><span class="sxs-lookup"><span data-stu-id="89f1e-130">Distinguishes variables from functions in a scope.</span></span>                                    |
| [<span data-ttu-id="89f1e-131">**\_ \_ \_ Сведения о var отладочного шейдера D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="89f1e-131">**D3D10\_SHADER\_DEBUG\_VAR\_INFO**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_var_info)             | <span data-ttu-id="89f1e-132">Содержит сведения о переменной.</span><span class="sxs-lookup"><span data-stu-id="89f1e-132">Contains information on a variable.</span></span>                                                   |
| [<span data-ttu-id="89f1e-133">**\_ \_ \_ DESC входной привязки шейдера \_ D3D10**</span><span class="sxs-lookup"><span data-stu-id="89f1e-133">**D3D10\_SHADER\_INPUT\_BIND\_DESC**</span></span>](/windows/win32/api/D3D10Shader/ns-d3d10shader-d3d10_shader_input_bind_desc)           | <span data-ttu-id="89f1e-134">Описывает привязку ресурса шейдера к входным данным шейдера.</span><span class="sxs-lookup"><span data-stu-id="89f1e-134">Describes how a shader resource is bound to a shader input.</span></span>                           |
| [<span data-ttu-id="89f1e-135">**\_Макрос шейдера \_ D3D**</span><span class="sxs-lookup"><span data-stu-id="89f1e-135">**D3D\_SHADER\_MACRO**</span></span>](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)                                 | <span data-ttu-id="89f1e-136">Определяет макрос шейдера.</span><span class="sxs-lookup"><span data-stu-id="89f1e-136">Defines a shader macro.</span></span>                                                               |
| [<span data-ttu-id="89f1e-137">**\_Тип D3D10 шейдера " \_ \_ DESC"**</span><span class="sxs-lookup"><span data-stu-id="89f1e-137">**D3D10\_SHADER\_TYPE\_DESC**</span></span>](/windows/win32/api/D3D10Shader/ns-d3d10shader-d3d10_shader_type_desc)                        | <span data-ttu-id="89f1e-138">Описывает тип переменной шейдера.</span><span class="sxs-lookup"><span data-stu-id="89f1e-138">Describes a shader-variable type.</span></span>                                                     |
| [<span data-ttu-id="89f1e-139">**D3D10ая \_ переменная шейдера \_ \_**</span><span class="sxs-lookup"><span data-stu-id="89f1e-139">**D3D10\_SHADER\_VARIABLE\_DESC**</span></span>](/windows/win32/api/D3D10Shader/ns-d3d10shader-d3d10_shader_variable_desc)                | <span data-ttu-id="89f1e-140">Описывает переменную шейдера.</span><span class="sxs-lookup"><span data-stu-id="89f1e-140">Describes a shader variable.</span></span>                                                          |
| [<span data-ttu-id="89f1e-141">**\_DESC параметра сигнатуры D3D10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="89f1e-141">**D3D10\_SIGNATURE\_PARAMETER\_DESC**</span></span>](/windows/win32/api/D3D10Shader/ns-d3d10shader-d3d10_signature_parameter_desc)        | <span data-ttu-id="89f1e-142">Описывает сигнатуру шейдера.</span><span class="sxs-lookup"><span data-stu-id="89f1e-142">Describes a shader signature.</span></span>                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="89f1e-143">См. также</span><span class="sxs-lookup"><span data-stu-id="89f1e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89f1e-144">Справочник по шейдерам</span><span class="sxs-lookup"><span data-stu-id="89f1e-144">Shader Reference</span></span>](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 



