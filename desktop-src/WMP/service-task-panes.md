---
title: Области задач службы
description: Области задач службы
ms.assetid: f626fa85-7590-4e87-bd5c-7ffdcb14be8b
keywords:
- Интернет-магазины проигрывателя Windows Media, области задач службы
- Интернет-магазины, области задач службы
- Введите 2 Интернет-магазина, области задач службы
- Интернет-магазины проигрывателя Windows Media, области задач
- Интернет-магазины, области задач
- Введите 2 Интернет-магазина, области задач
- Проигрыватель Windows Media, области задач службы
- Проигрыватель Windows Media, области задач
- области задач службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f882e46a7252792db5b551b25869c7711f9d31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068120"
---
# <a name="service-task-panes"></a><span data-ttu-id="ff800-112">Области задач службы</span><span class="sxs-lookup"><span data-stu-id="ff800-112">Service Task Panes</span></span>

<span data-ttu-id="ff800-113">В проигрывателе Windows Media 10 поставщики интернет-магазина могут настроить проигрыватель Windows Media так, чтобы он отображался в виде трех панелей задач, называемых областями задач службы.</span><span class="sxs-lookup"><span data-stu-id="ff800-113">In Windows Media Player 10, online store providers can configure Windows Media Player to display as many as three task panes, called service task panes.</span></span> <span data-ttu-id="ff800-114">Каждая область задач службы представлена настраиваемой кнопкой, которую проигрыватель Windows Media отображает в правой части панели задач "функции".</span><span class="sxs-lookup"><span data-stu-id="ff800-114">Each service task pane is represented by a customizable button that Windows Media Player displays on the right side of the Features taskbar.</span></span>

<span data-ttu-id="ff800-115">Каждая область задач службы содержит веб-страницу, которая является пользовательским интерфейсом для определенной функции Интернет-магазина. Внешний вид областей задач службы определяется XML-документом ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="ff800-115">Each service task pane hosts a webpage that is the user interface for a particular online store feature.The appearance of the service task panes is defined by the ServiceInfo XML document.</span></span> <span data-ttu-id="ff800-116">В этом документе области задач службы представлены тремя элементами: **ServiceTask1**, **ServiceTask2** и **ServiceTask3**.</span><span class="sxs-lookup"><span data-stu-id="ff800-116">In this document, the service task panes are represented by three elements: **ServiceTask1**, **ServiceTask2**, and **ServiceTask3**.</span></span> <span data-ttu-id="ff800-117">Эти области задач службы предназначены для предоставления следующих данных:</span><span class="sxs-lookup"><span data-stu-id="ff800-117">These service task panes are intended to provide the following:</span></span>

-   <span data-ttu-id="ff800-118">Музыкальная служба.</span><span class="sxs-lookup"><span data-stu-id="ff800-118">A music service.</span></span>
-   <span data-ttu-id="ff800-119">Служба видео.</span><span class="sxs-lookup"><span data-stu-id="ff800-119">A video service.</span></span>
-   <span data-ttu-id="ff800-120">Служба радио.</span><span class="sxs-lookup"><span data-stu-id="ff800-120">A radio service.</span></span>

<span data-ttu-id="ff800-121">Эти функции можно разместить в проигрывателе Windows Media в любом порядке, но **ServiceTask1** должна быть основной областью задач для участия в коммерческих действиях.</span><span class="sxs-lookup"><span data-stu-id="ff800-121">You can position these features in Windows Media Player in any order you like, but **ServiceTask1** must be the primary task pane for engaging in commercial activity.</span></span>

<span data-ttu-id="ff800-122">Веб-страница, размещенная в каждой области задач службы, имеет доступ к **внешнему** объекту.</span><span class="sxs-lookup"><span data-stu-id="ff800-122">The webpage hosted in each service task pane has access to the **External** object.</span></span> <span data-ttu-id="ff800-123">Этот объект предоставляет методы, свойства и событие, которые предоставляют специальные функциональные возможности для веб-страниц в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ff800-123">This object provides methods, properties, and an event that provide special functionality for webpages in Windows Media Player.</span></span> <span data-ttu-id="ff800-124">Например, можно использовать событие и свойства **внешнего** вида, чтобы внешний вид веб-страницы совпадал с цветовой схемой, выбранной пользователем для проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ff800-124">For instance, you can use the event and properties from **External** to make the appearance of your webpage match the color scheme that the user has chosen for Windows Media Player.</span></span>

<span data-ttu-id="ff800-125">В проигрывателе Windows Media 11 нет областей задач службы.</span><span class="sxs-lookup"><span data-stu-id="ff800-125">In Windows Media Player 11, there are no service task panes.</span></span> <span data-ttu-id="ff800-126">Вместо этого имеется одна вкладка **Интернет-магазинов** , на которой размещена Главная веб-страница для активного интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="ff800-126">Instead, there is a single **Online Stores** tab, which hosts the main webpage for the active online store.</span></span> <span data-ttu-id="ff800-127">В документе ServiceInfo Вкладка Интернет- **магазины** представлена элементом **ServiceTask1** . элементы **ServiceTask2** и **ServiceTask3** игнорируются.</span><span class="sxs-lookup"><span data-stu-id="ff800-127">In the ServiceInfo document, the **Online Stores** tab is represented by the **ServiceTask1** element; the **ServiceTask2** and **ServiceTask3** elements are ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff800-128">См. также</span><span class="sxs-lookup"><span data-stu-id="ff800-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff800-129">**Сведения о типе 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="ff800-129">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="ff800-130">**Внешний объект для Интернет-магазинов типа 2**</span><span class="sxs-lookup"><span data-stu-id="ff800-130">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="ff800-131">**Документ ServiceInfo для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="ff800-131">**ServiceInfo Document for a Type 2 Online Store**</span></span>](serviceinfo-document-for-a-type-2-online-store.md)
</dt> </dl>

 

 




