---
description: Извлекает маркер панель приложенийа автоскрытия, связанный с границей экрана. Это сообщение расширяет АБМ \_ жетаутохидебар, позволяя указать определенный монитор, который будет использоваться в ситуациях с несколькими мониторами.
title: Сообщение ABM_GETAUTOHIDEBAREX (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 538EA230-06DF-4441-A6AA-9DD613521BE1
api_name:
- ABM_GETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ef95739a1031efb199e6acd99686e0858a9630e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987518"
---
# <a name="abm_getautohidebarex-message"></a><span data-ttu-id="73074-104">\_Сообщение АБМ жетаутохидебарекс</span><span class="sxs-lookup"><span data-stu-id="73074-104">ABM\_GETAUTOHIDEBAREX message</span></span>

<span data-ttu-id="73074-105">Извлекает маркер панель приложенийа автоскрытия, связанный с границей экрана.</span><span class="sxs-lookup"><span data-stu-id="73074-105">Retrieves the handle to the autohide appbar associated with an edge of the screen.</span></span> <span data-ttu-id="73074-106">Это сообщение расширяет [**АБМ \_ жетаутохидебар**](abm-getautohidebar.md) , позволяя указать определенный монитор, который будет использоваться в ситуациях с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="73074-106">This message extends [**ABM\_GETAUTOHIDEBAR**](abm-getautohidebar.md) by enabling you to specify a particular monitor, for use in multiple monitor situations.</span></span>


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a><span data-ttu-id="73074-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="73074-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73074-108">*пабд*</span><span class="sxs-lookup"><span data-stu-id="73074-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="73074-109">Указатель на структуру [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) , которая указывает границы экрана и монитор.</span><span class="sxs-lookup"><span data-stu-id="73074-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that specifies the screen edge and monitor.</span></span> <span data-ttu-id="73074-110">При отправке этого сообщения необходимо указать члены **кбсизе**, **уедже** и **RC** . все остальные элементы игнорируются.</span><span class="sxs-lookup"><span data-stu-id="73074-110">You must specify the **cbSize**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73074-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73074-111">Return value</span></span>

<span data-ttu-id="73074-112">Возвращает маркер для панель приложенийа автоскрытия.</span><span class="sxs-lookup"><span data-stu-id="73074-112">Returns the handle to the autohide appbar.</span></span> <span data-ttu-id="73074-113">Возвращаемое значение равно **null** , если возникает ошибка или если панель приложений не связан с данным ребром данного монитора.</span><span class="sxs-lookup"><span data-stu-id="73074-113">The return value is **NULL** if an error occurs or if no autohide appbar is associated with the given edge of the given monitor.</span></span>

## <a name="requirements"></a><span data-ttu-id="73074-114">Требования</span><span class="sxs-lookup"><span data-stu-id="73074-114">Requirements</span></span>



| <span data-ttu-id="73074-115">Требование</span><span class="sxs-lookup"><span data-stu-id="73074-115">Requirement</span></span> | <span data-ttu-id="73074-116">Значение</span><span class="sxs-lookup"><span data-stu-id="73074-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73074-117">Header</span><span class="sxs-lookup"><span data-stu-id="73074-117">Header</span></span><br/> | <dl> <span data-ttu-id="73074-118"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="73074-118"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73074-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73074-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73074-120">**АБМ \_ жетаутохидебар**</span><span class="sxs-lookup"><span data-stu-id="73074-120">**ABM\_GETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="73074-121">**АБМ \_ сетаутохидебар**</span><span class="sxs-lookup"><span data-stu-id="73074-121">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> <dt>

[<span data-ttu-id="73074-122">**АБМ \_ сетаутохидебарекс**</span><span class="sxs-lookup"><span data-stu-id="73074-122">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 




