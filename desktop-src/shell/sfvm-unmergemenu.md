---
description: 'Уведомляет объект обратного вызова, что удаляется меню. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_UNMERGEMENU (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0255a41d-e8b4-48d2-931a-aa76ad83c18c
api_name:
- SFVM_UNMERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6c83df7ca42d66f320339901a176dc9d4d38ff37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986068"
---
# <a name="sfvm_unmergemenu-message"></a><span data-ttu-id="282b5-104">\_Сообщение сфвм унмержемену</span><span class="sxs-lookup"><span data-stu-id="282b5-104">SFVM\_UNMERGEMENU message</span></span>

<span data-ttu-id="282b5-105">Уведомляет объект обратного вызова, что удаляется меню.</span><span class="sxs-lookup"><span data-stu-id="282b5-105">Notifies the callback object that a menu is being removed.</span></span> <span data-ttu-id="282b5-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="282b5-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_UNMERGEMENU 

    lParam = (LPARAM)(HMENU) hmenuCurrent;

            
```



## <a name="parameters"></a><span data-ttu-id="282b5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="282b5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="282b5-108">*хменукуррент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="282b5-108">*hmenuCurrent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="282b5-109">Описатель удаляемого меню.</span><span class="sxs-lookup"><span data-stu-id="282b5-109">The handle of the menu that is being removed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="282b5-110">Требования</span><span class="sxs-lookup"><span data-stu-id="282b5-110">Requirements</span></span>



| <span data-ttu-id="282b5-111">Требование</span><span class="sxs-lookup"><span data-stu-id="282b5-111">Requirement</span></span> | <span data-ttu-id="282b5-112">Значение</span><span class="sxs-lookup"><span data-stu-id="282b5-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="282b5-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="282b5-113">Minimum supported client</span></span><br/> | <span data-ttu-id="282b5-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="282b5-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="282b5-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="282b5-115">Minimum supported server</span></span><br/> | <span data-ttu-id="282b5-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="282b5-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="282b5-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="282b5-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="282b5-118"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="282b5-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
