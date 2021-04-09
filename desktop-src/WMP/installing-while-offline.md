---
title: Установка в автономном режиме
description: Установка в автономном режиме
ms.assetid: 29d80b6b-161d-44a7-b91e-70766b849c55
keywords:
- Интернет-магазины проигрывателя Windows Media, установка в автономном режиме
- Интернет-магазины, установка в автономном режиме
- Введите 1 Интернет-магазины, установка в автономном режиме
- Тип 2. Интернет-магазины, установка в автономном режиме
- Интернет-магазины проигрывателя Windows Media, установка в автономном режиме
- Интернет-магазины, установка в автономном режиме
- Тип 1 Интернет-магазины, установки вне сети
- Тип 2 Интернет-магазинов, автономные установки
- Установка Интернет-магазинов в автономном режиме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cad7048926f218ea7be74a2522eb32c58241a017
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888600"
---
# <a name="installing-while-offline"></a><span data-ttu-id="c9f22-112">Установка в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="c9f22-112">Installing While Offline</span></span>

<span data-ttu-id="c9f22-113">Пользователи могут установить проигрыватель Windows Media, не подключенный к Интернету.</span><span class="sxs-lookup"><span data-stu-id="c9f22-113">Users can install Windows Media Player while not connected to the Internet.</span></span> <span data-ttu-id="c9f22-114">В этом случае программа установки проигрывателя Windows Media находит ServiceInfo.xml документ, указанный параметром командной строки *serviceInfo* .</span><span class="sxs-lookup"><span data-stu-id="c9f22-114">When this happens, Windows Media Player setup locates the ServiceInfo.xml document specified by the *ServiceInfo* command line parameter.</span></span> <span data-ttu-id="c9f22-115">Если **ключевой** атрибут соответствует параметру командной строки *дефаултсервице* , программа установки применяет сведения из следующих элементов к проигрывателю Windows Media:</span><span class="sxs-lookup"><span data-stu-id="c9f22-115">If the **Key** attribute matches the *DefaultService* command line parameter, setup applies information from the following elements to Windows Media Player:</span></span>

-   <span data-ttu-id="c9f22-116">FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="c9f22-116">FriendlyName.</span></span> <span data-ttu-id="c9f22-117">Понятное имя Интернет-магазина отображается в пользовательском интерфейсе проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c9f22-117">The friendly name of the online store is shown in the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="c9f22-118">Цвет.</span><span class="sxs-lookup"><span data-stu-id="c9f22-118">Color.</span></span> <span data-ttu-id="c9f22-119">Указанные цвета применяются к панели задач и кнопкам.</span><span class="sxs-lookup"><span data-stu-id="c9f22-119">The specified colors are applied to the taskbar and buttons.</span></span>
-   <span data-ttu-id="c9f22-120">ServiceTask1, ServiceTask2 и ServiceTask3.</span><span class="sxs-lookup"><span data-stu-id="c9f22-120">ServiceTask1, ServiceTask2, and ServiceTask3.</span></span> <span data-ttu-id="c9f22-121">Дочерние элементы ButtonText и Буттонтип задаются.</span><span class="sxs-lookup"><span data-stu-id="c9f22-121">The ButtonText and ButtonTip child elements are set.</span></span> <span data-ttu-id="c9f22-122">Атрибут URL-адреса не задан.</span><span class="sxs-lookup"><span data-stu-id="c9f22-122">The URL attribute is not set.</span></span> <span data-ttu-id="c9f22-123">URL-адрес задается после того, как пользователь подключается к Интернету, и проигрыватель Windows Media извлекает свой список интернет-магазинов обычным образом.</span><span class="sxs-lookup"><span data-stu-id="c9f22-123">URL is set once the user connects to the Internet and Windows Media Player retrieves its list of online stores in the normal fashion.</span></span>
-   <span data-ttu-id="c9f22-124">Изображение.</span><span class="sxs-lookup"><span data-stu-id="c9f22-124">Image.</span></span> <span data-ttu-id="c9f22-125">Задаются атрибуты Менуурл и Сервицеларжеурл.</span><span class="sxs-lookup"><span data-stu-id="c9f22-125">The MenuURL and ServiceLargeURL attributes are set.</span></span> <span data-ttu-id="c9f22-126">Эти URL-адреса должны указывать на образы, установленные на жестком диске пользователя с помощью протокола file://.</span><span class="sxs-lookup"><span data-stu-id="c9f22-126">These URLs must point to images you installed on the user's hard disk by using the file:// protocol.</span></span>

<span data-ttu-id="c9f22-127">Когда пользователь пытается просмотреть Интернет-магазин, проигрыватель Windows Media выводит сообщение с уведомлением о том, что требуется подключение к Интернету.</span><span class="sxs-lookup"><span data-stu-id="c9f22-127">When the user attempts to view the online store, Windows Media Player displays a message informing the user that an Internet connection is required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9f22-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c9f22-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9f22-129">**Элемент Color**</span><span class="sxs-lookup"><span data-stu-id="c9f22-129">**Color Element**</span></span>](color-element.md)
</dt> <dt>

[<span data-ttu-id="c9f22-130">**FriendlyName, элемент**</span><span class="sxs-lookup"><span data-stu-id="c9f22-130">**FriendlyName Element**</span></span>](friendlyname-element.md)
</dt> <dt>

[<span data-ttu-id="c9f22-131">**Элемент Image**</span><span class="sxs-lookup"><span data-stu-id="c9f22-131">**Image Element**</span></span>](image-element.md)
</dt> <dt>

[<span data-ttu-id="c9f22-132">**Сведения, общие для типа 1 и 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="c9f22-132">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="c9f22-133">**ServiceInfo, элемент**</span><span class="sxs-lookup"><span data-stu-id="c9f22-133">**ServiceInfo Element**</span></span>](serviceinfo-element.md)
</dt> <dt>

[<span data-ttu-id="c9f22-134">**ServiceTask1, элемент**</span><span class="sxs-lookup"><span data-stu-id="c9f22-134">**ServiceTask1 Element**</span></span>](servicetask1-element.md)
</dt> <dt>

[<span data-ttu-id="c9f22-135">**ServiceTask2, элемент**</span><span class="sxs-lookup"><span data-stu-id="c9f22-135">**ServiceTask2 Element**</span></span>](servicetask2-element.md)
</dt> <dt>

[<span data-ttu-id="c9f22-136">**ServiceTask3, элемент**</span><span class="sxs-lookup"><span data-stu-id="c9f22-136">**ServiceTask3 Element**</span></span>](servicetask3-element.md)
</dt> <dt>

[<span data-ttu-id="c9f22-137">**Настройка начального Интернет-магазина**</span><span class="sxs-lookup"><span data-stu-id="c9f22-137">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> <dt>

[<span data-ttu-id="c9f22-138">**Параметры командной строки программы установки для Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="c9f22-138">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




