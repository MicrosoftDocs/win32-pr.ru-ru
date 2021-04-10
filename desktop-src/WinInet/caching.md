---
title: Кэширование (Windows Internet)
description: Функции WinINet имеют простую, но гибкую встроенную поддержку кэширования.
ms.assetid: 44c268c9-a745-432a-8540-60d7e7d2cb2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e753d826ec3abe580b94158296562208dcbed44
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134914"
---
# <a name="caching-windows-internet"></a><span data-ttu-id="46e6d-103">Кэширование (Windows Internet)</span><span class="sxs-lookup"><span data-stu-id="46e6d-103">Caching (Windows Internet)</span></span>

<span data-ttu-id="46e6d-104">Функции WinINet имеют простую, но гибкую встроенную поддержку кэширования.</span><span class="sxs-lookup"><span data-stu-id="46e6d-104">The WinINet functions have simple, yet flexible, built-in caching support.</span></span> <span data-ttu-id="46e6d-105">Все данные, полученные из сети, кэшируются на жестком диске и извлекаются для последующих запросов.</span><span class="sxs-lookup"><span data-stu-id="46e6d-105">Any data retrieved from the network is cached on the hard disk and retrieved for subsequent requests.</span></span> <span data-ttu-id="46e6d-106">Приложение может управлять кэшированием каждого запроса.</span><span class="sxs-lookup"><span data-stu-id="46e6d-106">The application can control the caching on each request.</span></span> <span data-ttu-id="46e6d-107">Для HTTP-запросов с сервера большинство полученных заголовков также кэшируются.</span><span class="sxs-lookup"><span data-stu-id="46e6d-107">For http requests from the server, most headers received are also cached.</span></span> <span data-ttu-id="46e6d-108">Когда HTTP-запрос выполняется из кэша, кэшированные заголовки также возвращаются вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="46e6d-108">When an http request is satisfied from the cache, the cached headers are also returned to the caller.</span></span> <span data-ttu-id="46e6d-109">Это позволяет легко загружать данные независимо от того, поступают ли они из кэша или из сети.</span><span class="sxs-lookup"><span data-stu-id="46e6d-109">This makes data download seamless, whether the data is coming from the cache or from the network.</span></span>

<span data-ttu-id="46e6d-110">Приложения должны правильно выделить буфер для получения нужных результатов при использовании постоянных функций кэширования URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="46e6d-110">Applications must properly allocate a buffer in order to get the desired results when using the persistent URL caching functions.</span></span> <span data-ttu-id="46e6d-111">Дополнительные сведения см. [в разделе использование буферов](appendix-b-using-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="46e6d-111">For more information, see [Using Buffers](appendix-b-using-buffers.md).</span></span>

## <a name="cache-behavior-during-response-processing"></a><span data-ttu-id="46e6d-112">Поведение кэша во время обработки ответа</span><span class="sxs-lookup"><span data-stu-id="46e6d-112">Cache Behavior During Response Processing</span></span>

<span data-ttu-id="46e6d-113">Кэш WinINet совместим с директивами управления кэшем HTTP, описанными в RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="46e6d-113">The WinINet cache is compliant with the HTTP cache-control directives described in RFC 2616.</span></span> <span data-ttu-id="46e6d-114">Директивы управления кэшем и флаги набора приложений определяют, что может быть кэшировано; Однако WinINet определяет, что на самом деле кэшируется на основе следующего критерия:</span><span class="sxs-lookup"><span data-stu-id="46e6d-114">The cache-control directives and application set flags determine what may be cached; however, WinINet determines what is actually cached based on the following criterion:</span></span>

-   <span data-ttu-id="46e6d-115">WinINet кэширует только ответы HTTP и FTP.</span><span class="sxs-lookup"><span data-stu-id="46e6d-115">WinINet only caches HTTP and FTP responses.</span></span>
-   <span data-ttu-id="46e6d-116">Только хорошо обрабатываемые ответы могут храниться в кэше и использоваться в ответ на последующий запрос.</span><span class="sxs-lookup"><span data-stu-id="46e6d-116">Only well behaved responses may be stored by a cache and used in a reply to a subsequent Request.</span></span> <span data-ttu-id="46e6d-117">Правильно настроенные ответы определяются как ответы, которые успешно возвращают данные.</span><span class="sxs-lookup"><span data-stu-id="46e6d-117">Well behaved responses are defined as responses that return successfully.</span></span>
-   <span data-ttu-id="46e6d-118">По умолчанию WinINet кэширует успешные ответы, если только директива Cache-Control не используется с сервера, или определенный приложением флаг, не Заказывающий, что ответ может не кэшироваться.</span><span class="sxs-lookup"><span data-stu-id="46e6d-118">By default, WinINet will cache successful responses unless either a cache-control directive from the server, or an application-defined flag specifically denote that the response may not be cached.</span></span>
-   <span data-ttu-id="46e6d-119">Как правило, ответы на команду GET кэшируются, если выполняются указанные выше требования.</span><span class="sxs-lookup"><span data-stu-id="46e6d-119">In general, responses to the GET verb are cached if the requirements listed above are met.</span></span> <span data-ttu-id="46e6d-120">Ответы на команды размещения и POST не кэшируются при каких обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="46e6d-120">Responses to PUT and POST verbs are not cached under any circumstances.</span></span>
-   <span data-ttu-id="46e6d-121">Элементы будут кэшироваться даже при заполнении кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-121">Items will be cached even when the cache is full.</span></span> <span data-ttu-id="46e6d-122">Если добавленный элемент помещает кэш на предельный размер, то запланирована очистка кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-122">If an added item is puts the cache over the size limit, the cache scavenger is scheduled.</span></span> <span data-ttu-id="46e6d-123">По умолчанию в кэше не гарантируется, что элементы остаются более чем 10 минут.</span><span class="sxs-lookup"><span data-stu-id="46e6d-123">By default, items are not guaranteed to remain more than 10 minutes in the cache.</span></span> <span data-ttu-id="46e6d-124">Дополнительные сведения см. в разделе [Очистка кэша](#cache-scavenger) ниже.</span><span class="sxs-lookup"><span data-stu-id="46e6d-124">For more information, see the [Cache Scavenger](#cache-scavenger) section below.</span></span>
-   <span data-ttu-id="46e6d-125">По умолчанию протокол HTTPS кэшируется.</span><span class="sxs-lookup"><span data-stu-id="46e6d-125">Https is cached by default.</span></span> <span data-ttu-id="46e6d-126">Это управляется глобальным параметром, который не может быть переопределен директивами кэша, определяемыми приложением.</span><span class="sxs-lookup"><span data-stu-id="46e6d-126">This is managed by a global setting that cannot be overridden by application-defined cache directives.</span></span> <span data-ttu-id="46e6d-127">Чтобы переопределить глобальный параметр, выберите приложение "Свойства обозревателя" на панели управления и перейдите на вкладку "Дополнительно". Установите флажок "не сохранять зашифрованные страницы на диск" в разделе "безопасность".</span><span class="sxs-lookup"><span data-stu-id="46e6d-127">To override the global setting, select the Internet Options applet in the control panel, and go to the advanced tab. Check the "Do not save encrypted pages to disk" box under the "Security" section.</span></span>

## <a name="cache-scavenger"></a><span data-ttu-id="46e6d-128">Очистка кэша</span><span class="sxs-lookup"><span data-stu-id="46e6d-128">Cache Scavenger</span></span>

<span data-ttu-id="46e6d-129">Очистка кэша периодически удаляет элементы из кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-129">The cache scavenger periodically cleans items from the cache.</span></span> <span data-ttu-id="46e6d-130">Если элемент добавляется в кэш, а кэш полон, элемент добавляется в кэш и планируется очистка кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-130">If an item is added to the cache and the cache is full, the item is added to the cache and the cache scavenger is scheduled.</span></span> <span data-ttu-id="46e6d-131">Если очистка кэша завершает очистку, а кэш не достигает предела кэша, то для очистки планируется еще один цикл, когда в кэш добавляется другой элемент.</span><span class="sxs-lookup"><span data-stu-id="46e6d-131">If the cache scavenger completes a round of scavenging and the cache has not reached the cache limit, the scavenger is scheduled for another round when another item is added to the cache.</span></span> <span data-ttu-id="46e6d-132">Как правило, очистка планируется, когда добавленный элемент помещает кэш на предельный размер.</span><span class="sxs-lookup"><span data-stu-id="46e6d-132">In general, the scavenger is scheduled when an added item puts the cache over its size limit.</span></span> <span data-ttu-id="46e6d-133">По умолчанию минимальное время жизни в кэше составляет 10 минут, если иное не указано в директиве Cache-Control.</span><span class="sxs-lookup"><span data-stu-id="46e6d-133">By default, the minimum time to live in the cache is set to 10 minutes unless otherwise specified in a cache-control directive.</span></span> <span data-ttu-id="46e6d-134">При инициации очистки кэша не гарантируется, что самые старые элементы первыми будут удалены из кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-134">When the cache scavenger is initiated, there is no guarantee that the oldest items are the first to be deleted from the cache.</span></span>

<span data-ttu-id="46e6d-135">Кэш является общим для всех приложений WinINet на компьютере для одного и того же пользователя.</span><span class="sxs-lookup"><span data-stu-id="46e6d-135">The cache is shared across all WinINet applications on the computer for the same user.</span></span> <span data-ttu-id="46e6d-136">Начиная с Windows Vista и Windows Server 2008 размер кэша задается равным 1 или 32-го размер диска, минимальный размер 8 МБ и максимальный размер 50 МБ.</span><span class="sxs-lookup"><span data-stu-id="46e6d-136">Starting with Windows Vista and Windows Server 2008 the cache size is set to 1/32nd the size of the disk, with a minimum size of 8MB and a maximum size of 50MB.</span></span>

## <a name="using-flags-to-control-caching"></a><span data-ttu-id="46e6d-137">Использование флагов для управления кэшированием</span><span class="sxs-lookup"><span data-stu-id="46e6d-137">Using Flags to Control Caching</span></span>

<span data-ttu-id="46e6d-138">Флаги кэширования позволяют приложению управлять тем, когда и как оно использует кэш.</span><span class="sxs-lookup"><span data-stu-id="46e6d-138">The caching flags allow an application to control when and how it uses the cache.</span></span> <span data-ttu-id="46e6d-139">Эти флаги можно использовать отдельно или в сочетании с параметром *dwFlags* в функциях, обращающихся к информации или ресурсам в Интернете.</span><span class="sxs-lookup"><span data-stu-id="46e6d-139">These flags can be used alone or in combination with the *dwFlags* parameter in functions that access information or resources on the Internet.</span></span> <span data-ttu-id="46e6d-140">По умолчанию функции хранят все данные, загруженные из Интернета.</span><span class="sxs-lookup"><span data-stu-id="46e6d-140">By default, the functions store all data downloaded from the Internet.</span></span>

<span data-ttu-id="46e6d-141">Для управления кэшированием можно использовать следующие флаги.</span><span class="sxs-lookup"><span data-stu-id="46e6d-141">The following flags can be used to control caching.</span></span>



| <span data-ttu-id="46e6d-142">Значение</span><span class="sxs-lookup"><span data-stu-id="46e6d-142">Value</span></span>                                                                                                                                                  | <span data-ttu-id="46e6d-143">Значение</span><span class="sxs-lookup"><span data-stu-id="46e6d-143">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46e6d-144">**\_кэш флагов Интернета \_ \_ Async**</span><span class="sxs-lookup"><span data-stu-id="46e6d-144">**INTERNET\_FLAG\_CACHE\_ASYNC**</span></span>](api-flags.md)                                                                            | <span data-ttu-id="46e6d-145">Этот флаг ни на что не влияет.</span><span class="sxs-lookup"><span data-stu-id="46e6d-145">This flag has no effect.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="46e6d-146">**\_кэш флагов Интернета в \_ \_ случае \_ \_ сбоя NET**</span><span class="sxs-lookup"><span data-stu-id="46e6d-146">**INTERNET\_FLAG\_CACHE\_IF\_NET\_FAIL**</span></span>](api-flags.md)                                                              | <span data-ttu-id="46e6d-147">Возвращает ресурс из кэша в случае сбоя сетевого запроса ресурса из-за [ошибки \_ \_ \_ сброса подключения к Интернету](wininet-errors.md) или [ошибки подключения \_ \_ \_ к Интернету](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="46e6d-147">Returns the resource from the cache if the network request for the resource fails due to an [ERROR\_INTERNET\_CONNECTION\_RESET](wininet-errors.md) or [ERROR\_INTERNET\_CANNOT\_CONNECT](wininet-errors.md) error.</span></span> <span data-ttu-id="46e6d-148">Этот флаг используется [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="46e6d-148">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                                                                              |
| [<span data-ttu-id="46e6d-149">**\_ \_ кэш не Internet \_ Flag**</span><span class="sxs-lookup"><span data-stu-id="46e6d-149">**INTERNET\_FLAG\_DONT\_CACHE**</span></span>](api-flags.md)                                                                              | <span data-ttu-id="46e6d-150">Не кэширует данные локально или в любых шлюзах.</span><span class="sxs-lookup"><span data-stu-id="46e6d-150">Does not cache the data, either locally or in any gateways.</span></span> <span data-ttu-id="46e6d-151">Аналогично предпочтительному значению [**, \_ флаг Интернета \_ без \_ кэширования \_ записи**](api-flags.md).</span><span class="sxs-lookup"><span data-stu-id="46e6d-151">Identical to the preferred value, [**INTERNET\_FLAG\_NO\_CACHE\_WRITE**](api-flags.md).</span></span>                                                                                                                                                                                                                                                                                 |
|                                                                                                                                                        | <span data-ttu-id="46e6d-152">Указывает, что это отправка форм.</span><span class="sxs-lookup"><span data-stu-id="46e6d-152">Indicates that this is a Forms submission.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="46e6d-153">[**Интернет \_ Отправка флагов \_ из \_ кэша**](api-flags.md)[**\_ формы флагов Интернета \_ \_ Отправить**](api-flags.md)</span><span class="sxs-lookup"><span data-stu-id="46e6d-153">[**INTERNET\_FLAG\_FROM\_CACHE**](api-flags.md)[**INTERNET\_FLAG\_FORMS\_SUBMIT**](api-flags.md)</span></span> | <span data-ttu-id="46e6d-154">Не выполняет сетевые запросы.</span><span class="sxs-lookup"><span data-stu-id="46e6d-154">Does not make network requests.</span></span> <span data-ttu-id="46e6d-155">Все сущности возвращаются из кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-155">All entities are returned from the cache.</span></span> <span data-ttu-id="46e6d-156">Если запрошенный элемент отсутствует в кэше, возвращается подходящая ошибка, например \_ файл ошибок \_ не \_ найден.</span><span class="sxs-lookup"><span data-stu-id="46e6d-156">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="46e6d-157">Этот флаг используется только в функции [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) .</span><span class="sxs-lookup"><span data-stu-id="46e6d-157">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>                                                                                                                                                                                                       |
| [<span data-ttu-id="46e6d-158">**\_флаг Интернета \_ ФВД \_ назад**</span><span class="sxs-lookup"><span data-stu-id="46e6d-158">**INTERNET\_FLAG\_FWD\_BACK**</span></span>](api-flags.md)                                                                                  | <span data-ttu-id="46e6d-159">Указывает, что функция должна использовать копию ресурса, который в данный момент находится в кэше Интернета.</span><span class="sxs-lookup"><span data-stu-id="46e6d-159">Indicates that the function should use the copy of the resource that is currently in the Internet cache.</span></span> <span data-ttu-id="46e6d-160">Дата окончания срока действия и другие сведения о ресурсе не проверяются.</span><span class="sxs-lookup"><span data-stu-id="46e6d-160">The expiration date and other information about the resource is not checked.</span></span> <span data-ttu-id="46e6d-161">Если запрошенный элемент не найден в кэше Интернета, система пытается найти ресурс в сети.</span><span class="sxs-lookup"><span data-stu-id="46e6d-161">If the requested item is not found in the Internet cache, the system attempts to locate the resource on the network.</span></span> <span data-ttu-id="46e6d-162">Это значение было представлено в Microsoft Internet Explorer 5 и связано с операциями « **вперед** » и « **назад** » обозревателя Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="46e6d-162">This value was introduced in Microsoft Internet Explorer 5 and is associated with the **Forward** and **Back** button operations of Internet Explorer.</span></span> |
| [<span data-ttu-id="46e6d-163">**\_Гиперссылка для Internet Flag \_**</span><span class="sxs-lookup"><span data-stu-id="46e6d-163">**INTERNET\_FLAG\_HYPERLINK**</span></span>](api-flags.md)                                                                                 | <span data-ttu-id="46e6d-164">Заставляет приложение перезагружать ресурс, если срок действия не истек и время последнего изменения не возвращалось, когда ресурс был сохранен в кэше.</span><span class="sxs-lookup"><span data-stu-id="46e6d-164">Forces the application to reload a resource if no expire time and no last-modified time were returned when the resource was stored in the cache.</span></span>                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="46e6d-165">**\_флаг Интернета \_ сделать \_ постоянным**</span><span class="sxs-lookup"><span data-stu-id="46e6d-165">**INTERNET\_FLAG\_MAKE\_PERSISTENT**</span></span>](api-flags.md)                                                                    | <span data-ttu-id="46e6d-166">Больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="46e6d-166">No longer supported.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="46e6d-167">**\_флаг Интернета \_ должен \_ кэшировать \_ запрос**</span><span class="sxs-lookup"><span data-stu-id="46e6d-167">**INTERNET\_FLAG\_MUST\_CACHE\_REQUEST**</span></span>](api-flags.md)                                                             | <span data-ttu-id="46e6d-168">Вызывает создание временного файла, если файл не может быть кэширован.</span><span class="sxs-lookup"><span data-stu-id="46e6d-168">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="46e6d-169">Это аналогично предпочтительному значению, параметру [**Internet \_ Flag \_ требуется \_ файл**](api-flags.md).</span><span class="sxs-lookup"><span data-stu-id="46e6d-169">This is identical to the preferred value, [**INTERNET\_FLAG\_NEED\_FILE**](api-flags.md).</span></span>                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="46e6d-170">**для \_ флага Интернета \_ требуется \_ файл**</span><span class="sxs-lookup"><span data-stu-id="46e6d-170">**INTERNET\_FLAG\_NEED\_FILE**</span></span>](api-flags.md)                                                                                | <span data-ttu-id="46e6d-171">Вызывает создание временного файла, если файл не может быть кэширован.</span><span class="sxs-lookup"><span data-stu-id="46e6d-171">Causes a temporary file to be created if the file cannot be cached.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="46e6d-172">**\_флаг Интернета \_ без \_ записи в кэш \_**</span><span class="sxs-lookup"><span data-stu-id="46e6d-172">**INTERNET\_FLAG\_NO\_CACHE\_WRITE**</span></span>](api-flags.md)                                                                     | <span data-ttu-id="46e6d-173">Отклоняет все попытки функции для хранения данных, загруженных из Интернета в кэш.</span><span class="sxs-lookup"><span data-stu-id="46e6d-173">Rejects any attempt by the function to store data downloaded from the Internet in the cache.</span></span> <span data-ttu-id="46e6d-174">Этот флаг необходим, если приложению не требуется хранить загруженные ресурсы локально.</span><span class="sxs-lookup"><span data-stu-id="46e6d-174">This flag is necessary if the application does not want any downloaded resources to be stored locally.</span></span>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="46e6d-175">**\_флаг Интернета \_ нет \_ пользовательского интерфейса**</span><span class="sxs-lookup"><span data-stu-id="46e6d-175">**INTERNET\_FLAG\_NO\_UI**</span></span>](api-flags.md)                                                                                        | <span data-ttu-id="46e6d-176">Отключает диалоговое окно "файл cookie".</span><span class="sxs-lookup"><span data-stu-id="46e6d-176">Disables the cookie dialog box.</span></span> <span data-ttu-id="46e6d-177">Этот флаг может использоваться [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (только HTTP-запросы).</span><span class="sxs-lookup"><span data-stu-id="46e6d-177">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (HTTP requests only).</span></span>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="46e6d-178">**\_отключить флаг \_ Интернета**</span><span class="sxs-lookup"><span data-stu-id="46e6d-178">**INTERNET\_FLAG\_OFFLINE**</span></span>](api-flags.md)                                                                                     | <span data-ttu-id="46e6d-179">Предотвращает отправку запросов в сеть приложением.</span><span class="sxs-lookup"><span data-stu-id="46e6d-179">Prevents the application from sending requests to the network.</span></span> <span data-ttu-id="46e6d-180">Все запросы разрешаются с помощью ресурсов, хранящихся в кэше.</span><span class="sxs-lookup"><span data-stu-id="46e6d-180">All requests are resolved using the resources stored in the cache.</span></span> <span data-ttu-id="46e6d-181">Если ресурс отсутствует в кэше, возвращается подходящая ошибка, например \_ файл ошибок \_ не \_ найден.</span><span class="sxs-lookup"><span data-stu-id="46e6d-181">If the resource is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span>                                                                                                                                                                                                                            |
| [<span data-ttu-id="46e6d-182">**параметр INTERNET \_ Flag \_ pragma \ \_ Cache**</span><span class="sxs-lookup"><span data-stu-id="46e6d-182">**INTERNET\_FLAG\_PRAGMA\_NOCACHE**</span></span>](api-flags.md)                                                                      | <span data-ttu-id="46e6d-183">Вызывает принудительное разрешение запроса сервером-источником, даже если кэшированная копия существует на прокси-сервере.</span><span class="sxs-lookup"><span data-stu-id="46e6d-183">Forces the request to be resolved by the origin server, even if a cached copy exists on the proxy.</span></span> <span data-ttu-id="46e6d-184">Функция [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (только для запросов HTTP и HTTPS) и функция [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) используют этот флаг.</span><span class="sxs-lookup"><span data-stu-id="46e6d-184">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function (on HTTP and HTTPS requests only) and [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function use this flag.</span></span>                                                                                                                                                                                               |
| [<span data-ttu-id="46e6d-185">**\_Перезагрузка флага Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="46e6d-185">**INTERNET\_FLAG\_RELOAD**</span></span>](api-flags.md)                                                                                       | <span data-ttu-id="46e6d-186">Заставляет функцию получить запрошенный ресурс непосредственно из Интернета.</span><span class="sxs-lookup"><span data-stu-id="46e6d-186">Forces the function to retrieve the requested resource directly from the Internet.</span></span> <span data-ttu-id="46e6d-187">Загружаемые сведения хранятся в кэше.</span><span class="sxs-lookup"><span data-stu-id="46e6d-187">The information that is downloaded is stored in the cache.</span></span>                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="46e6d-188">**\_ \_ Повторная синхронизация ФЛАГа Интернета**</span><span class="sxs-lookup"><span data-stu-id="46e6d-188">**INTERNET\_FLAG\_RESYNCHRONIZE**</span></span>](api-flags.md)                                                                         | <span data-ttu-id="46e6d-189">Заставляет приложение выполнять условную загрузку ресурса из Интернета.</span><span class="sxs-lookup"><span data-stu-id="46e6d-189">Causes an application to perform a conditional download of the resource from the Internet.</span></span> <span data-ttu-id="46e6d-190">Если версия, хранящаяся в кэше, является актуальной, сведения загружаются из кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-190">If the version stored in the cache is current, the information is downloaded from the cache.</span></span> <span data-ttu-id="46e6d-191">В противном случае сведения перегружаются с сервера.</span><span class="sxs-lookup"><span data-stu-id="46e6d-191">Otherwise, the information is reloaded from the server.</span></span>                                                                                                                                                                                                                   |



 

## <a name="persistent-caching-functions"></a><span data-ttu-id="46e6d-192">Функции постоянного кэширования</span><span class="sxs-lookup"><span data-stu-id="46e6d-192">Persistent Caching Functions</span></span>

<span data-ttu-id="46e6d-193">Клиенты, которым требуются постоянные службы кэширования, используют функции постоянного кэширования, чтобы позволить приложениям сохранять данные в локальной файловой системе для последующего использования, например в ситуациях, когда канал с низкой пропускной способностью ограничивает доступ к данным, или доступ вообще недоступен.</span><span class="sxs-lookup"><span data-stu-id="46e6d-193">Clients that need persistent caching services use the persistent caching functions to allow their applications to save data in the local file system for subsequent use, such as in situations where a low-bandwidth link limits access to the data, or the access is not available at all.</span></span>

<span data-ttu-id="46e6d-194">Функции кэширования обеспечивают постоянное кэширование и просмотр в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="46e6d-194">The cache functions provide persistent caching and offline browsing.</span></span> <span data-ttu-id="46e6d-195">Если флаг [**Internet \_ флаг \_ \_ \_ записи кэша явно не**](api-flags.md) указывает кэширование, функции кэшируют все данные, загруженные из сети.</span><span class="sxs-lookup"><span data-stu-id="46e6d-195">Unless the [**INTERNET\_FLAG\_NO\_CACHE\_WRITE**](api-flags.md) flag explicitly specifies no caching, the functions cache all data downloaded from the network.</span></span> <span data-ttu-id="46e6d-196">Ответы на POST данные не кэшируются.</span><span class="sxs-lookup"><span data-stu-id="46e6d-196">The responses to POST data are not cached.</span></span>

## <a name="using-the-persistent-url-cache-functions"></a><span data-ttu-id="46e6d-197">Использование функций кэша постоянного URL-адреса</span><span class="sxs-lookup"><span data-stu-id="46e6d-197">Using the Persistent URL Cache Functions</span></span>

<span data-ttu-id="46e6d-198">Следующие функции кэша постоянных URL-адресов позволяют приложению получать доступ к информации, хранящейся в кэше, и управлять ею.</span><span class="sxs-lookup"><span data-stu-id="46e6d-198">The following persistent URL cache functions allow an application to access and manipulate information stored in the cache.</span></span>



| <span data-ttu-id="46e6d-199">Функция</span><span class="sxs-lookup"><span data-stu-id="46e6d-199">Function</span></span>                                                           | <span data-ttu-id="46e6d-200">Описание</span><span class="sxs-lookup"><span data-stu-id="46e6d-200">Description</span></span>                                                                                                                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46e6d-201">**коммитурлкачинтря**</span><span class="sxs-lookup"><span data-stu-id="46e6d-201">**CommitUrlCacheEntryA**</span></span>](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)               | <span data-ttu-id="46e6d-202">Кэширует данные в указанном файле в хранилище кэша и связывает их с заданным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="46e6d-202">Caches data in the specified file in the cache storage and associates it with the given URL.</span></span>                                                                  |
| [<span data-ttu-id="46e6d-203">**коммитурлкачинтрив**</span><span class="sxs-lookup"><span data-stu-id="46e6d-203">**CommitUrlCacheEntryW**</span></span>](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentryw)               | <span data-ttu-id="46e6d-204">Кэширует данные в указанном файле в хранилище кэша и связывает их с заданным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="46e6d-204">Caches data in the specified file in the cache storage and associates it with the given URL.</span></span>                                                                  |
| [<span data-ttu-id="46e6d-205">**креатеурлкачинтри**</span><span class="sxs-lookup"><span data-stu-id="46e6d-205">**CreateUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)                 | <span data-ttu-id="46e6d-206">Выделяет запрошенное хранилище кэша и создает локальное имя файла для сохранения записи кэша, соответствующей имени источника.</span><span class="sxs-lookup"><span data-stu-id="46e6d-206">Allocates the requested cache storage and creates a local file name for saving the cache entry that corresponds to the source name.</span></span>                           |
| [<span data-ttu-id="46e6d-207">**креатеурлкачеграуп**</span><span class="sxs-lookup"><span data-stu-id="46e6d-207">**CreateUrlCacheGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup)                 | <span data-ttu-id="46e6d-208">Создает идентификатор группы кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-208">Generates a cache group identification.</span></span>                                                                                                                       |
| [<span data-ttu-id="46e6d-209">**делетеурлкачинтри**</span><span class="sxs-lookup"><span data-stu-id="46e6d-209">**DeleteUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)                 | <span data-ttu-id="46e6d-210">Удаляет файл, связанный с именем источника из кэша, если файл существует.</span><span class="sxs-lookup"><span data-stu-id="46e6d-210">Removes the file associated with the source name from the cache, if the file exists.</span></span>                                                                          |
| [<span data-ttu-id="46e6d-211">**делетеурлкачеграуп**</span><span class="sxs-lookup"><span data-stu-id="46e6d-211">**DeleteUrlCacheGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-deleteurlcachegroup)                 | <span data-ttu-id="46e6d-212">Освобождает объект **GROUPID** и любое связанное состояние в файле индекса кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-212">Releases a **GROUPID** and any associated state in the cache index file.</span></span>                                                                                      |
| [<span data-ttu-id="46e6d-213">**финдклосеурлкаче**</span><span class="sxs-lookup"><span data-stu-id="46e6d-213">**FindCloseUrlCache**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)                     | <span data-ttu-id="46e6d-214">Закрывает указанный маркер перечисления.</span><span class="sxs-lookup"><span data-stu-id="46e6d-214">Closes the specified enumeration handle.</span></span>                                                                                                                      |
| [<span data-ttu-id="46e6d-215">**финдфирстурлкачинтри**</span><span class="sxs-lookup"><span data-stu-id="46e6d-215">**FindFirstUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)           | <span data-ttu-id="46e6d-216">Начинает перечисление кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-216">Begins the enumeration of the cache.</span></span>                                                                                                                          |
| [<span data-ttu-id="46e6d-217">**финдфирстурлкачинтрекс**</span><span class="sxs-lookup"><span data-stu-id="46e6d-217">**FindFirstUrlCacheEntryEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)       | <span data-ttu-id="46e6d-218">Начинает фильтрованное перечисление кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-218">Begins a filtered enumeration of the cache.</span></span>                                                                                                                   |
| [<span data-ttu-id="46e6d-219">**финднекстурлкачинтри**</span><span class="sxs-lookup"><span data-stu-id="46e6d-219">**FindNextUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)             | <span data-ttu-id="46e6d-220">Извлекает следующую запись в кэше.</span><span class="sxs-lookup"><span data-stu-id="46e6d-220">Retrieves the next entry in the cache.</span></span>                                                                                                                        |
| [<span data-ttu-id="46e6d-221">**финднекстурлкачинтрекс**</span><span class="sxs-lookup"><span data-stu-id="46e6d-221">**FindNextUrlCacheEntryEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)         | <span data-ttu-id="46e6d-222">Извлекает следующую запись в отфильтрованном перечислении кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-222">Retrieves the next entry in a filtered cache enumeration.</span></span>                                                                                                     |
| [<span data-ttu-id="46e6d-223">**жетурлкачинтринфо**</span><span class="sxs-lookup"><span data-stu-id="46e6d-223">**GetUrlCacheEntryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)               | <span data-ttu-id="46e6d-224">Извлекает сведения о записи кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-224">Retrieves information about a cache entry.</span></span>                                                                                                                    |
| [<span data-ttu-id="46e6d-225">**жетурлкачинтринфоекс**</span><span class="sxs-lookup"><span data-stu-id="46e6d-225">**GetUrlCacheEntryInfoEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoexa)           | <span data-ttu-id="46e6d-226">Выполняет поиск URL-адреса после преобразования любых кэшированных перенаправлений, которые будут применены в автономном режиме с помощью [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="46e6d-226">Searches for the URL after translating any cached redirections that would be applied in offline mode by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span>           |
| [<span data-ttu-id="46e6d-227">**реадурлкачинтристреам**</span><span class="sxs-lookup"><span data-stu-id="46e6d-227">**ReadUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)         | <span data-ttu-id="46e6d-228">Считывает кэшированные данные из потока, открытого с помощью [**ретриевеурлкачинтристреам**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span><span class="sxs-lookup"><span data-stu-id="46e6d-228">Reads the cached data from a stream that has been opened using [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span></span>                            |
| [<span data-ttu-id="46e6d-229">**ретриевеурлкачинтрифиле**</span><span class="sxs-lookup"><span data-stu-id="46e6d-229">**RetrieveUrlCacheEntryFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)     | <span data-ttu-id="46e6d-230">Извлекает запись кэша из кэша в виде файла.</span><span class="sxs-lookup"><span data-stu-id="46e6d-230">Retrieves a cache entry from the cache in the form of a file.</span></span>                                                                                                 |
| [<span data-ttu-id="46e6d-231">**ретриевеурлкачинтристреам**</span><span class="sxs-lookup"><span data-stu-id="46e6d-231">**RetrieveUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) | <span data-ttu-id="46e6d-232">Предоставляет наиболее эффективный и независимый от реализации способ доступа к данным кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-232">Provides the most efficient and implementation-independent way of accessing the cache data.</span></span>                                                                   |
| [<span data-ttu-id="46e6d-233">**сетурлкачинтриграуп**</span><span class="sxs-lookup"><span data-stu-id="46e6d-233">**SetUrlCacheEntryGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)             | <span data-ttu-id="46e6d-234">Добавляет или удаляет записи из группы кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-234">Adds or removes entries from a cache group.</span></span>                                                                                                                   |
| [<span data-ttu-id="46e6d-235">**сетурлкачинтринфо**</span><span class="sxs-lookup"><span data-stu-id="46e6d-235">**SetUrlCacheEntryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentryinfoa)               | <span data-ttu-id="46e6d-236">Задает указанные элементы структуры [**\_ \_ \_ сведений об элементе кэша Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) .</span><span class="sxs-lookup"><span data-stu-id="46e6d-236">Sets the specified members of the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure.</span></span>                                                |
| [<span data-ttu-id="46e6d-237">**унлоккурлкачинтрифиле**</span><span class="sxs-lookup"><span data-stu-id="46e6d-237">**UnlockUrlCacheEntryFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile)         | <span data-ttu-id="46e6d-238">Разблокирует запись кэша, которая была заблокирована, когда файл был извлечен для использования из кэша [**ретриевеурлкачинтрифиле**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea).</span><span class="sxs-lookup"><span data-stu-id="46e6d-238">Unlocks the cache entry that was locked when the file was retrieved for use from the cache by [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea).</span></span> |
| [<span data-ttu-id="46e6d-239">**унлоккурлкачинтристреам**</span><span class="sxs-lookup"><span data-stu-id="46e6d-239">**UnlockUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream)     | <span data-ttu-id="46e6d-240">Закрывает поток, полученный с помощью [**ретриевеурлкачинтристреам**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span><span class="sxs-lookup"><span data-stu-id="46e6d-240">Closes the stream that has been retrieved using [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span></span>                                           |



 

### <a name="enumerating-the-cache"></a><span data-ttu-id="46e6d-241">Перечисление кэша</span><span class="sxs-lookup"><span data-stu-id="46e6d-241">Enumerating the Cache</span></span>

<span data-ttu-id="46e6d-242">Функции [**финдфирстурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) и [**финднекстурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) перечисляют сведения, хранящиеся в кэше.</span><span class="sxs-lookup"><span data-stu-id="46e6d-242">The [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) and [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) functions enumerate the information stored in the cache.</span></span> <span data-ttu-id="46e6d-243">[**Финдфирстурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) запускает перечисление, используя шаблон поиска, буфер и размер буфера для создания маркера и возврата первой записи кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-243">[**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) starts the enumeration by taking a search pattern, a buffer, and a buffer size to create a handle and return the first cache entry.</span></span> <span data-ttu-id="46e6d-244">[**Финднекстурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) принимает маркер, созданный [**финдфирстурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya), буфер и размер буфера, чтобы вернуть следующую запись кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-244">[**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) takes the handle created by [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya), a buffer, and a buffer size to return the next cache entry.</span></span>

<span data-ttu-id="46e6d-245">Обе функции хранят информационную структуру [**\_ \_ записи \_ в кэше Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) в буфере.</span><span class="sxs-lookup"><span data-stu-id="46e6d-245">Both functions store an [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure in the buffer.</span></span> <span data-ttu-id="46e6d-246">Размер этой структуры различается для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="46e6d-246">The size of this structure varies for each entry.</span></span> <span data-ttu-id="46e6d-247">Если размер буфера, передаваемый любой из функций, недостаточен, функция завершается ошибкой, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку, \_ недостаточную для \_ буфера.</span><span class="sxs-lookup"><span data-stu-id="46e6d-247">If the buffer size passed to either function is insufficient, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="46e6d-248">Переменная размера буфера содержит размер буфера, который был необходим для получения этой записи кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-248">The buffer size variable contains the buffer size that was needed to retrieve that cache entry.</span></span> <span data-ttu-id="46e6d-249">Буфер, размер которого определяется переменной размера буфера, должен быть выделен, а функция должна вызываться повторно с новым буфером.</span><span class="sxs-lookup"><span data-stu-id="46e6d-249">A buffer of the size indicated by the buffer size variable should be allocated, and the function should be called again with the new buffer.</span></span>

<span data-ttu-id="46e6d-250">Структура [**\_ \_ \_ сведений о записи кэша Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) содержит размер структуры, URL-адрес кэшированной информации, имя локального файла, тип записи кэша, число использований, скорость попаданий, размер, время последнего изменения, срок действия, Последний доступ, время последней синхронизации, сведения о заголовке, размер сведений о заголовке и расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="46e6d-250">The [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure contains the structure size, URL of the cached information, local file name, cache entry type, use count, hit rate, size, last modified time, expiration, last access, last synchronized time, header information, header information size, and file name extension.</span></span>

<span data-ttu-id="46e6d-251">Функция [**финдфирстурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) принимает шаблон поиска, буфер, в котором хранится структура [**\_ \_ \_ сведений об элементе кэша Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) , и размер буфера.</span><span class="sxs-lookup"><span data-stu-id="46e6d-251">The [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) function takes a search pattern, a buffer that stores the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="46e6d-252">В настоящее время реализован только шаблон поиска по умолчанию, который возвращает все записи кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-252">Currently, only the default search pattern, which returns all cache entries, is implemented.</span></span>

<span data-ttu-id="46e6d-253">После перечисления кэша приложение должно вызвать [**финдклосеурлкаче**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) , чтобы закрыть обработчик перечисления кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-253">After the cache is enumerated, the application should call [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) to close the cache enumeration handle.</span></span>

<span data-ttu-id="46e6d-254">В следующем примере отображается URL-адрес каждой записи кэша в поле со списком, **IDC \_ качелист**.</span><span class="sxs-lookup"><span data-stu-id="46e6d-254">The following example displays each cache entry's URL in a list box, **IDC\_CacheList**.</span></span> <span data-ttu-id="46e6d-255">Он использует максимальный \_ \_ Размер записи \_ кэша \_ для первоначального выделения буфера, поскольку ранние версии API WinInet не перечисляют кэш должным образом.</span><span class="sxs-lookup"><span data-stu-id="46e6d-255">It uses MAX\_CACHE\_ENTRY\_INFO\_SIZE to initially allocate a buffer, since early versions of the WinINet API do not enumerate the cache properly otherwise.</span></span> <span data-ttu-id="46e6d-256">Более поздние версии выполняют перечисление кэша в правильном объеме и не имеют ограничения на размер кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-256">Later versions do enumerate the cache properly and there is no cache size limit.</span></span> <span data-ttu-id="46e6d-257">Все приложения, работающие на компьютерах с версией API WinINet из Internet Explorer 4,0, должны выделить буфер требуемого размера.</span><span class="sxs-lookup"><span data-stu-id="46e6d-257">All applications that run on computers with the version of the WinINet API from Internet Explorer 4.0 must allocate a buffer of the required size.</span></span> <span data-ttu-id="46e6d-258">Дополнительные сведения см. [в разделе использование буферов](appendix-b-using-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="46e6d-258">For more information, see [Using Buffers](appendix-b-using-buffers.md).</span></span>


```C++
int WINAPI EnumerateCacheOld(HWND hX)
{
    DWORD dwEntrySize;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;
    DWORD MAX_CACHE_ENTRY_INFO_SIZE = 4096;
    HANDLE hCacheDir;
    int nCount=0;

    SendDlgItemMessage(hX,IDC_CacheList,LB_RESETCONTENT,0,0);
    
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
    lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
    lpCacheEntry->dwStructSize = dwEntrySize;

again:

    hCacheDir = FindFirstUrlCacheEntry(NULL,
                                       lpCacheEntry,
                                       &dwEntrySize);
    if (!hCacheDir)                                             
    {
        delete[]lpCacheEntry;
        switch(GetLastError())
        {
            case ERROR_NO_MORE_ITEMS: 
                TCHAR tempout[80];
                _stprintf_s(tempout, 
                            80,   
                            TEXT("The number of cache entries = %d \n"),
                            nCount);
                MessageBox(hX,tempout,TEXT("Cache Enumeration"),MB_OK);
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return TRUE;
                break;
            case ERROR_INSUFFICIENT_BUFFER:
                lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                                new char[dwEntrySize];
                lpCacheEntry->dwStructSize = dwEntrySize;
                goto again;
                break;
            default:
                ErrorOut( hX,GetLastError(),
                          TEXT("FindNextUrlCacheEntry Init"));
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return FALSE;
        }
    }

    SendDlgItemMessage(hX,IDC_CacheList,LB_ADDSTRING,
                       0,(LPARAM)(lpCacheEntry->lpszSourceUrlName));
    nCount++;
    delete (lpCacheEntry);

    do 
    {
        dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
        lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
        lpCacheEntry->dwStructSize = dwEntrySize;

retry:
        if (!FindNextUrlCacheEntry(hCacheDir,
                                   lpCacheEntry, 
                                   &dwEntrySize))
        {
            delete[]lpCacheEntry;
            switch(GetLastError())
            {
                case ERROR_NO_MORE_ITEMS: 
                    TCHAR tempout[80];
                    _stprintf_s(tempout,
                                80,
                                TEXT("The number of cache entries = %d \n"),nCount);
                    MessageBox(hX,
                               tempout,
                               TEXT("Cache Enumeration"),MB_OK);
                    FindCloseUrlCache(hCacheDir);
                    return TRUE;
                    break;
                case ERROR_INSUFFICIENT_BUFFER:
                    lpCacheEntry = 
                             (LPINTERNET_CACHE_ENTRY_INFO) 
                              new char[dwEntrySize];
                    lpCacheEntry->dwStructSize = dwEntrySize;
                    goto retry;
                    break;
                default:
                    ErrorOut(hX,
                             GetLastError(),
                             TEXT("FindNextUrlCacheEntry Init"));
                    FindCloseUrlCache(hCacheDir);
                    return FALSE;
            }
        }

        SendDlgItemMessage(hX,
                           IDC_CacheList,LB_ADDSTRING,
                           0,
                          (LPARAM)(lpCacheEntry->lpszSourceUrlName));
        nCount++;
        delete[] lpCacheEntry;        
    }  while (TRUE);

    SetCursor(LoadCursor(NULL,IDC_ARROW));
    return TRUE;        
}
```



### <a name="retrieving-cache-entry-information"></a><span data-ttu-id="46e6d-259">Получение сведений о записи кэша</span><span class="sxs-lookup"><span data-stu-id="46e6d-259">Retrieving Cache Entry Information</span></span>

<span data-ttu-id="46e6d-260">Функция [**жетурлкачинтринфо**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) позволяет получить структуру [**\_ \_ \_ сведений об элементе кэша Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) для указанного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="46e6d-260">The [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) function lets you retrieve the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure for the specified URL.</span></span> <span data-ttu-id="46e6d-261">Эта структура содержит размер структуры, URL-адрес кэшированной информации, имя локального файла, тип записи кэша, число использований, коэффициент попаданий, размер, время последнего изменения, срок действия, Последний доступ, время последней синхронизации, сведения о заголовке, размер сведений о заголовке и расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="46e6d-261">This structure contains the structure size, URL of the cached information, local file name, cache entry type, use count, hit rate, size, last modified time, expiration, last access, last synchronized time, header information, header information size, and file name extension.</span></span>

<span data-ttu-id="46e6d-262">[**Жетурлкачинтринфо**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) принимает URL-адрес, буфер для структуры [**\_ \_ \_ сведений об элементе кэша Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) и размер буфера.</span><span class="sxs-lookup"><span data-stu-id="46e6d-262">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) accepts a URL, a buffer for an [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="46e6d-263">Если URL-адрес найден, сведения копируются в буфер.</span><span class="sxs-lookup"><span data-stu-id="46e6d-263">If the URL is found, the information is copied into the buffer.</span></span> <span data-ttu-id="46e6d-264">В противном случае происходит сбой функции, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) ВОЗВРАЩАЕТ \_ файл ошибки \_ не \_ найден.</span><span class="sxs-lookup"><span data-stu-id="46e6d-264">Otherwise, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="46e6d-265">Если размер буфера недостаточен для хранения данных записи кэша, функция завершается ошибкой, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку, \_ недостаточную для \_ буфера.</span><span class="sxs-lookup"><span data-stu-id="46e6d-265">If the buffer size is insufficient to store the cache entry information, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="46e6d-266">Размер, необходимый для получения сведений, хранится в переменной размера буфера.</span><span class="sxs-lookup"><span data-stu-id="46e6d-266">The size required to retrieve the information is stored in the buffer size variable.</span></span>

<span data-ttu-id="46e6d-267">[**Жетурлкачинтринфо**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) не выполняет синтаксический анализ URL-адреса, поэтому URL-адрес, содержащий привязку ( \# ), не будет найден в кэше, даже если ресурс кэшируется.</span><span class="sxs-lookup"><span data-stu-id="46e6d-267">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) does not do any URL parsing, so a URL that contains an anchor (\#) will not be found in the cache, even if the resource is cached.</span></span> <span data-ttu-id="46e6d-268">Например, если передается URL-адрес " https://example.com/example.htm\#sample ", функция возвращает \_ файл ошибки \_ не \_ найден, даже если https://example.com/example.htm в кэше находится "".</span><span class="sxs-lookup"><span data-stu-id="46e6d-268">For example, if the URL "https://example.com/example.htm\#sample" is passed, the function returns ERROR\_FILE\_NOT\_FOUND even if "https://example.com/example.htm" is in the cache.</span></span>

<span data-ttu-id="46e6d-269">В следующем примере извлекается информация о записи кэша для указанного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="46e6d-269">The following example retrieves the cache entry information for the specified URL.</span></span> <span data-ttu-id="46e6d-270">Затем функция отображает сведения о заголовке в поле ввода **\_ качедумп IDC** .</span><span class="sxs-lookup"><span data-stu-id="46e6d-270">The function then displays the header information in the **IDC\_CacheDump** edit box.</span></span>


```C++
int WINAPI GetCacheEntryInfo(HWND hX,LPTSTR lpszUrl)
{
    DWORD dwEntrySize=0;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;

    SetCursor(LoadCursor(NULL,IDC_WAIT));
    if (!GetUrlCacheEntryInfo(lpszUrl,NULL,&dwEntrySize))
    {
        if (GetLastError()!=ERROR_INSUFFICIENT_BUFFER)
        {
            ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
            lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                            new char[dwEntrySize];
    }
    else
        return FALSE; // should not be successful w/ NULL buffer
                      // and 0 size

    if (!GetUrlCacheEntryInfo(lpszUrl,lpCacheEntry,&dwEntrySize))
    {
        ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return FALSE;
    }
    else
    {
        if ((lpCacheEntry->dwHeaderInfoSize)!=0)
        {
            LPSTR(lpCacheEntry->lpHeaderInfo)
                                [lpCacheEntry->dwHeaderInfoSize]=TEXT('\0');
            SetDlgItemText(hX,IDC_Headers,
                           lpCacheEntry->lpHeaderInfo);
        }
        else
        {
            SetDlgItemText(hX,IDC_Headers,TEXT("None"));
        }

        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return TRUE;
    }
        
}
```



### <a name="creating-a-cache-entry"></a><span data-ttu-id="46e6d-271">Создание записи кэша</span><span class="sxs-lookup"><span data-stu-id="46e6d-271">Creating a Cache Entry</span></span>

<span data-ttu-id="46e6d-272">Приложение использует функции [**креатеурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) и [**коммитурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) для создания записи кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-272">An application uses the [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) and [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) functions to create a cache entry.</span></span>

<span data-ttu-id="46e6d-273">[**Креатеурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) принимает URL-адрес, ожидаемый размер файла и расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="46e6d-273">[**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) accepts the URL, expected file size, and file name extension.</span></span> <span data-ttu-id="46e6d-274">Затем функция создает локальное имя файла для сохранения записи кэша, которая соответствует URL-адресу и расширению имени файла.</span><span class="sxs-lookup"><span data-stu-id="46e6d-274">The function then creates a local file name for saving the cache entry that corresponds to the URL and file name extension.</span></span>

<span data-ttu-id="46e6d-275">С помощью имени локального файла запишите данные в локальный файл.</span><span class="sxs-lookup"><span data-stu-id="46e6d-275">Using the local file name, write the data into the local file.</span></span> <span data-ttu-id="46e6d-276">После того как данные записаны в локальный файл, приложение должно вызвать [**коммитурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span><span class="sxs-lookup"><span data-stu-id="46e6d-276">After the data has been written to the local file, the application should call [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span></span>

<span data-ttu-id="46e6d-277">[**Коммитурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) принимает URL-адрес, имя локального файла, срок действия, время последнего изменения, тип записи кэша, сведения о заголовке, размер сведений о заголовке и расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="46e6d-277">[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) accepts the URL, local file name, expiration, last modified time, cache entry type, header information, header information size, and file name extension.</span></span> <span data-ttu-id="46e6d-278">Затем функция кэширует данные в файле, указанном в хранилище кэша, и связывает его с заданным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="46e6d-278">The function then caches data in the file specified in the cache storage and associates it with the given URL.</span></span>

<span data-ttu-id="46e6d-279">В следующем примере используется локальное имя файла, созданное предыдущим вызовом [**креатеурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya), которое хранится в текстовом поле **IDC \_ локальный_файл**, чтобы сохранить текст из текстового поля, **IDC \_ качедумп**, в записи кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-279">The following example uses the local file name, created by a previous call to [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya), stored in the text box, **IDC\_LocalFile**, to store the text from the text box, **IDC\_CacheDump**, in the cache entry.</span></span> <span data-ttu-id="46e6d-280">После записи данных в файл с помощью **fopen**, **fprintf** и **фклосе** запись фиксируется с помощью [**коммитурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span><span class="sxs-lookup"><span data-stu-id="46e6d-280">After the data has been written to the file using **fopen**, **fprintf**, and **fclose**, the entry is committed using [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span></span>


```C++
int WINAPI CommitEntry(HWND hX)
{
    LPTSTR lpszUrl, lpszExt, lpszFileName;
    LPTSTR lpszData,lpszSize;
    DWORD dwSize;
    DWORD dwEntryType=0;
    FILE *lpfCacheEntry;
    LPFILETIME lpdtmExpire, lpdtmLastModified;
    LPSYSTEMTIME lpdtmSysTime;
    errno_t err;

    if( SendDlgItemMessage(hX,IDC_RBNormal,BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + NORMAL_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBSticky, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + STICKY_CACHE_ENTRY;
    }
    else if(SendDlgItemMessage( hX,IDC_RBSparse, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + SPARSE_CACHE_ENTRY;
    }
 

    if( SendDlgItemMessage(hX,IDC_RBCookie, BM_GETCHECK,0,0))
    {
            dwEntryType = dwEntryType + COOKIE_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBUrl, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + URLHISTORY_CACHE_ENTRY;
    }


    if( SendDlgItemMessage(hX,IDC_RBNone, BM_GETCHECK,0,0) )
    {
        dwEntryType=0;
    }
        
    lpdtmSysTime = new SYSTEMTIME;
    lpdtmExpire = new FILETIME;
    lpdtmLastModified = new FILETIME;

    GetLocalTime(lpdtmSysTime);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmExpire);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmLastModified);
    delete(lpdtmSysTime);

    lpszUrl = new TCHAR[MAX_PATH];
    lpszFileName = new TCHAR[MAX_PATH];
    lpszExt = new TCHAR[5];
    lpszSize = new TCHAR[10];

    GetDlgItemText(hX,IDC_SourceURL,lpszUrl,MAX_PATH);
    GetDlgItemText(hX,IDC_LocalFile,lpszFileName,MAX_PATH);
    GetDlgItemText(hX,IDC_FileExt,lpszExt,5);

    GetDlgItemText(hX,IDC_SizeLow,lpszSize,10);
    dwSize = (DWORD)_ttol(lpszSize);
    delete(lpszSize);

    if (dwSize==0)
    {
        if((MessageBox(hX,
                       TEXT("Incorrect File Size.\nUsing 8000 characters, Okay?\n"),
                       TEXT("Commit Entry"),MB_YESNO))
                        ==IDYES)
        {
            dwSize = 8000;
        }
        else
        {
            return FALSE;
        }
    }

    lpszData = new TCHAR[dwSize];
    GetDlgItemText(hX,IDC_CacheDump,lpszData,dwSize);
        
     err = _tfopen_s(&lpfCacheEntry,lpszFileName,_T("w"));
     if (err)
        return FALSE;
    fprintf(lpfCacheEntry,"%s",lpszData);
    fclose(lpfCacheEntry);
    delete(lpszData);

    if ( !CommitUrlCacheEntry( lpszUrl, 
                               lpszFileName, 
                               *lpdtmExpire,
                               *lpdtmLastModified, 
                               dwEntryType,
                               NULL,
                               0,
                               lpszExt,
                               0) )
    {
        ErrorOut(hX,GetLastError(),TEXT("Commit Cache Entry"));
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return FALSE;
    }
    else
    {
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return TRUE;
    }
}
```



### <a name="deleting-a-cache-entry"></a><span data-ttu-id="46e6d-281">Удаление записи кэша</span><span class="sxs-lookup"><span data-stu-id="46e6d-281">Deleting a Cache Entry</span></span>

<span data-ttu-id="46e6d-282">Функция [**делетеурлкачинтри**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) принимает URL-адрес и удаляет связанный с ним файл кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-282">The [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) function takes a URL and removes the cache file associated with it.</span></span> <span data-ttu-id="46e6d-283">Если файл кэша не существует, функция завершается ошибкой, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) ВОЗВРАЩАЕТ \_ файл ошибки \_ не \_ найден.</span><span class="sxs-lookup"><span data-stu-id="46e6d-283">If the cache file does not exist, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="46e6d-284">Если файл кэша в настоящий момент заблокирован или используется, функция завершается ошибкой, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает \_ отказ в доступе \_ .</span><span class="sxs-lookup"><span data-stu-id="46e6d-284">If the cache file is currently locked or in use, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span> <span data-ttu-id="46e6d-285">Файл удаляется после снятия блокировки.</span><span class="sxs-lookup"><span data-stu-id="46e6d-285">The file is deleted when unlocked.</span></span>

### <a name="retrieving-cache-entry-files"></a><span data-ttu-id="46e6d-286">Получение файлов записей кэша</span><span class="sxs-lookup"><span data-stu-id="46e6d-286">Retrieving Cache Entry Files</span></span>

<span data-ttu-id="46e6d-287">Для приложений, которым требуется имя файла ресурса, используйте функции [**ретриевеурлкачинтрифиле**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) и [**унлоккурлкачинтрифиле**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) .</span><span class="sxs-lookup"><span data-stu-id="46e6d-287">For applications that require the file name of a resource, use the [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) and [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) functions.</span></span> <span data-ttu-id="46e6d-288">Приложения, которым не требуется имя файла, должны использовать функции [**ретриевеурлкачинтристреам**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**реадурлкачинтристреам**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)и [**унлоккурлкачинтристреам**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) для получения информации в кэше.</span><span class="sxs-lookup"><span data-stu-id="46e6d-288">Applications that do not require the file name should use the [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream), and [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) functions to retrieve the information in the cache.</span></span>

<span data-ttu-id="46e6d-289">[**Ретриевеурлкачинтристреам**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) не выполняет синтаксический анализ URL-адреса, поэтому URL-адрес, содержащий привязку ( \# ), не будет найден в кэше, даже если ресурс кэшируется.</span><span class="sxs-lookup"><span data-stu-id="46e6d-289">[**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) does not do any URL parsing, so a URL that contains an anchor (\#) will not be found in the cache, even if the resource is cached.</span></span> <span data-ttu-id="46e6d-290">Например, если передается URL-адрес " https://example.com/example.htm\#sample ", функция возвращает \_ файл ошибки \_ не \_ найден, даже если https://example.com/example.htm в кэше находится "".</span><span class="sxs-lookup"><span data-stu-id="46e6d-290">For example, if the URL "https://example.com/example.htm\#sample" is passed, the function returns ERROR\_FILE\_NOT\_FOUND even if "https://example.com/example.htm" is in the cache.</span></span>

<span data-ttu-id="46e6d-291">[**Ретриевеурлкачинтрифиле**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) принимает URL-адрес, буфер, в котором хранится структура [**\_ \_ \_ сведений о записи кэша Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) , и размер буфера.</span><span class="sxs-lookup"><span data-stu-id="46e6d-291">[**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) accepts a URL, a buffer that stores the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="46e6d-292">Функция извлекается и блокируется для вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="46e6d-292">The function is retrieved and locked for the caller.</span></span>

<span data-ttu-id="46e6d-293">После того как данные в файле будут использованы, приложение должно вызвать [**унлоккурлкачинтрифиле**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) для разблокировки файла.</span><span class="sxs-lookup"><span data-stu-id="46e6d-293">After the information in the file has been used, the application should call [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) to unlock the file.</span></span>

### <a name="cache-groups"></a><span data-ttu-id="46e6d-294">Группы кэша</span><span class="sxs-lookup"><span data-stu-id="46e6d-294">Cache Groups</span></span>

<span data-ttu-id="46e6d-295">Чтобы создать группу кэша, необходимо вызвать функцию [**креатеурлкачеграуп**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) , чтобы создать объект **GROUPID** для группы кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-295">To create a cache group, the [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) function must be called to generate a **GROUPID** for the cache group.</span></span> <span data-ttu-id="46e6d-296">Записи можно добавить в группу кэша, предоставив URL-адрес записи кэша и \_ флаг добавления группы кэша Интернета в \_ \_ функцию [**сетурлкачинтриграуп**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) .</span><span class="sxs-lookup"><span data-stu-id="46e6d-296">Entries can be added to the cache group by supplying the cache entry's URL and the INTERNET\_CACHE\_GROUP\_ADD flag to the [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) function.</span></span> <span data-ttu-id="46e6d-297">Чтобы удалить запись кэша из группы, передайте ее URL-адрес и параметр \_ удаления группы кэша Интернета \_ \_ в [**сетурлкачинтриграуп**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).</span><span class="sxs-lookup"><span data-stu-id="46e6d-297">To remove a cache entry from a group, pass the cache entry's URL and the INTERNET\_CACHE\_GROUP\_REMOVE flag to [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).</span></span>

<span data-ttu-id="46e6d-298">Функции [**финдфирстурлкачинтрекс**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) и [**финднекстурлкачинтрекс**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) можно использовать для перечисления записей в указанной группе кэша.</span><span class="sxs-lookup"><span data-stu-id="46e6d-298">The [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) and [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) functions can be used to enumerate the entries in a specified cache group.</span></span> <span data-ttu-id="46e6d-299">После завершения перечисления функция должна вызвать [**финдклосеурлкаче**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache).</span><span class="sxs-lookup"><span data-stu-id="46e6d-299">After the enumeration is complete, the function should call [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache).</span></span>

## <a name="handling-structures-with-variable-size-information"></a><span data-ttu-id="46e6d-300">Обработка структур со сведениями о размере переменных</span><span class="sxs-lookup"><span data-stu-id="46e6d-300">Handling Structures with Variable Size Information</span></span>

<span data-ttu-id="46e6d-301">Кэш может содержать сведения о размере переменных для каждого хранимого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="46e6d-301">The cache can contain variable size information for each URL stored.</span></span> <span data-ttu-id="46e6d-302">Это отражено в структуре [**\_ сведений в \_ записи \_ кэша Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) .</span><span class="sxs-lookup"><span data-stu-id="46e6d-302">This is reflected in the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure.</span></span> <span data-ttu-id="46e6d-303">Когда функции кэша возвращают эту структуру, они создают буфер, который всегда имеет размер данных [**\_ \_ записи \_ кэша Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) плюс любые сведения о размере переменной.</span><span class="sxs-lookup"><span data-stu-id="46e6d-303">When the cache functions return this structure, they create a buffer that is always the size of [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) plus any variable size information.</span></span> <span data-ttu-id="46e6d-304">Если элемент указателя не **равен null**, он указывает на область памяти сразу после структуры.</span><span class="sxs-lookup"><span data-stu-id="46e6d-304">If a pointer member is not **NULL**, it points to the memory area immediately after the structure.</span></span> <span data-ttu-id="46e6d-305">При копировании буфера, возвращенного функцией, в другой буфер, необходимо исправить элементы указателя, чтобы они указывали на соответствующее место в новом буфере, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="46e6d-305">While copying the buffer returned by a function into another buffer, the pointer members should be fixed to point to the appropriate place in the new buffer, as the following example shows.</span></span>

``` syntax
lpDstCEInfo->lpszSourceUrlName = 
    (LPINTERNET_CACHE_ENTRY_INFO) ((LPBYTE) lpSrcCEInfo + 
       ((DWORD)(lpOldCEInfo->lpszSourceUrlName) - (DWORD)lpOldCEInfo));
```

<span data-ttu-id="46e6d-306">Некоторые функции кэша завершаются ошибкой, \_ недостаточным \_ сообщение об ошибке буфера, если указать буфер, который слишком мал для хранения данных записи кэша, полученных функцией.</span><span class="sxs-lookup"><span data-stu-id="46e6d-306">Some cache functions fail with the ERROR\_INSUFFICIENT\_BUFFER error message if you specify a buffer that is too small to contain the cache entry information retrieved by the function.</span></span> <span data-ttu-id="46e6d-307">В этом случае функция также возвращает необходимый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="46e6d-307">In this case, the function also returns the required size of the buffer.</span></span> <span data-ttu-id="46e6d-308">Затем можно выделить буфер соответствующего размера и вызвать функцию снова.</span><span class="sxs-lookup"><span data-stu-id="46e6d-308">You can then allocate a buffer of the appropriate size and call the function again.</span></span>

> [!Note]  
> <span data-ttu-id="46e6d-309">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="46e6d-309">WinINet does not support server implementations.</span></span> <span data-ttu-id="46e6d-310">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="46e6d-310">In addition, it should not be used from a service.</span></span> <span data-ttu-id="46e6d-311">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="46e6d-311">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 
