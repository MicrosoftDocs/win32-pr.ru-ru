---
description: Описывает буфер индексов.
ms.assetid: 5d45213e-b3c0-4eb7-a4f9-8d8730eb3899
title: Структура D3DINDEXBUFFER_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DINDEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0a0bf63e732541f9394231cd82c23ff71a584b1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000392"
---
# <a name="d3dindexbuffer_desc-structure"></a><span data-ttu-id="bab28-103">\_Структура D3DINDEXBUFFER DESC</span><span class="sxs-lookup"><span data-stu-id="bab28-103">D3DINDEXBUFFER\_DESC structure</span></span>

<span data-ttu-id="bab28-104">Описывает буфер индексов.</span><span class="sxs-lookup"><span data-stu-id="bab28-104">Describes an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab28-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bab28-105">Syntax</span></span>


```C++
typedef struct D3DINDEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
} D3DINDEXBUFFER_DESC, *LPD3DINDEXBUFFER_DESC;
```



## <a name="members"></a><span data-ttu-id="bab28-106">Члены</span><span class="sxs-lookup"><span data-stu-id="bab28-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bab28-107">**Формат**</span><span class="sxs-lookup"><span data-stu-id="bab28-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="bab28-108">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="bab28-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bab28-109">Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий формат поверхности данных буфера индекса.</span><span class="sxs-lookup"><span data-stu-id="bab28-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the index buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="bab28-110">**Тип**</span><span class="sxs-lookup"><span data-stu-id="bab28-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="bab28-111">Тип: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="bab28-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bab28-112">Член перечисляемого типа [**D3DRESOURCETYPE**](./d3dresourcetype.md) , определяющий этот ресурс в качестве буфера индекса.</span><span class="sxs-lookup"><span data-stu-id="bab28-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as an index buffer.</span></span>

</dd> <dt>

<span data-ttu-id="bab28-113">**Использование**</span><span class="sxs-lookup"><span data-stu-id="bab28-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="bab28-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bab28-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bab28-115">Сочетание одного или нескольких из следующих флагов с указанием использования для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="bab28-115">Combination of one or more of the following flags, specifying the usage for this resource.</span></span>



| <span data-ttu-id="bab28-116">Значение</span><span class="sxs-lookup"><span data-stu-id="bab28-116">Value</span></span>                                                                                                                                                                                                   | <span data-ttu-id="bab28-117">Значение</span><span class="sxs-lookup"><span data-stu-id="bab28-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DUSAGE_DONOTCLIP"></span><span id="d3dusage_donotclip"></span><dl> <span data-ttu-id="bab28-118"><dt>**D3DUSAGE \_ донотклип**</dt></span><span class="sxs-lookup"><span data-stu-id="bab28-118"><dt>**D3DUSAGE\_DONOTCLIP**</dt></span></span> </dl>                            | <span data-ttu-id="bab28-119">Задайте значение, чтобы указать, что содержимое буфера индекса никогда не потребует обрезки.</span><span class="sxs-lookup"><span data-stu-id="bab28-119">Set to indicate that the index buffer content will never require clipping.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_DYNAMIC"></span><span id="d3dusage_dynamic"></span><dl> <span data-ttu-id="bab28-120"><dt>**D3DUSAGE \_ dynamic**</dt></span><span class="sxs-lookup"><span data-stu-id="bab28-120"><dt>**D3DUSAGE\_DYNAMIC**</dt></span></span> </dl>                                  | <span data-ttu-id="bab28-121">Задайте значение, указывающее, что буферу индекса требуется динамическое использование памяти.</span><span class="sxs-lookup"><span data-stu-id="bab28-121">Set to indicate that the index buffer requires dynamic memory use.</span></span> <span data-ttu-id="bab28-122">Это полезно для драйверов, поскольку позволяет им определять место размещения буфера.</span><span class="sxs-lookup"><span data-stu-id="bab28-122">This is useful for drivers because it enables them to decide where to place the buffer.</span></span> <span data-ttu-id="bab28-123">Как правило, буферы статических индексов помещаются в видеопамять, а динамические буферы индексов помещаются в память AGP.</span><span class="sxs-lookup"><span data-stu-id="bab28-123">In general, static index buffers are placed in video memory and dynamic index buffers are placed in AGP memory.</span></span> <span data-ttu-id="bab28-124">Обратите внимание, что не существует отдельного статического использования. Если не указать D3DUSAGE \_ dynamic, буфер индекса становится статическим.</span><span class="sxs-lookup"><span data-stu-id="bab28-124">Note that there is no separate static usage; if you do not specify D3DUSAGE\_DYNAMIC the index buffer is made static.</span></span> <span data-ttu-id="bab28-125">D3DUSAGE \_ dynamic строго применяется с помощью \_ флагов блокировки D3DLOCK Discard и D3DLOCK \_ нуверврите.</span><span class="sxs-lookup"><span data-stu-id="bab28-125">D3DUSAGE\_DYNAMIC is strictly enforced through the D3DLOCK\_DISCARD and D3DLOCK\_NOOVERWRITE locking flags.</span></span> <span data-ttu-id="bab28-126">В результате D3DLOCK \_ Discard и D3DLOCK \_ нуверврите допустимы только для буферов индексов, созданных с помощью D3DUSAGE \_ dynamic; они не являются допустимыми флагами в статических буферах вершин.</span><span class="sxs-lookup"><span data-stu-id="bab28-126">As a result, D3DLOCK\_DISCARD and D3DLOCK\_NOOVERWRITE are only valid on index buffers created with D3DUSAGE\_DYNAMIC; they are not valid flags on static vertex buffers.</span></span><br/> <span data-ttu-id="bab28-127">Дополнительные сведения об использовании динамических буферов индексов см. [в разделе Использование динамических буферов вершин и индексов](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="bab28-127">For more information about using dynamic index buffers, see [Using Dynamic Vertex and Index Buffers](performance-optimizations.md).</span></span><br/> <span data-ttu-id="bab28-128">Обратите внимание, что D3DUSAGE \_ dynamic нельзя указывать в буферах управляемых индексов.</span><span class="sxs-lookup"><span data-stu-id="bab28-128">Note that D3DUSAGE\_DYNAMIC cannot be specified on managed index buffers.</span></span> <span data-ttu-id="bab28-129">Дополнительные сведения см. в разделе [Управление ресурсами (Direct3D 9)](managing-resources.md).</span><span class="sxs-lookup"><span data-stu-id="bab28-129">For more information, see [Managing Resources (Direct3D 9)](managing-resources.md).</span></span><br/> |
| <span id="D3DUSAGE_RTPATCHES"></span><span id="d3dusage_rtpatches"></span><dl> <span data-ttu-id="bab28-130"><dt>**D3DUSAGE \_ ртпатчес**</dt></span><span class="sxs-lookup"><span data-stu-id="bab28-130"><dt>**D3DUSAGE\_RTPATCHES**</dt></span></span> </dl>                            | <span data-ttu-id="bab28-131">Задает значение, указывающее, когда буфер индекса должен использоваться для рисования примитивов высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="bab28-131">Set to indicate when the index buffer is to be used for drawing high-order primitives.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DUSAGE_NPATCHES"></span><span id="d3dusage_npatches"></span><dl> <span data-ttu-id="bab28-132"><dt>**D3DUSAGE \_ нпатчес**</dt></span><span class="sxs-lookup"><span data-stu-id="bab28-132"><dt>**D3DUSAGE\_NPATCHES**</dt></span></span> </dl>                               | <span data-ttu-id="bab28-133">Задайте значение, указывающее, когда буфер индекса должен использоваться для рисования N исправлений.</span><span class="sxs-lookup"><span data-stu-id="bab28-133">Set to indicate when the index buffer is to be used for drawing N patches.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_POINTS"></span><span id="d3dusage_points"></span><dl> <span data-ttu-id="bab28-134"><dt>**\_Точки D3DUSAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="bab28-134"><dt>**D3DUSAGE\_POINTS**</dt></span></span> </dl>                                     | <span data-ttu-id="bab28-135">Задайте значение, указывающее, когда буфер индекса должен использоваться для объектов-спрайтов точек рисования или списков индексированных точек.</span><span class="sxs-lookup"><span data-stu-id="bab28-135">Set to indicate when the index buffer is to be used for drawing point sprites or indexed point lists.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="D3DUSAGE_SOFTWAREPROCESSING"></span><span id="d3dusage_softwareprocessing"></span><dl> <span data-ttu-id="bab28-136"><dt>**D3DUSAGE \_ софтварепроцессинг**</dt></span><span class="sxs-lookup"><span data-stu-id="bab28-136"><dt>**D3DUSAGE\_SOFTWAREPROCESSING**</dt></span></span> </dl> | <span data-ttu-id="bab28-137">Задает значение, указывающее, что буфер должен использоваться при обработке программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="bab28-137">Set to indicate that the buffer is to be used with software processing.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DUSAGE_WRITEONLY"></span><span id="d3dusage_writeonly"></span><dl> <span data-ttu-id="bab28-138"><dt>**D3DUSAGE \_ WRITEONLY**</dt></span><span class="sxs-lookup"><span data-stu-id="bab28-138"><dt>**D3DUSAGE\_WRITEONLY**</dt></span></span> </dl>                            | <span data-ttu-id="bab28-139">Информирует систему о том, что приложение записывает только в буфер индекса.</span><span class="sxs-lookup"><span data-stu-id="bab28-139">Informs the system that the application writes only to the index buffer.</span></span> <span data-ttu-id="bab28-140">Использование этого флага позволяет драйверу выбрать лучшее место в памяти для эффективных операций записи и подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="bab28-140">Using this flag enables the driver to choose the best memory location for efficient write operations and rendering.</span></span> <span data-ttu-id="bab28-141">Попытка чтения из буфера индекса, созданного с помощью этой возможности, может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="bab28-141">Attempts to read from an index buffer that is created with this capability can result in degraded performance.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="bab28-142">**Пул.**</span><span class="sxs-lookup"><span data-stu-id="bab28-142">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="bab28-143">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="bab28-143">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bab28-144">Член перечисляемого типа [**D3DPOOL**](./d3dpool.md) , указывающий класс памяти, выделенной для этого буфера индекса.</span><span class="sxs-lookup"><span data-stu-id="bab28-144">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this index buffer.</span></span>

</dd> <dt>

<span data-ttu-id="bab28-145">**Размер**</span><span class="sxs-lookup"><span data-stu-id="bab28-145">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="bab28-146">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bab28-146">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bab28-147">Размер буфера индекса в байтах.</span><span class="sxs-lookup"><span data-stu-id="bab28-147">Size of the index buffer, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bab28-148">Требования</span><span class="sxs-lookup"><span data-stu-id="bab28-148">Requirements</span></span>



| <span data-ttu-id="bab28-149">Требование</span><span class="sxs-lookup"><span data-stu-id="bab28-149">Requirement</span></span> | <span data-ttu-id="bab28-150">Значение</span><span class="sxs-lookup"><span data-stu-id="bab28-150">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bab28-151">Header</span><span class="sxs-lookup"><span data-stu-id="bab28-151">Header</span></span><br/> | <dl> <span data-ttu-id="bab28-152"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="bab28-152"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bab28-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bab28-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bab28-154">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="bab28-154">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="bab28-155">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="bab28-155">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc)
</dt> <dt>

[<span data-ttu-id="bab28-156">Буферы индексов (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bab28-156">Index Buffers (Direct3D 9)</span></span>](index-buffers.md)
</dt> </dl>

 

 
