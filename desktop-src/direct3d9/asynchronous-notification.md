---
description: Существует ряд интересных запросов к драйверу, который может быть создан приложением в случае отсутствия затрат на производительность.
ms.assetid: 81e1c5c5-03bc-4598-814e-14e56513e221
title: Асинхронное уведомление (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aee8acb791e2e1e2de7eb305cc19df4e7711e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701219"
---
# <a name="asynchronous-notification-direct3d-9"></a><span data-ttu-id="fa4eb-103">Асинхронное уведомление (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fa4eb-103">Asynchronous Notification (Direct3D 9)</span></span>

<span data-ttu-id="fa4eb-104">Существует ряд интересных запросов к драйверу, который может быть создан приложением в случае отсутствия затрат на производительность.</span><span class="sxs-lookup"><span data-stu-id="fa4eb-104">There are number of interesting queries on a driver that an application can make if there is no performance cost.</span></span> <span data-ttu-id="fa4eb-105">В Direct3D 7 и Direct3D 8 механизм синхронных запросов, а также очень хорошо работал для таких целей, как статистика, но не были добавлены критически важные для производительности запросы.</span><span class="sxs-lookup"><span data-stu-id="fa4eb-105">In Direct3D 7 and Direct3D 8, a synchronous query mechanism, GetInfo, worked well for things like statistics, but no performance-critical queries were added.</span></span> <span data-ttu-id="fa4eb-106">Существуют и другие вещи (например, ограждения), которые по сути являются асинхронными.</span><span class="sxs-lookup"><span data-stu-id="fa4eb-106">There are other things (like fences) that are inherently asynchronous.</span></span> <span data-ttu-id="fa4eb-107">Это простой API для выполнения как синхронных, так и асинхронных запросов.</span><span class="sxs-lookup"><span data-stu-id="fa4eb-107">This is a simple API to make both synchronous and asynchronous queries.</span></span> <span data-ttu-id="fa4eb-108">Сведения будут сняты с учета в Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="fa4eb-108">GetInfo will be retired in Direct3D 9.</span></span>

<span data-ttu-id="fa4eb-109">Создайте запрос с помощью [**IDirect3DDevice9:: CreateQuery**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="fa4eb-109">Create a query using [**IDirect3DDevice9::CreateQuery**](/windows/desktop/api).</span></span> <span data-ttu-id="fa4eb-110">Этот метод принимает D3DQUERYTYPE, который определяет, какой тип запроса необходимо сделать, и возвращает указатель на объект [**IDirect3DQuery9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="fa4eb-110">This method takes a D3DQUERYTYPE, which defines what kind of query to make and returns a pointer to an [**IDirect3DQuery9**](/windows/desktop/api) object.</span></span> <span data-ttu-id="fa4eb-111">Если тип запроса не поддерживается, вызов возвращает ошибку D3DERR \_ NOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="fa4eb-111">If the query type is not supported, the call returns an error D3DERR\_NOTAVAILABLE.</span></span> <span data-ttu-id="fa4eb-112">С помощью объекта Query приложение отправляет запрос в среду выполнения с помощью [**IDirect3DQuery9:: Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)и опрашивает состояние запроса с помощью [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="fa4eb-112">Using the query object, the application submits the query to the runtime using [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue), and polls the query status using [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span> <span data-ttu-id="fa4eb-113">Если результат запроса доступен, \_ возвращается s OK; в противном случае \_ возвращается значение s false.</span><span class="sxs-lookup"><span data-stu-id="fa4eb-113">If the query result is available, S\_OK is returned; otherwise, S\_FALSE is returned.</span></span> <span data-ttu-id="fa4eb-114">Предполагается, что приложение передает буфер соответствующего размера для результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="fa4eb-114">The application is expected to pass an appropriately sized buffer for the query results.</span></span>

<span data-ttu-id="fa4eb-115">Приложение может заставить среду выполнения принудительно сбрасывать запрос к драйверу с помощью D3DGETDATA \_ flush с [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="fa4eb-115">The application has an option to force the runtime to flush the query down to the driver by using D3DGETDATA\_FLUSH with [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span> <span data-ttu-id="fa4eb-116">Она вызывает сброс, вызывая драйвер для просмотра запроса.</span><span class="sxs-lookup"><span data-stu-id="fa4eb-116">It causes a flush, forcing the driver to see the query.</span></span> <span data-ttu-id="fa4eb-117">В этом случае D3DERR \_ девицелост возвращается, если устройство будет потеряно.</span><span class="sxs-lookup"><span data-stu-id="fa4eb-117">In this case, D3DERR\_DEVICELOST is returned if the device becomes lost.</span></span>

<span data-ttu-id="fa4eb-118">При потере устройства все запросы теряются, поэтому приложение должно их повторно создать.</span><span class="sxs-lookup"><span data-stu-id="fa4eb-118">All queries are lost when the device is lost, the application has to re-create them.</span></span> <span data-ttu-id="fa4eb-119">Если устройство не поддерживает запрос и Пкуерид имеет **значение NULL**, создание запроса завершится ошибкой с помощью D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="fa4eb-119">If the device does not support the query and the pQueryID is **NULL**, the query creation will fail with D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="fa4eb-120">В следующей таблице приведены важные сведения о каждом типе запроса.</span><span class="sxs-lookup"><span data-stu-id="fa4eb-120">The following table summaries important information about each query type.</span></span>



| <span data-ttu-id="fa4eb-121">куертитипе</span><span class="sxs-lookup"><span data-stu-id="fa4eb-121">QuertyType</span></span>                    | <span data-ttu-id="fa4eb-122">Допустимый флаг проблемы</span><span class="sxs-lookup"><span data-stu-id="fa4eb-122">Valid issue flag</span></span>              | <span data-ttu-id="fa4eb-123">Буфер GetData</span><span class="sxs-lookup"><span data-stu-id="fa4eb-123">GetData buffer</span></span>              | <span data-ttu-id="fa4eb-124">Параметры выполнения</span><span class="sxs-lookup"><span data-stu-id="fa4eb-124">Runtime</span></span>      | <span data-ttu-id="fa4eb-125">Неявное начало запроса</span><span class="sxs-lookup"><span data-stu-id="fa4eb-125">Implicit beginning of query</span></span> |
|-------------------------------|-------------------------------|-----------------------------|--------------|-----------------------------|
| <span data-ttu-id="fa4eb-126">D3DQUERYTYPE \_ вкаче</span><span class="sxs-lookup"><span data-stu-id="fa4eb-126">D3DQUERYTYPE\_VCACHE</span></span>          | <span data-ttu-id="fa4eb-127">D3DISSUE \_ конец</span><span class="sxs-lookup"><span data-stu-id="fa4eb-127">D3DISSUE\_END</span></span>                 | <span data-ttu-id="fa4eb-128">D3DDEVINFO \_ вкаче</span><span class="sxs-lookup"><span data-stu-id="fa4eb-128">D3DDEVINFO\_VCACHE</span></span>          | <span data-ttu-id="fa4eb-129">Розничная или отладочная</span><span class="sxs-lookup"><span data-stu-id="fa4eb-129">Retail/Debug</span></span> | <span data-ttu-id="fa4eb-130">креатедевице</span><span class="sxs-lookup"><span data-stu-id="fa4eb-130">CreateDevice</span></span>                |
| <span data-ttu-id="fa4eb-131">D3DQUERYTYPE \_ ResourceManager</span><span class="sxs-lookup"><span data-stu-id="fa4eb-131">D3DQUERYTYPE\_ResourceManager</span></span> | <span data-ttu-id="fa4eb-132">D3DISSUE \_ конец</span><span class="sxs-lookup"><span data-stu-id="fa4eb-132">D3DISSUE\_END</span></span>                 | <span data-ttu-id="fa4eb-133">D3DDEVINFO \_ ResourceManager</span><span class="sxs-lookup"><span data-stu-id="fa4eb-133">D3DDEVINFO\_ResourceManager</span></span> | <span data-ttu-id="fa4eb-134">Только Отладка</span><span class="sxs-lookup"><span data-stu-id="fa4eb-134">Debug only</span></span>   | <span data-ttu-id="fa4eb-135">Присутствует</span><span class="sxs-lookup"><span data-stu-id="fa4eb-135">Present</span></span>                     |
| <span data-ttu-id="fa4eb-136">D3DQUERYTYPE \_ вертексстатс</span><span class="sxs-lookup"><span data-stu-id="fa4eb-136">D3DQUERYTYPE\_VERTEXSTATS</span></span>     | <span data-ttu-id="fa4eb-137">D3DISSUE \_ конец</span><span class="sxs-lookup"><span data-stu-id="fa4eb-137">D3DISSUE\_END</span></span>                 | <span data-ttu-id="fa4eb-138">D3DDEVINFO \_ D3DVERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="fa4eb-138">D3DDEVINFO\_D3DVERTEXSTATS</span></span>  | <span data-ttu-id="fa4eb-139">Только Отладка</span><span class="sxs-lookup"><span data-stu-id="fa4eb-139">Debug only</span></span>   | <span data-ttu-id="fa4eb-140">Присутствует</span><span class="sxs-lookup"><span data-stu-id="fa4eb-140">Present</span></span>                     |
| <span data-ttu-id="fa4eb-141">\_Событие D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="fa4eb-141">D3DQUERYTYPE\_EVENT</span></span>           | <span data-ttu-id="fa4eb-142">D3DISSUE \_ конец</span><span class="sxs-lookup"><span data-stu-id="fa4eb-142">D3DISSUE\_END</span></span>                 | <span data-ttu-id="fa4eb-143">BOOL</span><span class="sxs-lookup"><span data-stu-id="fa4eb-143">BOOL</span></span>                        | <span data-ttu-id="fa4eb-144">Розничная или отладочная</span><span class="sxs-lookup"><span data-stu-id="fa4eb-144">Retail/Debug</span></span> | <span data-ttu-id="fa4eb-145">креатедевице</span><span class="sxs-lookup"><span data-stu-id="fa4eb-145">CreateDevice</span></span>                |
| <span data-ttu-id="fa4eb-146">D3DQUERYTYPE \_ перекрытия</span><span class="sxs-lookup"><span data-stu-id="fa4eb-146">D3DQUERYTYPE\_OCCLUSION</span></span>       | <span data-ttu-id="fa4eb-147">\_Начало D3DISSUE, D3DISSUE \_ конец</span><span class="sxs-lookup"><span data-stu-id="fa4eb-147">D3DISSUE\_BEGIN,D3DISSUE\_END</span></span> | <span data-ttu-id="fa4eb-148">DWORD</span><span class="sxs-lookup"><span data-stu-id="fa4eb-148">DWORD</span></span>                       | <span data-ttu-id="fa4eb-149">Розничная или отладочная</span><span class="sxs-lookup"><span data-stu-id="fa4eb-149">Retail/Debug</span></span> | <span data-ttu-id="fa4eb-150">Н/Д</span><span class="sxs-lookup"><span data-stu-id="fa4eb-150">N/A</span></span>                         |



 

<span data-ttu-id="fa4eb-151">Поле флагов для [**IDirect3DQuery9:: дата_выпуска**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):</span><span class="sxs-lookup"><span data-stu-id="fa4eb-151">Flags field for [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):</span></span>


```
#define D3DISSUE_END (1 << 0) 
// Tells the runtime to issue the end of a query, changing its state to 
//   "non-signaled" 
```




```
 
#define D3DISSUE_BEGIN (1 << 1) // Tells the runtime to issue the 
// beginning of a query. 
```



<span data-ttu-id="fa4eb-152">Поле Flags для [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):</span><span class="sxs-lookup"><span data-stu-id="fa4eb-152">Flags field for [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):</span></span>


```
 
#define D3DGETDATA_FLUSH (1 << 0) // Tells the runtime to flush 
// if the query is outstanding.
```



## <a name="related-topics"></a><span data-ttu-id="fa4eb-153">См. также</span><span class="sxs-lookup"><span data-stu-id="fa4eb-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa4eb-154">Советы по программированию</span><span class="sxs-lookup"><span data-stu-id="fa4eb-154">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
