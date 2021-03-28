---
title: Параметры создания мозаичных ресурсов
description: Существуют некоторые ограничения на тип ресурсов Direct3D, которые можно создать с помощью \_ флага D3D11 ресурса " \_ Разное" \_ . В этом разделе приводятся допустимые параметры для создания мозаичных ресурсов.
ms.assetid: 19A0EA7F-888D-4102-A5D2-F3B54775EDE8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b912325371c59bd46a6cc4245289b2fe5d32a924
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/13/2019
ms.locfileid: "103784866"
---
# <a name="tiled-resource-creation-parameters"></a><span data-ttu-id="2f93b-104">Параметры создания мозаичных ресурсов</span><span class="sxs-lookup"><span data-stu-id="2f93b-104">Tiled resource creation parameters</span></span>

<span data-ttu-id="2f93b-105">Существуют некоторые ограничения на тип ресурсов Direct3D, которые можно создать с помощью флага [**D3D11 \_ ресурса " \_ Разное \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) ".</span><span class="sxs-lookup"><span data-stu-id="2f93b-105">There are some constraints on the type of Direct3D resources that you can create with the [**D3D11\_RESOURCE\_MISC\_TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span> <span data-ttu-id="2f93b-106">В этом разделе приводятся допустимые параметры для создания мозаичных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2f93b-106">This section provides the valid parameters for creating tiled resources.</span></span>

<dl> <dt>

<span data-ttu-id="2f93b-107"><span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Поддерживаемый тип ресурсов**</span><span class="sxs-lookup"><span data-stu-id="2f93b-107"><span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Supported Resource Type**</span></span>
</dt> <dd>

<span data-ttu-id="2f93b-108">\[Массив Texture2D \] (включая \[ массив текстурекубе \] , который является вариантом массива Texture2D \[ \] ) или buffer.</span><span class="sxs-lookup"><span data-stu-id="2f93b-108">Texture2D\[Array\] (including TextureCube\[Array\], which is a variant of Texture2D\[Array\]) or Buffer.</span></span>

<span data-ttu-id="2f93b-109">**Не поддерживается:** Texture1D \[ array \] или Texture3D, но в будущем может поддерживаться Texture3D.</span><span class="sxs-lookup"><span data-stu-id="2f93b-109">**NOT supported:** Texture1D\[Array\] or Texture3D, but Texture3D might be supported in the future.</span></span>

</dd> <dt>

<span data-ttu-id="2f93b-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Поддерживаемое использование ресурсов**</span><span class="sxs-lookup"><span data-stu-id="2f93b-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Supported Resource Usage**</span></span>
</dt> <dd>

<span data-ttu-id="2f93b-111">\_Использование D3D11 \_ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2f93b-111">D3D11\_USAGE\_DEFAULT.</span></span>

<span data-ttu-id="2f93b-112">**Не поддерживается:** \_ \_ Динамическое использование D3D11, D3D11 \_ использование \_ промежуточного хранения или D3D11 \_ использование \_ неизменным.</span><span class="sxs-lookup"><span data-stu-id="2f93b-112">**NOT supported:** D3D11\_USAGE\_DYNAMIC, D3D11\_USAGE\_STAGING, or D3D11\_USAGE\_IMMUTABLE.</span></span>

</dd> <dt>

<span data-ttu-id="2f93b-113"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Поддерживаемые флаги для ресурсов**</span><span class="sxs-lookup"><span data-stu-id="2f93b-113"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Supported Resource Misc Flags**</span></span>
</dt> <dd>

<span data-ttu-id="2f93b-114">D3D11 \_ ресурсов \_ \_ (по определению), \_ Прочие \_ текстурекубе, \_ дравиндирект \_ args, \_ buffer \_ Разрешить \_ необработанные \_ представления \_ , \_ структурированный буфер, \_ \_ срез ресурсов или \_ Создание \_ MIPS.</span><span class="sxs-lookup"><span data-stu-id="2f93b-114">D3D11\_RESOURCE\_MISC\_TILED (by definition), \_MISC\_TEXTURECUBE, \_DRAWINDIRECT\_ARGS, \_BUFFER\_ALLOW\_RAW\_VIEWS, \_BUFFER\_STRUCTURED, \_RESOURCE\_CLAMP, or \_GENERATE\_MIPS.</span></span>

<span data-ttu-id="2f93b-115">**Не поддерживается:** \_ Общий, \_ Общий \_ кэйедмутекс, \_ \_ совместимый с GDI, \_ Общий \_ нсандле, \_ ограниченный \_ контент, \_ ограничение \_ общего \_ ресурса, \_ ограничение общего \_ \_ \_ драйвера ресурса, \_ защищенного или \_ пула плиток \_ .</span><span class="sxs-lookup"><span data-stu-id="2f93b-115">**NOT supported:** \_SHARED, \_SHARED\_KEYEDMUTEX, \_GDI\_COMPATIBLE, \_SHARED\_NTHANDLE, \_RESTRICTED\_CONTENT, \_RESTRICT\_SHARED\_RESOURCE, \_RESTRICT\_SHARED\_RESOURCE\_DRIVER, \_GUARDED, or \_TILE\_POOL.</span></span>

</dd> <dt>

<span data-ttu-id="2f93b-116"><span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Поддерживаемые флаги привязки**</span><span class="sxs-lookup"><span data-stu-id="2f93b-116"><span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Supported Bind Flags**</span></span>
</dt> <dd>

<span data-ttu-id="2f93b-117">D3D11 \_ Привязка \_ ресурса шейдера \_ , \_ \_ целевой объект прорисовки, \_ \_ трафарет глубины или \_ неупорядоченный \_ доступ.</span><span class="sxs-lookup"><span data-stu-id="2f93b-117">D3D11\_BIND\_SHADER\_RESOURCE, \_RENDER\_TARGET, \_DEPTH\_STENCIL, or \_UNORDERED\_ACCESS.</span></span>

<span data-ttu-id="2f93b-118">**Не поддерживается:** \_ Буфер КОНСТАНТы. \_ \_ \_ \[ Обратите внимание, что привязка мозаичного буфера как SRV/UAV/РТВ по-прежнему продолжается \] , \_ \_ буфер индекса, \_ потоковый \_ выход, \_ \_ декодер привязки или \_ \_ \_ видеокодировщик.</span><span class="sxs-lookup"><span data-stu-id="2f93b-118">**NOT supported:** \_CONSTANT\_BUFFER, \_VERTEX\_BUFFER \[note that binding a tiled Buffer as an SRV/UAV/RTV is still ok\], \_INDEX\_BUFFER, \_STREAM\_OUTPUT, \_BIND\_DECODER, or \_BIND\_VIDEO\_ENCODER.</span></span>

</dd> <dt>

<span data-ttu-id="2f93b-119"><span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Поддерживаемые форматы**</span><span class="sxs-lookup"><span data-stu-id="2f93b-119"><span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Supported Formats**</span></span>
</dt> <dd>

<span data-ttu-id="2f93b-120">Все форматы, которые будут доступны для определенной конфигурации независимо от разбиения на плитки с некоторыми исключениями.</span><span class="sxs-lookup"><span data-stu-id="2f93b-120">All formats that would be available for the given configuration regardless of it being tiled, with some exceptions.</span></span>

</dd> <dt>

<span data-ttu-id="2f93b-121"><span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**Поддерживаемые Сампледеск (число многовыборок, качество)**</span><span class="sxs-lookup"><span data-stu-id="2f93b-121"><span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**Supported SampleDesc (Multisample count, quality)**</span></span>
</dt> <dd>

<span data-ttu-id="2f93b-122">То, что будет поддерживаться для определенной конфигурации независимо от разбиения на плитки с некоторыми исключениями.</span><span class="sxs-lookup"><span data-stu-id="2f93b-122">Whatever would be supported for the given configuration regardless of it being tiled, with some exceptions.</span></span>

</dd> <dt>

<span data-ttu-id="2f93b-123"><span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Поддерживаемые значения width/height/Миплевелс/размера массива**</span><span class="sxs-lookup"><span data-stu-id="2f93b-123"><span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Supported Width/Height/MipLevels/ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="2f93b-124">Все экстенты, поддерживаемые Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="2f93b-124">Full extents supported by Direct3D 11.</span></span> <span data-ttu-id="2f93b-125">Ресурсы мозаичного заполнения не имеют ограничений на общий объем памяти, накладываемый на ресурсы без мозаичного заполнения.</span><span class="sxs-lookup"><span data-stu-id="2f93b-125">Tiled resources don't have the restriction on total memory size imposed on non-tiled resources.</span></span> <span data-ttu-id="2f93b-126">Ресурсы мозаичного заполнения ограничиваются только общими ограничениями виртуального адресного пространства.</span><span class="sxs-lookup"><span data-stu-id="2f93b-126">Tiled resources are only constrained by overall virtual address space limits.</span></span> <span data-ttu-id="2f93b-127">Сведения см. в разделе [адресное пространство, доступное для мозаичного заполнения ресурсов](address-space-available-for-tiled-resources.md).</span><span class="sxs-lookup"><span data-stu-id="2f93b-127">For info, see [Address space available for tiled resources](address-space-available-for-tiled-resources.md).</span></span>

</dd> </dl>

<span data-ttu-id="2f93b-128">Начальное содержимое пула памяти плиток не определено.</span><span class="sxs-lookup"><span data-stu-id="2f93b-128">The initial contents of tile pool memory are undefined.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f93b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="2f93b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f93b-130">Создание мозаичных ресурсов</span><span class="sxs-lookup"><span data-stu-id="2f93b-130">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




