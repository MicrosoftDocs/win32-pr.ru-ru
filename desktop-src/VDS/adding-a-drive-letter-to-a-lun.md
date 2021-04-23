---
description: Добавление буквы диска к LUN
ms.assetid: 3f350312-3f1f-4020-90d0-85521ea9c7c8
title: Добавление буквы диска к LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426a4f3bf720b21a02462edde4a381012d2084d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692220"
---
# <a name="adding-a-drive-letter-to-a-lun"></a><span data-ttu-id="61f23-103">Добавление буквы диска к LUN</span><span class="sxs-lookup"><span data-stu-id="61f23-103">Adding a Drive Letter to a LUN</span></span>

<span data-ttu-id="61f23-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="61f23-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="61f23-105">Буквы дисков можно назначать объектам томов напрямую; Однако если диск является объектом LUN, вы можете выполнить несколько дополнительных действий.</span><span class="sxs-lookup"><span data-stu-id="61f23-105">You can assign drive letters to volume objects directly; however, if your disk is a LUN object, you have a few additional steps.</span></span>

<span data-ttu-id="61f23-106">**Назначение буквы диска объекту LUN**</span><span class="sxs-lookup"><span data-stu-id="61f23-106">**To assign a drive letter to a LUN object**</span></span>

1.  <span data-ttu-id="61f23-107">При необходимости снимите маску LUN для локального узла.</span><span class="sxs-lookup"><span data-stu-id="61f23-107">If necessary, unmask the LUN to the local host.</span></span>
    > [!Note]  
    > <span data-ttu-id="61f23-108">Вы не можете выполнять административные операции с объектом LUN, который снят с маски на другой компьютер в текущем сеансе службы VDS.</span><span class="sxs-lookup"><span data-stu-id="61f23-108">You cannot perform software administrative operations on a LUN object that is unmasked to another computer within the current VDS session.</span></span>

     

2.  <span data-ttu-id="61f23-109">Вызовите метод [**ивдссервице:: reenumerat**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) на компьютере, на котором работает поставщик оборудования.</span><span class="sxs-lookup"><span data-stu-id="61f23-109">Invoke the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method on the computer that is running the hardware provider.</span></span>
3.  <span data-ttu-id="61f23-110">Инициализируйте LUN как базовый диск следующим образом:</span><span class="sxs-lookup"><span data-stu-id="61f23-110">Initialize the LUN as a basic disk as follows:</span></span>
    1.  <span data-ttu-id="61f23-111">Вызовите метод [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) объекта LUN, чтобы запросить интерфейс [**ивдсдиск**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) .</span><span class="sxs-lookup"><span data-stu-id="61f23-111">Invoke the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the LUN object to query for the [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) interface.</span></span>
    2.  <span data-ttu-id="61f23-112">Чтобы создать базовый пакет, вызовите метод [**ивдссвпровидер:: креатепакк**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) .</span><span class="sxs-lookup"><span data-stu-id="61f23-112">Invoke the [**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) method to create a basic pack.</span></span>
    3.  <span data-ttu-id="61f23-113">Вызовите метод [**ивдспакк:: адддиск**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) , чтобы добавить диск в новый пакет.</span><span class="sxs-lookup"><span data-stu-id="61f23-113">Invoke the [**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) method to add the disk to the new pack.</span></span>
4.  <span data-ttu-id="61f23-114">Создайте раздел на диске и получите объект тома следующим образом:</span><span class="sxs-lookup"><span data-stu-id="61f23-114">Create a partition on the disk and obtain the volume object as follows:</span></span>
    1.  <span data-ttu-id="61f23-115">Чтобы создать секцию, вызовите метод [**ивдскреатепартитионекс:: креатепартитионекс**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) .</span><span class="sxs-lookup"><span data-stu-id="61f23-115">Invoke the [**IVdsCreatePartitionEx::CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) method to create a partition.</span></span>
    2.  <span data-ttu-id="61f23-116">Вызовите метод [**ивдсасинк:: wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) асинхронного объекта, возвращаемого [**креатепартитионекс**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) , чтобы получить идентификатор тома из структуры [**\_ асинхронного \_ вывода VDS**](/windows/desktop/api/Vds/ns-vds-vds_async_output) .</span><span class="sxs-lookup"><span data-stu-id="61f23-116">Invoke the [**IVdsAsync::Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) method on the async object that is returned by [**CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) to get the volume identifier from the [**VDS\_ASYNC\_OUTPUT**](/windows/desktop/api/Vds/ns-vds-vds_async_output) structure.</span></span>
    3.  <span data-ttu-id="61f23-117">Передайте идентификатор тома в качестве параметра методу [**ивдссервице:: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) , чтобы получить указатель на объект тома.</span><span class="sxs-lookup"><span data-stu-id="61f23-117">Pass the volume identifier as a parameter to the [**IVdsService::GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) method to get a volume object pointer.</span></span>
5.  <span data-ttu-id="61f23-118">Чтобы назначить букву диска, вызовите метод [**ивдсволумемф:: аддакцесспас**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) .</span><span class="sxs-lookup"><span data-stu-id="61f23-118">Invoke the [**IVdsVolumeMF::AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) method to assign the drive letter.</span></span>

> [!Note]  
> <span data-ttu-id="61f23-119">Метод [**ивдсадванцеддиск:: ассигндривелеттер**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) назначает буквы дисков секциям без связанных томов, таких как разделы OEM или ESP.</span><span class="sxs-lookup"><span data-stu-id="61f23-119">The [**IVdsAdvancedDisk::AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) method assigns drive letters to partitions without associated volumes, such as OEM or ESP partitions.</span></span> <span data-ttu-id="61f23-120">Его нельзя использовать для назначения буквы диска объекту LUN.</span><span class="sxs-lookup"><span data-stu-id="61f23-120">You cannot use it to assign a drive letter to a LUN object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="61f23-121">См. также</span><span class="sxs-lookup"><span data-stu-id="61f23-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61f23-122">Использование VDS</span><span class="sxs-lookup"><span data-stu-id="61f23-122">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="61f23-123">**Ивдссервице:: перечисление**</span><span class="sxs-lookup"><span data-stu-id="61f23-123">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="61f23-124">**ивдсдиск**</span><span class="sxs-lookup"><span data-stu-id="61f23-124">**IVdsDisk**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[<span data-ttu-id="61f23-125">**Ивдссвпровидер:: Креатепакк**</span><span class="sxs-lookup"><span data-stu-id="61f23-125">**IVdsSwProvider::CreatePack**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[<span data-ttu-id="61f23-126">**Ивдспакк:: Адддиск**</span><span class="sxs-lookup"><span data-stu-id="61f23-126">**IVdsPack::AddDisk**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> <dt>

[<span data-ttu-id="61f23-127">**Ивдскреатепартитионекс:: Креатепартитионекс**</span><span class="sxs-lookup"><span data-stu-id="61f23-127">**IVdsCreatePartitionEx::CreatePartitionEx**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex)
</dt> <dt>

[<span data-ttu-id="61f23-128">**Ивдсасинк:: wait**</span><span class="sxs-lookup"><span data-stu-id="61f23-128">**IVdsAsync::Wait**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[<span data-ttu-id="61f23-129">**\_асинхронный \_ вывод VDS**</span><span class="sxs-lookup"><span data-stu-id="61f23-129">**VDS\_ASYNC\_OUTPUT**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_async_output)
</dt> <dt>

[<span data-ttu-id="61f23-130">**Ивдсволумемф:: Аддакцесспас**</span><span class="sxs-lookup"><span data-stu-id="61f23-130">**IVdsVolumeMF::AddAccessPath**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath)
</dt> <dt>

[<span data-ttu-id="61f23-131">**Ивдсадванцеддиск:: Ассигндривелеттер**</span><span class="sxs-lookup"><span data-stu-id="61f23-131">**IVdsAdvancedDisk::AssignDriveLetter**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter)
</dt> </dl>

 

 
