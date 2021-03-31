---
title: Использование диспетчера загрузки
description: Использование диспетчера загрузки
ms.assetid: f332a981-727f-4abc-a84e-76ab3e72b7f2
keywords:
- Интернет-магазины проигрывателя Windows Media, диспетчер загрузки
- Интернет-магазины, диспетчер загрузки
- Тип 2 Интернет-магазинов, диспетчер загрузки
- Проигрыватель Windows Media, диспетчер загрузки
- Диспетчер загрузки проигрывателя Windows Media
- Диспетчер загрузки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecb7b99ae36d3881fdf80eaad7d851205b9b2e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411401"
---
# <a name="using-the-download-manager"></a><span data-ttu-id="bf73e-109">Использование диспетчера загрузки</span><span class="sxs-lookup"><span data-stu-id="bf73e-109">Using the Download Manager</span></span>

<span data-ttu-id="bf73e-110">Пакет SDK проигрывателя Windows Media включает образец веб-страницы, демонстрирующий использование диспетчера загрузки для загрузки файлов на компьютер пользователя.</span><span class="sxs-lookup"><span data-stu-id="bf73e-110">The Windows Media Player SDK includes a sample webpage that demonstrates using the Download Manager to download files to the user's computer.</span></span> <span data-ttu-id="bf73e-111">Пример можно узнать в папке с именем веб-страницы, на которой установлен пакет SDK.</span><span class="sxs-lookup"><span data-stu-id="bf73e-111">You can locate the sample in the folder named WebPage where you installed the SDK.</span></span> <span data-ttu-id="bf73e-112">Имя файла — Sample. ASP.</span><span class="sxs-lookup"><span data-stu-id="bf73e-112">The name of the file is sample.asp.</span></span> <span data-ttu-id="bf73e-113">Образец предоставляет следующие функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="bf73e-113">The sample provides the following functionality:</span></span>

-   <span data-ttu-id="bf73e-114">Создает объект **довнлоадманажер** .</span><span class="sxs-lookup"><span data-stu-id="bf73e-114">Creates the **DownloadManager** object.</span></span>
-   <span data-ttu-id="bf73e-115">Создает объект **довнлоадколлектион** .</span><span class="sxs-lookup"><span data-stu-id="bf73e-115">Creates a **DownloadCollection** object.</span></span>
-   <span data-ttu-id="bf73e-116">Начинает загрузку пяти файлов при нажатии пользователем кнопки **загрузить**.</span><span class="sxs-lookup"><span data-stu-id="bf73e-116">Starts downloading five files when the user clicks **Download**.</span></span> <span data-ttu-id="bf73e-117">Пути к файлам по умолчанию приведены в примере.</span><span class="sxs-lookup"><span data-stu-id="bf73e-117">Default file paths are provided in the sample.</span></span> <span data-ttu-id="bf73e-118">Эти пути по умолчанию следует заменить расположением файлов на собственном сервере.</span><span class="sxs-lookup"><span data-stu-id="bf73e-118">You should replace these default paths with the locations of files on your own server.</span></span> <span data-ttu-id="bf73e-119">Можно изменить пути, изменив значения, назначенные глобальному массиву с именем g \_ сфилес.</span><span class="sxs-lookup"><span data-stu-id="bf73e-119">You can change the paths by changing the values assigned to the global array named g\_sFiles.</span></span>
-   <span data-ttu-id="bf73e-120">Отображает сведения о состоянии загрузки, когда пользователь выбирает его.</span><span class="sxs-lookup"><span data-stu-id="bf73e-120">Shows status information for a download when the user selects it.</span></span>
-   <span data-ttu-id="bf73e-121">Предоставляет элементы управления для приостановки, возобновления, отмены и удаления элемента загрузки.</span><span class="sxs-lookup"><span data-stu-id="bf73e-121">Provides controls to pause, resume, cancel, and remove a download item.</span></span>
-   <span data-ttu-id="bf73e-122">Хранит сведения о скачивании коллекций между сеансами с помощью файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="bf73e-122">Maintains information about download collections between sessions by using cookies.</span></span> <span data-ttu-id="bf73e-123">Это важно, так как пользователь может закрыть проигрыватель в любое время.</span><span class="sxs-lookup"><span data-stu-id="bf73e-123">This is important because the user can close the Player at any time.</span></span> <span data-ttu-id="bf73e-124">Кроме того, если пользователь переключает области задач в проигрывателе, сеанс Интернет-магазина завершается.</span><span class="sxs-lookup"><span data-stu-id="bf73e-124">Also, if the user switches task panes in the Player, the online store session ends.</span></span>
-   <span data-ttu-id="bf73e-125">По умолчанию использует загрузку в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="bf73e-125">Uses real-time downloading by default.</span></span> <span data-ttu-id="bf73e-126">Вы можете изменить поведение фоновой загрузки, изменив значение переменной с именем g \_ сдлтипе.</span><span class="sxs-lookup"><span data-stu-id="bf73e-126">You can change the behavior to background downloading by changing the value of the variable named g\_sDLType.</span></span> <span data-ttu-id="bf73e-127">Фоновая загрузка доступна для использования с операционной системой Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bf73e-127">Background downloading is available for use with the Microsoft Windows XP operating system.</span></span>
-   <span data-ttu-id="bf73e-128">Синхронизирует цвет фона с цветом проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="bf73e-128">Synchronizes the background color with the Player color.</span></span> <span data-ttu-id="bf73e-129">Эту функцию можно использовать для изменения внешнего вида Интернет-магазина, когда пользователь решает изменить цвет проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="bf73e-129">You can use this feature to make your online store change appearance when the user chooses to change the color of the Player.</span></span>

<span data-ttu-id="bf73e-130">Дополнительные сведения приведены в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bf73e-130">The following sections provide more information:</span></span>

-   [<span data-ttu-id="bf73e-131">Инициализация страницы</span><span class="sxs-lookup"><span data-stu-id="bf73e-131">Initializing the Page</span></span>](initializing-the-page.md)
-   [<span data-ttu-id="bf73e-132">Начало загрузки</span><span class="sxs-lookup"><span data-stu-id="bf73e-132">Starting the Downloads</span></span>](starting-the-downloads.md)
-   [<span data-ttu-id="bf73e-133">Получение сведений о состоянии</span><span class="sxs-lookup"><span data-stu-id="bf73e-133">Retrieving Status Information</span></span>](retrieving-status-information.md)
-   [<span data-ttu-id="bf73e-134">Обслуживание сведений о сеансе</span><span class="sxs-lookup"><span data-stu-id="bf73e-134">Maintaining Session Information</span></span>](maintaining-session-information.md)
-   [<span data-ttu-id="bf73e-135">Отладка страницы</span><span class="sxs-lookup"><span data-stu-id="bf73e-135">Debugging the Page</span></span>](debugging-the-page.md)

## <a name="related-topics"></a><span data-ttu-id="bf73e-136">См. также</span><span class="sxs-lookup"><span data-stu-id="bf73e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf73e-137">**Инструкции по программированию для Интернет-магазинов типа 2**</span><span class="sxs-lookup"><span data-stu-id="bf73e-137">**Programming Guide for Type 2 Online Stores**</span></span>](programming-guide-for-type-2-online-stores.md)
</dt> </dl>

 

 




