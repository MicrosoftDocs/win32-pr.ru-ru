---
description: Если приложение запрашивает уступающую блокировку, все файлы, для которых он запрашивает блокировки, должны быть открыты для перекрывающихся (асинхронных) входных и выходных данных с помощью функции CreateFile с \_ \_ флагом File Flag OVERLAPPED.
ms.assetid: 1595c03e-9f6d-456c-8164-fafba06bbd79
title: Операции оппортунистической блокировки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefd9b292747e89f5ebafd94cb8aa0e38833e8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545543"
---
# <a name="opportunistic-lock-operations"></a><span data-ttu-id="9839b-103">Операции оппортунистической блокировки</span><span class="sxs-lookup"><span data-stu-id="9839b-103">Opportunistic Lock Operations</span></span>

<span data-ttu-id="9839b-104">Если приложение запрашивает уступающую блокировку, все файлы, для которых он запрашивает блокировки, должны быть открыты для перекрывающихся (асинхронных) входных и выходных данных с помощью функции [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) с флагом **File \_ Flag \_ OVERLAPPED** .</span><span class="sxs-lookup"><span data-stu-id="9839b-104">If an application requests opportunistic locks, all files for which it requests locks must be opened for overlapped (asynchronous) input and output by using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the **FILE\_FLAG\_OVERLAPPED** flag.</span></span> <span data-ttu-id="9839b-105">После открытия файлов для работы с перекрытием можно использовать функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) с одним из следующих управляющих кодов для работы с этими файлами уступающей блокировкой:</span><span class="sxs-lookup"><span data-stu-id="9839b-105">After the files are opened for overlapped operation, you can use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with one of the following control codes to work with those files' opportunistic locks:</span></span>

<dl>

[<span data-ttu-id="9839b-106">**\_ \_ \_ Ожидание закрытия фсктл опбатч ACK \_**</span><span class="sxs-lookup"><span data-stu-id="9839b-106">**FSCTL\_OPBATCH\_ACK\_CLOSE\_PENDING**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[<span data-ttu-id="9839b-107">**ФСКТЛ \_ OPLOCK \_ break \_ ACK \_ No \_ 2**</span><span class="sxs-lookup"><span data-stu-id="9839b-107">**FSCTL\_OPLOCK\_BREAK\_ACK\_NO\_2**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[<span data-ttu-id="9839b-108">**ФСКТЛ \_ OPLOCK \_ break, \_ подтверждение**</span><span class="sxs-lookup"><span data-stu-id="9839b-108">**FSCTL\_OPLOCK\_BREAK\_ACKNOWLEDGE**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[<span data-ttu-id="9839b-109">**\_ \_ уведомление о разрыве фсктл OPLOCK \_**</span><span class="sxs-lookup"><span data-stu-id="9839b-109">**FSCTL\_OPLOCK\_BREAK\_NOTIFY**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[<span data-ttu-id="9839b-110">**\_ \_ Пакетная блокировка запроса фсктл \_**</span><span class="sxs-lookup"><span data-stu-id="9839b-110">**FSCTL\_REQUEST\_BATCH\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[<span data-ttu-id="9839b-111">**ФСКТЛ \_ запрос \_ фильтрации \_ оппортунистической блокировки**</span><span class="sxs-lookup"><span data-stu-id="9839b-111">**FSCTL\_REQUEST\_FILTER\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[<span data-ttu-id="9839b-112">**\_ \_ нежесткая блокировка запроса фсктл**</span><span class="sxs-lookup"><span data-stu-id="9839b-112">**FSCTL\_REQUEST\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[<span data-ttu-id="9839b-113">**\_Запрос фсктл \_ уровень жесткой блокировки \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="9839b-113">**FSCTL\_REQUEST\_OPLOCK\_LEVEL\_1**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[<span data-ttu-id="9839b-114">**\_Запрос фсктл \_ уровень жесткой блокировки \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="9839b-114">**FSCTL\_REQUEST\_OPLOCK\_LEVEL\_2**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

 

 
