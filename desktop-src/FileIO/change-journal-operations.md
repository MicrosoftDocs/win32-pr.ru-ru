---
description: Управляющие коды и структуры для использования с журналом изменений USN в файловой системе NTFS.
ms.assetid: 2215f0d4-6ac8-42a5-87a5-9c76d1fae3ed
title: Операции с журналом изменений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a52cda51d0efc4cbae1333fc197f42d6a5cc0f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684381"
---
# <a name="change-journal-operations"></a><span data-ttu-id="c2a50-103">Операции с журналом изменений</span><span class="sxs-lookup"><span data-stu-id="c2a50-103">Change Journal Operations</span></span>

<span data-ttu-id="c2a50-104">В следующем списке перечислены коды элементов управления, которые работают с журналом изменений USN в файловой системе NTFS.</span><span class="sxs-lookup"><span data-stu-id="c2a50-104">The following list identifies the control codes that work with the NTFS file system update sequence number (USN) change journal.</span></span>

-   [<span data-ttu-id="c2a50-105">**ФСКТЛ \_ создать \_ \_ журнал USN**</span><span class="sxs-lookup"><span data-stu-id="c2a50-105">**FSCTL\_CREATE\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal)
-   [<span data-ttu-id="c2a50-106">**ФСКТЛ \_ удалить \_ \_ журнал USN**</span><span class="sxs-lookup"><span data-stu-id="c2a50-106">**FSCTL\_DELETE\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal)
-   [<span data-ttu-id="c2a50-107">**\_Перечисление \_ данных USN фсктл \_**</span><span class="sxs-lookup"><span data-stu-id="c2a50-107">**FSCTL\_ENUM\_USN\_DATA**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data)
-   [<span data-ttu-id="c2a50-108">**\_маркер фсктл Mark \_**</span><span class="sxs-lookup"><span data-stu-id="c2a50-108">**FSCTL\_MARK\_HANDLE**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_mark_handle)
-   [<span data-ttu-id="c2a50-109">**ФСКТЛ \_ запрос \_ \_ журнала USN**</span><span class="sxs-lookup"><span data-stu-id="c2a50-109">**FSCTL\_QUERY\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal)
-   [<span data-ttu-id="c2a50-110">**ФСКТЛ \_ Чтение \_ \_ журнала USN**</span><span class="sxs-lookup"><span data-stu-id="c2a50-110">**FSCTL\_READ\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal)

<span data-ttu-id="c2a50-111">В следующем списке приведены сведения о структурах, относящиеся к журналу изменений USN файловой системы NTFS.</span><span class="sxs-lookup"><span data-stu-id="c2a50-111">The following list identifies the structures information that relates to the NTFS file system USN change journal.</span></span>

-   [<span data-ttu-id="c2a50-112">**Создание \_ \_ данных журнала \_ USN**</span><span class="sxs-lookup"><span data-stu-id="c2a50-112">**CREATE\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-create_usn_journal_data)
-   [<span data-ttu-id="c2a50-113">**Удаление \_ \_ данных журнала \_ USN**</span><span class="sxs-lookup"><span data-stu-id="c2a50-113">**DELETE\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-delete_usn_journal_data)
-   [<span data-ttu-id="c2a50-114">**пометить \_ \_ сведения об маркере**</span><span class="sxs-lookup"><span data-stu-id="c2a50-114">**MARK\_HANDLE\_INFO**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-mark_handle_info)
-   [<span data-ttu-id="c2a50-115">**\_данные ПЕРЕЧИСЛЕНИЯ \_ MFT**</span><span class="sxs-lookup"><span data-stu-id="c2a50-115">**MFT\_ENUM\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-mft_enum_data_v0)
-   [<span data-ttu-id="c2a50-116">**ЧТЕНИЕ \_ \_ данных журнала \_ USN**</span><span class="sxs-lookup"><span data-stu-id="c2a50-116">**READ\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0)
-   [<span data-ttu-id="c2a50-117">**\_данные журнала \_ USN**</span><span class="sxs-lookup"><span data-stu-id="c2a50-117">**USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_journal_data_v0)
-   [<span data-ttu-id="c2a50-118">**\_запись USN**</span><span class="sxs-lookup"><span data-stu-id="c2a50-118">**USN\_RECORD**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2)

 

 
