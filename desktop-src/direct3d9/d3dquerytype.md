---
description: Определяет тип запроса.
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: Перечисление D3DQUERYTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DQUERYTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 21cb3e2f2254d54caacd4217d3e0023446a0c6f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703834"
---
# <a name="d3dquerytype-enumeration"></a><span data-ttu-id="c943b-103">Перечисление D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="c943b-103">D3DQUERYTYPE enumeration</span></span>

<span data-ttu-id="c943b-104">Определяет тип запроса.</span><span class="sxs-lookup"><span data-stu-id="c943b-104">Identifies the query type.</span></span> <span data-ttu-id="c943b-105">Дополнительные сведения о запросах см. в разделе [запросы (Direct3D 9)](queries.md) .</span><span class="sxs-lookup"><span data-stu-id="c943b-105">For information about queries, see [Queries (Direct3D 9)](queries.md)</span></span>

## <a name="syntax"></a><span data-ttu-id="c943b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c943b-106">Syntax</span></span>


```C++
typedef enum D3DQUERYTYPE { 
  D3DQUERYTYPE_VCACHE             = 4,
  D3DQUERYTYPE_ResourceManager    = 5,
  D3DQUERYTYPE_VERTEXSTATS        = 6,
  D3DQUERYTYPE_EVENT              = 8,
  D3DQUERYTYPE_OCCLUSION          = 9,
  D3DQUERYTYPE_TIMESTAMP          = 10,
  D3DQUERYTYPE_TIMESTAMPDISJOINT  = 11,
  D3DQUERYTYPE_TIMESTAMPFREQ      = 12,
  D3DQUERYTYPE_PIPELINETIMINGS    = 13,
  D3DQUERYTYPE_INTERFACETIMINGS   = 14,
  D3DQUERYTYPE_VERTEXTIMINGS      = 15,
  D3DQUERYTYPE_PIXELTIMINGS       = 16,
  D3DQUERYTYPE_BANDWIDTHTIMINGS   = 17,
  D3DQUERYTYPE_CACHEUTILIZATION   = 18,
  D3DQUERYTYPE_MEMORYPRESSURE     = 19
} D3DQUERYTYPE, *LPD3DQUERYTYPE;
```



## <a name="constants"></a><span data-ttu-id="c943b-107">Константы</span><span class="sxs-lookup"><span data-stu-id="c943b-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c943b-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE \_ вкаче**</span><span class="sxs-lookup"><span data-stu-id="c943b-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE\_VCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="c943b-109">Запрос подсказок к драйверу о структуре данных для кэширования вершин.</span><span class="sxs-lookup"><span data-stu-id="c943b-109">Query for driver hints about data layout for vertex caching.</span></span>

</dd> <dt>

<span data-ttu-id="c943b-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE \_ ResourceManager**</span><span class="sxs-lookup"><span data-stu-id="c943b-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE\_ResourceManager**</span></span>
</dt> <dd>

<span data-ttu-id="c943b-111">Запросите диспетчер ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c943b-111">Query the resource manager.</span></span> <span data-ttu-id="c943b-112">Для этого запроса флаги поведения устройства должны включать [D3DCREATE \_ Отключить \_ \_ Управление драйверами](d3dcreate.md).</span><span class="sxs-lookup"><span data-stu-id="c943b-112">For this query, the device behavior flags must include [D3DCREATE\_DISABLE\_DRIVER\_MANAGEMENT](d3dcreate.md).</span></span>

</dd> <dt>

<span data-ttu-id="c943b-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE \_ вертексстатс**</span><span class="sxs-lookup"><span data-stu-id="c943b-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE\_VERTEXSTATS**</span></span>
</dt> <dd>

<span data-ttu-id="c943b-114">Запрос статистики вершин.</span><span class="sxs-lookup"><span data-stu-id="c943b-114">Query vertex statistics.</span></span>

</dd> <dt>

<span data-ttu-id="c943b-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**\_Событие D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="c943b-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**D3DQUERYTYPE\_EVENT**</span></span>
</dt> <dd>

<span data-ttu-id="c943b-116">Запрос всех и всех асинхронных событий, выданных из вызовов API.</span><span class="sxs-lookup"><span data-stu-id="c943b-116">Query for any and all asynchronous events that have been issued from API calls.</span></span>

</dd> <dt>

<span data-ttu-id="c943b-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE \_ перекрытия**</span><span class="sxs-lookup"><span data-stu-id="c943b-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="c943b-118">Запрос перекрытия возвращает число пикселей, пройденных в z-тестировании.</span><span class="sxs-lookup"><span data-stu-id="c943b-118">An occlusion query returns the number of pixels that pass z-testing.</span></span> <span data-ttu-id="c943b-119">Эти Пиксели используются для примитивов, выводимых между выпуском [**D3DISSUE \_ Begin**](d3dissue-begin.md) и [**D3DISSUE \_ End**](d3dissue-end.md).</span><span class="sxs-lookup"><span data-stu-id="c943b-119">These pixels are for primitives drawn between the issue of [**D3DISSUE\_BEGIN**](d3dissue-begin.md) and [**D3DISSUE\_END**](d3dissue-end.md).</span></span> <span data-ttu-id="c943b-120">Это позволяет приложению проверить результат перекрытия на 0.</span><span class="sxs-lookup"><span data-stu-id="c943b-120">This enables an application to check the occlusion result against 0.</span></span> <span data-ttu-id="c943b-121">Ноль полностью перекрыто, что означает, что Пиксели не видны в текущей положении камеры.</span><span class="sxs-lookup"><span data-stu-id="c943b-121">Zero is fully occluded, which means the pixels are not visible from the current camera position.</span></span>

</dd> <dt>

<span data-ttu-id="c943b-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**\_Отметка времени D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="c943b-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE\_TIMESTAMP**</span></span>
</dt> <dd>

<span data-ttu-id="c943b-123">Возвращает 64-разрядную отметку времени.</span><span class="sxs-lookup"><span data-stu-id="c943b-123">Returns a 64-bit timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="c943b-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE \_ тиместампдисжоинт**</span><span class="sxs-lookup"><span data-stu-id="c943b-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE\_TIMESTAMPDISJOINT**</span></span>
</dt> <dd>

<span data-ttu-id="c943b-125">Используйте этот запрос для уведомления приложения, если частота счетчика изменилась с \_ метки времени D3DQUERYTYPE.</span><span class="sxs-lookup"><span data-stu-id="c943b-125">Use this query to notify an application if the counter frequency has changed from the D3DQUERYTYPE\_TIMESTAMP.</span></span>

</dd> <dt>

<span data-ttu-id="c943b-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE \_ тиместампфрек**</span><span class="sxs-lookup"><span data-stu-id="c943b-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE\_TIMESTAMPFREQ**</span></span>
</dt> <dd>

<span data-ttu-id="c943b-127">Этот результат запроса имеет **значение true** , если значения из \_ запросов отметок времени D3DQUERYTYPE не могут быть непрерывными в течение всего времени \_ запроса D3DQUERYTYPE тиместампдисжоинт.</span><span class="sxs-lookup"><span data-stu-id="c943b-127">This query result is **TRUE** if the values from D3DQUERYTYPE\_TIMESTAMP queries cannot be guaranteed to be continuous throughout the duration of the D3DQUERYTYPE\_TIMESTAMPDISJOINT query.</span></span> <span data-ttu-id="c943b-128">В противном случае результат запроса будет иметь **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c943b-128">Otherwise, the query result is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="c943b-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE \_ пипелинетимингс**</span><span class="sxs-lookup"><span data-stu-id="c943b-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE\_PIPELINETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="c943b-130">Процент времени обработки данных конвейера.</span><span class="sxs-lookup"><span data-stu-id="c943b-130">Percent of time processing pipeline data.</span></span>

</dd> <dt>

<span data-ttu-id="c943b-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE \_ интерфацетимингс**</span><span class="sxs-lookup"><span data-stu-id="c943b-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE\_INTERFACETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="c943b-132">Процент времени обработки данных в драйвере.</span><span class="sxs-lookup"><span data-stu-id="c943b-132">Percent of time processing data in the driver.</span></span>

</dd> <dt>

<span data-ttu-id="c943b-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE \_ вертекстимингс**</span><span class="sxs-lookup"><span data-stu-id="c943b-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE\_VERTEXTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="c943b-134">Процент времени обработки данных шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="c943b-134">Percent of time processing vertex shader data.</span></span>

</dd> <dt>

<span data-ttu-id="c943b-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE \_ пикселтимингс**</span><span class="sxs-lookup"><span data-stu-id="c943b-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE\_PIXELTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="c943b-136">Процент времени обработки данных шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="c943b-136">Percent of time processing pixel shader data.</span></span>

</dd> <dt>

<span data-ttu-id="c943b-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE \_ бандвидстимингс**</span><span class="sxs-lookup"><span data-stu-id="c943b-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE\_BANDWIDTHTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="c943b-138">Сравнения измерений пропускной способности помогают понять производительность приложения.</span><span class="sxs-lookup"><span data-stu-id="c943b-138">Throughput measurement comparisons for help in understanding the performance of an application.</span></span>

</dd> <dt>

<span data-ttu-id="c943b-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE \_ качеутилизатион**</span><span class="sxs-lookup"><span data-stu-id="c943b-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE\_CACHEUTILIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="c943b-140">Измеряет производительность скорости попадания в кэш для текстур и индексированных вершин.</span><span class="sxs-lookup"><span data-stu-id="c943b-140">Measure the cache hit-rate performance for textures and indexed vertices.</span></span>

</dd> <dt>

<span data-ttu-id="c943b-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE \_ меморипрессуре**</span><span class="sxs-lookup"><span data-stu-id="c943b-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE\_MEMORYPRESSURE**</span></span>
</dt> <dd>

<span data-ttu-id="c943b-142">Эффективность выделения памяти, содержащейся в структуре [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .</span><span class="sxs-lookup"><span data-stu-id="c943b-142">Efficiency of memory allocation contained in a [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) structure.</span></span>



|                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c943b-143">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="c943b-143">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c943b-144">D3DQUERYTYPE \_ меморипрессуре доступен только в Direct3D9Ex, работающем в Windows 7 (или более текущей операционной системе).</span><span class="sxs-lookup"><span data-stu-id="c943b-144">D3DQUERYTYPE\_MEMORYPRESSURE is only available in Direct3D9Ex running on Windows 7 (or more current operating system).</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c943b-145">Требования</span><span class="sxs-lookup"><span data-stu-id="c943b-145">Requirements</span></span>



| <span data-ttu-id="c943b-146">Требование</span><span class="sxs-lookup"><span data-stu-id="c943b-146">Requirement</span></span> | <span data-ttu-id="c943b-147">Значение</span><span class="sxs-lookup"><span data-stu-id="c943b-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c943b-148">Header</span><span class="sxs-lookup"><span data-stu-id="c943b-148">Header</span></span><br/> | <dl> <span data-ttu-id="c943b-149"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c943b-149"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c943b-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c943b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c943b-151">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="c943b-151">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="c943b-152">**IDirect3DDevice9:: CreateQuery**</span><span class="sxs-lookup"><span data-stu-id="c943b-152">**IDirect3DDevice9::CreateQuery**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
