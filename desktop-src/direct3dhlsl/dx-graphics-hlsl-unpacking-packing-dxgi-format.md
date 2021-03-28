---
title: Распаковка и упаковка DXGI_FORMAT для изменения изображения In-Place
description: Файл D3DX \_ дксгиформатконверт. inl содержит функции преобразования встроенного формата, которые можно использовать в шейдере вычислений или шейдере пикселей на оборудовании Direct3D 11.
ms.assetid: 328c4488-9758-4359-a37b-ac50f20e2940
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c613a3f0068537733961b58a8a4c2b4528d21f25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329072"
---
# <a name="unpacking-and-packing-dxgi_format-for-in-place-image-editing"></a><span data-ttu-id="18920-103">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="18920-103">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>

<span data-ttu-id="18920-104">Файл D3DX \_ дксгиформатконверт. inl содержит функции преобразования встроенного формата, которые можно использовать в шейдере вычислений или шейдере пикселей на оборудовании Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="18920-104">The D3DX\_DXGIFormatConvert.inl file contains inline format conversion functions that you can use in the compute shader or pixel shader on Direct3D 11 hardware.</span></span> <span data-ttu-id="18920-105">Эти функции можно использовать в приложении для одновременного чтения и записи текстуры.</span><span class="sxs-lookup"><span data-stu-id="18920-105">You can use these functions in your application to simultaneously both read from and write to a texture.</span></span> <span data-ttu-id="18920-106">Это значит, что можно выполнять редактирование изображений на месте.</span><span class="sxs-lookup"><span data-stu-id="18920-106">That is, you can perform in-place image editing.</span></span> <span data-ttu-id="18920-107">Чтобы использовать эти функции преобразования встроенного формата, включите в \_ приложение файл D3DX дксгиформатконверт. inl.</span><span class="sxs-lookup"><span data-stu-id="18920-107">To use these inline format conversion functions, include the D3DX\_DXGIFormatConvert.inl file in your application.</span></span>

<span data-ttu-id="18920-108">Неупорядоченное представление доступа Direct3D 11 (UAV) ресурса Texture1D, Texture2D или Texture3D поддерживает чтение и запись в память из шейдера вычислений или шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="18920-108">Direct3D 11's Unordered Access View (UAV) of a Texture1D, Texture2D, or Texture3D resource supports random access reads and writes to memory from a compute shader or pixel shader.</span></span> <span data-ttu-id="18920-109">Однако Direct3D 11 поддерживает одновременно чтение из формата R32 uint и запись в него только в формате этой \_ \_ \_ текстуры.</span><span class="sxs-lookup"><span data-stu-id="18920-109">However, Direct3D 11 supports simultaneously both reading from and writing to only the DXGI\_FORMAT\_R32\_UINT texture format.</span></span> <span data-ttu-id="18920-110">Например, Direct3D 11 не поддерживает одновременно чтение из других и запись в другие, более полезные форматы, например, в формате DXGI \_ \_ R8G8B8A8 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="18920-110">For example, Direct3D 11 does not support simultaneously both reading from and writing to other, more useful formats, such as DXGI\_FORMAT\_R8G8B8A8\_UNORM.</span></span> <span data-ttu-id="18920-111">Можно использовать только UAV для записи произвольного доступа в такие форматы, или можно использовать только шейдер представление ресурсов (SRV) для чтения произвольного доступа из таких других форматов.</span><span class="sxs-lookup"><span data-stu-id="18920-111">You can use only a UAV to random access write to such other formats, or you can use only a Shader Resource View (SRV) to random access read from such other formats.</span></span> <span data-ttu-id="18920-112">Оборудование для преобразования формата недоступно для одновременного чтения из таких форматов и записи в них.</span><span class="sxs-lookup"><span data-stu-id="18920-112">Format conversion hardware is not available to simultaneously both read from and write to such other formats.</span></span>

<span data-ttu-id="18920-113">Тем не менее вы по-прежнему можете одновременно выполнять операции чтения и записи в таких форматах, применяя текстуру к формату R32 uint в формате DXGI \_ \_ \_ , при создании UAV, если исходный формат ресурса поддерживает приведение к \_ формату DXGI \_ R32 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="18920-113">However, you can still simultaneously both read from and write to such other formats by casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format when you create a UAV, as long as the original format of the resource supports casting to DXGI\_FORMAT\_R32\_UINT.</span></span> <span data-ttu-id="18920-114">В большинстве 32 форматов элементов поддерживается приведение к \_ формату DXGI \_ R32 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="18920-114">Most 32 bit per element formats support casting to DXGI\_FORMAT\_R32\_UINT.</span></span> <span data-ttu-id="18920-115">Путем приведения текстуры к формату \_ R32 uint в формате DXGI \_ \_ , при создании UAV можно одновременно выполнять операции чтения и записи в текстуру, если шейдер выполняет распаковку в ручном формате для чтения и упаковки при записи.</span><span class="sxs-lookup"><span data-stu-id="18920-115">By casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format when you create a UAV, you can then simultaneous perform reads and writes to the texture as long as the shader performs manual format unpacking on read and packing on write.</span></span>

<span data-ttu-id="18920-116">Преимуществом приведения текстуры к формату \_ \_ R32 uint формата DXGI \_ является то, что позже можно будет использовать соответствующий формат (например, в \_ формате DXGI \_ R16G16 \_ float) с другими представлениями на той же текстуре, например представления целевого объекта отрисовки (RTVs) или СРВС.</span><span class="sxs-lookup"><span data-stu-id="18920-116">The benefit of casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format is that later on you can use the appropriate format (for example, DXGI\_FORMAT\_R16G16\_FLOAT) with other views on the same texture, such as Render Target Views (RTVs) or SRVs.</span></span> <span data-ttu-id="18920-117">Таким образом, оборудование может выполнять Стандартный автоматический распаковки и упаковки, может выполнять фильтрацию текстур и т. д. в случае отсутствия ограничений на оборудование.</span><span class="sxs-lookup"><span data-stu-id="18920-117">Therefore, the hardware can perform the typical automatic format unpack and pack, can perform texture filtering, and so on where there are no hardware limitations.</span></span>

<span data-ttu-id="18920-118">В следующем сценарии требуется, чтобы приложение выполнило следующую последовательность действий для редактирования изображений на месте.</span><span class="sxs-lookup"><span data-stu-id="18920-118">The following scenario requires that an application take the following sequence of actions to perform in-place image editing.</span></span>

<span data-ttu-id="18920-119">Предположим, вы хотите создать текстуру, на которой можно использовать шейдер пикселей или шейдер для выполнения редактирования на месте, и необходимо, чтобы данные текстуры хранились в формате, который является потомком одного из следующих форматов, не имеющих тип:</span><span class="sxs-lookup"><span data-stu-id="18920-119">Suppose you want to make a texture on which you can use a pixel shader or compute shader to perform in-place editing, and you want the texture data to be stored in a format that is a descendant of one of the following TYPELESS formats:</span></span>

-   <span data-ttu-id="18920-120">\_Формат DXGI \_ R10G10B10A2 \_ тип</span><span class="sxs-lookup"><span data-stu-id="18920-120">DXGI\_FORMAT\_R10G10B10A2\_TYPELESS</span></span>
-   <span data-ttu-id="18920-121">\_Формат DXGI \_ R8G8B8A8 \_ тип</span><span class="sxs-lookup"><span data-stu-id="18920-121">DXGI\_FORMAT\_R8G8B8A8\_TYPELESS</span></span>
-   <span data-ttu-id="18920-122">\_Формат DXGI \_ B8G8R8A8 \_ тип</span><span class="sxs-lookup"><span data-stu-id="18920-122">DXGI\_FORMAT\_B8G8R8A8\_TYPELESS</span></span>
-   <span data-ttu-id="18920-123">\_Формат DXGI \_ B8G8R8X8 \_ тип</span><span class="sxs-lookup"><span data-stu-id="18920-123">DXGI\_FORMAT\_B8G8R8X8\_TYPELESS</span></span>
-   <span data-ttu-id="18920-124">\_Формат DXGI \_ R16G16 \_ тип</span><span class="sxs-lookup"><span data-stu-id="18920-124">DXGI\_FORMAT\_R16G16\_TYPELESS</span></span>

<span data-ttu-id="18920-125">Например, формат DXGI \_ \_ R10G10B10A2 UNORM Format \_ является потомком \_ формата DXGI \_ R10G10B10A2 \_ format.</span><span class="sxs-lookup"><span data-stu-id="18920-125">For example, the DXGI\_FORMAT\_R10G10B10A2\_UNORM format is a descendant of the DXGI\_FORMAT\_R10G10B10A2\_TYPELESS format.</span></span> <span data-ttu-id="18920-126">Таким образом, \_ Формат DXGI \_ R10G10B10A2 \_ UNORM поддерживает шаблон использования, описанный в следующей последовательности.</span><span class="sxs-lookup"><span data-stu-id="18920-126">Therefore, DXGI\_FORMAT\_R10G10B10A2\_UNORM supports the usage pattern that is described in the following sequence.</span></span> <span data-ttu-id="18920-127">Форматы, которые \_ \_ относятся к формату R32 \_ без типов, такие как \_ Формат DXGI \_ R32 float, просты в поддержке, \_ не требуя использования справки по преобразованию формата, описанной в следующей последовательности.</span><span class="sxs-lookup"><span data-stu-id="18920-127">Formats that descend from DXGI\_FORMAT\_R32\_TYPELESS, such as DXGI\_FORMAT\_R32\_FLOAT, are trivially supported without requiring any of the format conversion help that is described in the following sequence.</span></span>

<span data-ttu-id="18920-128">**Выполнение редактирования изображений на месте**</span><span class="sxs-lookup"><span data-stu-id="18920-128">**To perform in-place image editing**</span></span>

1.  <span data-ttu-id="18920-129">Создайте текстуру с соответствующим форматом, зависимым от типа, который указан в предыдущем сценарии, вместе с необходимыми флагами привязки, такими как D3D11 \_ BIND \_ неупорядоченный \_ доступ \| D3D11 \_ BIND \_ \_ Resource Shader.</span><span class="sxs-lookup"><span data-stu-id="18920-129">Create a texture with the appropriate TYPELESS-dependent format that is specified in the previous scenario together with the required bind flags, such as D3D11\_BIND\_UNORDERED\_ACCESS \| D3D11\_BIND\_SHADER\_RESOURCE.</span></span>
2.  <span data-ttu-id="18920-130">Для редактирования изображений на месте создайте UAV с \_ \_ \_ форматом DXGI R32 uint.</span><span class="sxs-lookup"><span data-stu-id="18920-130">For in-place image editing, create a UAV with the DXGI\_FORMAT\_R32\_UINT format.</span></span> <span data-ttu-id="18920-131">API Direct3D 11 обычно не допускает приведение между различными форматами семейства.</span><span class="sxs-lookup"><span data-stu-id="18920-131">The Direct3D 11 API typically does not allow casting between different format "families."</span></span> <span data-ttu-id="18920-132">Однако API Direct3D 11 создает исключение с форматом DXGI \_ \_ R32 \_ uint Format.</span><span class="sxs-lookup"><span data-stu-id="18920-132">However, the Direct3D 11 API makes an exception with the DXGI\_FORMAT\_R32\_UINT format.</span></span>
3.  <span data-ttu-id="18920-133">В выстроителе вычислений или шейдере пикселей используйте подходящий пакет встроенного формата и функции распаковки, которые предоставляются в \_ файле D3DX дксгиформатконверт. inl.</span><span class="sxs-lookup"><span data-stu-id="18920-133">In the compute shader or pixel shader, use the appropriate inline format pack and unpack functions that are provided in the D3DX\_DXGIFormatConvert.inl file.</span></span> <span data-ttu-id="18920-134">Например, предположим, что \_ Формат DXGI \_ R32 \_ uint UAV для текстуры действительно содержит формат DXGI \_ \_ R10G10B10A2 \_ UNORM-Format Data.</span><span class="sxs-lookup"><span data-stu-id="18920-134">For example, suppose the DXGI\_FORMAT\_R32\_UINT UAV of the texture really holds DXGI\_FORMAT\_R10G10B10A2\_UNORM-formatted data.</span></span> <span data-ttu-id="18920-135">После того как приложение считывает значение uint из UAV в шейдер, оно должно вызвать следующую функцию для распаковки формата текстуры:</span><span class="sxs-lookup"><span data-stu-id="18920-135">After the application reads a uint from the UAV into the shader, it must call the following function to unpack the texture format:</span></span>

    ```
    XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
    ```

    

    <span data-ttu-id="18920-136">Затем, чтобы записать данные в UAV в том же шейдере, приложение вызывает следующую функцию для упаковки данных шейдера в uint, которые приложение может записать в UAV:</span><span class="sxs-lookup"><span data-stu-id="18920-136">Then, to write to the UAV in the same shader, the application calls the following function to pack shader data into a uint that the application can write to the UAV:</span></span>

    ```
    UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
    ```

    

4.  <span data-ttu-id="18920-137">Затем приложение может создать другие представления, например СРВС, с требуемым форматом.</span><span class="sxs-lookup"><span data-stu-id="18920-137">The application can then create other views, such as SRVs, with the required format.</span></span> <span data-ttu-id="18920-138">Например, приложение может создать SRV с \_ \_ \_ форматом DXGI R10G10B10A2 UNORM, если ресурс был создан как \_ Формат DXGI \_ R10G10B10A2 Type без \_ типа.</span><span class="sxs-lookup"><span data-stu-id="18920-138">For example, the application can create a SRV with the DXGI\_FORMAT\_R10G10B10A2\_UNORM format if the resource was created as DXGI\_FORMAT\_R10G10B10A2\_TYPELESS.</span></span> <span data-ttu-id="18920-139">Когда шейдер получает доступ к этой SRV-записи, оборудование может выполнять автоматическое преобразование типов обычным образом.</span><span class="sxs-lookup"><span data-stu-id="18920-139">When a shader accesses that SRV, the hardware can perform automatic type conversion as usual.</span></span>

> [!Note]  
> <span data-ttu-id="18920-140">Если шейдер должен выполнять запись только в UAV или считывать как SRV, ни одно из этого преобразования не требуется, так как можно использовать полностью типизированный Уавс или СРВС.</span><span class="sxs-lookup"><span data-stu-id="18920-140">If the shader must write only to a UAV, or read as an SRV, none of this conversion work is needed because you can use fully typed UAVs or SRVs.</span></span> <span data-ttu-id="18920-141">Функции преобразования формата, предоставляемые в D3DX \_ дксгиформатконверт. inl, потенциально полезны только в том случае, если требуется выполнить одновременное чтение из UAV текстуры и запись в него.</span><span class="sxs-lookup"><span data-stu-id="18920-141">The format conversion functions provided in D3DX\_DXGIFormatConvert.inl are potentially useful only if you want to perform simultaneous reading from and writing to a UAV of a texture.</span></span>

 

<span data-ttu-id="18920-142">Ниже приведен список функций преобразования формата, которые включены в \_ файл D3DX дксгиформатконверт. inl.</span><span class="sxs-lookup"><span data-stu-id="18920-142">The following is the list of format conversion functions that are included in the D3DX\_DXGIFormatConvert.inl file.</span></span> <span data-ttu-id="18920-143">Эти функции классифицируются по \_ формату DXGI, который они распаковать и упаковать.</span><span class="sxs-lookup"><span data-stu-id="18920-143">These functions are categorized by the DXGI\_FORMAT that they unpack and pack.</span></span> <span data-ttu-id="18920-144">Каждый из поддерживаемых форматов в порядке убывания из одного из форматов без типа, перечисленных в предыдущем сценарии, и поддерживает приведение к \_ формату DXGI \_ R32 \_ uint в виде UAV.</span><span class="sxs-lookup"><span data-stu-id="18920-144">Each of the supported formats descends from one of the TYPELESS formats listed in the preceding scenario and supports casting to DXGI\_FORMAT\_R32\_UINT as a UAV.</span></span>

<dl> <dt>

<span data-ttu-id="18920-145"><span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>\_Формат DXGI \_ R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="18920-145"><span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>DXGI\_FORMAT\_R10G10B10A2\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="18920-146"><span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>\_Формат DXGI \_ R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="18920-146"><span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>DXGI\_FORMAT\_R10G10B10A2\_UINT</span></span>
</dt> <dd>


```
XMUINT4 D3DX_R10G10B10A2_UINT_to_UINT4(UINT packedInput)
UINT    D3DX_UINT4_to_R10G10B10A2_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="18920-147"><span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>\_Формат DXGI \_ R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="18920-147"><span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>DXGI\_FORMAT\_R8G8B8A8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="18920-148"><span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>\_Формат DXGI \_ R8G8B8A8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="18920-148"><span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="18920-149">\_Функция неточного типа использует инструкции шейдера, которые не имеют достаточно большой точности для получения точного ответа.</span><span class="sxs-lookup"><span data-stu-id="18920-149">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="18920-150">Альтернативная функция использует таблицу подстановки, хранящуюся в шейдере, чтобы обеспечить точное преобразование с плавающей запятой SRGB->.</span><span class="sxs-lookup"><span data-stu-id="18920-150">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="18920-151"><span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>\_Формат DXGI \_ R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="18920-151"><span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>DXGI\_FORMAT\_R8G8B8A8\_UINT</span></span>
</dt> <dd>


```
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(UINT packedInput)
XMUINT  D3DX_UINT4_to_R8G8B8A8_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="18920-152"><span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>\_Формат DXGI \_ R8G8B8A8 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="18920-152"><span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>DXGI\_FORMAT\_R8G8B8A8\_SNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_SNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="18920-153"><span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>\_Формат DXGI \_ R8G8B8A8 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="18920-153"><span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>DXGI\_FORMAT\_R8G8B8A8\_SINT</span></span>
</dt> <dd>


```
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(UINT packedInput)
UINT   D3DX_INT4_to_R8G8B8A8_SINT(XMINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="18920-154"><span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>\_Формат DXGI \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="18920-154"><span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_B8G8R8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="18920-155"><span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>\_Формат DXGI \_ B8G8R8A8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="18920-155"><span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="18920-156">\_Функция неточного типа использует инструкции шейдера, которые не имеют достаточно большой точности для получения точного ответа.</span><span class="sxs-lookup"><span data-stu-id="18920-156">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="18920-157">Альтернативная функция использует таблицу подстановки, хранящуюся в шейдере, чтобы обеспечить точное преобразование с плавающей запятой SRGB->.</span><span class="sxs-lookup"><span data-stu-id="18920-157">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="18920-158"><span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>\_Формат DXGI \_ B8G8R8X8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="18920-158"><span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>DXGI\_FORMAT\_B8G8R8X8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM(hlsl_precise XMFLOAT3 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="18920-159"><span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>\_Формат DXGI \_ B8G8R8X8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="18920-159"><span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(UINT packedInput) *
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(hlsl_precise XMFLOAT3 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="18920-160">\_Функция неточного типа использует инструкции шейдера, которые не имеют достаточно большой точности для получения точного ответа.</span><span class="sxs-lookup"><span data-stu-id="18920-160">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="18920-161">Альтернативная функция использует таблицу подстановки, хранящуюся в шейдере, чтобы обеспечить точное преобразование с плавающей запятой SRGB->.</span><span class="sxs-lookup"><span data-stu-id="18920-161">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="18920-162"><span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>\_Формат DXGI \_ R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="18920-162"><span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>DXGI\_FORMAT\_R16G16\_FLOAT</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_FLOAT(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="18920-163"><span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>\_Формат DXGI \_ R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="18920-163"><span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>DXGI\_FORMAT\_R16G16\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_UNORM(hlsl_precise FLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="18920-164"><span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>\_Формат DXGI \_ R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="18920-164"><span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>DXGI\_FORMAT\_R16G16\_UINT</span></span>
</dt> <dd>


```
XMUINT2 D3DX_R16G16_UINT_to_UINT2(UINT packedInput)
UINT    D3DX_UINT2_to_R16G16_UINT(XMUINT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="18920-165"><span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>\_Формат DXGI \_ R16G16 \_ снорм</span><span class="sxs-lookup"><span data-stu-id="18920-165"><span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>DXGI\_FORMAT\_R16G16\_SNORM</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_SNORM(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="18920-166"><span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>\_Формат DXGI \_ R16G16 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="18920-166"><span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>DXGI\_FORMAT\_R16G16\_SINT</span></span>
</dt> <dd>


```
XMINT2 D3DX_R16G16_SINT_to_INT2(UINT packedInput)
UINT   D3DX_INT2_to_R16G16_SINT(XMINT2 unpackedInput)
```



</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="18920-167">См. также</span><span class="sxs-lookup"><span data-stu-id="18920-167">Related Topics</span></span>

[<span data-ttu-id="18920-168">Руководство по программированию для HLSL</span><span class="sxs-lookup"><span data-stu-id="18920-168">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="18920-169">См. также</span><span class="sxs-lookup"><span data-stu-id="18920-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18920-170">Руководство по программированию для HLSL</span><span class="sxs-lookup"><span data-stu-id="18920-170">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




