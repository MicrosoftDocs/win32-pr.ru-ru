---
description: DFM_WM_INITMENUPOPUP сообщение — отправляется, когда раскрывающийся меню или подменю собирается стать активным. Это позволяет приложению изменять меню до его отображения, не изменяя весь меню.
title: Сообщение DFM_WM_INITMENUPOPUP (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 314e83f7-839d-4ca0-b5c1-842c5bf14923
api_name:
- DFM_WM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9df2700403dcdc0ce00b6d90d9c3a87d373b0a34
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097002"
---
# <a name="dfm_wm_initmenupopup-message"></a><span data-ttu-id="4d12d-104">\_Сообщение DFM WM \_ инитменупопуп</span><span class="sxs-lookup"><span data-stu-id="4d12d-104">DFM\_WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="4d12d-105">Посылается, когда раскрывающееся меню или подменю станет активным.</span><span class="sxs-lookup"><span data-stu-id="4d12d-105">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="4d12d-106">Это позволяет приложению изменять меню до его отображения, не изменяя весь меню.</span><span class="sxs-lookup"><span data-stu-id="4d12d-106">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a><span data-ttu-id="4d12d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d12d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d12d-108">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4d12d-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d12d-109">Маркер раскрывающегося меню или подменю.</span><span class="sxs-lookup"><span data-stu-id="4d12d-109">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="4d12d-110">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4d12d-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d12d-111">Слово нижнего порядка указывает относительное расположение элемента меню, начинающееся с нуля, которое открывает раскрывающееся меню или подменю.</span><span class="sxs-lookup"><span data-stu-id="4d12d-111">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="4d12d-112">Слово высокого порядка указывает, является ли раскрывающееся меню окном.</span><span class="sxs-lookup"><span data-stu-id="4d12d-112">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="4d12d-113">Если меню является меню окно, этот параметр имеет **значение true**; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="4d12d-113">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d12d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4d12d-114">Return value</span></span>

<span data-ttu-id="4d12d-115">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="4d12d-115">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d12d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4d12d-116">Requirements</span></span>



| <span data-ttu-id="4d12d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4d12d-117">Requirement</span></span> | <span data-ttu-id="4d12d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4d12d-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4d12d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d12d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4d12d-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4d12d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4d12d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d12d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4d12d-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4d12d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4d12d-123">Header</span><span class="sxs-lookup"><span data-stu-id="4d12d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d12d-124"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d12d-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




