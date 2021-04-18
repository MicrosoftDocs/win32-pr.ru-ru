---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT (D3dx12. h)
description: Шаблонная вспомогательная структура, используемая для инкапсуляции типа подобъекта и пар данных подобъектов в виде одного объекта, подходящего для описания потока.
ms.assetid: 4C59D483-6ED8-49BD-B91B-2A912AFE2409
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11353581dddc2bd0d438b955d1292b667fba39ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713982"
---
# <a name="cd3dx12_pipeline_state_stream_subobject-structure"></a><span data-ttu-id="a3a94-104">\_ \_ \_ \_ Структура подобъекта потока состояния конвейера CD3DX12</span><span class="sxs-lookup"><span data-stu-id="a3a94-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT structure</span></span>

<span data-ttu-id="a3a94-105">Шаблонная вспомогательная структура, используемая для инкапсуляции типа подобъекта и пар данных подобъектов в виде одного объекта, подходящего для описания потока.</span><span class="sxs-lookup"><span data-stu-id="a3a94-105">A templated helper structure used to encapsulate subobject type and subobject data pairs as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3a94-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3a94-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT {
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT;
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT operator=(InnerStructType const& i);
                                          operator InnerStructType() const;
};
```



## <a name="members"></a><span data-ttu-id="a3a94-107">Члены</span><span class="sxs-lookup"><span data-stu-id="a3a94-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a3a94-108">**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a3a94-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="a3a94-109">Создает новый, неинициализированный экземпляр \_ \_ \_ подобъекта потока состояния конвейера CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="a3a94-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT.</span></span>

</dd> <dt>

<span data-ttu-id="a3a94-110">**CD3DX12 \_ \_Подобъект \_ потока \_ состояния конвейера (** иннерструкттипе \* \* const &i) \* \*</span><span class="sxs-lookup"><span data-stu-id="a3a94-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT(** InnerStructType\*\* const &i)\*\*</span></span>
</dt> <dd>

<span data-ttu-id="a3a94-111">Создает \_ \_ \_ \_ экземпляр шаблона подобъекта потока состояния конвейера CD3DX12, инициализированный с типом подобъекта типа [**\_ \_ \_ подобъекта \_ состояния конвейера D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) и данными подобъекта, скопированными из *i*.</span><span class="sxs-lookup"><span data-stu-id="a3a94-111">Creates a new CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template instance, initialized with a subobject type of [**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) and subobject data copied from *i*.</span></span> <span data-ttu-id="a3a94-112">Типы подобъекта и тип данных подобъекта указаны как параметры шаблона, **Type** и **иннерструкттипе** соответственно.</span><span class="sxs-lookup"><span data-stu-id="a3a94-112">Both the subobject type and subobject data type are given as template parameters, **Type** and **InnerStructType**, respectively.</span></span> <span data-ttu-id="a3a94-113">Дополнительные сведения см. в разделе "Примечания" ниже.</span><span class="sxs-lookup"><span data-stu-id="a3a94-113">For more information, see Remarks below.</span></span>

</dd> <dt>

<span data-ttu-id="a3a94-114">**оператор = (** иннерструкттипе \* \* const& i) \* \*</span><span class="sxs-lookup"><span data-stu-id="a3a94-114">**operator=(** InnerStructType\*\* const& i)\*\*</span></span>
</dt> <dd>

<span data-ttu-id="a3a94-115">Оператор присваивания копирования.</span><span class="sxs-lookup"><span data-stu-id="a3a94-115">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="a3a94-116">**const оператора **иннерструкттипе**()**</span><span class="sxs-lookup"><span data-stu-id="a3a94-116">**operator **InnerStructType**() const**</span></span>
</dt> <dd>

<span data-ttu-id="a3a94-117">Неявное преобразование в тип данных подобъекта, заданный параметром шаблона **иннерструкттипе** .</span><span class="sxs-lookup"><span data-stu-id="a3a94-117">Implicit conversion to the subobject data type given by the **InnerStructType** template parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3a94-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3a94-118">Remarks</span></span>

<span data-ttu-id="a3a94-119">\_Подобъект \_ потока состояния конвейера CD3DX12 \_ \_ — это шаблон, определенный следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a3a94-119">CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT is a template defined as follows:</span></span>


```C++
template <typename InnerStructType, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE Type, typename DefaultArg = InnerStructType>
class alignas(void*) CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
{
private:
    D3D12_PIPELINE_STATE_SUBOBJECT_TYPE _Type;
    InnerStructType _Inner;
public:
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT() : _Type(Type), _Inner(DefaultArg()) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const& i) : _Type(Type), _Inner(i) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT& operator=(InnerStructType const& i) { _Inner = i; return *this; }
    operator InnerStructType() const { return _Inner; }
};  
          
```



<span data-ttu-id="a3a94-120">Параметр шаблона **иннерструкттипе** указывает тип данных подобъекта. то есть сведения о подобъекте, которые должны быть закодированы в поток.</span><span class="sxs-lookup"><span data-stu-id="a3a94-120">The template parameter **InnerStructType** specifies the subobject data type; that is, the subobject details to be encoded into a stream.</span></span> <span data-ttu-id="a3a94-121">**Тип** параметра шаблона задает тип подобъекта; то есть тип структуры, заданный параметром-шаблоном **иннерструкттипе**.</span><span class="sxs-lookup"><span data-stu-id="a3a94-121">The template parameter **Type** specifies the subobject type; that is, the type of the structure specified by the template parameter **InnerStructType**.</span></span> <span data-ttu-id="a3a94-122">Параметр шаблона **дефаултарг** указывает необязательное значение, в которое будут инициализироваться данные подобъекта, когда экземпляр соответствующего шаблона создается по умолчанию. Например, чтобы создать по умолчанию [**\_ \_ поток состояния конвейера \_ CD3DX12 \_ Blend \_**](cd3dx12-pipeline-state-stream-blend-desc.md) , инициализированный с общими режимами смешения по умолчанию с использованием [**CD3DX12 \_ по умолчанию**](cd3dx12-default.md).</span><span class="sxs-lookup"><span data-stu-id="a3a94-122">The template parameter **DefaultArg** specifies an optional value that the subobject data will be initialized to when an instance of the corresponding template instantiation is default-constructed; for example, to default-construct a [**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) initialized with common blend-state defaults using [**CD3DX12\_DEFAULT**](cd3dx12-default.md).</span></span>

<span data-ttu-id="a3a94-123">Ниже приведены определенные экземпляры шаблонов:</span><span class="sxs-lookup"><span data-stu-id="a3a94-123">Here are the template instantiations that are defined:</span></span>

-   [<span data-ttu-id="a3a94-124">**\_ \_ \_ Флаги потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="a3a94-124">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS**</span></span>](cd3dx12-pipeline-state-stream-flags.md)
-   [<span data-ttu-id="a3a94-125">**\_ \_ \_ \_ Маска узла потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="a3a94-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK**</span></span>](cd3dx12-pipeline-state-stream-node-mask.md)
-   [<span data-ttu-id="a3a94-126">**\_ \_ \_ \_ Корневая подпись потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="a3a94-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE**</span></span>](cd3dx12-pipeline-state-stream-root-signature.md)
-   [<span data-ttu-id="a3a94-127">**\_ \_ \_ \_ Схема ввода потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="a3a94-127">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT**</span></span>](cd3dx12-pipeline-state-stream-input-layout.md)
-   [<span data-ttu-id="a3a94-128">**\_Поток состояния конвейера CD3DX12. \_ \_ \_ \_ \_ вырезание значения чередования \_**</span><span class="sxs-lookup"><span data-stu-id="a3a94-128">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE**</span></span>](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)
-   [<span data-ttu-id="a3a94-129">**\_ \_ \_ \_ Топология примитива потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="a3a94-129">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY**</span></span>](cd3dx12-pipeline-state-stream-primitive-topology.md)
-   [<span data-ttu-id="a3a94-130">**\_Поток состояния конвейера CD3DX12 \_ \_ \_ и**</span><span class="sxs-lookup"><span data-stu-id="a3a94-130">**CD3DX12\_PIPELINE\_STATE\_STREAM\_VS**</span></span>](cd3dx12-pipeline-state-stream-vs.md)
-   [<span data-ttu-id="a3a94-131">**\_ \_ \_ GS потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="a3a94-131">**CD3DX12\_PIPELINE\_STATE\_STREAM\_GS**</span></span>](cd3dx12-pipeline-state-stream-gs.md)
-   [<span data-ttu-id="a3a94-132">**\_ \_ \_ \_ Выходные данные потока состояния конвейера \_ CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="a3a94-132">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT**</span></span>](cd3dx12-pipeline-state-stream-stream-output.md)
-   [<span data-ttu-id="a3a94-133">**\_Поток состояния конвейера CD3DX12 — \_ \_ \_ HS**</span><span class="sxs-lookup"><span data-stu-id="a3a94-133">**CD3DX12\_PIPELINE\_STATE\_STREAM\_HS**</span></span>](cd3dx12-pipeline-state-stream-hs.md)
-   [<span data-ttu-id="a3a94-134">**\_ \_ \_ DS потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="a3a94-134">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DS**</span></span>](cd3dx12-pipeline-state-stream-ds.md)
-   [<span data-ttu-id="a3a94-135">**\_Поток состояния конвейера CD3DX12 \_ \_ \_ PS**</span><span class="sxs-lookup"><span data-stu-id="a3a94-135">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PS**</span></span>](cd3dx12-pipeline-state-stream-ps.md)
-   [<span data-ttu-id="a3a94-136">**\_Поток состояния конвейера CD3DX12 \_ \_ \_ CS**</span><span class="sxs-lookup"><span data-stu-id="a3a94-136">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CS**</span></span>](cd3dx12-pipeline-state-stream-cs.md)
-   [<span data-ttu-id="a3a94-137">**CD3DX12 \_ конвейера \_ состояния \_ потока \_ Blend \_**</span><span class="sxs-lookup"><span data-stu-id="a3a94-137">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**</span></span>](cd3dx12-pipeline-state-stream-blend-desc.md)
-   [<span data-ttu-id="a3a94-138">**\_ \_ \_ \_ Трафарет глубины потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="a3a94-138">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil.md)
-   [<span data-ttu-id="a3a94-139">**\_ \_ Глубина потока состояния конвейера CD3DX12 \_ \_ \_ STENCIL1**</span><span class="sxs-lookup"><span data-stu-id="a3a94-139">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil1.md)
-   [<span data-ttu-id="a3a94-140">**\_ \_ \_ \_ \_ Формат трафарета глубины потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="a3a94-140">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil-format.md)
-   [<span data-ttu-id="a3a94-141">**Средство программной \_ \_ \_ прорисовки потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="a3a94-141">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER**</span></span>](cd3dx12-pipeline-state-stream-rasterizer.md)
-   [<span data-ttu-id="a3a94-142">**\_ \_ \_ \_ \_ Форматы целевого объекта подготовки потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="a3a94-142">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS**</span></span>](cd3dx12-pipeline-state-stream-render-target-formats.md)
-   [<span data-ttu-id="a3a94-143">**\_ \_ \_ \_ Пример DESC потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="a3a94-143">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC**</span></span>](cd3dx12-pipeline-state-stream-sample-desc.md)
-   [<span data-ttu-id="a3a94-144">**\_ \_ \_ \_ Образец маски потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="a3a94-144">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK**</span></span>](cd3dx12-pipeline-state-stream-sample-mask.md)
-   [<span data-ttu-id="a3a94-145">**\_Поток состояния конвейера CD3DX12, \_ \_ \_ кэшированный \_ PSO**</span><span class="sxs-lookup"><span data-stu-id="a3a94-145">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO**</span></span>](cd3dx12-pipeline-state-stream-cached-pso.md)

<span data-ttu-id="a3a94-146">Структура потока состояния конвейера [**CD3DX12 \_ \_ \_ \_ Blend \_**](cd3dx12-pipeline-state-stream-blend-desc.md), [**\_ \_ \_ \_ \_ набор элементов глубины потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-depth-stencil.md), [**\_ \_ глубина потока состояния конвейера CD3DX12 STENCIL1 \_ \_ \_**](cd3dx12-pipeline-state-stream-depth-stencil1.md)и [**CD3DX12 \_ \_ поток состояния конвейера \_ потока \_**](cd3dx12-pipeline-state-stream-rasterizer.md) состояний позволяют инициализировать данные вложенных объектов с общими значениями по умолчанию, используя [**CD3DX12 \_ по умолчанию**](cd3dx12-default.md).</span><span class="sxs-lookup"><span data-stu-id="a3a94-146">The [**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md), [**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**](cd3dx12-pipeline-state-stream-depth-stencil.md), [**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md), and [**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md) structures are defined to initialize their subobject data with common defaults using [**CD3DX12\_DEFAULT**](cd3dx12-default.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3a94-147">Требования</span><span class="sxs-lookup"><span data-stu-id="a3a94-147">Requirements</span></span>



| <span data-ttu-id="a3a94-148">Требование</span><span class="sxs-lookup"><span data-stu-id="a3a94-148">Requirement</span></span> | <span data-ttu-id="a3a94-149">Значение</span><span class="sxs-lookup"><span data-stu-id="a3a94-149">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a3a94-150">Header</span><span class="sxs-lookup"><span data-stu-id="a3a94-150">Header</span></span><br/> | <dl> <span data-ttu-id="a3a94-151"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3a94-151"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3a94-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3a94-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3a94-153">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="a3a94-153">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="a3a94-154">**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="a3a94-154">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

