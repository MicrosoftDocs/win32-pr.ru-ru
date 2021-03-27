---
description: Посылается, когда раскрывающееся меню или подменю станет активным. Это позволяет приложению изменять меню до его отображения, не изменяя весь меню.
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
ms.openlocfilehash: 1c89731bdffc0e7d902e6c83b9a4f208134b7cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143954"
---
# <a name="dfm_wm_initmenupopup-message"></a><span data-ttu-id="57c4b-104">\_Сообщение DFM WM \_ инитменупопуп</span><span class="sxs-lookup"><span data-stu-id="57c4b-104">DFM\_WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="57c4b-105">Посылается, когда раскрывающееся меню или подменю станет активным.</span><span class="sxs-lookup"><span data-stu-id="57c4b-105">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="57c4b-106">Это позволяет приложению изменять меню до его отображения, не изменяя весь меню.</span><span class="sxs-lookup"><span data-stu-id="57c4b-106">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a><span data-ttu-id="57c4b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="57c4b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57c4b-108">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="57c4b-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57c4b-109">Маркер раскрывающегося меню или подменю.</span><span class="sxs-lookup"><span data-stu-id="57c4b-109">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="57c4b-110">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="57c4b-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57c4b-111">Слово нижнего порядка указывает относительное расположение элемента меню, начинающееся с нуля, которое открывает раскрывающееся меню или подменю.</span><span class="sxs-lookup"><span data-stu-id="57c4b-111">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="57c4b-112">Слово высокого порядка указывает, является ли раскрывающееся меню окном.</span><span class="sxs-lookup"><span data-stu-id="57c4b-112">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="57c4b-113">Если меню является меню окно, этот параметр имеет **значение true**; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="57c4b-113">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57c4b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57c4b-114">Return value</span></span>

<span data-ttu-id="57c4b-115">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="57c4b-115">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="57c4b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="57c4b-116">Requirements</span></span>



| <span data-ttu-id="57c4b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="57c4b-117">Requirement</span></span> | <span data-ttu-id="57c4b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="57c4b-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="57c4b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57c4b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="57c4b-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="57c4b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="57c4b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57c4b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="57c4b-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="57c4b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="57c4b-123">Header</span><span class="sxs-lookup"><span data-stu-id="57c4b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="57c4b-124"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="57c4b-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




