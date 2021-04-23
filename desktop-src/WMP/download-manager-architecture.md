---
title: Архитектура диспетчера загрузки
description: Архитектура диспетчера загрузки
ms.assetid: cbd46bf2-613f-40ae-8506-2f3c5eb84ada
keywords:
- Интернет-магазины проигрывателя Windows Media, диспетчер загрузки
- Интернет-магазины, диспетчер загрузки
- Тип 2 Интернет-магазинов, диспетчер загрузки
- Проигрыватель Windows Media, диспетчер загрузки
- Диспетчер загрузки проигрывателя Windows Media
- Диспетчер загрузки
- Архитектура для диспетчера загрузки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0567c32430e0cc15ea589bed43e2e81ffb3a08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774096"
---
# <a name="download-manager-architecture"></a><span data-ttu-id="79926-110">Архитектура диспетчера загрузки</span><span class="sxs-lookup"><span data-stu-id="79926-110">Download Manager Architecture</span></span>

<span data-ttu-id="79926-111">Диспетчер загрузки проигрывателя Windows Media использует технологию COM.</span><span class="sxs-lookup"><span data-stu-id="79926-111">The Windows Media Player Download Manager uses COM technology.</span></span> <span data-ttu-id="79926-112">Функции по-прежнему пределяются в набор программных интерфейсов; можно написать программный код, использующий эти интерфейсы с помощью Microsoft JScript или C++.</span><span class="sxs-lookup"><span data-stu-id="79926-112">The functionality is distilled into a set of programming interfaces; you can write programming code that uses these interfaces by using Microsoft JScript or C++.</span></span>

<span data-ttu-id="79926-113">В языках сценариев для разделения функциональных возможностей программирования используется концепция объектов.</span><span class="sxs-lookup"><span data-stu-id="79926-113">The scripting languages use the concept of objects to divide programming functionality.</span></span> <span data-ttu-id="79926-114">Объектная модель **довнлоадманажер** использует несколько объектов для разделения методов и свойств на логическую организацию, которая группирует семантически связанные функции вместе.</span><span class="sxs-lookup"><span data-stu-id="79926-114">The **DownloadManager** object model uses several objects to divide the methods and properties into a logical organization that groups semantically related functions together.</span></span> <span data-ttu-id="79926-115">В следующих разделах содержатся сведения об объектах диспетчера загрузки.</span><span class="sxs-lookup"><span data-stu-id="79926-115">The following sections contain information about the Download Manager objects.</span></span>



| <span data-ttu-id="79926-116">Section</span><span class="sxs-lookup"><span data-stu-id="79926-116">Section</span></span>                                                                     | <span data-ttu-id="79926-117">Описание</span><span class="sxs-lookup"><span data-stu-id="79926-117">Description</span></span>                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79926-118">Сведения об объекте Довнлоадманажер</span><span class="sxs-lookup"><span data-stu-id="79926-118">About the DownloadManager Object</span></span>](#about-the-downloadmanager-object)       | <span data-ttu-id="79926-119">Объект **довнлоадманажер** представляет корневой объект для диспетчера загрузки проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="79926-119">The **DownloadManager** object represents the root object for the Windows Media Player Download Manager.</span></span> |
| [<span data-ttu-id="79926-120">Сведения об объекте Довнлоадколлектион</span><span class="sxs-lookup"><span data-stu-id="79926-120">About the DownloadCollection Object</span></span>](#about-the-downloadcollection-object) | <span data-ttu-id="79926-121">Объект **довнлоадколлектион** представляет коллекцию элементов загрузки.</span><span class="sxs-lookup"><span data-stu-id="79926-121">The **DownloadCollection** object represents a collection of download items.</span></span>                             |
| [<span data-ttu-id="79926-122">Сведения об объекте Довнлоадитем</span><span class="sxs-lookup"><span data-stu-id="79926-122">About the DownloadItem Object</span></span>](#about-the-downloaditem-object)             | <span data-ttu-id="79926-123">Объект **довнлоадитем** представляет отдельный запрос на скачивание.</span><span class="sxs-lookup"><span data-stu-id="79926-123">The **DownloadItem** object represents an individual download request.</span></span>                                   |



 

## <a name="about-the-downloadmanager-object"></a><span data-ttu-id="79926-124">Сведения об объекте Довнлоадманажер</span><span class="sxs-lookup"><span data-stu-id="79926-124">About the DownloadManager Object</span></span>

<span data-ttu-id="79926-125">**Довнлоадманажер** — это корневой объект для диспетчера загрузки проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="79926-125">**DownloadManager** is the root object for the Windows Media Player Download Manager.</span></span> <span data-ttu-id="79926-126">Доступ ко всем остальным объектам осуществляется через этот объект.</span><span class="sxs-lookup"><span data-stu-id="79926-126">All other objects are accessed through this object.</span></span> <span data-ttu-id="79926-127">Чтобы получить доступ к объекту **довнлоадманажер** , используйте следующий синтаксис JScript:</span><span class="sxs-lookup"><span data-stu-id="79926-127">To gain access to the **DownloadManager** object, use the following JScript syntax:</span></span>


```C++
var DownloadManager = external.DownloadManager;
```



<span data-ttu-id="79926-128">При этом создается экземпляр объекта **довнлоадманажер** , который затем можно использовать для получения дочерних объектов.</span><span class="sxs-lookup"><span data-stu-id="79926-128">This creates an instance of the **DownloadManager** object, which can then be used to retrieve the child objects.</span></span> <span data-ttu-id="79926-129">Например, следующий синтаксис извлекает первый элемент из коллекции загрузки с идентификатором 253675:</span><span class="sxs-lookup"><span data-stu-id="79926-129">For example, the following syntax retrieves the first item from the download collection that has id number 253675:</span></span>


```C++
var firstItem = DownloadManager.getDownloadCollection(253675).item(0);
```



## <a name="about-the-downloadcollection-object"></a><span data-ttu-id="79926-130">Сведения об объекте Довнлоадколлектион</span><span class="sxs-lookup"><span data-stu-id="79926-130">About the DownloadCollection Object</span></span>

<span data-ttu-id="79926-131">Объект **довнлоадколлектион** представляет коллекцию файлов для загрузки.</span><span class="sxs-lookup"><span data-stu-id="79926-131">The **DownloadCollection** object represents a collection of files to be downloaded.</span></span> <span data-ttu-id="79926-132">Этот объект можно использовать для определения количества загрузок в коллекции, удаления элементов из коллекции, получения определенного элемента загрузки и для запуска новой загрузки.</span><span class="sxs-lookup"><span data-stu-id="79926-132">You can use this object to determine how many downloads are in the collection, remove items from the collection, retrieve a specific download item, and to start a new download.</span></span> <span data-ttu-id="79926-133">При запуске новой загрузки автоматически добавляется скачивание в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="79926-133">Starting a new download automatically adds the download to the collection.</span></span>

## <a name="about-the-downloaditem-object"></a><span data-ttu-id="79926-134">Сведения об объекте Довнлоадитем</span><span class="sxs-lookup"><span data-stu-id="79926-134">About the DownloadItem Object</span></span>

<span data-ttu-id="79926-135">Объект **довнлоадитем** представляет отдельную загрузку.</span><span class="sxs-lookup"><span data-stu-id="79926-135">The **DownloadItem** object represents an individual download.</span></span> <span data-ttu-id="79926-136">Элементы скачивания всегда существуют в составе коллекции загрузки.</span><span class="sxs-lookup"><span data-stu-id="79926-136">Download items always exist as part of a download collection.</span></span> <span data-ttu-id="79926-137">Этот объект используется для получения сведений о загружаемом элементе, а также для приостановки, возобновления или отмены скачивания.</span><span class="sxs-lookup"><span data-stu-id="79926-137">Use this object to retrieve information about the download item and to pause, resume, or cancel the download in progress.</span></span>

<span data-ttu-id="79926-138">При отмене загрузки элемент скачивания остается на месте в коллекции загрузок.</span><span class="sxs-lookup"><span data-stu-id="79926-138">When you cancel a download, the download item remains in place in its download collection.</span></span> <span data-ttu-id="79926-139">В данном случае это **довнлоадколлектион**. **довнлоадстате** получает значение 4, означающее отмену.</span><span class="sxs-lookup"><span data-stu-id="79926-139">In this case, **downloadCollection**.**downloadState** retrieves a value of 4, meaning canceled.</span></span>

<span data-ttu-id="79926-140">Можно использовать **довнлоадитем**. **ход выполнения** для информирования пользователя о том, какая часть файла была перенесена или сколько осталось для загрузки.</span><span class="sxs-lookup"><span data-stu-id="79926-140">You can use **downloadItem**.**progress** to inform the user about how much of the file has been transferred or how much remains to be downloaded.</span></span> <span data-ttu-id="79926-141">Это значение можно использовать для оценки оставшегося времени.</span><span class="sxs-lookup"><span data-stu-id="79926-141">You might use this value to estimate the time remaining as well.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79926-142">См. также</span><span class="sxs-lookup"><span data-stu-id="79926-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79926-143">**Диспетчер загрузки**</span><span class="sxs-lookup"><span data-stu-id="79926-143">**Download Manager**</span></span>](download-manager.md)
</dt> </dl>

 

 




