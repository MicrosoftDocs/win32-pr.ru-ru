---
title: Модель объектов
description: В следующей таблице перечислены типы объектов, которыми можно управлять с помощью различных наборов API, предоставляемых платформой фильтрации Windows (WFP).
ms.assetid: 6931583f-785c-4e27-b5e4-d185d23a54ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa90b4757a39617616c6f83b6b79fe322b2e64c8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104069612"
---
# <a name="object-model"></a><span data-ttu-id="3d44b-103">Модель объектов</span><span class="sxs-lookup"><span data-stu-id="3d44b-103">Object Model</span></span>

<span data-ttu-id="3d44b-104">В следующей таблице перечислены типы объектов, которыми можно управлять с помощью различных наборов API, предоставляемых платформой фильтрации Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="3d44b-104">The following table lists the object types that can be manipulated through the various API sets supplied by the Windows Filtering Platform (WFP).</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3d44b-105">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="3d44b-105">Object Type</span></span></th>
<th><span data-ttu-id="3d44b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="3d44b-106">Description</span></span></th>
<th><span data-ttu-id="3d44b-107">Примеры свойств</span><span class="sxs-lookup"><span data-stu-id="3d44b-107">Sample Properties</span></span></th>
<th><span data-ttu-id="3d44b-108">Пример</span><span class="sxs-lookup"><span data-stu-id="3d44b-108">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d44b-109">Фильтр</span><span class="sxs-lookup"><span data-stu-id="3d44b-109">Filter</span></span></td>
<td><span data-ttu-id="3d44b-110">Правило, которое управляет классификацией.</span><span class="sxs-lookup"><span data-stu-id="3d44b-110">A rule that governs classification.</span></span> <span data-ttu-id="3d44b-111">При соблюдении условий вызывается действие.</span><span class="sxs-lookup"><span data-stu-id="3d44b-111">If the conditions are met, the action is invoked.</span></span> <br/> <span data-ttu-id="3d44b-112">Это наиболее сложный объект, предоставляемый платформой WFP, так как он связывает все остальные типы объектов.</span><span class="sxs-lookup"><span data-stu-id="3d44b-112">This is the most complex object exposed by WFP since it ties together all the other object types.</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="3d44b-113">Массив условий</span><span class="sxs-lookup"><span data-stu-id="3d44b-113">Array of conditions</span></span></li>
<li><span data-ttu-id="3d44b-114">Действие (разрешить, блокировать, выноску)</span><span class="sxs-lookup"><span data-stu-id="3d44b-114">Action (Permit, Block, Callout)</span></span></li>
<li><span data-ttu-id="3d44b-115"><a href="filter-weight-assignment.md">Weight</a></span><span class="sxs-lookup"><span data-stu-id="3d44b-115"><a href="filter-weight-assignment.md">Weight</a></span></span></li>
<li><span data-ttu-id="3d44b-116">Контекст</span><span class="sxs-lookup"><span data-stu-id="3d44b-116">Context</span></span></li>
</ul></td>
<td><span data-ttu-id="3d44b-117">&quot;Блокировать трафик с TCP-портом, превышающим 1024.&quot;</span><span class="sxs-lookup"><span data-stu-id="3d44b-117">&quot;Block traffic with a TCP port greater than 1024.&quot;</span></span> <br/> <span data-ttu-id="3d44b-118">&quot;Выноски ИДЕНТИФИКАТОРов для всего незащищенного трафика.&quot;</span><span class="sxs-lookup"><span data-stu-id="3d44b-118">&quot;Callout to IDS for all traffic that is not secured.&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d44b-119">Выноска</span><span class="sxs-lookup"><span data-stu-id="3d44b-119">Callout</span></span></td>
<td><span data-ttu-id="3d44b-120">Набор функций, участвующих в процессе классификации.</span><span class="sxs-lookup"><span data-stu-id="3d44b-120">A set of functions that participate in the classification process.</span></span><br/> <span data-ttu-id="3d44b-121">Это позволяет выполнять обработку пользовательских пакетов при выполнении определенных условий.</span><span class="sxs-lookup"><span data-stu-id="3d44b-121">It allows for custom packet processing to be done when certain conditions are met.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="3d44b-122">ID</span><span class="sxs-lookup"><span data-stu-id="3d44b-122">ID</span></span></li>
<li><span data-ttu-id="3d44b-123">Применимый слой</span><span class="sxs-lookup"><span data-stu-id="3d44b-123">Applicable layer</span></span></li>
</ul></td>
<td><span data-ttu-id="3d44b-124">Драйвер NAT</span><span class="sxs-lookup"><span data-stu-id="3d44b-124">The NAT driver</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d44b-125">Уровень</span><span class="sxs-lookup"><span data-stu-id="3d44b-125">Layer</span></span></td>
<td><span data-ttu-id="3d44b-126">Контейнер фильтра в обработчике фильтров.</span><span class="sxs-lookup"><span data-stu-id="3d44b-126">A filter container in the filter engine.</span></span> <br/> <span data-ttu-id="3d44b-127">Представляет конкретную точку в обработке сетевого трафика, в которой вызывается обработчик фильтра.</span><span class="sxs-lookup"><span data-stu-id="3d44b-127">Represents a specific point in network traffic processing where the filter engine is invoked.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="3d44b-128">Схема фильтров, которые могут быть добавлены к слою</span><span class="sxs-lookup"><span data-stu-id="3d44b-128">Schema for filters that can be added to the layer</span></span></li>
</ul></td>
<td><span data-ttu-id="3d44b-129">Уровень входящего транспорта</span><span class="sxs-lookup"><span data-stu-id="3d44b-129">The Inbound Transport Layer</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d44b-130">Подслой</span><span class="sxs-lookup"><span data-stu-id="3d44b-130">Sub-layer</span></span></td>
<td><span data-ttu-id="3d44b-131">Вспомогательный компонент слоя, используемый при <a href="filter-arbitration.md">арбитраже фильтра</a>.</span><span class="sxs-lookup"><span data-stu-id="3d44b-131">A sub-component of a layer, used in <a href="filter-arbitration.md">filter arbitration</a>.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="3d44b-132">Вес</span><span class="sxs-lookup"><span data-stu-id="3d44b-132">Weight</span></span></li>
</ul></td>
<td><span data-ttu-id="3d44b-133">Подуровень туннеля IPsec</span><span class="sxs-lookup"><span data-stu-id="3d44b-133">The IPsec Tunnel sub-layer</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d44b-134">Поставщик</span><span class="sxs-lookup"><span data-stu-id="3d44b-134">Provider</span></span></td>
<td><span data-ttu-id="3d44b-135">Поставщик политики, который создал решение для WFP.</span><span class="sxs-lookup"><span data-stu-id="3d44b-135">A policy provider that has built a solution on WFP.</span></span><br/> <span data-ttu-id="3d44b-136">Он используется исключительно для управления; Он не влияет на обработку пакетов во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="3d44b-136">It is used solely for management; it does not affect run-time packet processing.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="3d44b-137">ID</span><span class="sxs-lookup"><span data-stu-id="3d44b-137">ID</span></span></li>
<li><span data-ttu-id="3d44b-138">Имя службы</span><span class="sxs-lookup"><span data-stu-id="3d44b-138">Service name</span></span></li>
</ul></td>
<td><span data-ttu-id="3d44b-139">Брандмауэр Windows в режиме повышенной безопасности</span><span class="sxs-lookup"><span data-stu-id="3d44b-139">Windows Firewall with Advanced Security</span></span><br/> <span data-ttu-id="3d44b-140">Стороннее приложение фильтрации URL-адресов</span><span class="sxs-lookup"><span data-stu-id="3d44b-140">A 3rd-party URL filtering application</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d44b-141">Контекст поставщика</span><span class="sxs-lookup"><span data-stu-id="3d44b-141">Provider Context</span></span></td>
<td><span data-ttu-id="3d44b-142">Большой двоичный объект данных, используемый поставщиком политики для хранения произвольных контекстных данных.</span><span class="sxs-lookup"><span data-stu-id="3d44b-142">A data blob used by a policy provider to store arbitrary context information.</span></span> <br/> <span data-ttu-id="3d44b-143">Он используется для передачи пользовательской информации о конфигурации в выноску.</span><span class="sxs-lookup"><span data-stu-id="3d44b-143">It is used to pass custom configuration information to a callout.</span></span><br/> <span data-ttu-id="3d44b-144">Наиболее распространенным способом использования контекстных сведений является наличие фильтров, ссылающихся на контекст поставщика.</span><span class="sxs-lookup"><span data-stu-id="3d44b-144">The most common way to use the context information is to have filters reference a provider context.</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="3d44b-145">ID</span><span class="sxs-lookup"><span data-stu-id="3d44b-145">ID</span></span></li>
<li><span data-ttu-id="3d44b-146">Большой двоичный объект данных</span><span class="sxs-lookup"><span data-stu-id="3d44b-146">Data blob</span></span></li>
</ul></td>
<td><span data-ttu-id="3d44b-147">Протокол IPsec сохраняет параметры проверки подлинности в модуле базовой фильтрации (BFE).</span><span class="sxs-lookup"><span data-stu-id="3d44b-147">IPsec stores authentication settings in the Base Filtering Engine ( BFE).</span></span> <span data-ttu-id="3d44b-148">&quot;Свойство Context &quot; фильтра указывает параметры проверки подлинности, которые будет использовать для трафика, описанного фильтром.</span><span class="sxs-lookup"><span data-stu-id="3d44b-148">The &quot;Context&quot; property of a filter indicates the authentication settings to use for the traffic that the filter describes.</span></span><br/> <span data-ttu-id="3d44b-149">Оболочка выбора сертификации SSL будет хранить сведения о сертификации в контексте поставщика.</span><span class="sxs-lookup"><span data-stu-id="3d44b-149">The SSL certification selection shim will store certification information in a provider context.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3d44b-150">Типы объектов, предоставляемые API WFP, имеют одинаковую семантику.</span><span class="sxs-lookup"><span data-stu-id="3d44b-150">The object types exposed by WFP API have consistent semantics.</span></span> <span data-ttu-id="3d44b-151">Действия Add, Enumerate, Subscribe и т. д. аналогичны для всех типов объектов.</span><span class="sxs-lookup"><span data-stu-id="3d44b-151">The actions of add, enumerate, subscribe, and so on are similar for all object types.</span></span>

<span data-ttu-id="3d44b-152">Каждый тип объекта представлен структурой данных (например, [**фвпм \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)).</span><span class="sxs-lookup"><span data-stu-id="3d44b-152">Each object type is represented by a data structure (for example, [**FWPM\_FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)).</span></span> <span data-ttu-id="3d44b-153">Чтобы свести к сведению количество различных структур данных, предоставляемых API WFP, одна и та же структура данных используется для добавления новых объектов и получения существующих.</span><span class="sxs-lookup"><span data-stu-id="3d44b-153">In order to minimize the number of different data structures exposed by the WFP API, the same data structure is used for both adding new objects and retrieving existing ones.</span></span> <span data-ttu-id="3d44b-154">Таким словами, в каждой структуре данных могут содержаться поля, которые игнорируются при добавлении нового объекта, так как эти поля заполняются модулем базовой фильтрации (BFE), а не вызывающим.</span><span class="sxs-lookup"><span data-stu-id="3d44b-154">Thus, there may be fields in each data structure that are ignored when adding a new object since these fields are filled in by the Base Filtering Engine (BFE), and not by the caller.</span></span> <span data-ttu-id="3d44b-155">Например, структура данных **фвпм \_ FILTER0** имеет поле **филтерид** , содержащее **LUID** соответствующего **фвпс \_ FILTER0**.</span><span class="sxs-lookup"><span data-stu-id="3d44b-155">For example, an **FWPM\_FILTER0** data structure has a **filterId** field that contains the **LUID** of the corresponding **FWPS\_FILTER0**.</span></span> <span data-ttu-id="3d44b-156">Этот **LUID** назначается BFE, поэтому это поле не учитывается в вызове [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).</span><span class="sxs-lookup"><span data-stu-id="3d44b-156">This **LUID** is assigned by BFE, and thus, this field is ignored in the call to [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d44b-157">См. также</span><span class="sxs-lookup"><span data-stu-id="3d44b-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d44b-158">Управление объектами</span><span class="sxs-lookup"><span data-stu-id="3d44b-158">Object Management</span></span>](object-management.md)
</dt> </dl>

 

 





