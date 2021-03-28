---
description: 'Уведомляет объект обратного вызова сайта контейнера. Используется только в том случае, если IObjectWithSite:: SetSite не поддерживается и используется Шкреатешеллфолдервиевекс. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: Сообщение SFVM_SETISFV (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83021f1d6d52286f08e8ec7bd51bbaa806c17c7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986100"
---
# <a name="sfvm_setisfv-message"></a><span data-ttu-id="5a6b7-105">\_Сообщение сфвм сетисфв</span><span class="sxs-lookup"><span data-stu-id="5a6b7-105">SFVM\_SETISFV message</span></span>

<span data-ttu-id="5a6b7-106">\[Это уведомление поддерживается в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5a6b7-106">\[This notification is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="5a6b7-107">В последующих версиях Windows она может не поддерживаться.\]</span><span class="sxs-lookup"><span data-stu-id="5a6b7-107">It might be unsupported in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="5a6b7-108">Уведомляет объект обратного вызова сайта контейнера.</span><span class="sxs-lookup"><span data-stu-id="5a6b7-108">Notifies the callback object of the container site.</span></span> <span data-ttu-id="5a6b7-109">Используется только в том случае, если [**IObjectWithSite:: SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) не поддерживается и используется [**шкреатешеллфолдервиевекс**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) .</span><span class="sxs-lookup"><span data-stu-id="5a6b7-109">This is used only when [**IObjectWithSite::SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) is not supported and [**SHCreateShellFolderViewEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) is used.</span></span> <span data-ttu-id="5a6b7-110">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="5a6b7-110">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_SETISFV
    lParam = (LPARAM)(IUnknown*) site;
            
```



## <a name="parameters"></a><span data-ttu-id="5a6b7-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a6b7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a6b7-112">*сайт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a6b7-112">*site* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6b7-113">Указатель на интерфейс [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) сайта контейнера.</span><span class="sxs-lookup"><span data-stu-id="5a6b7-113">A pointer to the container site's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a6b7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5a6b7-114">Requirements</span></span>



| <span data-ttu-id="5a6b7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5a6b7-115">Requirement</span></span> | <span data-ttu-id="5a6b7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5a6b7-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5a6b7-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a6b7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5a6b7-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5a6b7-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5a6b7-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a6b7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5a6b7-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5a6b7-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5a6b7-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5a6b7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a6b7-122"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a6b7-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
