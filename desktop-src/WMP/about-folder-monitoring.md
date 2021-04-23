---
title: О мониторинге папок
description: О мониторинге папок
ms.assetid: d3d83e60-ecc7-4501-a6dd-15f7680a6ec9
keywords:
- Проигрыватель Windows Media, мониторинг папок
- Объектная модель проигрывателя Windows Media, мониторинг папок
- Объектная модель, мониторинг папок
- Элемент управления ActiveX проигрывателя Windows Media, мониторинг папок
- Элемент управления ActiveX, мониторинг папок
- Элемент управления ActiveX мобильных устройств проигрывателя Windows Media, мониторинг папок
- Проигрыватель Windows Media Mobile, мониторинг папок
- мониторинг папок
- мониторинг папок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3d6af341df706cd85c4158197b27babad09c86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412474"
---
# <a name="about-folder-monitoring"></a><span data-ttu-id="e86fb-112">О мониторинге папок</span><span class="sxs-lookup"><span data-stu-id="e86fb-112">About Folder Monitoring</span></span>

<span data-ttu-id="e86fb-113">Проигрыватель Windows Media может отслеживать папки, содержащие цифровые файлы мультимедиа, и обновлять библиотеку при добавлении или удалении файлов.</span><span class="sxs-lookup"><span data-stu-id="e86fb-113">Windows Media Player can monitor folders that contain digital media files and update the library when files are added or removed.</span></span> <span data-ttu-id="e86fb-114">Эта функция мониторинга папок обеспечивается интерфейсом [ивмпфолдермониторсервицес](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) .</span><span class="sxs-lookup"><span data-stu-id="e86fb-114">This folder monitoring functionality is provided by the [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) interface.</span></span>

<span data-ttu-id="e86fb-115">Чтобы использовать службы наблюдения за папками, необходимо создать объект Player в удаленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="e86fb-115">To use the folder monitoring services, you must create the Player object in a remote state.</span></span> <span data-ttu-id="e86fb-116">Дополнительные сведения об удаленном взаимодействии см. [в разделе Удаленное взаимодействие с элементом управления проигрывателя Windows Media](remoting-the-windows-media-player-control.md).</span><span class="sxs-lookup"><span data-stu-id="e86fb-116">For more information about remoting, see [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).</span></span> <span data-ttu-id="e86fb-117">После создания удаленного экземпляра проигрывателя получите указатель на интерфейс **ивмпфолдермониторсервицес** , вызвав **QueryInterface** в интерфейсе [ивмпплайер](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) .</span><span class="sxs-lookup"><span data-stu-id="e86fb-117">After you have created a remoted instance of the player, obtain a pointer to the **IWMPFolderMonitorServices** interface by calling **QueryInterface** on the [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) interface.</span></span>

<span data-ttu-id="e86fb-118">Проигрыватель Windows Media хранит список отслеживаемых папок.</span><span class="sxs-lookup"><span data-stu-id="e86fb-118">Windows Media Player keeps a list of folders that are being monitored.</span></span> <span data-ttu-id="e86fb-119">Чтобы получить список наблюдаемых папок, используйте методы [ивмпфолдермониторсервицес:: Get \_ Count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) и [ивмпфолдермониторсервицес:: Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) .</span><span class="sxs-lookup"><span data-stu-id="e86fb-119">To get a list of monitored folders, use the [IWMPFolderMonitorServices::get\_count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) and [IWMPFolderMonitorServices::item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) methods.</span></span> <span data-ttu-id="e86fb-120">Чтобы добавить папки в список или удалить их из списка, используйте методы [ивмпфолдермониторсервицес:: Add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) и [Remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) соответственно.</span><span class="sxs-lookup"><span data-stu-id="e86fb-120">To add folders to the list or remove them from the list, use the [IWMPFolderMonitorServices::add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) and [remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) methods, respectively.</span></span>

<span data-ttu-id="e86fb-121">**Запуск проверки**</span><span class="sxs-lookup"><span data-stu-id="e86fb-121">**Starting a Scan**</span></span>

<span data-ttu-id="e86fb-122">Наблюдение за папками обычно является фоновым процессом, который не требуется вызывать явным образом.</span><span class="sxs-lookup"><span data-stu-id="e86fb-122">Monitoring of folders is normally a background process that does not need to be called explicitly.</span></span> <span data-ttu-id="e86fb-123">Если вы хотите активно сканировать папку, вызовите [ивмпфолдермониторсервицес:: стартскан](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan).</span><span class="sxs-lookup"><span data-stu-id="e86fb-123">If you want to actively scan a folder, call [IWMPFolderMonitorServices::startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan).</span></span> <span data-ttu-id="e86fb-124">Вы можете прерывать выполнение проверки с помощью метода [ивмпфолдермониторсервицес:: стопскан](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) .</span><span class="sxs-lookup"><span data-stu-id="e86fb-124">You can stop a scan in progress with the [IWMPFolderMonitorServices::stopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) method.</span></span>

<span data-ttu-id="e86fb-125">**Получение состояния мониторинга папки**</span><span class="sxs-lookup"><span data-stu-id="e86fb-125">**Retrieving the Folder Monitoring Status**</span></span>

<span data-ttu-id="e86fb-126">**Ивмпфолдермониторсервицес** предоставляет функциональные возможности для получения состояния процесса наблюдения за папками.</span><span class="sxs-lookup"><span data-stu-id="e86fb-126">**IWMPFolderMonitorServices** provides functionality for retrieving the status of the folder monitoring process.</span></span>

<span data-ttu-id="e86fb-127">Сканирование папок выполняется в два прохода.</span><span class="sxs-lookup"><span data-stu-id="e86fb-127">Folder scanning is done in two passes.</span></span> <span data-ttu-id="e86fb-128">При первом прохождении проигрыватель сканирует папки, имена которых находятся в списке наблюдаемых папок, по одному и создает список файлов, которые будут добавлены в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="e86fb-128">In the first pass, the Player scans the folders named in the monitored folders list one by one and builds a list of files to be added to the library.</span></span> <span data-ttu-id="e86fb-129">Во втором прохождении он просматривает список файлов и добавляет файлы в библиотеку, а также удаляет все элементы мультимедиа из библиотеки, соответствующие физические файлы которой были удалены из файловой системы.</span><span class="sxs-lookup"><span data-stu-id="e86fb-129">In the second pass, it goes through the list of files and adds the files to the library, and also removes any media items from the library whose corresponding physical files have been deleted from the file system.</span></span>

<span data-ttu-id="e86fb-130">Событие [фолдерсканстатечанже](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) используется для уведомления программы при каждом переключении проигрывателя на новое состояние.</span><span class="sxs-lookup"><span data-stu-id="e86fb-130">The [FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) event is used to notify your program whenever the Player switches to a new state.</span></span> <span data-ttu-id="e86fb-131">Можно также получить текущее состояние, вызвав [Get \_ scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate).</span><span class="sxs-lookup"><span data-stu-id="e86fb-131">You can also retrieve the current state by calling [get\_scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate).</span></span> <span data-ttu-id="e86fb-132">При запуске первого прохода текущее значение состояния — Вмпфсссканнинг.</span><span class="sxs-lookup"><span data-stu-id="e86fb-132">When the first pass starts, the current state value is wmpfssScanning.</span></span> <span data-ttu-id="e86fb-133">Во время второго прохода состояние переключается на Вмпфссупдатинг.</span><span class="sxs-lookup"><span data-stu-id="e86fb-133">During the second pass, the state switches to wmpfssUpdating.</span></span> <span data-ttu-id="e86fb-134">После завершения процесса состояние изменится на Вмпфссстоппед.</span><span class="sxs-lookup"><span data-stu-id="e86fb-134">After the process is finished, the state changes to wmpfssStopped.</span></span>

<span data-ttu-id="e86fb-135">Пока проигрыватель сканирует отслеживаемые папки на первом этапе, вызовите [Get \_ сканнедфилескаунт](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) , чтобы проверить количество проверенных файлов.</span><span class="sxs-lookup"><span data-stu-id="e86fb-135">While the Player is scanning the monitored folders on the first pass, call [get\_scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) to check how many files have been scanned.</span></span> <span data-ttu-id="e86fb-136">Метод [Get \_ куррентфолдер](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) будет указывать, в какой папке в данный момент выполняется сканирование.</span><span class="sxs-lookup"><span data-stu-id="e86fb-136">The [get\_currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) method will tell you which folder is currently being scanned.</span></span>

<span data-ttu-id="e86fb-137">После запуска второго прохода вызовите [Get \_ аддедфилескаунт](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) , чтобы проверить, сколько файлов было добавлено в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="e86fb-137">After the second pass starts, call [get\_addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) to check how many files have been added to the library.</span></span> <span data-ttu-id="e86fb-138">Метод [Get \_ updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) сообщит о ходе выполнения второго прохода в процентах от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="e86fb-138">The [get\_updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) method will tell you the progress of the second pass, as a percentage from 0 to 100.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e86fb-139">См. также</span><span class="sxs-lookup"><span data-stu-id="e86fb-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e86fb-140">**Сведения об объектной модели проигрывателя**</span><span class="sxs-lookup"><span data-stu-id="e86fb-140">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="e86fb-141">**Интерфейс Ивмпфолдермониторсервицес**</span><span class="sxs-lookup"><span data-stu-id="e86fb-141">**IWMPFolderMonitorServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
</dt> </dl>

 

 




