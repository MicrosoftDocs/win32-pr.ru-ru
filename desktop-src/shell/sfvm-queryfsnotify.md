---
description: СФВМ \_ куерифснотифи может быть изменен или недоступен.
ms.assetid: 5d777115-bae3-47c4-9edc-c99c40a4f926
title: Сообщение SFVM_QUERYFSNOTIFY (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4416bda249e3ec0f2a0c0f2d45ac353961e180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272850"
---
# <a name="sfvm_queryfsnotify-message"></a><span data-ttu-id="c48d0-103">\_Сообщение сфвм куерифснотифи</span><span class="sxs-lookup"><span data-stu-id="c48d0-103">SFVM\_QUERYFSNOTIFY message</span></span>

<span data-ttu-id="c48d0-104">\[**Сфвм \_ КУЕРИФСНОТИФИ** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="c48d0-104">\[**SFVM\_QUERYFSNOTIFY** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c48d0-105">В последующих версиях он может быть изменен или недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="c48d0-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="c48d0-106">Позволяет объекту обратного вызова зарегистрировать папку, чтобы изменения в представлении этой папки создавали уведомления.</span><span class="sxs-lookup"><span data-stu-id="c48d0-106">Allows the callback object to register a folder so that changes to that folder's view will generate notifications.</span></span> <span data-ttu-id="c48d0-107">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="c48d0-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_QUERYFSNOTIFY 
    lParam = (LPARAM)(SHChangeNotifyEntry*) shcne;
            
```



## <a name="parameters"></a><span data-ttu-id="c48d0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c48d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c48d0-109">*шкне* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c48d0-109">*shcne* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c48d0-110">Структура для хранения ПИДЛ элемента для отслеживания событий и указания, следует ли выполнять наблюдение за вложенными папками этого элемента.</span><span class="sxs-lookup"><span data-stu-id="c48d0-110">A structure to hold the PIDL of the item to watch for events and an indication whether subfolders of that item should also be watched.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c48d0-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c48d0-111">Requirements</span></span>



| <span data-ttu-id="c48d0-112">Требование</span><span class="sxs-lookup"><span data-stu-id="c48d0-112">Requirement</span></span> | <span data-ttu-id="c48d0-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c48d0-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c48d0-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c48d0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c48d0-115">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c48d0-115">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c48d0-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c48d0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c48d0-117">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c48d0-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c48d0-118">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c48d0-118">End of client support</span></span><br/>    | <span data-ttu-id="c48d0-119">Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="c48d0-119">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="c48d0-120">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="c48d0-120">End of server support</span></span><br/>    | <span data-ttu-id="c48d0-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c48d0-121">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="c48d0-122">Header</span><span class="sxs-lookup"><span data-stu-id="c48d0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c48d0-123"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="c48d0-123"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
