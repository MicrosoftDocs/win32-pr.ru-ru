---
description: В API таблицы распределенной маршрутизации (DRT) используются следующие функции.
ms.assetid: 1ceff217-d410-47fa-99a2-8588f001859e
title: Функции таблиц распределенной маршрутизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd48c3a60f458285ce5f607f9ab6bcf7a557cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663351"
---
# <a name="distributed-routing-table-functions"></a><span data-ttu-id="3915f-103">Функции таблиц распределенной маршрутизации</span><span class="sxs-lookup"><span data-stu-id="3915f-103">Distributed Routing Table Functions</span></span>

<span data-ttu-id="3915f-104">В API таблицы распределенной маршрутизации (DRT) используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="3915f-104">The Distributed Routing Table (DRT) API utilizes the following functions.</span></span>

## <a name="lifetime-management-functions"></a><span data-ttu-id="3915f-105">Функции управления жизненным циклом</span><span class="sxs-lookup"><span data-stu-id="3915f-105">Lifetime Management Functions</span></span>



| <span data-ttu-id="3915f-106">Функция</span><span class="sxs-lookup"><span data-stu-id="3915f-106">Function</span></span>                                           | <span data-ttu-id="3915f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3915f-107">Description</span></span>                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3915f-108">**дртопен**</span><span class="sxs-lookup"><span data-stu-id="3915f-108">**DrtOpen**</span></span>](/windows/desktop/api/drt/nf-drt-drtopen)                         | <span data-ttu-id="3915f-109">Создает локальный экземпляр DRT с использованием критериев, заданных в структуре [**\_ параметров DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .</span><span class="sxs-lookup"><span data-stu-id="3915f-109">Creates a local DRT instance using criteria specified by the [**DRT\_SETTINGS**](/windows/desktop/api/drt/ns-drt-drt_settings) structure.</span></span>  |
| [<span data-ttu-id="3915f-110">**дртклосе**</span><span class="sxs-lookup"><span data-stu-id="3915f-110">**DrtClose**</span></span>](/windows/desktop/api/drt/nf-drt-drtclose)                       | <span data-ttu-id="3915f-111">Закрывает и удаляет локальный экземпляр DRT.</span><span class="sxs-lookup"><span data-stu-id="3915f-111">Closes and removes the local instance of the DRT.</span></span>                                                              |
| [<span data-ttu-id="3915f-112">**дртжетевентдата**</span><span class="sxs-lookup"><span data-stu-id="3915f-112">**DrtGetEventData**</span></span>](/windows/desktop/api/drt/nf-drt-drtgeteventdata)         | <span data-ttu-id="3915f-113">Извлекает данные события, связанные с сигнальным событием.</span><span class="sxs-lookup"><span data-stu-id="3915f-113">Retrieves event data associated with a signaled event.</span></span>                                                         |
| [<span data-ttu-id="3915f-114">**дртжетевентдатасизе**</span><span class="sxs-lookup"><span data-stu-id="3915f-114">**DrtGetEventDataSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgeteventdatasize) | <span data-ttu-id="3915f-115">Возвращает размер структуры [**\_ \_ данных события DRT**](/windows/desktop/api/drt/ns-drt-drt_event_data) , связанной с сигнальным событием.</span><span class="sxs-lookup"><span data-stu-id="3915f-115">Returns the size of the [**DRT\_EVENT\_DATA**](/windows/desktop/api/drt/ns-drt-drt_event_data) structure associated with a signaled event.</span></span> |



 

## <a name="module-management-functions"></a><span data-ttu-id="3915f-116">Функции управления модулями</span><span class="sxs-lookup"><span data-stu-id="3915f-116">Module Management Functions</span></span>



| <span data-ttu-id="3915f-117">Функция</span><span class="sxs-lookup"><span data-stu-id="3915f-117">Function</span></span>                                                                           | <span data-ttu-id="3915f-118">Описание</span><span class="sxs-lookup"><span data-stu-id="3915f-118">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3915f-119">**дрткреатепнрпбутстрапресолвер**</span><span class="sxs-lookup"><span data-stu-id="3915f-119">**DrtCreatePnrpBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver)           | <span data-ttu-id="3915f-120">Создает сопоставитель начальной загрузки на основе протокола PNRP.</span><span class="sxs-lookup"><span data-stu-id="3915f-120">Creates a bootstrap resolver based on the PNRP protocol.</span></span>                                                                              |
| [<span data-ttu-id="3915f-121">**дртделетепнрпбутстрапресолвер**</span><span class="sxs-lookup"><span data-stu-id="3915f-121">**DrtDeletePnrpBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletepnrpbootstrapresolver)           | <span data-ttu-id="3915f-122">Удаляет сопоставитель загрузчика на основе протокола PNRP.</span><span class="sxs-lookup"><span data-stu-id="3915f-122">Deletes a bootstrap resolver based on the PNRP protocol.</span></span>                                                                              |
| [<span data-ttu-id="3915f-123">**дрткреатеднсбутстрапресолвер**</span><span class="sxs-lookup"><span data-stu-id="3915f-123">**DrtCreateDnsBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatednsbootstrapresolver)             | <span data-ttu-id="3915f-124">Создает поставщик начальной загрузки, который будет обращаться к хорошо известному узлу по имени.</span><span class="sxs-lookup"><span data-stu-id="3915f-124">Creates a bootstrap provider that will contact a well known host by name.</span></span>                                                             |
| [<span data-ttu-id="3915f-125">**дртделетеднсбутстрапресолвер**</span><span class="sxs-lookup"><span data-stu-id="3915f-125">**DrtDeleteDnsBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletednsbootstrapresolver)             | <span data-ttu-id="3915f-126">Удаляет поставщик начальной загрузки, который свяжется с известным узлом по имени.</span><span class="sxs-lookup"><span data-stu-id="3915f-126">Deletes a bootstrap provider that will contact a well known host by name.</span></span>                                                             |
| [<span data-ttu-id="3915f-127">**DrtCreateIpv6UdpTransport**</span><span class="sxs-lookup"><span data-stu-id="3915f-127">**DrtCreateIpv6UdpTransport**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)                     | <span data-ttu-id="3915f-128">Создает транспорт на основе протокола IPv6 UDP.</span><span class="sxs-lookup"><span data-stu-id="3915f-128">Creates a transport based on the IPv6 UDP protocol.</span></span>                                                                                   |
| [<span data-ttu-id="3915f-129">**DrtDeleteIpv6UdpTransport**</span><span class="sxs-lookup"><span data-stu-id="3915f-129">**DrtDeleteIpv6UdpTransport**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeleteipv6udptransport)                     | <span data-ttu-id="3915f-130">Удаляет транспорт на основе протокола IPv6 UDP.</span><span class="sxs-lookup"><span data-stu-id="3915f-130">Deletes a transport based on the IPv6 UDP protocol.</span></span>                                                                                   |
| [<span data-ttu-id="3915f-131">**дрткреатедериведкэйсекуритипровидер**</span><span class="sxs-lookup"><span data-stu-id="3915f-131">**DrtCreateDerivedKeySecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) | <span data-ttu-id="3915f-132">Создает поставщик безопасности производного ключа для DRT.</span><span class="sxs-lookup"><span data-stu-id="3915f-132">Creates a derived key security provider for the DRT.</span></span>                                                                                  |
| [<span data-ttu-id="3915f-133">**дрткреатедериведкэй**</span><span class="sxs-lookup"><span data-stu-id="3915f-133">**DrtCreateDerivedKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatederivedkey)                                 | <span data-ttu-id="3915f-134">Создает ключ, который можно использовать с помощью [**дртрегистеркэй**](/windows/desktop/api/drt/nf-drt-drtregisterkey) , когда DRT использует поставщик безопасности производного ключа.</span><span class="sxs-lookup"><span data-stu-id="3915f-134">Creates a key that can be utilized by [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) when the DRT is using a derived key security provider.</span></span> |
| [<span data-ttu-id="3915f-135">**дртделетедериведкэйсекуритипровидер**</span><span class="sxs-lookup"><span data-stu-id="3915f-135">**DrtDeleteDerivedKeySecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider) | <span data-ttu-id="3915f-136">Удаляет производный поставщик безопасности ключа для DRT.</span><span class="sxs-lookup"><span data-stu-id="3915f-136">Deletes a derived key security provider for the DRT.</span></span>                                                                                  |
| [<span data-ttu-id="3915f-137">**дрткреатенуллсекуритипровидер**</span><span class="sxs-lookup"><span data-stu-id="3915f-137">**DrtCreateNullSecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider)             | <span data-ttu-id="3915f-138">Создает поставщик безопасности со значением NULL.</span><span class="sxs-lookup"><span data-stu-id="3915f-138">Creates a null security provider.</span></span> <span data-ttu-id="3915f-139">Этому поставщику безопасности не требуются узлы для проверки подлинности ключей.</span><span class="sxs-lookup"><span data-stu-id="3915f-139">This security provider does not require nodes to authenticate keys.</span></span>                                 |
| [<span data-ttu-id="3915f-140">**дртделетенуллсекуритипровидер**</span><span class="sxs-lookup"><span data-stu-id="3915f-140">**DrtDeleteNullSecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletenullsecurityprovider)             | <span data-ttu-id="3915f-141">Удаляет поставщик безопасности со значением NULL.</span><span class="sxs-lookup"><span data-stu-id="3915f-141">Deletes a null security provider.</span></span>                                                                                                     |



 

## <a name="registration-functions"></a><span data-ttu-id="3915f-142">Функции регистрации</span><span class="sxs-lookup"><span data-stu-id="3915f-142">Registration Functions</span></span>



| <span data-ttu-id="3915f-143">Функция</span><span class="sxs-lookup"><span data-stu-id="3915f-143">Function</span></span>                                     | <span data-ttu-id="3915f-144">Описание</span><span class="sxs-lookup"><span data-stu-id="3915f-144">Description</span></span>                                                    |
|----------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="3915f-145">**дртрегистеркэй**</span><span class="sxs-lookup"><span data-stu-id="3915f-145">**DrtRegisterKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtregisterkey)     | <span data-ttu-id="3915f-146">Регистрирует ключ в DRT.</span><span class="sxs-lookup"><span data-stu-id="3915f-146">Registers a key in the DRT.</span></span>                                    |
| [<span data-ttu-id="3915f-147">**дртупдатекэй**</span><span class="sxs-lookup"><span data-stu-id="3915f-147">**DrtUpdateKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtupdatekey)         | <span data-ttu-id="3915f-148">Обновляет данные приложения, связанные с зарегистрированным ключом.</span><span class="sxs-lookup"><span data-stu-id="3915f-148">Updates the application data associated with a registered key.</span></span> |
| [<span data-ttu-id="3915f-149">**дртунрегистеркэй**</span><span class="sxs-lookup"><span data-stu-id="3915f-149">**DrtUnregisterKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtunregisterkey) | <span data-ttu-id="3915f-150">Отменяет регистрацию ключа в DRT.</span><span class="sxs-lookup"><span data-stu-id="3915f-150">Deregisters a key from the DRT.</span></span>                                |



 

## <a name="search-functions"></a><span data-ttu-id="3915f-151">Функции поиска</span><span class="sxs-lookup"><span data-stu-id="3915f-151">Search Functions</span></span>



| <span data-ttu-id="3915f-152">Функция</span><span class="sxs-lookup"><span data-stu-id="3915f-152">Function</span></span>                                                 | <span data-ttu-id="3915f-153">Описание</span><span class="sxs-lookup"><span data-stu-id="3915f-153">Description</span></span>                                                                                                                                                                                                             |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3915f-154">**дртстартсеарч**</span><span class="sxs-lookup"><span data-stu-id="3915f-154">**DrtStartSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtstartsearch)                 | <span data-ttu-id="3915f-155">Выполняет поиск ключа в DRT, используя критерии, указанные в [**структуре \_ \_ сведений о поиске DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) .</span><span class="sxs-lookup"><span data-stu-id="3915f-155">Searches the DRT for a key using criteria specified in the [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) structure.</span></span>                                                                                                      |
| [<span data-ttu-id="3915f-156">**дртконтинуесеарч**</span><span class="sxs-lookup"><span data-stu-id="3915f-156">**DrtContinueSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtcontinuesearch)           | <span data-ttu-id="3915f-157">Возобновляет поиск \_ \_ по пути поиска DRT \_ для ключа в DRT.</span><span class="sxs-lookup"><span data-stu-id="3915f-157">Continues a DRT\_SEARCH\_RETURN\_PATH search for a key in the DRT.</span></span> <span data-ttu-id="3915f-158">Эта функция используется только в том случае, если флаг **фитеративе** имеет значение **true** в связанной [**структуре \_ \_ сведений о поиске DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) .</span><span class="sxs-lookup"><span data-stu-id="3915f-158">This function is used only when the **fIterative** flag is set to **TRUE** in the associated [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) structure.</span></span> |
| [<span data-ttu-id="3915f-159">**дртжетсеарчресулт**</span><span class="sxs-lookup"><span data-stu-id="3915f-159">**DrtGetSearchResult**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)         | <span data-ttu-id="3915f-160">Извлекает результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="3915f-160">Retrieves the search result(s).</span></span>                                                                                                                                                                                         |
| [<span data-ttu-id="3915f-161">**дртжетсеарчресултсизе**</span><span class="sxs-lookup"><span data-stu-id="3915f-161">**DrtGetSearchResultSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchresultsize) | <span data-ttu-id="3915f-162">Возвращает размер следующего доступного результата поиска.</span><span class="sxs-lookup"><span data-stu-id="3915f-162">Returns the size of the next available search result.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="3915f-163">**дртжетсеарчпас**</span><span class="sxs-lookup"><span data-stu-id="3915f-163">**DrtGetSearchPath**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchpath)             | <span data-ttu-id="3915f-164">Возвращает список узлов, которые были обращены во время операции поиска.</span><span class="sxs-lookup"><span data-stu-id="3915f-164">Returns a list of nodes contacted during the search operation.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="3915f-165">**дртжетсеарчпассизе**</span><span class="sxs-lookup"><span data-stu-id="3915f-165">**DrtGetSearchPathSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize)     | <span data-ttu-id="3915f-166">Возвращает размер пути поиска, который представляет количество узлов, используемых в операции поиска.</span><span class="sxs-lookup"><span data-stu-id="3915f-166">Returns the size of the search path, which represents the number of nodes utilized in the search operation.</span></span>                                                                                                             |
| [<span data-ttu-id="3915f-167">**дртендсеарч**</span><span class="sxs-lookup"><span data-stu-id="3915f-167">**DrtEndSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtendsearch)                     | <span data-ttu-id="3915f-168">Отменяет Поиск ключа в DRT, в результате чего возвращение результатов с помощью [**\_ \_ результатов поиска DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) останавливается.</span><span class="sxs-lookup"><span data-stu-id="3915f-168">Cancels a search for a key in a DRT, and as a result, the return of results via [**DRT\_SEARCH\_RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) is stopped.</span></span> <span data-ttu-id="3915f-169">Этот API можно вызвать в любой точке после выполнения поиска.</span><span class="sxs-lookup"><span data-stu-id="3915f-169">This API can be called at any point after a search is issued.</span></span>              |



 

## <a name="instance-name-functions"></a><span data-ttu-id="3915f-170">Функции имени экземпляра</span><span class="sxs-lookup"><span data-stu-id="3915f-170">Instance Name Functions</span></span>



| <span data-ttu-id="3915f-171">Функция</span><span class="sxs-lookup"><span data-stu-id="3915f-171">Function</span></span>                                                 | <span data-ttu-id="3915f-172">Описание</span><span class="sxs-lookup"><span data-stu-id="3915f-172">Description</span></span>                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="3915f-173">**дртжетинстанценаме**</span><span class="sxs-lookup"><span data-stu-id="3915f-173">**DrtGetInstanceName**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetinstancename)         | <span data-ttu-id="3915f-174">Возвращает имя, связанное с экземпляром DRT.</span><span class="sxs-lookup"><span data-stu-id="3915f-174">Gets the name associated with a DRT instance.</span></span>                    |
| [<span data-ttu-id="3915f-175">**дртжетинстанценамесизе**</span><span class="sxs-lookup"><span data-stu-id="3915f-175">**DrtGetInstanceNameSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetinstancenamesize) | <span data-ttu-id="3915f-176">Возвращает размер имени экземпляра таблицы распределенной маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="3915f-176">Returns the size of the Distributed Routing Table instance name.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3915f-177">См. также</span><span class="sxs-lookup"><span data-stu-id="3915f-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3915f-178">Перечисление таблиц распределенной маршрутизации</span><span class="sxs-lookup"><span data-stu-id="3915f-178">Distributed Routing Table Enumerations</span></span>](distributed-routing-table-enumerations.md)
</dt> <dt>

[<span data-ttu-id="3915f-179">Структуры таблиц распределенной маршрутизации</span><span class="sxs-lookup"><span data-stu-id="3915f-179">Distributed Routing Table Structures</span></span>](distributed-routing-table-structures.md)
</dt> <dt>

[<span data-ttu-id="3915f-180">Справочник по распределенной маршрутизации API таблиц</span><span class="sxs-lookup"><span data-stu-id="3915f-180">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



