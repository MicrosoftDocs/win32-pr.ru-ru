---
description: Описывает, как точки повторного анализа обеспечивают поведение файловой системы, которое отчасти от поведения, ожидаемого большинством разработчиков Windows.
ms.assetid: 1aaebda9-0013-4282-9ae1-7c829e171942
title: Точки повторного анализа и операции с файлами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1132197cd689157cd9f219afa5bfc1474b587c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265953"
---
# <a name="reparse-points-and-file-operations"></a><span data-ttu-id="1ea2e-103">Точки повторного анализа и операции с файлами</span><span class="sxs-lookup"><span data-stu-id="1ea2e-103">Reparse Points and File Operations</span></span>

<span data-ttu-id="1ea2e-104">*Точки повторного анализа* обеспечивают поведение файловой системы, которое отчасти от поведения, которое большинство разработчиков Windows может привыкли, поэтому при написании приложений, работающих с файлами, крайне важно для надежных и надежных приложений, предназначенных для доступа к файловым системам, поддерживающим точки повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="1ea2e-104">*Reparse points* enable file system behavior that departs from the behavior most Windows developers may be accustomed to, therefore being aware of these behaviors when writing applications that manipulate files is vital to robust and reliable applications intended to access file systems that support reparse points.</span></span> <span data-ttu-id="1ea2e-105">Эти рекомендации будут зависеть от конкретной реализации и связанного поведения фильтра файловой системы определенной точки повторного анализа, которая может быть определена пользователем.</span><span class="sxs-lookup"><span data-stu-id="1ea2e-105">The extent of these considerations will depend on the specific implementation and associated file system filter behavior of a particular reparse point, which can be user-defined.</span></span> <span data-ttu-id="1ea2e-106">Дополнительные сведения см. в разделе [точки повторного анализа](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="1ea2e-106">For more information, see [Reparse Points](reparse-points.md).</span></span>

<span data-ttu-id="1ea2e-107">Рассмотрим следующие примеры использования реализаций точек повторного анализа NTFS, включая подключенные папки, связанные файлы и сервер удаленного хранилища (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="1ea2e-107">Consider the following examples regarding NTFS reparse point implementations, which include mounted folders, linked files, and the Microsoft Remote Storage Server:</span></span>

-   <span data-ttu-id="1ea2e-108">Приложения резервного копирования, использующие [файловые потоки](file-streams.md) , должны указывать **\_ \_ данные повторного анализа резервного копирования** в структуре [**\_ \_ идентификатора потока Win32**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) при резервном копировании файлов с помощью точек повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="1ea2e-108">Backup applications that use [file streams](file-streams.md) should specify **BACKUP\_REPARSE\_DATA** in the [**WIN32\_STREAM\_ID**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) structure when backing up files with reparse points.</span></span>
-   <span data-ttu-id="1ea2e-109">В приложениях, использующих функцию [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , необходимо указать флаг **файла \_ Открыть флаг \_ \_ \_ точки повторной обработки** при открытии файла, если это точка повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="1ea2e-109">Applications that use the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function should specify the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag when opening the file if it is a reparse point.</span></span> <span data-ttu-id="1ea2e-110">Дополнительные сведения см. в разделе [Создание и открытие файлов](creating-and-opening-files.md).</span><span class="sxs-lookup"><span data-stu-id="1ea2e-110">For more information, see [Creating and Opening Files](creating-and-opening-files.md).</span></span>
-   <span data-ttu-id="1ea2e-111">Для процесса [дефрагментации файлов](defragmenting-files.md) требуется специальная обработка точек повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="1ea2e-111">The process of [defragmenting files](defragmenting-files.md) requires special handling for reparse points.</span></span>
-   <span data-ttu-id="1ea2e-112">Приложения для обнаружения вирусов должны искать точки повторного анализа, указывающие на связанные файлы.</span><span class="sxs-lookup"><span data-stu-id="1ea2e-112">Virus detection applications should search for reparse points that indicate linked files.</span></span>
-   <span data-ttu-id="1ea2e-113">Большинство приложений должны выполнять специальные действия для файлов, которые были перемещены в долгосрочное хранение, если только уведомлять пользователя о том, что для получения файла может потребоваться некоторое время.</span><span class="sxs-lookup"><span data-stu-id="1ea2e-113">Most applications should take special actions for files that have been moved to long-term storage, if only to notify the user that it may take a while to retrieve the file.</span></span>
-   <span data-ttu-id="1ea2e-114">Функция [**опенфилебид**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) либо открывает файл, либо точку повторной обработки в зависимости от использования флага **файла \_ флаг \_ открытия \_ \_ точки** повторной обработки.</span><span class="sxs-lookup"><span data-stu-id="1ea2e-114">The [**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) function will either open the file or the reparse point, depending on the use of the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag.</span></span>
-   <span data-ttu-id="1ea2e-115">Символьные ссылки в качестве точек повторного анализа имеют определенные [аспекты программирования](symbolic-link-programming-considerations.md) .</span><span class="sxs-lookup"><span data-stu-id="1ea2e-115">Symbolic links, as reparse points, have certain [programming considerations](symbolic-link-programming-considerations.md) specific to them.</span></span>
-   <span data-ttu-id="1ea2e-116">Действия по управлению томами для чтения записей журнала изменений номеров последовательных обновлений (USN) требует особой обработки точек повторного анализа при [**использовании \_ записи USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) и [**считывания структур \_ \_ \_ данных журнала USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) .</span><span class="sxs-lookup"><span data-stu-id="1ea2e-116">Volume management activities for reading update sequence number (USN) change journal records require special handling for reparse points when using the [**USN\_RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**READ\_USN\_JOURNAL\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) structures.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ea2e-117">См. также</span><span class="sxs-lookup"><span data-stu-id="1ea2e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ea2e-118">Определение того, является ли каталог подключенной папкой</span><span class="sxs-lookup"><span data-stu-id="1ea2e-118">Determining Whether a Directory Is a Mounted Folder</span></span>](determining-whether-a-directory-is-a-volume-mount-point.md)
</dt> <dt>

[<span data-ttu-id="1ea2e-119">Создание подключенных папок</span><span class="sxs-lookup"><span data-stu-id="1ea2e-119">Creating Mounted Folders</span></span>](mounting-and-dismounting-a-volume.md)
</dt> <dt>

[<span data-ttu-id="1ea2e-120">Символьные эффекты ссылок в функциях файловых систем</span><span class="sxs-lookup"><span data-stu-id="1ea2e-120">Symbolic Link Effects on File Systems Functions</span></span>](symbolic-link-effects-on-file-systems-functions.md)
</dt> </dl>

 

 
