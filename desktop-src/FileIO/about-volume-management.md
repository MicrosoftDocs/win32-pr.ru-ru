---
description: Тома реализуются драйвером устройства, который называется диспетчером томов.
ms.assetid: 424ddbd9-5692-45ef-95fb-7b00b09e3205
title: Об управлении томами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0767d137eeecaa4ded060382b689b5ea3780dcbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684386"
---
# <a name="about-volume-management"></a><span data-ttu-id="64abd-103">Об управлении томами</span><span class="sxs-lookup"><span data-stu-id="64abd-103">About Volume Management</span></span>

<span data-ttu-id="64abd-104">Тома реализуются драйвером устройства, который называется диспетчером томов.</span><span class="sxs-lookup"><span data-stu-id="64abd-104">Volumes are implemented by a device driver called a volume manager.</span></span> <span data-ttu-id="64abd-105">Примеры включают диспетчер Фтдиск, Диспетчер логических дисков (LDM) и Диспетчер логических томов VERITAS (LVM).</span><span class="sxs-lookup"><span data-stu-id="64abd-105">Examples include the FtDisk Manager, the Logical Disk Manager (LDM), and the VERITAS Logical Volume Manager (LVM).</span></span> <span data-ttu-id="64abd-106">Диспетчеры томов обеспечивают уровень физической абстракции, защиту данных (с использованием какого-либо вида RAID) и производительность.</span><span class="sxs-lookup"><span data-stu-id="64abd-106">Volume managers provide a layer of physical abstraction, data protection (using some form of RAID), and performance.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="64abd-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="64abd-107">In this section</span></span>



| <span data-ttu-id="64abd-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="64abd-108">Topic</span></span>                                                                       | <span data-ttu-id="64abd-109">Описание</span><span class="sxs-lookup"><span data-stu-id="64abd-109">Description</span></span>                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64abd-110">Распознавание файловой системы</span><span class="sxs-lookup"><span data-stu-id="64abd-110">File System Recognition</span></span>](file-system-recognition.md)<br/>           | <span data-ttu-id="64abd-111">Цель распознавания файловой системы заключается в том, чтобы операционная система Windows могла использовать дополнительный параметр для допустимой, но нераспознанной файловой системы, отличной от «RAW».</span><span class="sxs-lookup"><span data-stu-id="64abd-111">The goal of file system recognition is to allow the Windows operating system to have an additional option for a valid but unrecognized file system other than "RAW".</span></span><br/>                                                                                                         |
| [<span data-ttu-id="64abd-112">Именование тома</span><span class="sxs-lookup"><span data-stu-id="64abd-112">Naming a Volume</span></span>](naming-a-volume.md)<br/>                           | <span data-ttu-id="64abd-113">Метка — это понятное для пользователя имя, которое назначается тому (обычно конечному пользователю), чтобы упростить его распознавание.</span><span class="sxs-lookup"><span data-stu-id="64abd-113">A label is a user-friendly name that is assigned to a volume, usually by an end user, to make it easier to recognize.</span></span> <span data-ttu-id="64abd-114">Том может иметь метку, букву диска, и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="64abd-114">A volume can have a label, a drive letter, both, or neither.</span></span> <span data-ttu-id="64abd-115">Чтобы задать метку для тома, используйте функцию [**сетволумелабел**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) .</span><span class="sxs-lookup"><span data-stu-id="64abd-115">To set the label for a volume, use the [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) function.</span></span><br/> |
| [<span data-ttu-id="64abd-116">Перечисление томов</span><span class="sxs-lookup"><span data-stu-id="64abd-116">Enumerating Volumes</span></span>](enumerating-volumes.md)<br/>                   | <span data-ttu-id="64abd-117">Чтобы создать полный список томов на компьютере или управлять каждым томом, можно перечислить тома.</span><span class="sxs-lookup"><span data-stu-id="64abd-117">To make a complete list of the volumes on a computer, or to manipulate each volume in turn, you can enumerate volumes.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="64abd-118">Получение сведений о томе</span><span class="sxs-lookup"><span data-stu-id="64abd-118">Obtaining Volume Information</span></span>](obtaining-volume-information.md)<br/> | <span data-ttu-id="64abd-119">Перед доступом к файлам и каталогам на заданном томе следует определить возможности файловой системы с помощью функции [**жетволумеинформатион**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) .</span><span class="sxs-lookup"><span data-stu-id="64abd-119">Before you access files and directories on a given volume, you should determine the capabilities of the file system by using the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function.</span></span><br/>                                                                              |
| [<span data-ttu-id="64abd-120">Журналы изменений</span><span class="sxs-lookup"><span data-stu-id="64abd-120">Change Journals</span></span>](change-journals.md)<br/>                           | <span data-ttu-id="64abd-121">При внесении каких-либо изменений в файл или каталог в томе журнал изменений USN для этого тома обновляется с описанием изменения и имени файла или каталога.</span><span class="sxs-lookup"><span data-stu-id="64abd-121">When any change is made to a file or directory in a volume, the USN change journal for that volume is updated with a description of the change and the name of the file or directory.</span></span><br/>                                                                                        |
| [<span data-ttu-id="64abd-122">Подключенные папки</span><span class="sxs-lookup"><span data-stu-id="64abd-122">Mounted Folders</span></span>](volume-mount-points.md)<br/>                       | <span data-ttu-id="64abd-123">С помощью подключенных папок можно объединять разнородные файловые системы, такие как файловая система NTFS, 16-разрядная файловая система FAT и файловая система ISO-9660 на компакт-диске, в одну логическую файловую систему на одном томе NTFS.</span><span class="sxs-lookup"><span data-stu-id="64abd-123">Using mounted folders, you can unify disparate file systems such as the NTFS file system, a 16-bit FAT file system, and an ISO-9660 file system on a CD-ROM drive into one logical file system on a single NTFS volume.</span></span><br/>                                                      |
| [<span data-ttu-id="64abd-124">Основная таблица файлов</span><span class="sxs-lookup"><span data-stu-id="64abd-124">Master File Table</span></span>](master-file-table.md)<br/>                       | <span data-ttu-id="64abd-125">Все сведения о файле, включая его размер, дату и время, разрешения и содержимое данных, хранятся либо в записях главной файловой таблицы (MFT), либо в пространстве, расположенном за пределами MFT, которое описывается записями MFT.</span><span class="sxs-lookup"><span data-stu-id="64abd-125">All information about a file, including its size, time and date stamps, permissions, and data content, is stored either in master file table (MFT) entries, or in space outside the MFT that is described by MFT entries.</span></span><br/>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="64abd-126">См. также</span><span class="sxs-lookup"><span data-stu-id="64abd-126">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="64abd-127">[Технический справочник по основным дискам и томам](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="64abd-127">[Basic Disks and Volumes Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="64abd-128">[Технический справочник по динамическим дискам и томам](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="64abd-128">[Dynamic Disks and Volumes Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="64abd-129">Справочник по управлению томами</span><span class="sxs-lookup"><span data-stu-id="64abd-129">Volume Management Reference</span></span>](volume-management-reference.md)
</dt> </dl>

 

