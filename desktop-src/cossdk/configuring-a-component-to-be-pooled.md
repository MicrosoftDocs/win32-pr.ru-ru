---
description: Компонент можно настроить для объединения в пул только в том случае, если он правильно написан для поддержки пула. Дополнительные сведения об этих требованиях см. в разделе Требования для объектов в пуле.
ms.assetid: ffd812cc-811e-4f2a-8736-d1cb22d5abb7
title: Настройка компонента для объединения в пул
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780f7e1d9128b213b138e63b9dfa7e0f40642681
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142622"
---
# <a name="configuring-a-component-to-be-pooled"></a><span data-ttu-id="c7e26-104">Настройка компонента для объединения в пул</span><span class="sxs-lookup"><span data-stu-id="c7e26-104">Configuring a Component to Be Pooled</span></span>

<span data-ttu-id="c7e26-105">Компонент можно настроить для объединения в пул только в том случае, если он правильно написан для поддержки пула.</span><span class="sxs-lookup"><span data-stu-id="c7e26-105">You can configure a component to be pooled only when it is correctly written to support being pooled.</span></span> <span data-ttu-id="c7e26-106">Дополнительные сведения об этих требованиях см. в разделе [требования для объектов в пуле](requirements-for-poolable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c7e26-106">For details of these requirements, see [Requirements for Poolable Objects](requirements-for-poolable-objects.md).</span></span>

> [!Note]  
> <span data-ttu-id="c7e26-107">По умолчанию компонент не настроен для объединения в пул.</span><span class="sxs-lookup"><span data-stu-id="c7e26-107">By default, a component is not configured to be pooled.</span></span>

 

<span data-ttu-id="c7e26-108">При настройке компонента для объединения в пул можно указать следующие свойства, чтобы определить, как COM+ обслуживает пул.</span><span class="sxs-lookup"><span data-stu-id="c7e26-108">When you configure a component to be pooled, you can specify the following properties to determine how COM+ maintains the pool:</span></span>

-   <span data-ttu-id="c7e26-109">**Минимальный размер пула.**</span><span class="sxs-lookup"><span data-stu-id="c7e26-109">**Minimum pool size.**</span></span> <span data-ttu-id="c7e26-110">Представляет количество объектов, создаваемых при запуске приложения, и минимальное количество объектов, которые хранятся в пуле во время выполнения приложения.</span><span class="sxs-lookup"><span data-stu-id="c7e26-110">Represents the number of objects that are created when the application starts and the minimum number of objects that are maintained in the pool while the application is running.</span></span> <span data-ttu-id="c7e26-111">Если количество доступных объектов в пуле падает ниже указанного минимума, создаются новые объекты для удовлетворения любых необработанных запросов объектов и повторного заполнения пула.</span><span class="sxs-lookup"><span data-stu-id="c7e26-111">If the number of available objects in the pool drops below the specified minimum, new objects are created to meet any outstanding object requests and refill the pool.</span></span> <span data-ttu-id="c7e26-112">Если количество доступных объектов в пуле больше минимального, то эти избыточные объекты уничтожаются во время цикла очистки.</span><span class="sxs-lookup"><span data-stu-id="c7e26-112">If the number of available objects in the pool is greater than the minimum number, those surplus objects are destroyed during a clean-up cycle.</span></span>
-   <span data-ttu-id="c7e26-113">**Максимальный размер пула.**</span><span class="sxs-lookup"><span data-stu-id="c7e26-113">**Maximum pool size.**</span></span> <span data-ttu-id="c7e26-114">Представляет максимальное количество объектов в составе пула, создаваемых диспетчером пула, активно используемых клиентами и неактивными в пуле.</span><span class="sxs-lookup"><span data-stu-id="c7e26-114">Represents the maximum number of pooled objects that the pooling manager will create, both actively used by clients and inactive in the pool.</span></span> <span data-ttu-id="c7e26-115">При создании объектов диспетчер пула служб проверяет, что максимальный размер пула не достигнут, и, если нет, диспетчер пула создает новый экземпляр объекта, который будет выделился клиенту.</span><span class="sxs-lookup"><span data-stu-id="c7e26-115">When creating objects, the pooling manager checks to verify that the maximum pool size has not been reached and, if it hasn't, the pool manager creates a new instance of the object to dispense to the client.</span></span> <span data-ttu-id="c7e26-116">Если достигнут максимальный размер пула, клиентские запросы будут поставлены в очередь и получат первый доступный объект из пула на основе первого обслуживаемого.</span><span class="sxs-lookup"><span data-stu-id="c7e26-116">If the maximum pool size has been reached, client requests will be queued and will receive the first available object from the pool on a first-come first-served basis.</span></span> <span data-ttu-id="c7e26-117">Время ожидания запросов на создание объектов истекает через указанный период.</span><span class="sxs-lookup"><span data-stu-id="c7e26-117">Object creation requests will time-out after a specified period.</span></span>
-   <span data-ttu-id="c7e26-118">**Время ожидания создания (МС).**</span><span class="sxs-lookup"><span data-stu-id="c7e26-118">**Creation timeout (ms).**</span></span> <span data-ttu-id="c7e26-119">Указывает, как долго клиент будет ожидать в миллисекундах, чтобы объект был возвращен из пула после вызова [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="c7e26-119">Specifies how long a client will wait, in milliseconds, for an object to be returned from the pool after a call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="c7e26-120">Если клиентский вызов завершается неудачно, возвращается ошибка E \_ timeout.</span><span class="sxs-lookup"><span data-stu-id="c7e26-120">If the client call is unsuccessful, the error E\_TIMEOUT is returned.</span></span>

<span data-ttu-id="c7e26-121">**Задание свойств, связанных с пулом**</span><span class="sxs-lookup"><span data-stu-id="c7e26-121">**To set pooling-related properties**</span></span>

1.  <span data-ttu-id="c7e26-122">В области сведений средства администрирования "службы компонентов" щелкните правой кнопкой мыши компонент, который требуется настроить, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="c7e26-122">In the details pane of the Component Services administrative tool, right-click the component that you want to configure, and then click **Properties**.</span></span>

2.  <span data-ttu-id="c7e26-123">В диалоговом окне Свойства компонента перейдите на вкладку **Активация** .</span><span class="sxs-lookup"><span data-stu-id="c7e26-123">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="c7e26-124">Чтобы включить использование пула объектов для компонента, установите флажок **включить пул объектов** .</span><span class="sxs-lookup"><span data-stu-id="c7e26-124">To enable object pooling for the component, select the **Enable object pooling** check box.</span></span>

4.  <span data-ttu-id="c7e26-125">В поле **Минимальный размер пула** введите минимальное число объектов этого типа в пуле.</span><span class="sxs-lookup"><span data-stu-id="c7e26-125">In the **Minimum pool size** box, enter the minimum number of objects of this type in the pool.</span></span> <span data-ttu-id="c7e26-126">Для пула будет поддерживаться по крайней мере столько объектов.</span><span class="sxs-lookup"><span data-stu-id="c7e26-126">The pool will be maintained to have at least this many objects.</span></span>

5.  <span data-ttu-id="c7e26-127">В поле u введите максимальное число объектов этого типа в пуле.</span><span class="sxs-lookup"><span data-stu-id="c7e26-127">In the u box, enter the maximum number of objects of this type in the pool.</span></span> <span data-ttu-id="c7e26-128">Количество объектов, активированных и отключенных, никогда не будет превышать это значение.</span><span class="sxs-lookup"><span data-stu-id="c7e26-128">The number of objects, both activated and deactivated, will never exceed this value.</span></span>

6.  <span data-ttu-id="c7e26-129">В поле **время ожидания создания (МС)** введите время в миллисекундах, в течение которого клиент будет ожидать объект в пуле, если он недоступен немедленно.</span><span class="sxs-lookup"><span data-stu-id="c7e26-129">In the **Creation timeout (ms)** box, enter the amount of time, in milliseconds, a client will wait for a pooled object if one is not immediately available.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7e26-130">См. также</span><span class="sxs-lookup"><span data-stu-id="c7e26-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7e26-131">Мониторинг статистики объектов</span><span class="sxs-lookup"><span data-stu-id="c7e26-131">Monitoring Object Statistics</span></span>](monitoring-object-statistics.md)
</dt> </dl>

 

 
