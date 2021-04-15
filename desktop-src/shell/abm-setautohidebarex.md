---
description: Регистрирует или отменяет регистрацию панель приложенийа автоскрытия для заданной границы экрана. Это сообщение расширяет АБМ \_ сетаутохидебар, позволяя указать определенный монитор, который будет использоваться в ситуациях с несколькими мониторами.
title: Сообщение ABM_SETAUTOHIDEBAREX (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C437727C-3FF6-4598-9D81-A39FCC2EF1C4
api_name:
- ABM_SETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba4e1474d3b57465fa68446fd7ab787c9a62570b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104998888"
---
# <a name="abm_setautohidebarex-message"></a><span data-ttu-id="9b823-104">\_Сообщение АБМ сетаутохидебарекс</span><span class="sxs-lookup"><span data-stu-id="9b823-104">ABM\_SETAUTOHIDEBAREX message</span></span>

<span data-ttu-id="9b823-105">Регистрирует или отменяет регистрацию панель приложенийа автоскрытия для заданной границы экрана.</span><span class="sxs-lookup"><span data-stu-id="9b823-105">Registers or unregisters an autohide appbar for a given edge of the screen.</span></span> <span data-ttu-id="9b823-106">Это сообщение расширяет [**АБМ \_ сетаутохидебар**](abm-setautohidebar.md) , позволяя указать определенный монитор, который будет использоваться в ситуациях с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="9b823-106">This message extends [**ABM\_SETAUTOHIDEBAR**](abm-setautohidebar.md) by enabling you to specify a particular monitor, for use in multiple monitor situations.</span></span>


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="9b823-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b823-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b823-108">*пабд*</span><span class="sxs-lookup"><span data-stu-id="9b823-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="9b823-109">Указатель на структуру [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="9b823-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="9b823-110">Установите для члена **lParam** значение **true** , чтобы зарегистрировать панель приложений, или **false** , чтобы отменить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="9b823-110">Set the **lParam** member is to **TRUE** to register the appbar or **FALSE** to unregister it.</span></span> <span data-ttu-id="9b823-111">При отправке этого сообщения необходимо указать члены **кбсизе**, **HWND**, **уедже**, **RC** и **lParam** . все остальные элементы игнорируются.</span><span class="sxs-lookup"><span data-stu-id="9b823-111">You must specify the **cbSize**, **hWnd**, **uEdge**, **rc**, and **lParam** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b823-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b823-112">Return value</span></span>

<span data-ttu-id="9b823-113">Возвращает **true** при успешном выполнении, или **false** , если возникла ошибка или если панель приложений автоматически был зарегистрирован для данного объекта на данном мониторе.</span><span class="sxs-lookup"><span data-stu-id="9b823-113">Returns **TRUE** if successful, or **FALSE** if an error occurs or if an autohide appbar is already registered for the given edge on the given monitor.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b823-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9b823-114">Remarks</span></span>

<span data-ttu-id="9b823-115">Система допускает только одно автоматическое скрытие панель приложений для каждого края каждого монитора.</span><span class="sxs-lookup"><span data-stu-id="9b823-115">The system allows only one autohide appbar for each edge of each monitor.</span></span> <span data-ttu-id="9b823-116">Монитор определяется членом **RC** , а ребро определяется членом **уедже** структуры [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="9b823-116">The monitor is determined by the **rc** member and the edge is determined by the **uEdge** member of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b823-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9b823-117">Requirements</span></span>



| <span data-ttu-id="9b823-118">Требование</span><span class="sxs-lookup"><span data-stu-id="9b823-118">Requirement</span></span> | <span data-ttu-id="9b823-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9b823-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b823-120">Header</span><span class="sxs-lookup"><span data-stu-id="9b823-120">Header</span></span><br/> | <dl> <span data-ttu-id="9b823-121"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b823-121"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b823-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b823-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b823-123">**АБМ \_ жетаутохидебар**</span><span class="sxs-lookup"><span data-stu-id="9b823-123">**ABM\_GETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="9b823-124">**АБМ \_ жетаутохидебарекс**</span><span class="sxs-lookup"><span data-stu-id="9b823-124">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="9b823-125">**АБМ \_ сетаутохидебар**</span><span class="sxs-lookup"><span data-stu-id="9b823-125">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> </dl>

 

 




