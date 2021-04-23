---
description: Управление каталогами с помощью таблицы записей каталога, дескрипторов каталогов, точек повторного анализа.
title: Локальные файловые системы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f624ef1999b81adb63ba1d5b7e349259cabd53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812520"
---
# <a name="local-file-systems"></a><span data-ttu-id="730fd-103">Локальные файловые системы</span><span class="sxs-lookup"><span data-stu-id="730fd-103">Local File Systems</span></span>

<span data-ttu-id="730fd-104">*Файловая система* позволяет приложениям хранить и извлекать файлы на запоминающих устройствах.</span><span class="sxs-lookup"><span data-stu-id="730fd-104">A *file system* enables applications to store and retrieve files on storage devices.</span></span> <span data-ttu-id="730fd-105">Файлы помещаются в иерархическую структуру.</span><span class="sxs-lookup"><span data-stu-id="730fd-105">Files are placed in a hierarchical structure.</span></span> <span data-ttu-id="730fd-106">Файловая система задает соглашения об именовании для файлов и формат для указания пути к файлу в древовидной структуре.</span><span class="sxs-lookup"><span data-stu-id="730fd-106">The file system specifies naming conventions for files and the format for specifying the path to a file in the tree structure.</span></span>

<span data-ttu-id="730fd-107">Каждая файловая система состоит из одного или нескольких драйверов и библиотек динамической компоновки, определяющих форматы данных и функции файловой системы.</span><span class="sxs-lookup"><span data-stu-id="730fd-107">Each file system consists of one or more drivers and dynamic-link libraries that define the data formats and features of the file system.</span></span> <span data-ttu-id="730fd-108">Файловые системы могут существовать на различных типах запоминающих устройств, включая жесткие диски, устройства смены дисков, съемные оптические диски, модули резервного копирования ленты и карты памяти.</span><span class="sxs-lookup"><span data-stu-id="730fd-108">File systems can exist on many different types of storage devices, including hard disks, jukeboxes, removable optical disks, tape back-up units, and memory cards.</span></span>

<span data-ttu-id="730fd-109">Все файловые системы, поддерживаемые Windows, имеют следующие компоненты хранения:</span><span class="sxs-lookup"><span data-stu-id="730fd-109">All file systems supported by Windows have the following storage components:</span></span>

-   <span data-ttu-id="730fd-110">Volume.</span><span class="sxs-lookup"><span data-stu-id="730fd-110">Volumes.</span></span> <span data-ttu-id="730fd-111">*Том* — это коллекция каталогов и файлов.</span><span class="sxs-lookup"><span data-stu-id="730fd-111">A *volume* is a collection of directories and files.</span></span>
-   <span data-ttu-id="730fd-112">Каталогов.</span><span class="sxs-lookup"><span data-stu-id="730fd-112">Directories.</span></span> <span data-ttu-id="730fd-113">*Каталог* — это иерархическая коллекция файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="730fd-113">A *directory* is a hierarchical collection of directories and files.</span></span>
-   <span data-ttu-id="730fd-114">Файла.</span><span class="sxs-lookup"><span data-stu-id="730fd-114">Files.</span></span> <span data-ttu-id="730fd-115">*Файл* — это логическая группировка связанных данных.</span><span class="sxs-lookup"><span data-stu-id="730fd-115">A *file* is a logical grouping of related data.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="730fd-116">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="730fd-116">In this section</span></span>



| <span data-ttu-id="730fd-117">Раздел</span><span class="sxs-lookup"><span data-stu-id="730fd-117">Topic</span></span>                                                                | <span data-ttu-id="730fd-118">Описание</span><span class="sxs-lookup"><span data-stu-id="730fd-118">Description</span></span>                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="730fd-119">Управление каталогом</span><span class="sxs-lookup"><span data-stu-id="730fd-119">Directory Management</span></span>](directory-management.md)<br/>          | <span data-ttu-id="730fd-120">*Каталог* — это иерархическая коллекция файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="730fd-120">A *directory* is a hierarchical collection of directories and files.</span></span> <span data-ttu-id="730fd-121">Единственным ограничением на количество файлов, которые могут содержаться в одном каталоге, является физический размер диска, на котором расположен каталог.</span><span class="sxs-lookup"><span data-stu-id="730fd-121">The only constraint on the number of files that can be contained in a single directory is the physical size of the disk on which the directory is located.</span></span><br/> |
| [<span data-ttu-id="730fd-122">Управление дисками</span><span class="sxs-lookup"><span data-stu-id="730fd-122">Disk Management</span></span>](disk-management.md)<br/>                    | <span data-ttu-id="730fd-123">*Жесткий диск* — это жесткий диск внутри компьютера, который хранит и обеспечивает сравнительно быстрый доступ к большим объемам данных.</span><span class="sxs-lookup"><span data-stu-id="730fd-123">A *hard disk* is a rigid disk inside a computer that stores and provides relatively quick access to large amounts of data.</span></span> <span data-ttu-id="730fd-124">Это тип хранилища, наиболее часто используемый в Windows.</span><span class="sxs-lookup"><span data-stu-id="730fd-124">It is the type of storage most often used with Windows.</span></span> <span data-ttu-id="730fd-125">Система также поддерживает съемные носители.</span><span class="sxs-lookup"><span data-stu-id="730fd-125">The system also supports removable media.</span></span><br/>    |
| [<span data-ttu-id="730fd-126">Управление файлами</span><span class="sxs-lookup"><span data-stu-id="730fd-126">File Management</span></span>](file-management.md)<br/>                    | <span data-ttu-id="730fd-127">*Объект File* предоставляет представление ресурса (физического устройства или ресурса, расположенного на физическом устройстве), которое может управляться системой ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="730fd-127">A *file object* provides a representation of a resource (either a physical device or a resource located on a physical device) that can be managed by the I/O system.</span></span><br/>                                                            |
| [<span data-ttu-id="730fd-128">Транзакционная NTFS (TxF)</span><span class="sxs-lookup"><span data-stu-id="730fd-128">Transactional NTFS (TxF)</span></span>](transactional-ntfs-portal.md)<br/> | <span data-ttu-id="730fd-129">Транзакционная NTFS (TxF) позволяет выполнять операции с файлами на томе файловой системы NTFS в транзакции.</span><span class="sxs-lookup"><span data-stu-id="730fd-129">Transactional NTFS (TxF) allows file operations on an NTFS file system volume to be performed in a transaction.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="730fd-130">Управление томами</span><span class="sxs-lookup"><span data-stu-id="730fd-130">Volume Management</span></span>](volume-management.md)<br/>                | <span data-ttu-id="730fd-131">Самым высоким уровнем организации в файловой системе является *том*.</span><span class="sxs-lookup"><span data-stu-id="730fd-131">The highest level of organization in the file system is the *volume*.</span></span> <span data-ttu-id="730fd-132">Файловая система находится на томе.</span><span class="sxs-lookup"><span data-stu-id="730fd-132">A file system resides on a volume.</span></span><br/>                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="730fd-133">См. также</span><span class="sxs-lookup"><span data-stu-id="730fd-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="730fd-134">[Технический справочник по файловой системе FAT](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="730fd-134">[FAT Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="730fd-135">[Технологии файловых систем](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="730fd-135">[File Systems Technologies](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="730fd-136">[Технический справочник по NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="730fd-136">[NTFS Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span></span>
</dt> </dl>

 

