---
description: Посылается окну-владельцу элемента управления или пункта меню при создании элемента управления или меню.
ms.assetid: 4584a3da-6c92-4ecd-8cf2-e4afc1b8321d
title: Сообщение DFM_WM_MEASUREITEM (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c4ad79acf221ecaabf9060940ad2514422bef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423705"
---
# <a name="dfm_wm_measureitem-message"></a><span data-ttu-id="bfbfe-103">\_Сообщение DFM WM \_ меасуреитем</span><span class="sxs-lookup"><span data-stu-id="bfbfe-103">DFM\_WM\_MEASUREITEM message</span></span>

<span data-ttu-id="bfbfe-104">Посылается окну-владельцу элемента управления или пункта меню при создании элемента управления или меню.</span><span class="sxs-lookup"><span data-stu-id="bfbfe-104">Sent to the owner window of a control or menu item when the control or menu is created.</span></span>


```C++
DFM_WM_MEASUREITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPMEASUREITEMSTRUCT) lpMeasureItem;

            
```



## <a name="parameters"></a><span data-ttu-id="bfbfe-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="bfbfe-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfbfe-106">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bfbfe-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfbfe-107">Значение элемента **ктлид** структуры [**меасуреитемструкт**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) , на которое указывает параметр *лпмеасуреитем* .</span><span class="sxs-lookup"><span data-stu-id="bfbfe-107">The value of the **CtlID** member of the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lpMeasureItem* parameter.</span></span> <span data-ttu-id="bfbfe-108">Это значение определяет элемент управления, который отправил сообщение **DFM \_ WM \_ меасуреитем** .</span><span class="sxs-lookup"><span data-stu-id="bfbfe-108">This value identifies the control that sent the **DFM\_WM\_MEASUREITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="bfbfe-109">*лпмеасуреитем* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bfbfe-109">*lpMeasureItem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfbfe-110">Указатель на структуру [**меасуреитемструкт**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) , содержащую Размеры рисуемого владельцем элемента управления или пункта меню.</span><span class="sxs-lookup"><span data-stu-id="bfbfe-110">A pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that contains the dimensions of the owner-drawn control or menu item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bfbfe-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="bfbfe-111">Remarks</span></span>

<span data-ttu-id="bfbfe-112">Когда окно владельца получает сообщение **DFM \_ WM \_ меасуреитем** , владелец заполняет структуру [**меасуреитемструкт**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) , на которую указывает параметр *лпмеасуреитем* сообщения, и возвращает значение, которое информирует систему о размерах элемента управления.</span><span class="sxs-lookup"><span data-stu-id="bfbfe-112">When the owner window receives the **DFM\_WM\_MEASUREITEM** message, the owner fills in the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lpMeasureItem* parameter of the message and returns; this informs the system of the dimensions of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfbfe-113">Требования</span><span class="sxs-lookup"><span data-stu-id="bfbfe-113">Requirements</span></span>



| <span data-ttu-id="bfbfe-114">Требование</span><span class="sxs-lookup"><span data-stu-id="bfbfe-114">Requirement</span></span> | <span data-ttu-id="bfbfe-115">Значение</span><span class="sxs-lookup"><span data-stu-id="bfbfe-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bfbfe-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bfbfe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bfbfe-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bfbfe-117">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bfbfe-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bfbfe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bfbfe-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bfbfe-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bfbfe-120">Header</span><span class="sxs-lookup"><span data-stu-id="bfbfe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfbfe-121"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfbfe-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
