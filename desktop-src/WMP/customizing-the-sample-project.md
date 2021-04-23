---
title: Настройка примера проекта
description: Настройка примера проекта
ms.assetid: 26031971-3d1b-4175-8fb3-f13b6c17dd01
keywords:
- Интернет-магазины проигрывателя Windows Media, Настройка образцов проектов
- Интернет-магазины, Настройка образцов проектов
- Тип 2 Интернет-магазинов, Настройка образцов проектов
- Интернет-магазины проигрывателя Windows Media, примеры проектов
- Интернет-магазины, примеры проектов
- Тип 2 Интернет-магазинов, примеры проектов
- Настройка образцов проектов
- Примеры, тип 2 Интернет-магазинов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aeec3ebcb74304cd5181783e9c457d6a149b0cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986763"
---
# <a name="customizing-the-sample-project"></a><span data-ttu-id="a076c-111">Настройка примера проекта</span><span class="sxs-lookup"><span data-stu-id="a076c-111">Customizing the Sample Project</span></span>

<span data-ttu-id="a076c-112">При создании собственного Интернет-магазина вам потребуется изменить реализации следующих методов в файле с именем Йоурпрожект. cpp:</span><span class="sxs-lookup"><span data-stu-id="a076c-112">When creating your own online store, you will want to change the implementations of the following methods in the file named YourProject.cpp:</span></span>

-   <span data-ttu-id="a076c-113">**Циаурпрожект:: алловплай**.</span><span class="sxs-lookup"><span data-stu-id="a076c-113">**CYourProject::allowPlay**.</span></span> <span data-ttu-id="a076c-114">Используйте эту функцию, чтобы применить бизнес-правила для воспроизведения защищенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="a076c-114">Use this function to apply your business rules for permitting playback of protected content.</span></span>
-   <span data-ttu-id="a076c-115">**Циаурпрожект:: Allow кдбурн**.</span><span class="sxs-lookup"><span data-stu-id="a076c-115">**CYourProject::allow CDBurn**.</span></span> <span data-ttu-id="a076c-116">Эта функция используется для применения бизнес-правил, позволяющих пользователям копировать защищенное содержимое на компакт-диск.</span><span class="sxs-lookup"><span data-stu-id="a076c-116">Use this function to apply your business rules for allowing users to copy protected content to a CD.</span></span>
-   <span data-ttu-id="a076c-117">**Циаурпрожект:: алловпдатрансфер**.</span><span class="sxs-lookup"><span data-stu-id="a076c-117">**CYourProject::allowPDATransfer**.</span></span> <span data-ttu-id="a076c-118">Эта функция используется для применения бизнес-правил, позволяющих пользователям передавать защищенное содержимое на портативное устройство.</span><span class="sxs-lookup"><span data-stu-id="a076c-118">Use this function to apply your business rules for allowing users to transfer protected content to a portable device.</span></span>
-   <span data-ttu-id="a076c-119">**Циаурпрожект:: стартбаккграундпроцессинг**.</span><span class="sxs-lookup"><span data-stu-id="a076c-119">**CYourProject::startBackgroundProcessing**.</span></span> <span data-ttu-id="a076c-120">Используйте эту функцию, чтобы инициировать все необходимые задачи фоновой обработки.</span><span class="sxs-lookup"><span data-stu-id="a076c-120">Use this function to initiate any background processing tasks you require.</span></span> <span data-ttu-id="a076c-121">Например, вы можете использовать эту возможность для проверки лицензий с истекшим сроком действия.</span><span class="sxs-lookup"><span data-stu-id="a076c-121">For example, you might use this as an opportunity to check for expired licenses.</span></span>
-   <span data-ttu-id="a076c-122">**Циаурпрожект::D евицеаваилабле**.</span><span class="sxs-lookup"><span data-stu-id="a076c-122">**CYourProject::deviceAvailable**.</span></span> <span data-ttu-id="a076c-123">Эта функция предназначена для запуска любых задач, связанных с подключенным устройством.</span><span class="sxs-lookup"><span data-stu-id="a076c-123">Use this function to initiate any tasks related to a connected device.</span></span>
-   <span data-ttu-id="a076c-124">**Циаурпрожект::P репарефорсинк**.</span><span class="sxs-lookup"><span data-stu-id="a076c-124">**CYourProject::prepareForSync**.</span></span> <span data-ttu-id="a076c-125">Эта функция используется для выполнения необходимых задач непосредственно перед синхронизацией цифровых носителей с устройством.</span><span class="sxs-lookup"><span data-stu-id="a076c-125">Use this function to perform necessary tasks just before synchronizing digital media to the device.</span></span>
-   <span data-ttu-id="a076c-126">**Циаурпрожект:: сервицеевент**.</span><span class="sxs-lookup"><span data-stu-id="a076c-126">**CYourProject::serviceEvent**.</span></span> <span data-ttu-id="a076c-127">Эта функция используется для начала и завершения задач, которые необходимо выполнить, когда Интернет-магазин активен.</span><span class="sxs-lookup"><span data-stu-id="a076c-127">Use this function to begin and end tasks that you want to run when your online store is the active one.</span></span>
-   <span data-ttu-id="a076c-128">**Циаурпрожект:: стопбаккграундпроцессинг**.</span><span class="sxs-lookup"><span data-stu-id="a076c-128">**CYourProject::stopBackgroundProcessing**.</span></span> <span data-ttu-id="a076c-129">Используйте эту функцию, чтобы отключить все задачи фоновой обработки, запущенные в проигрывателе Windows Media с именем **циаурпрожект:: стартбаккграундпроцессинг**.</span><span class="sxs-lookup"><span data-stu-id="a076c-129">Use this function to stop any background processing tasks you started when Windows Media Player called **CYourProject::startBackgroundProcessing**.</span></span>

## <a name="working-with-media-and-playlist-objects"></a><span data-ttu-id="a076c-130">Работа с объектами мультимедиа и списками воспроизведения</span><span class="sxs-lookup"><span data-stu-id="a076c-130">Working with Media and Playlist Objects</span></span>

<span data-ttu-id="a076c-131">Метод **алловплай** предоставляет указатель на интерфейс **ивмпмедиа** в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="a076c-131">The **allowPlay** method provides a pointer to the **IWMPMedia** interface as a parameter.</span></span> <span data-ttu-id="a076c-132">Этот интерфейс является интерфейсом проигрывателя Windows Media, представляющим мультимедийные объекты.</span><span class="sxs-lookup"><span data-stu-id="a076c-132">This interface is the Windows Media Player interface that represents media objects.</span></span> <span data-ttu-id="a076c-133">Вызывая методы для этого интерфейса, можно работать с атрибутами и свойствами отдельного элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a076c-133">By calling the methods on this interface, you can work with the attributes and properties of an individual media item.</span></span>

<span data-ttu-id="a076c-134">Методы **алловкдбурн** и **алловпдатрансфер** предоставляют указатель на интерфейс **ивмпплайлист** в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="a076c-134">The **allowCDBurn** and **allowPDATransfer** methods provide a pointer to the **IWMPPlaylist** interface as a parameter.</span></span> <span data-ttu-id="a076c-135">Этот интерфейс является интерфейсом проигрывателя Windows Media, представляющим объекты списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a076c-135">This interface is the Windows Media Player interface that represents playlist objects.</span></span> <span data-ttu-id="a076c-136">Вызывая методы этого интерфейса, можно работать с атрибутами и свойствами списка воспроизведения, добавлять элементы в список воспроизведения или удалять элементы из списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a076c-136">By calling the methods on this interface, you can work with the attributes and properties of a playlist, add items to a playlist, or remove items from a playlist.</span></span>

<span data-ttu-id="a076c-137">Сведения о том, как удалить элемент из списка воспроизведения программным способом, см. в разделе Реализация **калловбаседиалог <T> :: онремовемедиафромплайлист**.</span><span class="sxs-lookup"><span data-stu-id="a076c-137">To learn how to remove an item from a playlist programmatically, see the implementation of **CAllowBaseDialog<T>::OnRemoveMediaFromPlaylist**.</span></span> <span data-ttu-id="a076c-138">Дополнительные сведения о работе с объектами мультимедиа и списками воспроизведения см. в разделе [объектная модель проигрывателя для языков сценариев](player-object-model-for-scripting-languages.md).</span><span class="sxs-lookup"><span data-stu-id="a076c-138">To learn more about working with media and playlist objects, see [Player Object Model for Scripting Languages](player-object-model-for-scripting-languages.md).</span></span>

## <a name="code-that-can-be-removed"></a><span data-ttu-id="a076c-139">Код, который можно удалить</span><span class="sxs-lookup"><span data-stu-id="a076c-139">Code That Can Be Removed</span></span>

<span data-ttu-id="a076c-140">Вам, вероятно, потребуется удалить код, который открывает диалоговые окна, так как маловероятно, что пользователи будут выбирать, какие элементы мультимедиа можно воспроизвести или скопировать.</span><span class="sxs-lookup"><span data-stu-id="a076c-140">You will probably want to remove the code that opens dialog boxes because it is unlikely that you will want users deciding which media items can be played or copied.</span></span> <span data-ttu-id="a076c-141">В Йоурпрожект. h удалите следующий код:</span><span class="sxs-lookup"><span data-stu-id="a076c-141">From YourProject.h, remove the following code:</span></span>

-   <span data-ttu-id="a076c-142">Объявление **калловбаседиалог**.</span><span class="sxs-lookup"><span data-stu-id="a076c-142">The declaration of **CAllowBaseDialog**.</span></span>
-   <span data-ttu-id="a076c-143">Объявление **калловбурндиалог**.</span><span class="sxs-lookup"><span data-stu-id="a076c-143">The declaration of **CAllowBurnDialog**.</span></span>
-   <span data-ttu-id="a076c-144">Объявление **калловтрансфердиалог**.</span><span class="sxs-lookup"><span data-stu-id="a076c-144">The declaration of **CAllowTransferDialog**.</span></span>

<span data-ttu-id="a076c-145">Из Йоурпрожект. cpp удалите следующий код:</span><span class="sxs-lookup"><span data-stu-id="a076c-145">From YourProject.cpp, remove the following code:</span></span>

-   <span data-ttu-id="a076c-146">Реализация **калловбаседиалог <T> :: онинитдиалог**.</span><span class="sxs-lookup"><span data-stu-id="a076c-146">The implementation of **CAllowBaseDialog<T>::OnInitDialog**.</span></span>
-   <span data-ttu-id="a076c-147">Реализация **калловбаседиалог <T> :: онремовемедиафромплайлист**.</span><span class="sxs-lookup"><span data-stu-id="a076c-147">The implementation of **CAllowBaseDialog<T>::OnRemoveMediaFromPlaylist**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a076c-148">См. также</span><span class="sxs-lookup"><span data-stu-id="a076c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a076c-149">**Создание подключаемого модуля для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="a076c-149">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




