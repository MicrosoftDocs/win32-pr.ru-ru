---
description: СФВМ \_ сисидлист может быть изменен или недоступен.
ms.assetid: 488f696d-aa71-4727-bbd2-c99e7d245d85
title: Сообщение SFVM_THISIDLIST (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86e24199e5adbb895c8d1d5fc36bfff0c109bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818617"
---
# <a name="sfvm_thisidlist-message"></a><span data-ttu-id="0dcc8-103">\_Сообщение сфвм сисидлист</span><span class="sxs-lookup"><span data-stu-id="0dcc8-103">SFVM\_THISIDLIST message</span></span>

<span data-ttu-id="0dcc8-104">\[**Сфвм \_ СИСИДЛИСТ** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="0dcc8-104">\[**SFVM\_THISIDLIST** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0dcc8-105">В последующих версиях он может быть изменен или недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="0dcc8-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="0dcc8-106">Позволяет объекту обратного вызова указать указатель представления на список идентификаторов элементов (ПИДЛ).</span><span class="sxs-lookup"><span data-stu-id="0dcc8-106">Allows the callback object to specify the view's pointer to an item identifier list (PIDL).</span></span> <span data-ttu-id="0dcc8-107">Используется, только если не удалось выполнить [**иперсистидлист:: сетидлист**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) и [**IPersistFolder2:: жеткурфолдер**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) .</span><span class="sxs-lookup"><span data-stu-id="0dcc8-107">This is used only when [**IPersistIDList::SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) and [**IPersistFolder2::GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) have failed.</span></span> <span data-ttu-id="0dcc8-108">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="0dcc8-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_THISIDLIST
    lParam = (LPARAM)(LPITEMIDLIST*) pidl;
            
```



## <a name="parameters"></a><span data-ttu-id="0dcc8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0dcc8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dcc8-110">*Пидл* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0dcc8-110">*pidl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0dcc8-111">Адрес ПИДЛ представления.</span><span class="sxs-lookup"><span data-stu-id="0dcc8-111">The address of the view's PIDL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0dcc8-112">Требования</span><span class="sxs-lookup"><span data-stu-id="0dcc8-112">Requirements</span></span>



| <span data-ttu-id="0dcc8-113">Требование</span><span class="sxs-lookup"><span data-stu-id="0dcc8-113">Requirement</span></span> | <span data-ttu-id="0dcc8-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0dcc8-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0dcc8-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0dcc8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0dcc8-116">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0dcc8-116">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0dcc8-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0dcc8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0dcc8-118">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0dcc8-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0dcc8-119">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0dcc8-119">End of client support</span></span><br/>    | <span data-ttu-id="0dcc8-120">Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="0dcc8-120">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="0dcc8-121">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="0dcc8-121">End of server support</span></span><br/>    | <span data-ttu-id="0dcc8-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0dcc8-122">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="0dcc8-123">Header</span><span class="sxs-lookup"><span data-stu-id="0dcc8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dcc8-124"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dcc8-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
