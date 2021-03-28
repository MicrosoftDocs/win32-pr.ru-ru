---
description: Регистрирует или отменяет регистрацию панель приложенийа автоскрытия для заданной границы экрана. Если в системе установлено несколько мониторов, используется монитор, содержащий основную панель задач.
title: Сообщение ABM_SETAUTOHIDEBAR (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0cbd6c9c-e83f-41f8-91ed-81afaa24f524
api_name:
- ABM_SETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 53ca89008dda1233d12a7f0a9588803776ba1181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984385"
---
# <a name="abm_setautohidebar-message"></a><span data-ttu-id="0e05c-104">\_Сообщение АБМ сетаутохидебар</span><span class="sxs-lookup"><span data-stu-id="0e05c-104">ABM\_SETAUTOHIDEBAR message</span></span>

<span data-ttu-id="0e05c-105">Регистрирует или отменяет регистрацию панель приложенийа автоскрытия для заданной границы экрана.</span><span class="sxs-lookup"><span data-stu-id="0e05c-105">Registers or unregisters an autohide appbar for a given edge of the screen.</span></span> <span data-ttu-id="0e05c-106">Если в системе установлено несколько мониторов, используется монитор, содержащий основную панель задач.</span><span class="sxs-lookup"><span data-stu-id="0e05c-106">If the system has multiple monitors, the monitor that contains the primary taskbar is used.</span></span>

> [!Note]  
> <span data-ttu-id="0e05c-107">Чтобы зарегистрировать или отменить регистрацию панель приложенийов для автоскрытия на определенном мониторе, используйте [**АБМ \_ сетаутохидебарекс**](abm-setautohidebarex.md).</span><span class="sxs-lookup"><span data-stu-id="0e05c-107">To register or unregister an autohide appbar on a specific monitor, use [**ABM\_SETAUTOHIDEBAREX**](abm-setautohidebarex.md).</span></span>

 


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="0e05c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e05c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e05c-109">*пабд*</span><span class="sxs-lookup"><span data-stu-id="0e05c-109">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="0e05c-110">Указатель на структуру [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="0e05c-110">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="0e05c-111">Присвойте  члену lParam **значение true** , чтобы зарегистрировать панель приложений, или **false** , чтобы отменить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="0e05c-111">Set the **lParam** member to **TRUE** to register the appbar or **FALSE** to unregister it.</span></span> <span data-ttu-id="0e05c-112">При отправке этого сообщения необходимо указать члены **кбсизе**, **HWND**, **уедже** и **lParam** . все остальные элементы игнорируются.</span><span class="sxs-lookup"><span data-stu-id="0e05c-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **lParam** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e05c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e05c-113">Return value</span></span>

<span data-ttu-id="0e05c-114">Возвращает **значение true** в случае успеха или **значение false** , если возникла ошибка или если панель приложений с автоматическим скрытием уже зарегистрирован для данного ребра.</span><span class="sxs-lookup"><span data-stu-id="0e05c-114">Returns **TRUE** if successful, or **FALSE** if an error occurs or if an autohide appbar is already registered for the given edge.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e05c-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="0e05c-115">Remarks</span></span>

<span data-ttu-id="0e05c-116">Система допускает только одно автоматическое скрытие панель приложений для каждого края экрана.</span><span class="sxs-lookup"><span data-stu-id="0e05c-116">The system allows only one autohide appbar for each edge of the screen.</span></span> <span data-ttu-id="0e05c-117">Это определяется в том случае, если задан элемент **уедже** структуры [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="0e05c-117">This is determined when the member **uEdge** of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e05c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0e05c-118">Requirements</span></span>



| <span data-ttu-id="0e05c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0e05c-119">Requirement</span></span> | <span data-ttu-id="0e05c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0e05c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e05c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e05c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0e05c-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0e05c-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0e05c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e05c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0e05c-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0e05c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e05c-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0e05c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e05c-126"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e05c-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e05c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e05c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e05c-128">**АБМ \_ сетаутохидебар**</span><span class="sxs-lookup"><span data-stu-id="0e05c-128">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="0e05c-129">**АБМ \_ жетаутохидебарекс**</span><span class="sxs-lookup"><span data-stu-id="0e05c-129">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="0e05c-130">**АБМ \_ сетаутохидебарекс**</span><span class="sxs-lookup"><span data-stu-id="0e05c-130">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 




