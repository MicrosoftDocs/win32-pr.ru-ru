---
title: Резервное копирование и восстановление лицензий
description: Резервное копирование и восстановление лицензий
ms.assetid: 59be02fe-f207-4161-8765-9a88a8050248
keywords:
- Пакет SDK для Windows Media Format, резервное копирование лицензий
- Windows Media Format SDK, восстановление лицензий
- Пакет SDK для Windows Media Format, резервное копирование и восстановление лицензий
- Расширенный формат систем (ASF), резервное копирование лицензий
- ASF (Расширенный системный формат), резервное копирование лицензий
- Расширенный формат систем (ASF), восстановление лицензий
- ASF (Расширенный системный формат), восстановление лицензий
- Расширенный формат систем (ASF), резервное копирование и восстановление лицензий
- ASF (Расширенный системный формат), резервное копирование и восстановление лицензий
- Управление цифровыми правами (DRM), резервное копирование лицензий
- DRM (Управление цифровыми правами), резервное копирование лицензий
- Управление цифровыми правами (DRM), восстановление лицензий
- DRM (Управление цифровыми правами), восстановление лицензий
- Управление цифровыми правами (DRM), резервное копирование и восстановление лицензий
- DRM (Управление цифровыми правами), резервное копирование и восстановление лицензий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10d8e76c191225288a1021e08e4c77e7e14f3c6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788785"
---
# <a name="backing-up-and-restoring-licenses"></a><span data-ttu-id="5449e-118">Резервное копирование и восстановление лицензий</span><span class="sxs-lookup"><span data-stu-id="5449e-118">Backing Up and Restoring Licenses</span></span>

<span data-ttu-id="5449e-119">Процессы резервного копирования и восстановления являются асинхронными.</span><span class="sxs-lookup"><span data-stu-id="5449e-119">The backup and restore processes are asynchronous.</span></span> <span data-ttu-id="5449e-120">Они запускаются, когда пользователь выбирает команду меню или параметр в приложении для резервного копирования или восстановления лицензий.</span><span class="sxs-lookup"><span data-stu-id="5449e-120">They are triggered when the user selects a menu command or option in the application to back up or restore licenses.</span></span> <span data-ttu-id="5449e-121">Необходимо разрешить пользователю указывать расположения для резервного копирования и восстановления лицензий.</span><span class="sxs-lookup"><span data-stu-id="5449e-121">You should allow the user to specify the locations where licenses must be backed up to and restored from.</span></span>

<span data-ttu-id="5449e-122">Для резервного копирования лицензий выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5449e-122">To back up licenses:</span></span>

1.  <span data-ttu-id="5449e-123">Для создания объекта резервного хранилища используйте функцию [**вмкреатебаккупресторер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) .</span><span class="sxs-lookup"><span data-stu-id="5449e-123">Use the [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) function to create the backup restorer object.</span></span>
2.  <span data-ttu-id="5449e-124">Вызовите метод [**ивмбаккупресторепропс:: сбой setprop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) , чтобы задать путь резервного копирования (расположение, в котором будут записываться файлы, например: \\ или D: \\ Licenses).</span><span class="sxs-lookup"><span data-stu-id="5449e-124">Call the [**IWMBackupRestoreProps::SetProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) method to set the backup path (the location where you will write the files, such as A:\\ or D:\\Licenses).</span></span>
3.  <span data-ttu-id="5449e-125">Вызовите метод [**ивмлиценсебаккуп:: баккуплиценсес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) , чтобы создать резервную копию лицензий по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="5449e-125">Call the [**IWMLicenseBackup::BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) method to back up the licenses to the specified path.</span></span>

<span data-ttu-id="5449e-126">В метод [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) отправляются следующие события:</span><span class="sxs-lookup"><span data-stu-id="5449e-126">The following events are sent to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method:</span></span>

-   <span data-ttu-id="5449e-127">**ВМТ \_ БАККУПРЕСТОРЕ \_ Begin** указывает, что процесс резервного копирования запущен.</span><span class="sxs-lookup"><span data-stu-id="5449e-127">**WMT\_BACKUPRESTORE\_BEGIN** indicates the backup process has started.</span></span>
-   <span data-ttu-id="5449e-128">**ВМТ \_ БАККУПРЕСТОРЕ \_ конец** указывает, что процесс резервного копирования завершен.</span><span class="sxs-lookup"><span data-stu-id="5449e-128">**WMT\_BACKUPRESTORE\_END** indicates the backup process has been completed.</span></span>
-   <span data-ttu-id="5449e-129">**ВМТ \_ \_Лицензия с ограниченным доступом** указывает, что не удается создать резервную копию одной или нескольких лицензий, так как право владельца содержимого не разрешено.</span><span class="sxs-lookup"><span data-stu-id="5449e-129">**WMT\_RESTRICTED\_LICENSE** indicates that one or more licenses cannot be backed up because the right has been disallowed by the content owner.</span></span>

<span data-ttu-id="5449e-130">Идентификатор ключа также включается в сообщение.</span><span class="sxs-lookup"><span data-stu-id="5449e-130">The key ID is also included in this message.</span></span> <span data-ttu-id="5449e-131">Если вы реализовали базу данных для защищенных файлов, содержащую идентификатор ключа и метаданные, можно отобразить сообщение для пользователя с указанным названием (например, название песни), для которого невозможно создать резервную копию лицензии.</span><span class="sxs-lookup"><span data-stu-id="5449e-131">If you have implemented a database for protected files that includes the key ID and metadata, you can display a message to the user with the specific title (such as a song title) for which the license cannot be backed up.</span></span> <span data-ttu-id="5449e-132">В противном случае сообщение должно быть универсальным и информировать пользователя о том, что не удается создать резервную копию некоторых лицензий.</span><span class="sxs-lookup"><span data-stu-id="5449e-132">Otherwise, the message must be generic and inform the user that some licenses cannot be backed up.</span></span>

<span data-ttu-id="5449e-133">Чтобы восстановить лицензии, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5449e-133">To restore licenses:</span></span>

1.  <span data-ttu-id="5449e-134">Для создания объекта резервного хранилища используйте функцию **вмкреатебаккупресторер** .</span><span class="sxs-lookup"><span data-stu-id="5449e-134">Use the **WMCreateBackupRestorer** function to create the backup restorer object.</span></span>
2.  <span data-ttu-id="5449e-135">Вызовите метод **ивмбаккупресторепропс:: сбой setprop** , чтобы задать путь восстановления к расположению, в котором выполняется резервное копирование лицензий.</span><span class="sxs-lookup"><span data-stu-id="5449e-135">Call the **IWMBackupRestoreProps::SetProp** method to set the restore path to the location where licenses are backed up.</span></span>
3.  <span data-ttu-id="5449e-136">Вызовите метод [**ивмлиценсересторе:: ресторелиценсес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) , чтобы восстановить лицензии из этого расположения.</span><span class="sxs-lookup"><span data-stu-id="5449e-136">Call the [**IWMLicenseRestore::RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) method to restore licenses from that location.</span></span>

<span data-ttu-id="5449e-137">В метод [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) отправляются следующие события:</span><span class="sxs-lookup"><span data-stu-id="5449e-137">The following events are sent to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method:</span></span>

-   <span data-ttu-id="5449e-138">**ВМТ \_ \_Подключение баккупресторе** указывает, что приложение подключается к службе управления лицензиями.</span><span class="sxs-lookup"><span data-stu-id="5449e-138">**WMT\_BACKUPRESTORE\_CONNECTING** indicates that the application is connecting to the License Management Service.</span></span>
-   <span data-ttu-id="5449e-139">**ВМТ \_ БАККУПРЕСТОРЕ \_ Отключение** указывает, что приложение отключается от службы управления лицензиями.</span><span class="sxs-lookup"><span data-stu-id="5449e-139">**WMT\_BACKUPRESTORE\_DISCONNECTING** indicates that the application is disconnecting from the License Management Service.</span></span>
-   <span data-ttu-id="5449e-140">**ВМТ \_ БАККУПРЕСТОРЕ \_ Begin** указывает, что процесс восстановления запущен.</span><span class="sxs-lookup"><span data-stu-id="5449e-140">**WMT\_BACKUPRESTORE\_BEGIN** indicates the restore process has started.</span></span>
-   <span data-ttu-id="5449e-141">**ВМТ \_ БАККУПРЕСТОРЕ \_** указывает на завершение процесса восстановления.</span><span class="sxs-lookup"><span data-stu-id="5449e-141">**WMT\_BACKUPRESTORE\_END** indicates the restore process has been completed.</span></span>

> [!Note]  
> <span data-ttu-id="5449e-142">DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="5449e-142">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5449e-143">См. также</span><span class="sxs-lookup"><span data-stu-id="5449e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5449e-144">**Функции цифровых Rights Management**</span><span class="sxs-lookup"><span data-stu-id="5449e-144">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="5449e-145">**Интерфейс Ивмбаккупресторепропс**</span><span class="sxs-lookup"><span data-stu-id="5449e-145">**IWMBackupRestoreProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops)
</dt> <dt>

[<span data-ttu-id="5449e-146">**Интерфейс Ивмлиценсебаккуп**</span><span class="sxs-lookup"><span data-stu-id="5449e-146">**IWMLicenseBackup Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)
</dt> <dt>

[<span data-ttu-id="5449e-147">**Интерфейс Ивмлиценсересторе**</span><span class="sxs-lookup"><span data-stu-id="5449e-147">**IWMLicenseRestore Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)
</dt> </dl>

 

 




