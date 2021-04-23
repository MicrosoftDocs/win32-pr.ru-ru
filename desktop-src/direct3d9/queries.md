---
description: Существует несколько типов запросов, которые предназначены для запроса состояния ресурсов.
ms.assetid: 2c65d199-141d-43a7-b513-4cb4459d7c27
title: Запросы (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f450aa7015d4b66ad28b6c4d0632b2995bedd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894085"
---
# <a name="queries-direct3d-9"></a><span data-ttu-id="2eddd-103">Запросы (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2eddd-103">Queries (Direct3D 9)</span></span>

<span data-ttu-id="2eddd-104">Существует несколько типов запросов, которые предназначены для запроса состояния ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2eddd-104">There are several types of queries which are designed to query the status of resources.</span></span> <span data-ttu-id="2eddd-105">Состояние данного ресурса включает состояние графического процессора (GPU), состояние драйвера или состояние среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="2eddd-105">The status of a given resource includes graphics processing unit (GPU) status, driver status, or runtime status.</span></span> <span data-ttu-id="2eddd-106">Чтобы понять разницу между различными типами запросов, необходимо понимать состояния запросов.</span><span class="sxs-lookup"><span data-stu-id="2eddd-106">To understand the difference between the different query types, you need to understand the query states.</span></span> <span data-ttu-id="2eddd-107">На следующей схеме перехода состояния объясняются все состояния запросов.</span><span class="sxs-lookup"><span data-stu-id="2eddd-107">The following state transition diagram explains each of the query states.</span></span>

![Диаграмма, показывающая переходы между состояниями запросов](images/queries.png)

<span data-ttu-id="2eddd-109">На схеме показаны три состояния, каждое из которых определяется круговыми кругами.</span><span class="sxs-lookup"><span data-stu-id="2eddd-109">The diagram shows three states, each defined by circles.</span></span> <span data-ttu-id="2eddd-110">Каждая из сплошных линий — это события, управляемые приложениями, которые вызывают переход между состояниями.</span><span class="sxs-lookup"><span data-stu-id="2eddd-110">Each of the solid lines are application-driven events that cause a state transition.</span></span> <span data-ttu-id="2eddd-111">Пунктирная линия является событием, управляемым на основе ресурсов, которое переключает запрос из выданного состояния в сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="2eddd-111">The dashed line is a resource-driven event that switches a query from the issued state to the signaled state.</span></span> <span data-ttu-id="2eddd-112">Каждое из этих состояний имеет другую цель:</span><span class="sxs-lookup"><span data-stu-id="2eddd-112">Each of these states has a different purpose:</span></span>

-   <span data-ttu-id="2eddd-113">Сигнальное состояние похоже на состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="2eddd-113">The signaled state is like an idle state.</span></span> <span data-ttu-id="2eddd-114">Объект запроса создан и ожидает, пока приложение выдаст запрос.</span><span class="sxs-lookup"><span data-stu-id="2eddd-114">The query object has been generated and is waiting for the application to issue the query.</span></span> <span data-ttu-id="2eddd-115">После завершения запроса и передачи обратно в сигнальное состояние можно получить ответ на запрос.</span><span class="sxs-lookup"><span data-stu-id="2eddd-115">Once a query has completed and transitioned back to the signaled state, the answer to the query can be retrieved.</span></span>
-   <span data-ttu-id="2eddd-116">Состояние здания похоже на промежуточную область для запроса.</span><span class="sxs-lookup"><span data-stu-id="2eddd-116">The building state is like a staging area for a query.</span></span> <span data-ttu-id="2eddd-117">Из состояния здания был выдан запрос (с помощью вызова [**D3DISSUE \_ Begin**](d3dissue-begin.md)), но еще не перешел в состояние выданного.</span><span class="sxs-lookup"><span data-stu-id="2eddd-117">From the building state, a query has been issued (by calling [**D3DISSUE\_BEGIN**](d3dissue-begin.md)) but has not yet transitioned to the issued state.</span></span> <span data-ttu-id="2eddd-118">Когда приложение выдает окончание запроса (путем вызова [**D3DISSUE \_ End**](d3dissue-end.md)), запрос переходит в состояние «выдано».</span><span class="sxs-lookup"><span data-stu-id="2eddd-118">When an application issues a query end (by calling [**D3DISSUE\_END**](d3dissue-end.md)), the query transitions to the issued state.</span></span>
-   <span data-ttu-id="2eddd-119">Выданное состояние означает, что запрашиваемый ресурс имеет контроль над запросом.</span><span class="sxs-lookup"><span data-stu-id="2eddd-119">The issued state means that the resource being queried has control of the query.</span></span> <span data-ttu-id="2eddd-120">Когда ресурс завершит свою работу, ресурс переводит конечный автомат в сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="2eddd-120">Once the resource finishes its work, the resource transitions the state machine to the signaled state.</span></span> <span data-ttu-id="2eddd-121">Во время выданного состояния приложение должно выполнить опрос, чтобы обнаружить переход в сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="2eddd-121">During the issued state, the application must poll to detect the transition to the signaled state.</span></span> <span data-ttu-id="2eddd-122">После перехода в сигнальное состояние метод [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) возвращает приложению результат запроса (через аргумент).</span><span class="sxs-lookup"><span data-stu-id="2eddd-122">Once the transition to the signaled state occurs, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) returns the query result (through an argument) to the application.</span></span>

<span data-ttu-id="2eddd-123">В следующей таблице перечислены доступные типы запросов.</span><span class="sxs-lookup"><span data-stu-id="2eddd-123">The following table lists the available query types.</span></span>



| <span data-ttu-id="2eddd-124">Тип запроса</span><span class="sxs-lookup"><span data-stu-id="2eddd-124">Query Type</span></span>        | <span data-ttu-id="2eddd-125">Событие проблемы</span><span class="sxs-lookup"><span data-stu-id="2eddd-125">Issue Event</span></span>                                                                      | <span data-ttu-id="2eddd-126">Буфер GetData</span><span class="sxs-lookup"><span data-stu-id="2eddd-126">GetData buffer</span></span>                                                              | <span data-ttu-id="2eddd-127">Параметры выполнения</span><span class="sxs-lookup"><span data-stu-id="2eddd-127">Runtime</span></span>      | <span data-ttu-id="2eddd-128">Неявное начало запроса</span><span class="sxs-lookup"><span data-stu-id="2eddd-128">Implicit beginning of query</span></span>                      |
|-------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------|--------------------------------------------------|
| <span data-ttu-id="2eddd-129">бандвидстимингс</span><span class="sxs-lookup"><span data-stu-id="2eddd-129">BANDWIDTHTIMINGS</span></span>  | <span data-ttu-id="2eddd-130">[**D3DISSUE \_ Начало**](d3dissue-begin.md), [ **D3DISSUE \_**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="2eddd-130">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="2eddd-131">**D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="2eddd-131">**D3DDEVINFO\_D3D9BANDWIDTHTIMINGS**</span></span>](d3ddevinfo-d3d9bandwidthtimings.md) | <span data-ttu-id="2eddd-132">Розничная или отладочная</span><span class="sxs-lookup"><span data-stu-id="2eddd-132">Retail/Debug</span></span> | <span data-ttu-id="2eddd-133">Н/Д</span><span class="sxs-lookup"><span data-stu-id="2eddd-133">N/A</span></span>                                              |
| <span data-ttu-id="2eddd-134">качеутилизатион</span><span class="sxs-lookup"><span data-stu-id="2eddd-134">CACHEUTILIZATION</span></span>  | <span data-ttu-id="2eddd-135">[**D3DISSUE \_ Начало**](d3dissue-begin.md), [ **D3DISSUE \_**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="2eddd-135">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="2eddd-136">**D3DDEVINFO \_ D3D9CACHEUTILIZATION**</span><span class="sxs-lookup"><span data-stu-id="2eddd-136">**D3DDEVINFO\_D3D9CACHEUTILIZATION**</span></span>](d3ddevinfo-d3d9cacheutilization.md) | <span data-ttu-id="2eddd-137">Розничная или отладочная</span><span class="sxs-lookup"><span data-stu-id="2eddd-137">Retail/Debug</span></span> | <span data-ttu-id="2eddd-138">Н/Д</span><span class="sxs-lookup"><span data-stu-id="2eddd-138">N/A</span></span>                                              |
| <span data-ttu-id="2eddd-139">ЖУРНАЛЕ</span><span class="sxs-lookup"><span data-stu-id="2eddd-139">EVENT</span></span>             | [<span data-ttu-id="2eddd-140">**D3DISSUE \_ конец**</span><span class="sxs-lookup"><span data-stu-id="2eddd-140">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="2eddd-141">BOOL</span><span class="sxs-lookup"><span data-stu-id="2eddd-141">BOOL</span></span>                                                                        | <span data-ttu-id="2eddd-142">Розничная или отладочная</span><span class="sxs-lookup"><span data-stu-id="2eddd-142">Retail/Debug</span></span> | [<span data-ttu-id="2eddd-143">**креатедевице**</span><span class="sxs-lookup"><span data-stu-id="2eddd-143">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| <span data-ttu-id="2eddd-144">интерфацетимингс</span><span class="sxs-lookup"><span data-stu-id="2eddd-144">INTERFACETIMINGS</span></span>  | <span data-ttu-id="2eddd-145">[**D3DISSUE \_ Начало**](d3dissue-begin.md), [ **D3DISSUE \_**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="2eddd-145">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="2eddd-146">**D3DDEVINFO \_ D3D9INTERFACETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="2eddd-146">**D3DDEVINFO\_D3D9INTERFACETIMINGS**</span></span>](d3ddevinfo-d3d9interfacetimings.md) | <span data-ttu-id="2eddd-147">Розничная или отладочная</span><span class="sxs-lookup"><span data-stu-id="2eddd-147">Retail/Debug</span></span> | <span data-ttu-id="2eddd-148">Н/Д</span><span class="sxs-lookup"><span data-stu-id="2eddd-148">N/A</span></span>                                              |
| <span data-ttu-id="2eddd-149">ПЕРЕКРЫТИЯ</span><span class="sxs-lookup"><span data-stu-id="2eddd-149">OCCLUSION</span></span>         | <span data-ttu-id="2eddd-150">[**D3DISSUE \_ Начало**](d3dissue-begin.md), [ **D3DISSUE \_**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="2eddd-150">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | <span data-ttu-id="2eddd-151">DWORD</span><span class="sxs-lookup"><span data-stu-id="2eddd-151">DWORD</span></span>                                                                       | <span data-ttu-id="2eddd-152">Розничная или отладочная</span><span class="sxs-lookup"><span data-stu-id="2eddd-152">Retail/Debug</span></span> | <span data-ttu-id="2eddd-153">Н/Д</span><span class="sxs-lookup"><span data-stu-id="2eddd-153">N/A</span></span>                                              |
| <span data-ttu-id="2eddd-154">пипелинетимингс</span><span class="sxs-lookup"><span data-stu-id="2eddd-154">PIPELINETIMINGS</span></span>   | <span data-ttu-id="2eddd-155">[**D3DISSUE \_ Начало**](d3dissue-begin.md), [ **D3DISSUE \_**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="2eddd-155">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="2eddd-156">**D3DDEVINFO \_ D3D9PIPELINETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="2eddd-156">**D3DDEVINFO\_D3D9PIPELINETIMINGS**</span></span>](d3ddevinfo-d3d9pipelinetimings.md)   | <span data-ttu-id="2eddd-157">Розничная или отладочная</span><span class="sxs-lookup"><span data-stu-id="2eddd-157">Retail/Debug</span></span> | <span data-ttu-id="2eddd-158">Н/Д</span><span class="sxs-lookup"><span data-stu-id="2eddd-158">N/A</span></span>                                              |
| <span data-ttu-id="2eddd-159">RESOURCEMANAGER</span><span class="sxs-lookup"><span data-stu-id="2eddd-159">RESOURCEMANAGER</span></span>   | [<span data-ttu-id="2eddd-160">**D3DISSUE \_ конец**</span><span class="sxs-lookup"><span data-stu-id="2eddd-160">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="2eddd-161">**D3DDEVINFO \_ ResourceManager**</span><span class="sxs-lookup"><span data-stu-id="2eddd-161">**D3DDEVINFO\_ResourceManager**</span></span>](d3ddevinfo-resourcemanager.md)           | <span data-ttu-id="2eddd-162">Только Отладка</span><span class="sxs-lookup"><span data-stu-id="2eddd-162">Debug only</span></span>   | [<span data-ttu-id="2eddd-163">**Настоящее**</span><span class="sxs-lookup"><span data-stu-id="2eddd-163">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| <span data-ttu-id="2eddd-164">timestamp</span><span class="sxs-lookup"><span data-stu-id="2eddd-164">TIMESTAMP</span></span>         | [<span data-ttu-id="2eddd-165">**D3DISSUE \_ конец**</span><span class="sxs-lookup"><span data-stu-id="2eddd-165">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="2eddd-166">UINT64</span><span class="sxs-lookup"><span data-stu-id="2eddd-166">UINT64</span></span>                                                                      | <span data-ttu-id="2eddd-167">Розничная или отладочная</span><span class="sxs-lookup"><span data-stu-id="2eddd-167">Retail/Debug</span></span> | <span data-ttu-id="2eddd-168">Н/Д</span><span class="sxs-lookup"><span data-stu-id="2eddd-168">N/A</span></span>                                              |
| <span data-ttu-id="2eddd-169">тиместампдисжоинт</span><span class="sxs-lookup"><span data-stu-id="2eddd-169">TIMESTAMPDISJOINT</span></span> | <span data-ttu-id="2eddd-170">[**D3DISSUE \_ Начало**](d3dissue-begin.md), [ **D3DISSUE \_**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="2eddd-170">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | <span data-ttu-id="2eddd-171">BOOL</span><span class="sxs-lookup"><span data-stu-id="2eddd-171">BOOL</span></span>                                                                        | <span data-ttu-id="2eddd-172">Розничная или отладочная</span><span class="sxs-lookup"><span data-stu-id="2eddd-172">Retail/Debug</span></span> | <span data-ttu-id="2eddd-173">Н/Д</span><span class="sxs-lookup"><span data-stu-id="2eddd-173">N/A</span></span>                                              |
| <span data-ttu-id="2eddd-174">тиместампфрек</span><span class="sxs-lookup"><span data-stu-id="2eddd-174">TIMESTAMPFREQ</span></span>     | [<span data-ttu-id="2eddd-175">**D3DISSUE \_ конец**</span><span class="sxs-lookup"><span data-stu-id="2eddd-175">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="2eddd-176">UINT64</span><span class="sxs-lookup"><span data-stu-id="2eddd-176">UINT64</span></span>                                                                      | <span data-ttu-id="2eddd-177">Розничная или отладочная</span><span class="sxs-lookup"><span data-stu-id="2eddd-177">Retail/Debug</span></span> | <span data-ttu-id="2eddd-178">Н/Д</span><span class="sxs-lookup"><span data-stu-id="2eddd-178">N/A</span></span>                                              |
| <span data-ttu-id="2eddd-179">вкаче</span><span class="sxs-lookup"><span data-stu-id="2eddd-179">VCACHE</span></span>            | [<span data-ttu-id="2eddd-180">**D3DISSUE \_ конец**</span><span class="sxs-lookup"><span data-stu-id="2eddd-180">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="2eddd-181">**D3DDEVINFO \_ вкаче**</span><span class="sxs-lookup"><span data-stu-id="2eddd-181">**D3DDEVINFO\_VCACHE**</span></span>](d3ddevinfo-vcache.md)                             | <span data-ttu-id="2eddd-182">Розничная или отладочная</span><span class="sxs-lookup"><span data-stu-id="2eddd-182">Retail/Debug</span></span> | [<span data-ttu-id="2eddd-183">**креатедевице**</span><span class="sxs-lookup"><span data-stu-id="2eddd-183">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| <span data-ttu-id="2eddd-184">вертексстатс</span><span class="sxs-lookup"><span data-stu-id="2eddd-184">VERTEXSTATS</span></span>       | [<span data-ttu-id="2eddd-185">**D3DISSUE \_ конец**</span><span class="sxs-lookup"><span data-stu-id="2eddd-185">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="2eddd-186">**D3DDEVINFO \_ D3DVERTEXSTATS**</span><span class="sxs-lookup"><span data-stu-id="2eddd-186">**D3DDEVINFO\_D3DVERTEXSTATS**</span></span>](d3ddevinfo-d3dvertexstats.md)             | <span data-ttu-id="2eddd-187">Только Отладка</span><span class="sxs-lookup"><span data-stu-id="2eddd-187">Debug only</span></span>   | [<span data-ttu-id="2eddd-188">**Настоящее**</span><span class="sxs-lookup"><span data-stu-id="2eddd-188">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| <span data-ttu-id="2eddd-189">вертекстимингс</span><span class="sxs-lookup"><span data-stu-id="2eddd-189">VERTEXTIMINGS</span></span>     | <span data-ttu-id="2eddd-190">[**D3DISSUE \_ Начало**](d3dissue-begin.md), [ **D3DISSUE \_**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="2eddd-190">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="2eddd-191">**D3DDEVINFO \_ D3D9STAGETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="2eddd-191">**D3DDEVINFO\_D3D9STAGETIMINGS**</span></span>](d3ddevinfo-d3d9stagetimings.md)         | <span data-ttu-id="2eddd-192">Розничная или отладочная</span><span class="sxs-lookup"><span data-stu-id="2eddd-192">Retail/Debug</span></span> | <span data-ttu-id="2eddd-193">Н/Д</span><span class="sxs-lookup"><span data-stu-id="2eddd-193">N/A</span></span>                                              |



 

<span data-ttu-id="2eddd-194">Для некоторых запросов требуется событие Begin и End, а для других требуется только завершающее событие.</span><span class="sxs-lookup"><span data-stu-id="2eddd-194">Some of the queries require a begin and end event, while others only require an end event.</span></span> <span data-ttu-id="2eddd-195">Запросы, для которых требуется событие End, начинаются только при возникновении другого неявного события (которое перечислено в таблице).</span><span class="sxs-lookup"><span data-stu-id="2eddd-195">The queries that only require an end event begin when another implicit event occurs (which is listed in the table).</span></span> <span data-ttu-id="2eddd-196">Все запросы возвращают ответ, за исключением запроса события, ответ которого всегда равен **true**.</span><span class="sxs-lookup"><span data-stu-id="2eddd-196">All queries return an answer, except the event query whose answer is always **TRUE**.</span></span> <span data-ttu-id="2eddd-197">Приложение использует либо состояние запроса, либо код возврата [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="2eddd-197">An application uses either the state of the query or the return code of [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span>

## <a name="create-a-query"></a><span data-ttu-id="2eddd-198">Создание запроса</span><span class="sxs-lookup"><span data-stu-id="2eddd-198">Create a Query</span></span>

<span data-ttu-id="2eddd-199">Перед созданием запроса можно проверить, поддерживает ли среда выполнения запросы, вызвав [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) со **следующим указателем** :</span><span class="sxs-lookup"><span data-stu-id="2eddd-199">Before you create a query, you can check to see if the runtime supports queries by calling [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) with a **NULL** pointer like this:</span></span>


```
IDirect3DQuery9* pEventQuery;

// Create a device pointer m_pd3dDevice

// Create a query object
HRESULT hr = m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, NULL);
```



<span data-ttu-id="2eddd-200">Этот метод возвращает код успешного выполнения, если может быть создан запрос. в противном случае возвращается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="2eddd-200">This method returns a success code if a query can be created; otherwise it returns an error code.</span></span> <span data-ttu-id="2eddd-201">После выполнения [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) можно создать объект запроса следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2eddd-201">Once [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) succeeds, you can create a query object like this:</span></span>


```
IDirect3DQuery9* pEventQuery;
m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);
```



<span data-ttu-id="2eddd-202">Если этот вызов будет выполнен, создается объект запроса.</span><span class="sxs-lookup"><span data-stu-id="2eddd-202">If this call succeeds, a query object is created.</span></span> <span data-ttu-id="2eddd-203">Запрос в основном бездействует в сигнальном состоянии (с неинициализированным ответом), ожидающим выполнения.</span><span class="sxs-lookup"><span data-stu-id="2eddd-203">The query is essentially idle in the signaled state (with an uninitialized answer) waiting to be issued.</span></span> <span data-ttu-id="2eddd-204">Завершив работу с запросом, отпустите его как любой другой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2eddd-204">When you are finished with the query, release it like any other interface.</span></span>

## <a name="issue-a-query"></a><span data-ttu-id="2eddd-205">Выдача запроса</span><span class="sxs-lookup"><span data-stu-id="2eddd-205">Issue a Query</span></span>

<span data-ttu-id="2eddd-206">Приложение изменяет состояние запроса, выдавая запрос.</span><span class="sxs-lookup"><span data-stu-id="2eddd-206">An application changes a query state by issuing a query.</span></span> <span data-ttu-id="2eddd-207">Ниже приведен пример выдачи запроса.</span><span class="sxs-lookup"><span data-stu-id="2eddd-207">Here is an example of issuing a query:</span></span>


```
IDirect3DQuery9* pEventQuery;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Issue a Begin event
pEventQuery->Issue(D3DISSUE_BEGIN);

or

// Issue an End event
pEventQuery->Issue(D3DISSUE_END);
```



<span data-ttu-id="2eddd-208">Запрос в сигнальном состоянии будет перенесен следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2eddd-208">A query in the signaled state will transition like this when issued:</span></span>



| <span data-ttu-id="2eddd-209">Тип проблемы</span><span class="sxs-lookup"><span data-stu-id="2eddd-209">Issue Type</span></span>                                | <span data-ttu-id="2eddd-210">Запрос переходит к.</span><span class="sxs-lookup"><span data-stu-id="2eddd-210">Query Transitions to the .</span></span> <span data-ttu-id="2eddd-211">.</span><span class="sxs-lookup"><span data-stu-id="2eddd-211">.</span></span> <span data-ttu-id="2eddd-212">.</span><span class="sxs-lookup"><span data-stu-id="2eddd-212">.</span></span> |
|-------------------------------------------|--------------------------------|
| [<span data-ttu-id="2eddd-213">**\_Начало D3DISSUE**</span><span class="sxs-lookup"><span data-stu-id="2eddd-213">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="2eddd-214">Состояние сборки.</span><span class="sxs-lookup"><span data-stu-id="2eddd-214">Building state.</span></span>                |
| [<span data-ttu-id="2eddd-215">**D3DISSUE \_ конец**</span><span class="sxs-lookup"><span data-stu-id="2eddd-215">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="2eddd-216">Состояние выдано.</span><span class="sxs-lookup"><span data-stu-id="2eddd-216">Issued state.</span></span>                  |



 

<span data-ttu-id="2eddd-217">Запрос в состоянии здания будет перенесен следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2eddd-217">A query in the building state will transition like this when issued:</span></span>



| <span data-ttu-id="2eddd-218">Тип проблемы</span><span class="sxs-lookup"><span data-stu-id="2eddd-218">Issue Type</span></span>                                | <span data-ttu-id="2eddd-219">Запрос переходит к.</span><span class="sxs-lookup"><span data-stu-id="2eddd-219">Query Transitions to the .</span></span> <span data-ttu-id="2eddd-220">.</span><span class="sxs-lookup"><span data-stu-id="2eddd-220">.</span></span> <span data-ttu-id="2eddd-221">.</span><span class="sxs-lookup"><span data-stu-id="2eddd-221">.</span></span>                                            |
|-------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="2eddd-222">**\_Начало D3DISSUE**</span><span class="sxs-lookup"><span data-stu-id="2eddd-222">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="2eddd-223">(Нет перехода, остается в состоянии здания.</span><span class="sxs-lookup"><span data-stu-id="2eddd-223">(No transition, stays in the building state.</span></span> <span data-ttu-id="2eddd-224">Перезапускает скобку запроса.)</span><span class="sxs-lookup"><span data-stu-id="2eddd-224">Restarts the query bracket.)</span></span> |
| [<span data-ttu-id="2eddd-225">**D3DISSUE \_ конец**</span><span class="sxs-lookup"><span data-stu-id="2eddd-225">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="2eddd-226">Состояние выдано.</span><span class="sxs-lookup"><span data-stu-id="2eddd-226">Issued state.</span></span>                                                             |



 

<span data-ttu-id="2eddd-227">Запрос в выданном состоянии будет перенесен следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2eddd-227">A query in the issued state will transition like this when issued:</span></span>



| <span data-ttu-id="2eddd-228">Тип проблемы</span><span class="sxs-lookup"><span data-stu-id="2eddd-228">Issue Type</span></span>                                | <span data-ttu-id="2eddd-229">Запрос переходит к.</span><span class="sxs-lookup"><span data-stu-id="2eddd-229">Query Transitions to the .</span></span> <span data-ttu-id="2eddd-230">.</span><span class="sxs-lookup"><span data-stu-id="2eddd-230">.</span></span> <span data-ttu-id="2eddd-231">.</span><span class="sxs-lookup"><span data-stu-id="2eddd-231">.</span></span>                    |
|-------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="2eddd-232">**\_Начало D3DISSUE**</span><span class="sxs-lookup"><span data-stu-id="2eddd-232">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="2eddd-233">Состояние сборки и перезапускает скобку запроса.</span><span class="sxs-lookup"><span data-stu-id="2eddd-233">Building state and restarts the query bracket.</span></span>    |
| [<span data-ttu-id="2eddd-234">**D3DISSUE \_ конец**</span><span class="sxs-lookup"><span data-stu-id="2eddd-234">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="2eddd-235">Выданное состояние после прерывания существующего запроса.</span><span class="sxs-lookup"><span data-stu-id="2eddd-235">Issued state after abandoning the existing query.</span></span> |



 

## <a name="check-the-query-state-and-get-the-answer-to-the-query"></a><span data-ttu-id="2eddd-236">Проверка состояния запроса и получение ответа на запрос</span><span class="sxs-lookup"><span data-stu-id="2eddd-236">Check the Query State and Get the Answer to the Query</span></span>

<span data-ttu-id="2eddd-237">Метод [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) выполняет два действия:</span><span class="sxs-lookup"><span data-stu-id="2eddd-237">[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) does two things:</span></span>

1.  <span data-ttu-id="2eddd-238">Возвращает состояние запроса в коде возврата.</span><span class="sxs-lookup"><span data-stu-id="2eddd-238">Returns the query state in the return code.</span></span>
2.  <span data-ttu-id="2eddd-239">Возвращает ответ на запрос в *pData*.</span><span class="sxs-lookup"><span data-stu-id="2eddd-239">Returns the answer to the query in *pData*.</span></span>

<span data-ttu-id="2eddd-240">В каждом из трех состояний запроса приведены коды возврата [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) :</span><span class="sxs-lookup"><span data-stu-id="2eddd-240">From each of the three query states, here are the [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) return codes:</span></span>



| <span data-ttu-id="2eddd-241">Состояние запроса</span><span class="sxs-lookup"><span data-stu-id="2eddd-241">Query State</span></span> | <span data-ttu-id="2eddd-242">Код возврата GetData</span><span class="sxs-lookup"><span data-stu-id="2eddd-242">GetData return code</span></span> |
|-------------|---------------------|
| <span data-ttu-id="2eddd-243">Сигнал</span><span class="sxs-lookup"><span data-stu-id="2eddd-243">Signaled</span></span>    | <span data-ttu-id="2eddd-244">\_ОК</span><span class="sxs-lookup"><span data-stu-id="2eddd-244">S\_OK</span></span>               |
| <span data-ttu-id="2eddd-245">Сборка</span><span class="sxs-lookup"><span data-stu-id="2eddd-245">Building</span></span>    | <span data-ttu-id="2eddd-246">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="2eddd-246">Error code</span></span>          |
| <span data-ttu-id="2eddd-247">Выдано</span><span class="sxs-lookup"><span data-stu-id="2eddd-247">Issued</span></span>      | <span data-ttu-id="2eddd-248">S \_ false</span><span class="sxs-lookup"><span data-stu-id="2eddd-248">S\_FALSE</span></span>            |



 

<span data-ttu-id="2eddd-249">Например, если запрос находится в состоянии «выдано» и ответ на запрос недоступен, функция [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) возвращает \_ значение false.</span><span class="sxs-lookup"><span data-stu-id="2eddd-249">For example, when a query is in the issued state and the answer to the query is not available, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) returns S\_FALSE.</span></span> <span data-ttu-id="2eddd-250">Когда ресурс завершает свою работу и приложение выпустило завершение запроса, ресурс переводит запрос в сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="2eddd-250">When the resource finishes its work and the application has issued a query end, the resource transitions the query to the signaled state.</span></span> <span data-ttu-id="2eddd-251">Из состояния "сигнал" функция **GetData** возвращает S \_ ОК, что означает, что ответ на запрос также возвращается в *pData*.</span><span class="sxs-lookup"><span data-stu-id="2eddd-251">From the signaled state, **GetData** returns S\_OK which means that the answer to the query is also returned in *pData*.</span></span> <span data-ttu-id="2eddd-252">Например, ниже приведена последовательность событий для возврата количества пикселей, рисуемых в последовательности отрисовки.</span><span class="sxs-lookup"><span data-stu-id="2eddd-252">For instance, here is the sequence of events to return the number of pixels drawn in a render sequence:</span></span>

-   <span data-ttu-id="2eddd-253">создание запроса;</span><span class="sxs-lookup"><span data-stu-id="2eddd-253">Create the query.</span></span>
-   <span data-ttu-id="2eddd-254">Выдача события Begin.</span><span class="sxs-lookup"><span data-stu-id="2eddd-254">Issue a begin event.</span></span>
-   <span data-ttu-id="2eddd-255">Нарисуйте что-нибудь.</span><span class="sxs-lookup"><span data-stu-id="2eddd-255">Draw something.</span></span>
-   <span data-ttu-id="2eddd-256">Выдача завершающего события.</span><span class="sxs-lookup"><span data-stu-id="2eddd-256">Issue an end event.</span></span>

<span data-ttu-id="2eddd-257">Ниже приведена соответствующая последовательность кода.</span><span class="sxs-lookup"><span data-stu-id="2eddd-257">The following is the corresponding sequence of code:</span></span>


```
IDirect3DQuery9* pOcclusionQuery;
DWORD numberOfPixelsDrawn;

m_pD3DDevice->CreateQuery(D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery);

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_BEGIN);

// API render loop
...
Draw(...)
...

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pOcclusionQuery->GetData( &numberOfPixelsDrawn, 
                                  sizeof(DWORD), D3DGETDATA_FLUSH ))
    ;
```



<span data-ttu-id="2eddd-258">Эти строки кода выполняют несколько задач:</span><span class="sxs-lookup"><span data-stu-id="2eddd-258">These lines of code do several things:</span></span>

-   <span data-ttu-id="2eddd-259">Вызовите [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) , чтобы получить количество рисуемых пикселей.</span><span class="sxs-lookup"><span data-stu-id="2eddd-259">Call [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) to return the number of pixels drawn.</span></span>
-   <span data-ttu-id="2eddd-260">Укажите [**D3DGETDATA \_ flush**](d3dgetdata-flush.md) , чтобы разрешить ресурсу переводить запрос в сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="2eddd-260">Specify [**D3DGETDATA\_FLUSH**](d3dgetdata-flush.md) to enable the resource to transition the query to the signaled state.</span></span>
-   <span data-ttu-id="2eddd-261">Опросить ресурс запроса, вызвав метод [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) из цикла.</span><span class="sxs-lookup"><span data-stu-id="2eddd-261">Poll the query resource by calling [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) from a loop.</span></span> <span data-ttu-id="2eddd-262">Пока метод **GetData** возвращает \_ значение false, это означает, что ресурс еще не вернул ответ.</span><span class="sxs-lookup"><span data-stu-id="2eddd-262">As long as **GetData** returns S\_FALSE, this means the resource has not returned the answer yet.</span></span>

<span data-ttu-id="2eddd-263">Возвращаемое значение [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) , по сути, указывает, в каком состоянии находится запрос.</span><span class="sxs-lookup"><span data-stu-id="2eddd-263">The return value of [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) essentially tells you in what state the query is.</span></span> <span data-ttu-id="2eddd-264">Возможные значения: S \_ OK, s \_ false и ошибка.</span><span class="sxs-lookup"><span data-stu-id="2eddd-264">Possible values are S\_OK, S\_FALSE, and an error.</span></span> <span data-ttu-id="2eddd-265">Не вызывайте **GetData** для запроса, который находится в состоянии здания.</span><span class="sxs-lookup"><span data-stu-id="2eddd-265">Do not call **GetData** on a query that is in the building state.</span></span>

-   <span data-ttu-id="2eddd-266">\_ОК означает, что ресурс (GPU или драйвер или среда выполнения) завершен.</span><span class="sxs-lookup"><span data-stu-id="2eddd-266">S\_OK means the resource (GPU or driver, or runtime) is finished.</span></span> <span data-ttu-id="2eddd-267">Запрос возвращается в сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="2eddd-267">The query is returning to the signaled state.</span></span> <span data-ttu-id="2eddd-268">Ответ (если таковой имеется) возвращается методом [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="2eddd-268">The answer (if any) is being returned by [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span>
-   <span data-ttu-id="2eddd-269">\_Значение false означает, что ресурс (GPU или драйвер или среда выполнения) еще не может вернуть ответ.</span><span class="sxs-lookup"><span data-stu-id="2eddd-269">S\_FALSE means the resource (GPU or driver, or runtime) cannot return an answer yet.</span></span> <span data-ttu-id="2eddd-270">Это может быть вызвано тем, что графический процессор не завершен или пока не просмотрел работу.</span><span class="sxs-lookup"><span data-stu-id="2eddd-270">This could be because the GPU is not finished or has not seen the work yet.</span></span>
-   <span data-ttu-id="2eddd-271">Ошибка означает, что запрос создал ошибку, которую невозможно восстановить.</span><span class="sxs-lookup"><span data-stu-id="2eddd-271">An error means that the query has generated an error from which it cannot recover.</span></span> <span data-ttu-id="2eddd-272">Это может быть так, если устройство потеряно во время выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="2eddd-272">This could be the case if the device is lost during a query.</span></span> <span data-ttu-id="2eddd-273">После создания запроса об ошибке (отличном от S \_ false) запрос должен быть создан повторно, что приведет к перезапуску последовательности запросов из сигнального состояния.</span><span class="sxs-lookup"><span data-stu-id="2eddd-273">Once a query has generated an error (other than S\_FALSE), the query must be recreated which will restart the query sequence from the signaled state.</span></span>

<span data-ttu-id="2eddd-274">Вместо указания [**D3DGETDATA \_ flush**](d3dgetdata-flush.md), которая предоставляет более актуальную информацию, можно указать ноль, которая является более неплотной, если запрос находится в состоянии «выдано».</span><span class="sxs-lookup"><span data-stu-id="2eddd-274">Instead of specifying [**D3DGETDATA\_FLUSH**](d3dgetdata-flush.md), which provides more up-to-date information, you could supply zero which is a more light-weight check if the query is in the issued state.</span></span> <span data-ttu-id="2eddd-275">Если указать нуль, то [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) не будет сбрасывать буфер команд.</span><span class="sxs-lookup"><span data-stu-id="2eddd-275">Supplying zero will cause [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) to not flush the command buffer.</span></span> <span data-ttu-id="2eddd-276">По этой причине необходимо соблюдать осторожность, чтобы избежать циклов инфинате (Дополнительные сведения см. в разделе **GetData** ).</span><span class="sxs-lookup"><span data-stu-id="2eddd-276">For this reason, care must be taken to avoid infinate loops (see **GetData** for details).</span></span> <span data-ttu-id="2eddd-277">Так как среда выполнения помещает в очередь работу в буфере команд, **D3DGETDATA \_ flush** — это механизм сброса буфера команд в драйвер (и, следовательно, графический процессор; см. раздел [Точная профилирование вызовов API Direct3D (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span><span class="sxs-lookup"><span data-stu-id="2eddd-277">Since the runtime queues up work in the command buffer, **D3DGETDATA\_FLUSH** is a mechanism for flushing the command buffer to the driver (and hence the GPU; see [Accurately Profiling Direct3D API Calls (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="2eddd-278">Во время очистки буфера команд запрос может перейти в сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="2eddd-278">During the command buffer flush, a query may transition to the signaled state.</span></span>

## <a name="example-an-event-query"></a><span data-ttu-id="2eddd-279">Пример. запрос события</span><span class="sxs-lookup"><span data-stu-id="2eddd-279">Example: An Event Query</span></span>

<span data-ttu-id="2eddd-280">Запрос события не поддерживает событие Begin.</span><span class="sxs-lookup"><span data-stu-id="2eddd-280">An event query does not support a begin event.</span></span>

-   <span data-ttu-id="2eddd-281">создание запроса;</span><span class="sxs-lookup"><span data-stu-id="2eddd-281">Create the query.</span></span>
-   <span data-ttu-id="2eddd-282">Выдача завершающего события.</span><span class="sxs-lookup"><span data-stu-id="2eddd-282">Issue an end event.</span></span>
-   <span data-ttu-id="2eddd-283">Опросить, пока GPU не простаивает.</span><span class="sxs-lookup"><span data-stu-id="2eddd-283">Poll until the GPU is idle.</span></span>
-   <span data-ttu-id="2eddd-284">Выдача завершающего события.</span><span class="sxs-lookup"><span data-stu-id="2eddd-284">Issue an end event.</span></span>


```
IDirect3DQuery9* pEventQuery = NULL;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

... // API calls

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
```



<span data-ttu-id="2eddd-285">Это последовательность команд, которые запрос на событие использует для профилирования вызовов интерфейса прикладного программирования (API) (см. раздел [Точная профилирование вызовов API Direct3D (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span><span class="sxs-lookup"><span data-stu-id="2eddd-285">This is the sequence of commands an event query uses to profile application programming interface (API) calls (see [Accurately Profiling Direct3D API Calls (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="2eddd-286">В этой последовательности используются маркеры, помогающие управлять объемом работы в буфере команд.</span><span class="sxs-lookup"><span data-stu-id="2eddd-286">This sequence uses markers to help control the amount of work in the command buffer.</span></span>

<span data-ttu-id="2eddd-287">Обратите внимание, что приложения должны уделять особое внимание значительным затратам на очистку буфера команд, так как в этом случае операционная система переключается в режим ядра, что приводит к снижению производительности немалым.</span><span class="sxs-lookup"><span data-stu-id="2eddd-287">Note that applications should pay special attention to the large cost associated with flushing the command buffer because this causes the operating system to switch into kernel mode, thus incurring a sizeable performance penalty.</span></span> <span data-ttu-id="2eddd-288">Приложения также должны знать о расходе циклов ЦП, ожидая завершения запросов.</span><span class="sxs-lookup"><span data-stu-id="2eddd-288">Applications should also be aware of wasting CPU cycles by waiting for queries to complete.</span></span>

<span data-ttu-id="2eddd-289">Запросы — это оптимизация, которую следует использовать во время отрисовки для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="2eddd-289">Queries are an optimization to be used during rendering to increase performance.</span></span> <span data-ttu-id="2eddd-290">Поэтому не стоит тратить время на ожидание завершения запроса.</span><span class="sxs-lookup"><span data-stu-id="2eddd-290">Therefore, it is not beneficial to spend time waiting for a query to finish.</span></span> <span data-ttu-id="2eddd-291">Если выдается запрос и результаты еще не готовы к моменту их проверки приложением, то попытки оптимизации не выполнялись успешно, а отрисовка должна продолжаться как обычно.</span><span class="sxs-lookup"><span data-stu-id="2eddd-291">If a query is issued and if the results are not yet ready by the time the application checks for them, the attempt at optimizing did not succeed and rendering should continue as normal.</span></span>

<span data-ttu-id="2eddd-292">Классический пример — во время отбора перекрытия.</span><span class="sxs-lookup"><span data-stu-id="2eddd-292">The classic example of this is during Occlusion Culling.</span></span> <span data-ttu-id="2eddd-293">Вместо приведенного выше цикла **while** приложение, использующее запросы, может реализовать перекрытияное извлечение, чтобы проверить, завершился ли запрос на время, необходимое для результата.</span><span class="sxs-lookup"><span data-stu-id="2eddd-293">Instead of the **while** loop above, an application using queries can implement occlusion culling to check to see if a query had finished by the time it needs the result.</span></span> <span data-ttu-id="2eddd-294">Если запрос не завершен, продолжайте (как наихудший сценарий), как если проверяемый объект не перекрыто (т. е. он является видимым) и готовит его к просмотру.</span><span class="sxs-lookup"><span data-stu-id="2eddd-294">If the query has not finished, continue (as a worst-case scenario) as if the object being tested against is not occluded (i.e. it is visible) and render it.</span></span> <span data-ttu-id="2eddd-295">Код будет выглядеть примерно так:</span><span class="sxs-lookup"><span data-stu-id="2eddd-295">The code would look similar to the following.</span></span>


```
IDirect3DQuery9* pOcclusionQuery = NULL;
m_pD3DDevice->CreateQuery( D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery );

// Add a begin marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_BEGIN );

... // API calls

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_END );

// Avoid flushing and letting the CPU go idle by not using a while loop.
// Check if queries are finished:
DWORD dwOccluded = 0;
if( S_FALSE == pOcclusionQuery->GetData( &dwOccluded, sizeof(DWORD), 0 ) )
{
    // Query is not done yet or object not occluded; avoid flushing/wait by continuing with worst-case scenario
    pSomeComplexMesh->Render();
}
else if( dwOccluded != 0 )
{
    // Query is done and object is not occluded.
    pSomeComplexMesh->Render();
}
```



## <a name="related-topics"></a><span data-ttu-id="2eddd-296">См. также</span><span class="sxs-lookup"><span data-stu-id="2eddd-296">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2eddd-297">Дополнительные разделы</span><span class="sxs-lookup"><span data-stu-id="2eddd-297">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 
