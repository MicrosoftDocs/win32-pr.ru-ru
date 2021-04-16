---
title: Объект резервного хранилища архивации
description: Объект резервного хранилища архивации
ms.assetid: 83ce28c0-fd17-46ff-94c0-d28124a0e56a
keywords:
- Windows Media Format SDK, объекты резервного копирования
- Расширенный формат систем (ASF), объекты резервного копирования
- ASF (Расширенный системный формат), объекты восстановления резервных копий
- объекты, объекты резервного хранилища
- Резервное хранилище архивации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d08e8bec9bb7bbc2a45fbf632e69d230a2536633
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105672249"
---
# <a name="backup-restorer-object"></a><span data-ttu-id="aa812-108">Объект резервного хранилища архивации</span><span class="sxs-lookup"><span data-stu-id="aa812-108">Backup Restorer Object</span></span>

<span data-ttu-id="aa812-109">Средство резервного копирования предоставляет интерфейсы для управления резервными копиями лицензий, обычно на съемные носители, а затем восстанавливает их на новый компьютер.</span><span class="sxs-lookup"><span data-stu-id="aa812-109">The backup restorer provides interfaces to handle backing up licenses, typically onto removable media, and then restoring those licenses onto a new computer.</span></span>

<span data-ttu-id="aa812-110">Объект резервного хранилища создается функцией [**вмкреатебаккупресторер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) , которая устанавливает указатель на интерфейс [**ивмлиценсебаккуп**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) .</span><span class="sxs-lookup"><span data-stu-id="aa812-110">The backup restorer object is created by the [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) function, which sets a pointer to an [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) interface.</span></span> <span data-ttu-id="aa812-111">Другие интерфейсы объекта резервного хранилища можно получить, вызвав метод **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="aa812-111">The other interfaces of the backup restorer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="aa812-112">Объект резервного хранилища поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="aa812-112">The following interfaces are supported by the backup restorer object.</span></span>



| <span data-ttu-id="aa812-113">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="aa812-113">Interface</span></span>                                              | <span data-ttu-id="aa812-114">Описание</span><span class="sxs-lookup"><span data-stu-id="aa812-114">Description</span></span>                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa812-115">**ивмбаккупресторепропс**</span><span class="sxs-lookup"><span data-stu-id="aa812-115">**IWMBackupRestoreProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops) | <span data-ttu-id="aa812-116">Задает и получает свойства, необходимые для интерфейсов [**ивмлиценсебаккуп**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) и [**ивмлиценсересторе**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) .</span><span class="sxs-lookup"><span data-stu-id="aa812-116">Sets and retrieves properties required by the [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) and [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) interfaces.</span></span> |
| [<span data-ttu-id="aa812-117">**ивмлиценсебаккуп**</span><span class="sxs-lookup"><span data-stu-id="aa812-117">**IWMLicenseBackup**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)           | <span data-ttu-id="aa812-118">Резервное копирование лицензий, как правило, для их восстановления на другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="aa812-118">Backs up licenses, typically so that they can be restored onto another computer.</span></span>                                                                          |
| [<span data-ttu-id="aa812-119">**ивмлиценсересторе**</span><span class="sxs-lookup"><span data-stu-id="aa812-119">**IWMLicenseRestore**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)         | <span data-ttu-id="aa812-120">Восстанавливает лицензии.</span><span class="sxs-lookup"><span data-stu-id="aa812-120">Restores licenses.</span></span>                                                                                                                                        |



 

<span data-ttu-id="aa812-121">Для использования объекта резервного хранилища в приложении должен быть реализован следующий интерфейс обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="aa812-121">The following callback interface must be implemented by the application in order to use the backup restorer object.</span></span>



| <span data-ttu-id="aa812-122">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="aa812-122">Interface</span></span>                                      | <span data-ttu-id="aa812-123">Описание</span><span class="sxs-lookup"><span data-stu-id="aa812-123">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="aa812-124">**ивмстатускаллбакк**</span><span class="sxs-lookup"><span data-stu-id="aa812-124">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="aa812-125">Получает сообщения о состоянии от процессов, выполняемых в отдельном потоке.</span><span class="sxs-lookup"><span data-stu-id="aa812-125">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="aa812-126">См. также</span><span class="sxs-lookup"><span data-stu-id="aa812-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa812-127">**Резервное копирование и восстановление лицензий**</span><span class="sxs-lookup"><span data-stu-id="aa812-127">**Backing Up and Restoring Licenses**</span></span>](backing-up-and-restoring-licenses.md)
</dt> <dt>

[<span data-ttu-id="aa812-128">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="aa812-128">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




