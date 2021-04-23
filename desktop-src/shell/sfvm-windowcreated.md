---
description: 'Уведомляет объект обратного вызова, что окно представления папок создается. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_WINDOWCREATED (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b57eb1d8-a897-4358-a855-89e152035eff
api_name:
- SFVM_WINDOWCREATED
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d545feadecdaadbf776f94e653df8b71150ac05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986093"
---
# <a name="sfvm_windowcreated-message"></a><span data-ttu-id="3023a-104">\_Сообщение сфвм WINDOWCREATED</span><span class="sxs-lookup"><span data-stu-id="3023a-104">SFVM\_WINDOWCREATED message</span></span>

<span data-ttu-id="3023a-105">Уведомляет объект обратного вызова, что окно представления папок создается.</span><span class="sxs-lookup"><span data-stu-id="3023a-105">Notifies the callback object that the folder view window is being created.</span></span> <span data-ttu-id="3023a-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="3023a-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_WINDOWCREATED 

    wParam = (WPARAM)(HWND) hwndView;

            
```



## <a name="parameters"></a><span data-ttu-id="3023a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3023a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3023a-108">*хвндвиев* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3023a-108">*hwndView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3023a-109">Обработчик окна представления папки.</span><span class="sxs-lookup"><span data-stu-id="3023a-109">The folder view's window handle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3023a-110">Требования</span><span class="sxs-lookup"><span data-stu-id="3023a-110">Requirements</span></span>



| <span data-ttu-id="3023a-111">Требование</span><span class="sxs-lookup"><span data-stu-id="3023a-111">Requirement</span></span> | <span data-ttu-id="3023a-112">Значение</span><span class="sxs-lookup"><span data-stu-id="3023a-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3023a-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3023a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3023a-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3023a-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3023a-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3023a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3023a-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3023a-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3023a-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3023a-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="3023a-118"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="3023a-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
