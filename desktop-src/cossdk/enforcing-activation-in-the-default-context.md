---
description: Настроенный COM-компонент обычно активируется в собственном контексте; Это значит, что COM+ ссылается на сведения каталога компонентов, чтобы предоставить все настроенные службы.
ms.assetid: 09dc7165-22b1-4eca-9591-d83e85556f3f
title: Принудительная активация в контексте по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41599f71dc37c37c1a9a574d274ca2858835e2df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539425"
---
# <a name="enforcing-activation-in-the-default-context"></a><span data-ttu-id="87707-103">Принудительная активация в контексте по умолчанию</span><span class="sxs-lookup"><span data-stu-id="87707-103">Enforcing Activation in the Default Context</span></span>

<span data-ttu-id="87707-104">Настроенный COM-компонент обычно активируется в собственном контексте; Это значит, что COM+ ссылается на сведения о каталоге компонента, чтобы предоставить все настроенные службы.</span><span class="sxs-lookup"><span data-stu-id="87707-104">A configured COM component is usually activated in its own context; that is, COM+ references the component's catalog information to provide any configured services.</span></span> <span data-ttu-id="87707-105">Однако можно активировать настроенный компонент в контексте по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="87707-105">However, you can choose to activate a configured component in the default context.</span></span> <span data-ttu-id="87707-106">Базовый COM-компонент — зарегистрированный компонент, который не содержит сведений о каталоге COM+, обычно активируется в контексте по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="87707-106">A base COM component—a registered component that has no COM+ catalog information—is usually activated in the default context.</span></span>

<span data-ttu-id="87707-107">Активация COM-компонента в контексте по умолчанию предоставляет три основных преимущества производительности, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="87707-107">Activating a COM component in the default context provides three major performance benefits, as follows:</span></span>

-   <span data-ttu-id="87707-108">Системные ресурсы сохраняются путем ограничения количества создаваемых контекстов.</span><span class="sxs-lookup"><span data-stu-id="87707-108">You save system resources by limiting the number of contexts that are created.</span></span>
-   <span data-ttu-id="87707-109">Вы увеличиваете производительность, ограничивая количество вызовов между контекстами.</span><span class="sxs-lookup"><span data-stu-id="87707-109">You increase performance by limiting the number of cross-context calls.</span></span> <span data-ttu-id="87707-110">Поскольку для вызовов между контекстами требуется маршалирование, для COM-объекта, активируемого в контексте по умолчанию, гораздо быстрее выполнять вызовы других объектов в контексте по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="87707-110">Because calls across contexts require marshaling, it is much faster for a COM object activated in the default context to make calls to other objects in the default context.</span></span> <span data-ttu-id="87707-111">В этом случае производительность (вызовов в одном и том же контексте) аналогична производительности вызова подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="87707-111">The performance in this case (of calls within the same context) is similar to that of calling a subroutine.</span></span>
-   <span data-ttu-id="87707-112">Вы можете импортировать старые приложения COM в COM+ и запустить их без проблем.</span><span class="sxs-lookup"><span data-stu-id="87707-112">You can import older COM applications into COM+ and run them without a problem.</span></span> <span data-ttu-id="87707-113">Например, у вас может быть несколько старых приложений COM, реализованных в соответствии с предположением, что это позволяло передавать ссылки на объекты в подразделении без маршалирования ссылок.</span><span class="sxs-lookup"><span data-stu-id="87707-113">For example, you may have several older COM applications implemented under the assumption that it was allowable to pass object references within an apartment without marshaling the references.</span></span> <span data-ttu-id="87707-114">Эти COM-приложения не работают при импорте в COM+, так как ссылки на объекты передаются через границы контекста.</span><span class="sxs-lookup"><span data-stu-id="87707-114">These COM applications do not work when imported into COM+ because the object references are passed across context boundaries.</span></span> <span data-ttu-id="87707-115">Однако этот тип приложения COM можно запустить при импорте, если вы используете средство администрирования "службы компонентов", чтобы пометить все классы в приложении как которые **должны быть активированы в контексте по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="87707-115">However, you can make this type of COM application run when imported if you use the Component Services administrative tool to mark all the classes in the application as **Must be activated in the default context**.</span></span>

<span data-ttu-id="87707-116">Основным недостатком активации настроенного компонента в контексте по умолчанию является то, что COM+ не предоставляет какие-либо настроенные службы компонента.</span><span class="sxs-lookup"><span data-stu-id="87707-116">The major disadvantage to activating a configured component in the default context is that COM+ does not provide any of the component's configured services.</span></span> <span data-ttu-id="87707-117">Существует компромисс между улучшенной производительностью и возможностью использования служб COM+.</span><span class="sxs-lookup"><span data-stu-id="87707-117">There is a trade-off between enhanced performance and the ability to use COM+ services.</span></span>

<span data-ttu-id="87707-118">Например, предположим, что компоненту COM не требуются какие-либо службы COM+ (такие [как транзакции](com--transactions.md), [JIT-активация](com--just-in-time-activation.md), [события](com--events.md), [очереди компонентов](com--queued-components.md), [Синхронизация](com--synchronization.md)или [пул объектов](com--object-pooling.md)) и что компонент выполняет ряд вызовов к другим COM-компонентам, которые могут быть активированы в контексте по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="87707-118">For example, assume that a COM component does not require any COM+ services (such as [Transactions](com--transactions.md), [Just-in-Time Activation](com--just-in-time-activation.md), [Events](com--events.md), [Queued Components](com--queued-components.md), [Synchronization](com--synchronization.md), or [Object Pooling](com--object-pooling.md)) and that the component makes a number of calls to other COM components that may be activated in the default context.</span></span> <span data-ttu-id="87707-119">В этом случае рекомендуется активировать вызывающий компонент в контексте по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="87707-119">In this case, it would be a good idea to activate the calling component in the default context.</span></span>

<span data-ttu-id="87707-120">Если компоненту COM требуются службы COM+, он не может быть помечен как **должен быть активирован в контексте по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="87707-120">If the COM component requires COM+ services, it cannot be marked as **Must be activated in the default context**.</span></span> <span data-ttu-id="87707-121">Кроме того, нет фактического повышения производительности, если COM-объект, активированный в контексте по умолчанию, выполняет несколько вызовов объектов в других контекстах.</span><span class="sxs-lookup"><span data-stu-id="87707-121">In addition, there is no real performance gain if a COM object activated in the default context makes a number of calls to objects in other contexts.</span></span> <span data-ttu-id="87707-122">(Дополнительные сведения см. в разделе [контексты](com--contexts.md).)</span><span class="sxs-lookup"><span data-stu-id="87707-122">(For more detail, see [Contexts](com--contexts.md).)</span></span>

<span data-ttu-id="87707-123">**Принудительное применение активации в контексте по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="87707-123">**To enforce activation in the default context**</span></span>

1.  <span data-ttu-id="87707-124">В области сведений средства администрирования "службы компонентов" щелкните правой кнопкой мыши компонент (расположенный в папке **Components** любого выбранного приложения COM+), который требуется активировать в контексте по умолчанию, и выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="87707-124">In the details pane of the Component Services administrative tool, right-click the component (located within the **Components** folder of any selected COM+ application) that you want to activate in the default context and then click **Properties**.</span></span>

2.  <span data-ttu-id="87707-125">В диалоговом окне Свойства компонента перейдите на вкладку **Активация** .</span><span class="sxs-lookup"><span data-stu-id="87707-125">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="87707-126">Установите флажок **должен быть активирован в контексте по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="87707-126">Select the **Must be activated in the default context** check box.</span></span>

4.  <span data-ttu-id="87707-127">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="87707-127">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="87707-128">При запуске настроенного компонента в контексте по умолчанию COM+ не активирует ни одну из настроенных служб для этого компонента.</span><span class="sxs-lookup"><span data-stu-id="87707-128">When you run a configured component in the default context, COM+ does not activate any of the configured services for that component.</span></span> <span data-ttu-id="87707-129">Эти службы снова становятся доступными при снятии флажка **необходимо активировать в контексте по умолчанию** и последующем запуске настроенного компонента в собственном контексте.</span><span class="sxs-lookup"><span data-stu-id="87707-129">These services are available again when you uncheck the **Must be activated in the default context** check box and subsequently run the configured component in its own context.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="87707-130">См. также</span><span class="sxs-lookup"><span data-stu-id="87707-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87707-131">Основные понятия JIT-активации COM+</span><span class="sxs-lookup"><span data-stu-id="87707-131">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="87707-132">Принудительная активация в контексте вызывающего объекта</span><span class="sxs-lookup"><span data-stu-id="87707-132">Enforcing Activation in the Caller's Context</span></span>](enforcing-activation-in-the-caller-s-context.md)
</dt> </dl>

 

 



