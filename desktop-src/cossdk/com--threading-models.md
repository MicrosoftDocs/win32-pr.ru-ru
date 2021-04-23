---
description: Модели потоков COM+ спроектированы вокруг коллекции объектов, называемой апартаментом. Подразделение — это коллекция контекстов, содержащихся в процессе.
ms.assetid: c73fb4c5-20ae-4873-afd2-4f40eb47bade
title: Модели потоков COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f07b065861c042e68add633368a9c8b8ba41b2
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "103819844"
---
# <a name="com-threading-models"></a><span data-ttu-id="1a7a5-104">Модели потоков COM+</span><span class="sxs-lookup"><span data-stu-id="1a7a5-104">COM+ Threading Models</span></span>

<span data-ttu-id="1a7a5-105">Модели потоков COM+ спроектированы вокруг коллекции объектов, называемой апартаментом.</span><span class="sxs-lookup"><span data-stu-id="1a7a5-105">COM+ threading models are designed around an object collection called an apartment.</span></span> <span data-ttu-id="1a7a5-106">Подразделение — это коллекция контекстов, содержащихся в процессе, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="1a7a5-106">An apartment is a collection of contexts contained in a process, as shown in the following illustration.</span></span>

![Схема, показывающая коллекцию контекстов в действии в пределах подразделения внутри процесса.](images/6b86fe3b-262a-483a-a418-67d60f9a5d68.png)

<span data-ttu-id="1a7a5-108">Вызовы в апартаменте являются прямыми, а вызовы между апартаментами (вне процесса) являются непрямыми и нуждаются в коде прокси-сервера и заглушки.</span><span class="sxs-lookup"><span data-stu-id="1a7a5-108">Calls within an apartment are direct, while calls across apartments (out-of-process) are indirect and require proxy and stub code.</span></span> <span data-ttu-id="1a7a5-109">Подразделения позволяют объектам с разными свойствами синхронизации и повторного входа и иметь две категории: однопотоковые и многопоточные.</span><span class="sxs-lookup"><span data-stu-id="1a7a5-109">Apartments allow for objects with different synchronization and reentrancy properties and have two categories: single-threaded and multithreaded.</span></span> <span data-ttu-id="1a7a5-110">Объекты в однопотоковом апартаменте (STA) выполняются в определенном потоке, в котором они были созданы.</span><span class="sxs-lookup"><span data-stu-id="1a7a5-110">Objects in a single-threaded apartment (STA) execute on the particular thread in which they were created.</span></span> <span data-ttu-id="1a7a5-111">STA допускают выполнение только одного метода за раз.</span><span class="sxs-lookup"><span data-stu-id="1a7a5-111">STAs allow only one method to execute at a time.</span></span> <span data-ttu-id="1a7a5-112">Они предназначены для пользовательских интерфейсов и используют очередь сообщений Microsoft Windows для обработки входящих вызовов.</span><span class="sxs-lookup"><span data-stu-id="1a7a5-112">They are designed for user interfaces and rely on the Microsoft Windows message queue to process incoming calls.</span></span>

<span data-ttu-id="1a7a5-113">Объекты в многопоточном апартаменте (MTA) выполняются в любом потоке и позволяют одновременно выполнять любое количество методов.</span><span class="sxs-lookup"><span data-stu-id="1a7a5-113">Objects in a multithreaded apartment (MTA) execute on any thread and allow any number of methods to occur simultaneously.</span></span> <span data-ttu-id="1a7a5-114">MTA поддерживает неявное перевход.</span><span class="sxs-lookup"><span data-stu-id="1a7a5-114">MTAs support reentrance implicitly.</span></span>

<span data-ttu-id="1a7a5-115">Классы COM+ помечены свойством **ThreadingModel** , которое позволяет COM+ создавать объект в надлежащем апартаменте.</span><span class="sxs-lookup"><span data-stu-id="1a7a5-115">COM+ classes are marked with a **ThreadingModel** property that allows COM+ to create the object in the proper apartment.</span></span> <span data-ttu-id="1a7a5-116">Чтобы определить, в каком апартаменте создается объект, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) использует свойство **ThreadingModel** .</span><span class="sxs-lookup"><span data-stu-id="1a7a5-116">To determine which apartment an object is created in, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) uses the **ThreadingModel** property.</span></span>

<span data-ttu-id="1a7a5-117">Потоки должны вызывать [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) , прежде чем они смогут использовать COM+.</span><span class="sxs-lookup"><span data-stu-id="1a7a5-117">Threads must call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) before they can use COM+.</span></span> <span data-ttu-id="1a7a5-118">При этом они создаются в правильном апартаменте и контексте.</span><span class="sxs-lookup"><span data-stu-id="1a7a5-118">This creates them inside the correct apartment and context.</span></span> <span data-ttu-id="1a7a5-119">Главный контейнер потока определяется как первый STA, вызываемый методом **CoInitializeEx**.</span><span class="sxs-lookup"><span data-stu-id="1a7a5-119">The main thread apartment is determined to be the first STA called by **CoInitializeEx**.</span></span> <span data-ttu-id="1a7a5-120">Обычно это связано с основным потоком процесса.</span><span class="sxs-lookup"><span data-stu-id="1a7a5-120">This is usually associated with the main thread of a process.</span></span> <span data-ttu-id="1a7a5-121">**CoInitializeEx** указывает тип подразделения, требуемого для потока, установив следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="1a7a5-121">**CoInitializeEx** indicates the type of apartment required by the thread by setting the following flags:</span></span>

-   <span data-ttu-id="1a7a5-122">**СОинициализация \_ Многопоточное — находит** поток в одном многопоточном апартаменте.</span><span class="sxs-lookup"><span data-stu-id="1a7a5-122">**COINIT\_MULTITHREADED**—Locates the thread in the single multithreaded apartment.</span></span>
-   <span data-ttu-id="1a7a5-123">**СОинициализация \_ АПАРТМЕНТСРЕАДЕД**— помещает поток в Новый STA.</span><span class="sxs-lookup"><span data-stu-id="1a7a5-123">**COINIT\_APARTMENTTHREADED**—Places the thread into a new STA.</span></span>

<span data-ttu-id="1a7a5-124">В следующих подразделах этого раздела приводятся дополнительные сведения об использовании потоков моделей и апартаментов в COM+.</span><span class="sxs-lookup"><span data-stu-id="1a7a5-124">The following topics in this section provide more information about using threading models and apartments in COM+:</span></span>

-   [<span data-ttu-id="1a7a5-125">Атрибут модели потоков</span><span class="sxs-lookup"><span data-stu-id="1a7a5-125">Threading Model Attribute</span></span>](threading-model-attribute.md)
-   [<span data-ttu-id="1a7a5-126">Нейтральные подразделения</span><span class="sxs-lookup"><span data-stu-id="1a7a5-126">Neutral Apartments</span></span>](neutral-apartments.md)

## <a name="related-topics"></a><span data-ttu-id="1a7a5-127">См. также</span><span class="sxs-lookup"><span data-stu-id="1a7a5-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a7a5-128">Процессы, потоки и подразделения</span><span class="sxs-lookup"><span data-stu-id="1a7a5-128">Processes, Threads, and Apartments</span></span>](/windows/desktop/com/processes--threads--and-apartments)
</dt> <dt>

[<span data-ttu-id="1a7a5-129">**ThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="1a7a5-129">**ThreadingModel**</span></span>](components.md)
</dt> </dl>

 

 
