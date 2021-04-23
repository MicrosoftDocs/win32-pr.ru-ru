---
description: Статистику объектов можно отслеживать по мере выполнения приложения. Таким образом можно точно настроить характеристики пула объектов, чтобы обеспечить баланс производительности и ресурсов, которые вы хотели бы иметь.
ms.assetid: 57987cc1-8bb5-4bbd-a425-fda2e5a8b597
title: Мониторинг статистики объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f438bc7081546083f1930fe31f16a2198b09b48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342202"
---
# <a name="monitoring-object-statistics"></a><span data-ttu-id="80992-104">Мониторинг статистики объектов</span><span class="sxs-lookup"><span data-stu-id="80992-104">Monitoring Object Statistics</span></span>

<span data-ttu-id="80992-105">Статистику объектов можно отслеживать по мере выполнения приложения.</span><span class="sxs-lookup"><span data-stu-id="80992-105">You can monitor object statistics as an application runs.</span></span> <span data-ttu-id="80992-106">Таким образом можно точно настроить характеристики пула объектов, чтобы обеспечить баланс производительности и ресурсов, которые вы хотели бы иметь.</span><span class="sxs-lookup"><span data-stu-id="80992-106">By doing so, you can fine-tune the object pool characteristics to achieve the balance in performance and resources that you would like to have.</span></span>

<span data-ttu-id="80992-107">Можно отслеживать состояние всех объектов, настроенных для поддержки статистики объектов и отчетов о событиях.</span><span class="sxs-lookup"><span data-stu-id="80992-107">You can monitor status for any objects that are configured to support object statistics and event reporting.</span></span> <span data-ttu-id="80992-108">Включение статистики объектов имеет очень небольшое снижение производительности.</span><span class="sxs-lookup"><span data-stu-id="80992-108">Enabling object statistics has a very slight performance overhead.</span></span>

<span data-ttu-id="80992-109">**Включение статистики объектов**</span><span class="sxs-lookup"><span data-stu-id="80992-109">**To enable object statistics**</span></span>

1.  <span data-ttu-id="80992-110">В области сведений средства администрирования "службы компонентов" щелкните правой кнопкой мыши компонент, который необходимо настроить, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="80992-110">In the details pane of the Component Services administrative tool, right-click the component that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="80992-111">В диалоговом окне Свойства компонента перейдите на вкладку **Активация** .</span><span class="sxs-lookup"><span data-stu-id="80992-111">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="80992-112">Чтобы включить статистику объектов для компонента, в разделе **контекст активации** установите флажок **компонент поддерживает события и статистику** .</span><span class="sxs-lookup"><span data-stu-id="80992-112">To enable object statistics for the component, under **Activation Context**, select the **Component supports events and statistics** check box.</span></span>

<span data-ttu-id="80992-113">**Наблюдение за состоянием объекта**</span><span class="sxs-lookup"><span data-stu-id="80992-113">**To monitor object status**</span></span>

1.  <span data-ttu-id="80992-114">В дереве консоли средства администрирования "службы компонентов" Откройте папку для приложения, содержащего компоненты, которые требуется отслеживать.</span><span class="sxs-lookup"><span data-stu-id="80992-114">In the console tree of the Component Services administrative tool, open the folder for the application that includes the components you want to monitor.</span></span>

2.  <span data-ttu-id="80992-115">Щелкните правой кнопкой мыши папку **компоненты** , наведите указатель на пункт **вид** и выберите пункт **представление состояния**.</span><span class="sxs-lookup"><span data-stu-id="80992-115">Right-click the **Components** folder, point to **View**, and then click **Status View**.</span></span> <span data-ttu-id="80992-116">Теперь на панели подробностей отображается представление состояние всех компонентов в приложении.</span><span class="sxs-lookup"><span data-stu-id="80992-116">The details pane now displays the status view for all components in the application.</span></span> <span data-ttu-id="80992-117">В следующей таблице описаны шесть столбцов в представлении "состояние".</span><span class="sxs-lookup"><span data-stu-id="80992-117">The following table describes the six columns in the status view.</span></span>

    

    | <span data-ttu-id="80992-118">Столбец</span><span class="sxs-lookup"><span data-stu-id="80992-118">Column</span></span>                        | <span data-ttu-id="80992-119">Описание</span><span class="sxs-lookup"><span data-stu-id="80992-119">Description</span></span>                                                                                                                                                                                                                |
    |-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="80992-120">**ProgID:**</span><span class="sxs-lookup"><span data-stu-id="80992-120">**ProgID**</span></span><br/>         | <span data-ttu-id="80992-121">Определяет конкретный компонент.</span><span class="sxs-lookup"><span data-stu-id="80992-121">Identifies a specific component.</span></span><br/>                                                                                                                                                                                |
    | <span data-ttu-id="80992-122">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="80992-122">**Objects**</span></span><br/>        | <span data-ttu-id="80992-123">Показывает количество объектов, удерживаемых на данный момент клиентскими ссылками.</span><span class="sxs-lookup"><span data-stu-id="80992-123">Shows the number of objects that are currently held by client references.</span></span><br/>                                                                                                                                       |
    | <span data-ttu-id="80992-124">**Activate**</span><span class="sxs-lookup"><span data-stu-id="80992-124">**Activated**</span></span><br/>      | <span data-ttu-id="80992-125">Показывает количество объектов, активированных в данный момент.</span><span class="sxs-lookup"><span data-stu-id="80992-125">Shows the number of objects that are currently activated.</span></span> <br/>                                                                                                                                                      |
    | <span data-ttu-id="80992-126">**Составе пула**</span><span class="sxs-lookup"><span data-stu-id="80992-126">**Pooled**</span></span><br/>         | <span data-ttu-id="80992-127">Показывает общее число объектов, созданных пулом, включая используемые объекты и деактивируемые объекты.</span><span class="sxs-lookup"><span data-stu-id="80992-127">Shows the total number of objects created by the pool, including objects that are in use and objects that are deactivated.</span></span><br/>                                                                                      |
    | <span data-ttu-id="80992-128">**В вызове**</span><span class="sxs-lookup"><span data-stu-id="80992-128">**In Call**</span></span><br/>        | <span data-ttu-id="80992-129">Определяет объекты в вызове.</span><span class="sxs-lookup"><span data-stu-id="80992-129">Identifies objects in call.</span></span><br/>                                                                                                                                                                                     |
    | <span data-ttu-id="80992-130">**Время вызова (МС)**</span><span class="sxs-lookup"><span data-stu-id="80992-130">**Call Time (ms)**</span></span><br/> | <span data-ttu-id="80992-131">Показывает среднюю продолжительность вызова (в миллисекундах) вызовов методов, выполненных за последние 20 секунд (до 20 вызовов).</span><span class="sxs-lookup"><span data-stu-id="80992-131">Shows the average call duration (in milliseconds) of method calls made in the last 20 seconds (up to 20 calls).</span></span> <span data-ttu-id="80992-132">Время вызова измеряется в объекте и не включает время, используемое для обхода сети.</span><span class="sxs-lookup"><span data-stu-id="80992-132">Call time is measured at the object and does not include the time used to traverse the network.</span></span><br/> |

    

     

## <a name="related-topics"></a><span data-ttu-id="80992-133">См. также</span><span class="sxs-lookup"><span data-stu-id="80992-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80992-134">Настройка компонента для объединения в пул</span><span class="sxs-lookup"><span data-stu-id="80992-134">Configuring a Component to Be Pooled</span></span>](configuring-a-component-to-be-pooled.md)
</dt> </dl>

 

 




