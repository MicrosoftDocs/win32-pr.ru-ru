---
description: Определяет класс памяти, который содержит буферы для ресурса.
ms.assetid: 29720b5f-16d7-4bd9-a7bd-e4dbfb00070b
title: Перечисление D3DPOOL (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPOOL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dc1d69d094b2f810855f9ce2116c472ba8ab605e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647851"
---
# <a name="d3dpool-enumeration"></a><span data-ttu-id="5d900-103">Перечисление D3DPOOL</span><span class="sxs-lookup"><span data-stu-id="5d900-103">D3DPOOL enumeration</span></span>

<span data-ttu-id="5d900-104">Определяет класс памяти, который содержит буферы для ресурса.</span><span class="sxs-lookup"><span data-stu-id="5d900-104">Defines the memory class that holds the buffers for a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d900-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d900-105">Syntax</span></span>


```C++
typedef enum D3DPOOL { 
  D3DPOOL_DEFAULT      = 0,
  D3DPOOL_MANAGED      = 1,
  D3DPOOL_SYSTEMMEM    = 2,
  D3DPOOL_SCRATCH      = 3,
  D3DPOOL_FORCE_DWORD  = 0x7fffffff
} D3DPOOL, *LPD3DPOOL;
```



## <a name="constants"></a><span data-ttu-id="5d900-106">Константы</span><span class="sxs-lookup"><span data-stu-id="5d900-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5d900-107"><span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**D3DPOOL \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="5d900-107"><span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**D3DPOOL\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="5d900-108">Ресурсы помещаются в пул памяти, наиболее подходящий для набора использований, запрошенных для данного ресурса.</span><span class="sxs-lookup"><span data-stu-id="5d900-108">Resources are placed in the memory pool most appropriate for the set of usages requested for the given resource.</span></span> <span data-ttu-id="5d900-109">Обычно это видеопамять, включая как локальную видеопамять, так и память AGP.</span><span class="sxs-lookup"><span data-stu-id="5d900-109">This is usually video memory, including both local video memory and AGP memory.</span></span> <span data-ttu-id="5d900-110">Пул D3DPOOL \_ по умолчанию отличается от D3DPOOL \_ Managed и D3DPOOL \_ системмем и указывает, что ресурс помещается в предпочтительную память для доступа к устройству.</span><span class="sxs-lookup"><span data-stu-id="5d900-110">The D3DPOOL\_DEFAULT pool is separate from D3DPOOL\_MANAGED and D3DPOOL\_SYSTEMMEM, and it specifies that the resource is placed in the preferred memory for device access.</span></span> <span data-ttu-id="5d900-111">Обратите внимание, что D3DPOOL \_ по умолчанию никогда не указывает, что \_ \_ в качестве типа пула памяти для этого ресурса следует выбрать D3DPOOL Managed или D3DPOOL системмем.</span><span class="sxs-lookup"><span data-stu-id="5d900-111">Note that D3DPOOL\_DEFAULT never indicates that either D3DPOOL\_MANAGED or D3DPOOL\_SYSTEMMEM should be chosen as the memory pool type for this resource.</span></span> <span data-ttu-id="5d900-112">Текстуры, помещенные в \_ пул D3DPOOL по умолчанию, не могут быть заблокированы, если они не являются динамическими текстурами или являются частными, FourCC, форматами драйверов.</span><span class="sxs-lookup"><span data-stu-id="5d900-112">Textures placed in the D3DPOOL\_DEFAULT pool cannot be locked unless they are dynamic textures or they are private, FOURCC, driver formats.</span></span> <span data-ttu-id="5d900-113">Для доступа к незаблокированным текстурам необходимо использовать такие функции, как [**IDirect3DDevice9:: упдатесурфаце**](/windows/desktop/api), [**IDirect3DDevice9:: упдатетекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9:: Жетфронтбуффердата**](/windows/desktop/api)и [**IDirect3DDevice9:: жетрендертаржетдата**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="5d900-113">To access unlockable textures, you must use functions such as [**IDirect3DDevice9::UpdateSurface**](/windows/desktop/api), [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9::GetFrontBufferData**](/windows/desktop/api), and [**IDirect3DDevice9::GetRenderTargetData**](/windows/desktop/api).</span></span> <span data-ttu-id="5d900-114">\_Управляемый D3DPOOL, скорее всего, является лучшим выбором по сравнению с D3DPOOL \_ по умолчанию для большинства приложений.</span><span class="sxs-lookup"><span data-stu-id="5d900-114">D3DPOOL\_MANAGED is probably a better choice than D3DPOOL\_DEFAULT for most applications.</span></span> <span data-ttu-id="5d900-115">Обратите внимание, что некоторые текстуры, созданные в собственных форматах пикселей, неизвестные для среды выполнения Direct3D, могут быть заблокированы.</span><span class="sxs-lookup"><span data-stu-id="5d900-115">Note that some textures created in driver-proprietary pixel formats, unknown to the Direct3D runtime, can be locked.</span></span> <span data-ttu-id="5d900-116">Также обратите внимание, что, в отличие от задних буферов цепочки, буферы рендеринга, буфера вершин и буферы индексов могут быть заблокированы.</span><span class="sxs-lookup"><span data-stu-id="5d900-116">Also note that - unlike textures - swap chain back buffers, render targets, vertex buffers, and index buffers can be locked.</span></span> <span data-ttu-id="5d900-117">При потере устройства ресурсы, созданные с помощью D3DPOOL \_ по умолчанию, должны быть освобождены перед вызовом [**IDirect3DDevice9:: Reset**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="5d900-117">When a device is lost, resources created using D3DPOOL\_DEFAULT must be released before calling [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="5d900-118">Дополнительные сведения см. в разделе [потерянные устройства (Direct3D 9)](lost-devices.md).</span><span class="sxs-lookup"><span data-stu-id="5d900-118">For more information, see [Lost Devices (Direct3D 9)](lost-devices.md).</span></span>

<span data-ttu-id="5d900-119">При создании ресурсов с D3DPOOL \_ по умолчанию, если память видеоадаптера уже зафиксирована, управляемые ресурсы будут исключены, чтобы освободить память для удовлетворения запроса.</span><span class="sxs-lookup"><span data-stu-id="5d900-119">When creating resources with D3DPOOL\_DEFAULT, if video card memory is already committed, managed resources will be evicted to free enough memory to satisfy the request.</span></span>

</dd> <dt>

<span data-ttu-id="5d900-120"><span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**\_Управляемый D3DPOOL**</span><span class="sxs-lookup"><span data-stu-id="5d900-120"><span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**D3DPOOL\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="5d900-121">При необходимости ресурсы автоматически копируются в память, доступную для устройств.</span><span class="sxs-lookup"><span data-stu-id="5d900-121">Resources are copied automatically to device-accessible memory as needed.</span></span> <span data-ttu-id="5d900-122">Управляемые ресурсы поддерживаются системной памятью, и при потере устройства их не нужно создавать повторно.</span><span class="sxs-lookup"><span data-stu-id="5d900-122">Managed resources are backed by system memory and do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="5d900-123">Дополнительные сведения см. в разделе [Управление ресурсами (Direct3D 9)](managing-resources.md) .</span><span class="sxs-lookup"><span data-stu-id="5d900-123">See [Managing Resources (Direct3D 9)](managing-resources.md) for more information.</span></span> <span data-ttu-id="5d900-124">Управляемые ресурсы могут быть заблокированы.</span><span class="sxs-lookup"><span data-stu-id="5d900-124">Managed resources can be locked.</span></span> <span data-ttu-id="5d900-125">Напрямую изменяется только копия системной памяти.</span><span class="sxs-lookup"><span data-stu-id="5d900-125">Only the system-memory copy is directly modified.</span></span> <span data-ttu-id="5d900-126">При необходимости Direct3D копирует изменения в память, доступную для драйвера.</span><span class="sxs-lookup"><span data-stu-id="5d900-126">Direct3D copies your changes to driver-accessible memory as needed.</span></span>



|                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d900-127">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="5d900-127">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="5d900-128">\_Управляемый D3DPOOL является допустимым с [**IDirect3DDevice9**](/windows/desktop/api), однако он недопустим для [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).</span><span class="sxs-lookup"><span data-stu-id="5d900-128">D3DPOOL\_MANAGED is valid with [**IDirect3DDevice9**](/windows/desktop/api); however, it is not valid with [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5d900-129"><span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL \_ системмем**</span><span class="sxs-lookup"><span data-stu-id="5d900-129"><span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="5d900-130">Ресурсы помещаются в память, которая обычно не доступна для устройства Direct3D.</span><span class="sxs-lookup"><span data-stu-id="5d900-130">Resources are placed in memory that is not typically accessible by the Direct3D device.</span></span> <span data-ttu-id="5d900-131">Это выделение памяти потребляет системную память, но не уменьшает объем оперативной памяти.</span><span class="sxs-lookup"><span data-stu-id="5d900-131">This memory allocation consumes system RAM but does not reduce pageable RAM.</span></span> <span data-ttu-id="5d900-132">Эти ресурсы не нужно создавать повторно при потере устройства.</span><span class="sxs-lookup"><span data-stu-id="5d900-132">These resources do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="5d900-133">Ресурсы в этом пуле могут быть заблокированы и могут использоваться в качестве источника операции [**IDirect3DDevice9:: упдатесурфаце**](/windows/desktop/api) или [**IDirect3DDevice9:: упдатетекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) к ресурсу памяти, созданному с помощью D3DPOOL \_ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5d900-133">Resources in this pool can be locked and can be used as the source for a [**IDirect3DDevice9::UpdateSurface**](/windows/desktop/api) or [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) operation to a memory resource created with D3DPOOL\_DEFAULT.</span></span>

</dd> <dt>

<span data-ttu-id="5d900-134"><span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL \_**</span><span class="sxs-lookup"><span data-stu-id="5d900-134"><span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL\_SCRATCH**</span></span>
</dt> <dd>

<span data-ttu-id="5d900-135">Ресурсы размещаются в ОЗУ системы и не требуют повторного создания при потере устройства.</span><span class="sxs-lookup"><span data-stu-id="5d900-135">Resources are placed in system RAM and do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="5d900-136">Эти ресурсы не связаны с ограничениями размера устройства или формата.</span><span class="sxs-lookup"><span data-stu-id="5d900-136">These resources are not bound by device size or format restrictions.</span></span> <span data-ttu-id="5d900-137">По этой причине доступ к этим ресурсам не может осуществляться с помощью устройства Direct3D, они не задаются как текстуры или целевые объекты прорисовки.</span><span class="sxs-lookup"><span data-stu-id="5d900-137">Because of this, these resources cannot be accessed by the Direct3D device nor set as textures or render targets.</span></span> <span data-ttu-id="5d900-138">Однако эти ресурсы всегда можно создавать, блокировать и копировать.</span><span class="sxs-lookup"><span data-stu-id="5d900-138">However, these resources can always be created, locked, and copied.</span></span>

</dd> <dt>

<span data-ttu-id="5d900-139"><span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="5d900-139"><span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="5d900-140">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="5d900-140">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="5d900-141">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="5d900-141">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="5d900-142">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="5d900-142">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d900-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d900-143">Remarks</span></span>

<span data-ttu-id="5d900-144">Все типы пулов являются допустимыми для всех ресурсов, включая буферы вершин, буферы индексов, текстуры и поверхности.</span><span class="sxs-lookup"><span data-stu-id="5d900-144">All pool types are valid with all resources including: vertex buffers, index buffers, textures, and surfaces.</span></span>

<span data-ttu-id="5d900-145">В следующих таблицах указываются ограничения для типов пула для целевых объектов рендеринга, наборов элементов глубины и динамических и mipmap использования.</span><span class="sxs-lookup"><span data-stu-id="5d900-145">The following tables indicate restrictions on pool types for render targets, depth stencils, and dynamic and mipmap usages.</span></span> <span data-ttu-id="5d900-146">Значение x означает совместимую комбинацию; отсутствие x означает несовместимость.</span><span class="sxs-lookup"><span data-stu-id="5d900-146">An x indicates a compatible combination; lack of an x indicates incompatibility.</span></span>



| <span data-ttu-id="5d900-147">пул</span><span class="sxs-lookup"><span data-stu-id="5d900-147">Pool</span></span>               | <span data-ttu-id="5d900-148">D3DUSAGE \_ рендертаржет</span><span class="sxs-lookup"><span data-stu-id="5d900-148">D3DUSAGE\_RENDERTARGET</span></span> | <span data-ttu-id="5d900-149">D3DUSAGE \_ депсстенЦил</span><span class="sxs-lookup"><span data-stu-id="5d900-149">D3DUSAGE\_DEPTHSTENCIL</span></span> |
|--------------------|------------------------|------------------------|
| <span data-ttu-id="5d900-150">D3DPOOL \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5d900-150">D3DPOOL\_DEFAULT</span></span>   | <span data-ttu-id="5d900-151">x</span><span class="sxs-lookup"><span data-stu-id="5d900-151">x</span></span>                      | <span data-ttu-id="5d900-152">x</span><span class="sxs-lookup"><span data-stu-id="5d900-152">x</span></span>                      |
| <span data-ttu-id="5d900-153">\_Управляемый D3DPOOL</span><span class="sxs-lookup"><span data-stu-id="5d900-153">D3DPOOL\_MANAGED</span></span>   |                        |                        |
| <span data-ttu-id="5d900-154">D3DPOOL \_</span><span class="sxs-lookup"><span data-stu-id="5d900-154">D3DPOOL\_SCRATCH</span></span>   |                        |                        |
| <span data-ttu-id="5d900-155">D3DPOOL \_ системмем</span><span class="sxs-lookup"><span data-stu-id="5d900-155">D3DPOOL\_SYSTEMMEM</span></span> |                        |                        |



 



| <span data-ttu-id="5d900-156">пул</span><span class="sxs-lookup"><span data-stu-id="5d900-156">Pool</span></span>               | <span data-ttu-id="5d900-157">D3DUSAGE \_ dynamic</span><span class="sxs-lookup"><span data-stu-id="5d900-157">D3DUSAGE\_DYNAMIC</span></span> | <span data-ttu-id="5d900-158">D3DUSAGE \_ аутоженмипмап</span><span class="sxs-lookup"><span data-stu-id="5d900-158">D3DUSAGE\_AUTOGENMIPMAP</span></span> |
|--------------------|-------------------|-------------------------|
| <span data-ttu-id="5d900-159">D3DPOOL \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5d900-159">D3DPOOL\_DEFAULT</span></span>   | <span data-ttu-id="5d900-160">x</span><span class="sxs-lookup"><span data-stu-id="5d900-160">x</span></span>                 | <span data-ttu-id="5d900-161">x</span><span class="sxs-lookup"><span data-stu-id="5d900-161">x</span></span>                       |
| <span data-ttu-id="5d900-162">\_Управляемый D3DPOOL</span><span class="sxs-lookup"><span data-stu-id="5d900-162">D3DPOOL\_MANAGED</span></span>   |                   | <span data-ttu-id="5d900-163">x</span><span class="sxs-lookup"><span data-stu-id="5d900-163">x</span></span>                       |
| <span data-ttu-id="5d900-164">D3DPOOL \_</span><span class="sxs-lookup"><span data-stu-id="5d900-164">D3DPOOL\_SCRATCH</span></span>   |                   |                         |
| <span data-ttu-id="5d900-165">D3DPOOL \_ системмем</span><span class="sxs-lookup"><span data-stu-id="5d900-165">D3DPOOL\_SYSTEMMEM</span></span> | <span data-ttu-id="5d900-166">x</span><span class="sxs-lookup"><span data-stu-id="5d900-166">x</span></span>                 |                         |



 

<span data-ttu-id="5d900-167">Дополнительные сведения о типах использования см. в разделе [**D3DUSAGE**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="5d900-167">For more information about usage types, see [**D3DUSAGE**](d3dusage.md).</span></span>

<span data-ttu-id="5d900-168">Пулы нельзя смешивать для различных объектов, содержащихся в одном ресурсе (MIP уровни в mipmap), и при выборе пула его нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="5d900-168">Pools cannot be mixed for different objects contained within one resource (mip levels in a mipmap) and, when a pool is chosen, it cannot be changed.</span></span>

<span data-ttu-id="5d900-169">Приложения должны использовать D3DPOOL \_ , управляемые для большинства статических ресурсов, так как это позволяет приложению работать с потерянными устройствами.</span><span class="sxs-lookup"><span data-stu-id="5d900-169">Applications should use D3DPOOL\_MANAGED for most static resources because this saves the application from having to deal with lost devices.</span></span> <span data-ttu-id="5d900-170">(Управляемые ресурсы восстанавливаются средой выполнения.) Это особенно полезно для систем с архитектурой унифицированной памяти.</span><span class="sxs-lookup"><span data-stu-id="5d900-170">(Managed resources are restored by the runtime.) This is especially beneficial for unified memory architecture (UMA) systems.</span></span> <span data-ttu-id="5d900-171">Другие динамические ресурсы не являются хорошим соответствием для \_ управляемого D3DPOOL.</span><span class="sxs-lookup"><span data-stu-id="5d900-171">Other dynamic resources are not a good match for D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="5d900-172">На самом деле буферы индексов и буферы вершин нельзя создавать с помощью D3DPOOL \_ , управляемых вместе с D3DUSAGE \_ dynamic.</span><span class="sxs-lookup"><span data-stu-id="5d900-172">In fact, index buffers and vertex buffers cannot be created using D3DPOOL\_MANAGED together with D3DUSAGE\_DYNAMIC.</span></span>

<span data-ttu-id="5d900-173">Для динамических текстур иногда желательно использовать пару видеопамяти и текстур системной памяти, выделить видеопамять с помощью D3DPOOL \_ по умолчанию и системной памяти с помощью D3DPOOL \_ системмем.</span><span class="sxs-lookup"><span data-stu-id="5d900-173">For dynamic textures, it is sometimes desirable to use a pair of video memory and system memory textures, allocating the video memory using D3DPOOL\_DEFAULT and the system memory using D3DPOOL\_SYSTEMMEM.</span></span> <span data-ttu-id="5d900-174">Можно блокировать и изменять биты текстуры системной памяти с помощью метода блокировки.</span><span class="sxs-lookup"><span data-stu-id="5d900-174">You can lock and modify the bits of the system memory texture using a locking method.</span></span> <span data-ttu-id="5d900-175">Затем можно обновить текстуру видеопамяти с помощью [**IDirect3DDevice9:: упдатетекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span><span class="sxs-lookup"><span data-stu-id="5d900-175">Then you can update the video memory texture using [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d900-176">Требования</span><span class="sxs-lookup"><span data-stu-id="5d900-176">Requirements</span></span>



| <span data-ttu-id="5d900-177">Требование</span><span class="sxs-lookup"><span data-stu-id="5d900-177">Requirement</span></span> | <span data-ttu-id="5d900-178">Значение</span><span class="sxs-lookup"><span data-stu-id="5d900-178">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d900-179">Header</span><span class="sxs-lookup"><span data-stu-id="5d900-179">Header</span></span><br/> | <dl> <span data-ttu-id="5d900-180"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d900-180"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d900-181">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d900-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d900-182">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="5d900-182">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="5d900-183">**D3DUSAGE**</span><span class="sxs-lookup"><span data-stu-id="5d900-183">**D3DUSAGE**</span></span>](d3dusage.md)
</dt> <dt>

[<span data-ttu-id="5d900-184">**IDirect3DDevice9:: Креатекубетекстуре**</span><span class="sxs-lookup"><span data-stu-id="5d900-184">**IDirect3DDevice9::CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
</dt> <dt>

[<span data-ttu-id="5d900-185">**IDirect3DDevice9:: Креатеиндексбуффер**</span><span class="sxs-lookup"><span data-stu-id="5d900-185">**IDirect3DDevice9::CreateIndexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
</dt> <dt>

[<span data-ttu-id="5d900-186">**IDirect3DDevice9:: Креатетекстуре**</span><span class="sxs-lookup"><span data-stu-id="5d900-186">**IDirect3DDevice9::CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
</dt> <dt>

[<span data-ttu-id="5d900-187">**IDirect3DDevice9:: Креатеволуметекстуре**</span><span class="sxs-lookup"><span data-stu-id="5d900-187">**IDirect3DDevice9::CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
</dt> <dt>

[<span data-ttu-id="5d900-188">**IDirect3DDevice9:: Креатевертексбуффер**</span><span class="sxs-lookup"><span data-stu-id="5d900-188">**IDirect3DDevice9::CreateVertexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
</dt> <dt>

[<span data-ttu-id="5d900-189">**D3DINDEXBUFFER \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="5d900-189">**D3DINDEXBUFFER\_DESC**</span></span>](d3dindexbuffer-desc.md)
</dt> <dt>

[<span data-ttu-id="5d900-190">**D3DSURFACE \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="5d900-190">**D3DSURFACE\_DESC**</span></span>](d3dsurface-desc.md)
</dt> <dt>

[<span data-ttu-id="5d900-191">**D3DVERTEXBUFFER \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="5d900-191">**D3DVERTEXBUFFER\_DESC**</span></span>](d3dvertexbuffer-desc.md)
</dt> <dt>

[<span data-ttu-id="5d900-192">**D3DVOLUME \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="5d900-192">**D3DVOLUME\_DESC**</span></span>](d3dvolume-desc.md)
</dt> </dl>

 

 
