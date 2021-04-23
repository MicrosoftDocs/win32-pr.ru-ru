---
description: Извлекает маркер панель приложенийа автоскрытия, связанный с границей экрана. Если в системе установлено несколько мониторов, используется монитор, содержащий основную панель задач.
title: Сообщение ABM_GETAUTOHIDEBAR (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 545dd1d9-8cbb-4ff3-b871-4908ecac56db
api_name:
- ABM_GETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 979825a9dbc28a89e3579419542877faacbace45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143996"
---
# <a name="abm_getautohidebar-message"></a><span data-ttu-id="3a724-104">\_Сообщение АБМ жетаутохидебар</span><span class="sxs-lookup"><span data-stu-id="3a724-104">ABM\_GETAUTOHIDEBAR message</span></span>

<span data-ttu-id="3a724-105">Извлекает маркер панель приложенийа автоскрытия, связанный с границей экрана.</span><span class="sxs-lookup"><span data-stu-id="3a724-105">Retrieves the handle to the autohide appbar associated with an edge of the screen.</span></span> <span data-ttu-id="3a724-106">Если в системе установлено несколько мониторов, используется монитор, содержащий основную панель задач.</span><span class="sxs-lookup"><span data-stu-id="3a724-106">If the system has multiple monitors, the monitor that contains the primary taskbar is used.</span></span>

> [!Note]  
> <span data-ttu-id="3a724-107">Чтобы запросить автоматическое скрытие панель приложений на определенном мониторе, используйте [**АБМ \_ жетаутохидебарекс**](abm-getautohidebarex.md).</span><span class="sxs-lookup"><span data-stu-id="3a724-107">To query for an autohide appbar on a specific monitor, use [**ABM\_GETAUTOHIDEBAREX**](abm-getautohidebarex.md).</span></span>

 


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a><span data-ttu-id="3a724-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a724-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a724-109">*пабд*</span><span class="sxs-lookup"><span data-stu-id="3a724-109">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="3a724-110">Указатель на структуру [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) , указывающую границу экрана.</span><span class="sxs-lookup"><span data-stu-id="3a724-110">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that specifies the screen edge.</span></span> <span data-ttu-id="3a724-111">При отправке этого сообщения необходимо указать члены **кбсизе** и **уедже** ; все остальные элементы игнорируются.</span><span class="sxs-lookup"><span data-stu-id="3a724-111">You must specify the **cbSize** and **uEdge** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a724-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a724-112">Return value</span></span>

<span data-ttu-id="3a724-113">Возвращает маркер для панель приложенийа автоскрытия.</span><span class="sxs-lookup"><span data-stu-id="3a724-113">Returns the handle to the autohide appbar.</span></span> <span data-ttu-id="3a724-114">Возвращаемое значение равно **null** , если возникает ошибка или если панель приложений не связан с данным ребром.</span><span class="sxs-lookup"><span data-stu-id="3a724-114">The return value is **NULL** if an error occurs or if no autohide appbar is associated with the given edge.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a724-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3a724-115">Requirements</span></span>



| <span data-ttu-id="3a724-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3a724-116">Requirement</span></span> | <span data-ttu-id="3a724-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3a724-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a724-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a724-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3a724-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3a724-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3a724-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a724-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3a724-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3a724-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a724-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3a724-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a724-123"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a724-123"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a724-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a724-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a724-125">**АБМ \_ сетаутохидебар**</span><span class="sxs-lookup"><span data-stu-id="3a724-125">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> <dt>

[<span data-ttu-id="3a724-126">**АБМ \_ жетаутохидебарекс**</span><span class="sxs-lookup"><span data-stu-id="3a724-126">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="3a724-127">**АБМ \_ сетаутохидебарекс**</span><span class="sxs-lookup"><span data-stu-id="3a724-127">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 




