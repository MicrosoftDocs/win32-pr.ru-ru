---
description: 'Позволяет объекту обратного вызова изменять всплывающее меню проводника Windows перед отображением. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_INITMENUPOPUP (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9d7e96e9-c52e-43bd-945b-05db33c8dfd0
api_name:
- SFVM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1f9a2a169b232fe3ad16eeee8816536ed81c74dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986077"
---
# <a name="sfvm_initmenupopup-message"></a><span data-ttu-id="23ab6-104">\_Сообщение сфвм инитменупопуп</span><span class="sxs-lookup"><span data-stu-id="23ab6-104">SFVM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="23ab6-105">Позволяет объекту обратного вызова изменять всплывающее меню проводника Windows перед отображением.</span><span class="sxs-lookup"><span data-stu-id="23ab6-105">Allows the callback object to modify a Windows Explorer pop-up menu before it is displayed.</span></span> <span data-ttu-id="23ab6-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="23ab6-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_INITMENUPOPUP 

    wParam = (WPARAM)(int) idCmd,nIndex;

    lParam = (LPARAM)(HMENU) hmenu;

            
```



## <a name="parameters"></a><span data-ttu-id="23ab6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="23ab6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23ab6-108">*идкмд \_ ниндекс* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="23ab6-108">*idCmd\_nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23ab6-109">Младшее слово этого параметра содержит значение первого идентификатора команды, зарезервированного для клиентских команд.</span><span class="sxs-lookup"><span data-stu-id="23ab6-109">The low-order word of this parameter holds the value of the first command ID reserved for client commands.</span></span> <span data-ttu-id="23ab6-110">Слово в высоком порядке содержит индекс меню.</span><span class="sxs-lookup"><span data-stu-id="23ab6-110">The high-order word holds the index of the menu.</span></span>

</dd> <dt>

<span data-ttu-id="23ab6-111">*HMENU* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="23ab6-111">*hmenu* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="23ab6-112">Маркер меню.</span><span class="sxs-lookup"><span data-stu-id="23ab6-112">The menu's handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23ab6-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="23ab6-113">Remarks</span></span>

<span data-ttu-id="23ab6-114">Объект представления системных папок отправляет это сообщение, если выбрано меню, но перед его отображением.</span><span class="sxs-lookup"><span data-stu-id="23ab6-114">The system folder view object sends this message when a menu is selected, but before it is displayed.</span></span> <span data-ttu-id="23ab6-115">Обработайте это сообщение, если, например, необходимо включить или отключить команды меню.</span><span class="sxs-lookup"><span data-stu-id="23ab6-115">Process this message if, for instance, you need to enable or disable menu commands.</span></span> <span data-ttu-id="23ab6-116">Всплывающее меню может быть следующим:</span><span class="sxs-lookup"><span data-stu-id="23ab6-116">The popup menu can be:</span></span>

-   <span data-ttu-id="23ab6-117">Меню файл, Правка или вид.</span><span class="sxs-lookup"><span data-stu-id="23ab6-117">The File, Edit, or View menu.</span></span>
-   <span data-ttu-id="23ab6-118">Меню верхнего уровня, определенное клиентом.</span><span class="sxs-lookup"><span data-stu-id="23ab6-118">A top-level menu defined by the client.</span></span>
-   <span data-ttu-id="23ab6-119">Определяемое клиентом подменю.</span><span class="sxs-lookup"><span data-stu-id="23ab6-119">A client-defined submenu.</span></span>

## <a name="requirements"></a><span data-ttu-id="23ab6-120">Требования</span><span class="sxs-lookup"><span data-stu-id="23ab6-120">Requirements</span></span>



| <span data-ttu-id="23ab6-121">Требование</span><span class="sxs-lookup"><span data-stu-id="23ab6-121">Requirement</span></span> | <span data-ttu-id="23ab6-122">Значение</span><span class="sxs-lookup"><span data-stu-id="23ab6-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="23ab6-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="23ab6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="23ab6-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="23ab6-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="23ab6-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="23ab6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="23ab6-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="23ab6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="23ab6-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="23ab6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="23ab6-128"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="23ab6-128"><dt>Shlobj.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23ab6-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23ab6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23ab6-130">**СФВМ \_ мержемену**</span><span class="sxs-lookup"><span data-stu-id="23ab6-130">**SFVM\_MERGEMENU**</span></span>](sfvm-mergemenu.md)
</dt> </dl>

 

 
