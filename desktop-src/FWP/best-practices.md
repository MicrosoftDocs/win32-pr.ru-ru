---
title: Рекомендации (платформа фильтрации Windows)
description: Следующий список содержит рекомендации по разработке приложений с помощью API платформы фильтрации Windows (WFP).
ms.assetid: 017ff210-8666-466e-8424-c95e750fd5ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac43f103e0076945d566e26a1706bdec22916db
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533674"
---
# <a name="best-practices-windows-filtering-platform"></a><span data-ttu-id="1871c-103">Рекомендации (платформа фильтрации Windows)</span><span class="sxs-lookup"><span data-stu-id="1871c-103">Best Practices (Windows Filtering Platform)</span></span>

<span data-ttu-id="1871c-104">Следующий список содержит рекомендации по разработке приложений с помощью API платформы фильтрации Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="1871c-104">The following list contains best practices for developing applications using the Windows Filtering Platform (WFP) API.</span></span>

-   <span data-ttu-id="1871c-105">Используйте динамические сеансы.</span><span class="sxs-lookup"><span data-stu-id="1871c-105">Use dynamic sessions.</span></span>

    <span data-ttu-id="1871c-106">Многие приложения добавляют объекты политики фильтрации при запуске, а затем удаляют эти объекты по мере их завершения.</span><span class="sxs-lookup"><span data-stu-id="1871c-106">Many applications add filtering policy objects at start, and then delete these objects at stop.</span></span> <span data-ttu-id="1871c-107">Используя динамический сеанс, вы гарантируете, что эти объекты будут удалены даже в случае сбоя приложения.</span><span class="sxs-lookup"><span data-stu-id="1871c-107">By using a dynamic session, you guarantee that these objects are deleted even if the application crashes.</span></span> <span data-ttu-id="1871c-108">Более того, простое закрытие обработчика подсистемы на этапе «останавливается» является более эффективным, чем выполнение отдельных вызовов для удаления каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="1871c-108">Furthermore, simply closing the engine handle at stop is more efficient than making individual calls to delete each object.</span></span>

-   <span data-ttu-id="1871c-109">Либо обрабатывайте время ожидания транзакций, либо задайте для сеанса **ткснваиттимеаутинмсек** значение Infinite, чтобы предотвратить время ожидания.</span><span class="sxs-lookup"><span data-stu-id="1871c-109">Either handle transaction timeouts gracefully or set the session **txnWaitTimeoutInMSec** to infinite to prevent timeouts.</span></span>

    <span data-ttu-id="1871c-110">Даже если не используются явные транзакции, большинство вызовов все еще выполняются в неявной транзакции и, таким образом, могут истечет время ожидания.</span><span class="sxs-lookup"><span data-stu-id="1871c-110">Even if you do not use explicit transactions, most calls are still executed under an implicit transaction and thus can timeout.</span></span>

-   <span data-ttu-id="1871c-111">Используйте явные транзакции для объединения связанных операций добавления или удаления в одну транзакцию.</span><span class="sxs-lookup"><span data-stu-id="1871c-111">Use explicit transactions to combine related add or delete operations into a single transaction.</span></span>

    <span data-ttu-id="1871c-112">Это более эффективно и позволяет легко очищать частичные результаты по путям ошибок.</span><span class="sxs-lookup"><span data-stu-id="1871c-112">This is more efficient and makes it easy to clean up partial results in error paths.</span></span>

-   <span data-ttu-id="1871c-113">Используйте строки, совместимые с MUI.</span><span class="sxs-lookup"><span data-stu-id="1871c-113">Use MUI compliant strings.</span></span>

    <span data-ttu-id="1871c-114">Все локализуемые строки хранятся в общей структуре данных: [**фвпм \_ отобразить \_ data0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0).</span><span class="sxs-lookup"><span data-stu-id="1871c-114">All the localizable strings are stored in a common data structure: [**FWPM\_DISPLAY\_DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0).</span></span> <span data-ttu-id="1871c-115">Строки в этой структуре могут быть непрямыми строками типа, поддерживаемого [**шлоадиндиректстринг**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span><span class="sxs-lookup"><span data-stu-id="1871c-115">The strings within this structure can be indirect strings of the type supported by [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span></span> <span data-ttu-id="1871c-116">Перед возвратом структуры **фвпм \_ \_ data0** в любой из функций непрямые строки разрешаются в указанный строковый ресурс с помощью языкового стандарта вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="1871c-116">Before an **FWPM\_DISPLAY\_DATA0** structure is returned by any of the functions, the indirect strings are resolved to the specified string resource using the caller's locale.</span></span>

-   <span data-ttu-id="1871c-117">Свяжите все объекты с поставщиком.</span><span class="sxs-lookup"><span data-stu-id="1871c-117">Associate all objects to a provider.</span></span>

    <span data-ttu-id="1871c-118">Если в системе установлено несколько поставщиков, это упрощает средство диагностики для определения того, кто их добавил.</span><span class="sxs-lookup"><span data-stu-id="1871c-118">When multiple providers are installed on the system, this makes it is easier for diagnostic tools to determine who added what.</span></span>

-   <span data-ttu-id="1871c-119">Добавьте фильтры в свой подслой.</span><span class="sxs-lookup"><span data-stu-id="1871c-119">Add filters to your own sublayer.</span></span>

    <span data-ttu-id="1871c-120">После попадания в подслоям завершающего фильтра не вычисляются дополнительные фильтры в этом подслое.</span><span class="sxs-lookup"><span data-stu-id="1871c-120">Once a terminating filter in a sublayer is hit, no more filters in that sublayer are evaluated.</span></span> <span data-ttu-id="1871c-121">Таким образом, при добавлении фильтров в тот же подуровень, что и другой поставщик, можно предотвратить вызов фильтров друг друга, что приведет к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="1871c-121">Thus, if you add your filters to the same sublayer as another provider, you may prevent each other's filters from being invoked, resulting in unexpected results.</span></span>

-   <span data-ttu-id="1871c-122">Используйте принудительное применение уровня приложения (ALE), а не фильтрацию по пакетам.</span><span class="sxs-lookup"><span data-stu-id="1871c-122">Use Application Layer Enforcement (ALE) rather than packet-oriented filtering.</span></span>

    <span data-ttu-id="1871c-123">Фильтрация на уровне пакетов выполняется очень долго.</span><span class="sxs-lookup"><span data-stu-id="1871c-123">Filtering at the packet layer is slow.</span></span>

-   <span data-ttu-id="1871c-124">Фильтрация ошибок ICMP и событий RST перед их созданием.</span><span class="sxs-lookup"><span data-stu-id="1871c-124">Filter ICMP errors and RST events before they are generated.</span></span>

    <span data-ttu-id="1871c-125">Это более эффективный способ фильтрации этих событий после их создания.</span><span class="sxs-lookup"><span data-stu-id="1871c-125">This is more efficient that filtering these events after they are generated.</span></span>

-   <span data-ttu-id="1871c-126">Выполнять проверку пакетов на уровне потокового или датаграмма, а не на транспортном уровне.</span><span class="sxs-lookup"><span data-stu-id="1871c-126">Perform packet inspection at Stream/Datagram Data layer rather than at the Transport layer.</span></span>

    <span data-ttu-id="1871c-127">Это относится к разработке выносок.</span><span class="sxs-lookup"><span data-stu-id="1871c-127">This applies to developing callouts.</span></span> <span data-ttu-id="1871c-128">Дополнительные сведения см. в разделе [рекомендации по программированию драйвера выноски](/windows-hardware/drivers/network/callout-driver-programming-considerations) в комплекте драйверов для Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="1871c-128">For more information, see [Callout Driver Programming Considerations](/windows-hardware/drivers/network/callout-driver-programming-considerations) in the Windows Driver Kit (WDK).</span></span>

-   <span data-ttu-id="1871c-129">При использовании сложных фильтров учитывайте влияние на производительность.</span><span class="sxs-lookup"><span data-stu-id="1871c-129">Consider performance implications when using complex filters.</span></span>

    <span data-ttu-id="1871c-130">Начиная с Windows 7 и Windows Server 2008 R2 можно создавать фильтры с несколькими условиями, в которых используется один и тот же ключ поля.</span><span class="sxs-lookup"><span data-stu-id="1871c-130">Starting in Windows 7 and Windows Server 2008 R2, filters can be created with multiple conditions which use the same field key.</span></span> <span data-ttu-id="1871c-131">Это позволяет создавать сложные политики с меньшим количеством фильтров.</span><span class="sxs-lookup"><span data-stu-id="1871c-131">This allows complex policies to be created with fewer filters.</span></span> <span data-ttu-id="1871c-132">Однако такие сложные фильтры могут привести к снижению производительности для классификации механизма фильтрации WFP.</span><span class="sxs-lookup"><span data-stu-id="1871c-132">However such complex filters might incur a slower performance for the WFP filter engine to classify.</span></span> <span data-ttu-id="1871c-133">Необходимо выполнить оценку, чтобы определить, оказывает ли использование таких фильтров негативное влияние на общую производительность вашего решения.</span><span class="sxs-lookup"><span data-stu-id="1871c-133">An evaluation should be made to determine whether use of such filters causes an adverse effect on the overall performance of your solution.</span></span>

 

 
