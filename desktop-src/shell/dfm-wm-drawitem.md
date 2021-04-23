---
description: Посылается родительскому окну рисуемого владельцем элемента управления или меню при изменении визуального аспекта элемента управления или меню.
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: Сообщение DFM_WM_DRAWITEM (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67255fea5c39bebc995e5c53d90378536b12921b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984293"
---
# <a name="dfm_wm_drawitem-message"></a><span data-ttu-id="01066-103">\_Сообщение DFM WM \_ DRAWITEM</span><span class="sxs-lookup"><span data-stu-id="01066-103">DFM\_WM\_DRAWITEM message</span></span>

<span data-ttu-id="01066-104">Посылается родительскому окну рисуемого владельцем элемента управления или меню при изменении визуального аспекта элемента управления или меню.</span><span class="sxs-lookup"><span data-stu-id="01066-104">Sent to the parent window of an owner-drawn control or menu when a visual aspect of the control or menu has changed.</span></span>


```C++
DFM_WM_DRAWITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPDRAWITEMSTRUCT) lpDrawItem;

            
```



## <a name="parameters"></a><span data-ttu-id="01066-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="01066-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01066-106">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01066-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01066-107">Идентификатор элемента управления, отправившего сообщение **DFM \_ WM \_ DRAWITEM** .</span><span class="sxs-lookup"><span data-stu-id="01066-107">The identifier of the control that sent the **DFM\_WM\_DRAWITEM** message.</span></span> <span data-ttu-id="01066-108">Если сообщение было отправлено меню, этот параметр равен нулю.</span><span class="sxs-lookup"><span data-stu-id="01066-108">If the message was sent by a menu, this parameter is zero.</span></span>

</dd> <dt>

<span data-ttu-id="01066-109">*лпдравитем* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="01066-109">*lpDrawItem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01066-110">Указатель на структуру [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , содержащую сведения о рисуемом элементе, и требуемый тип рисования.</span><span class="sxs-lookup"><span data-stu-id="01066-110">A pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure containing information about the item to be drawn and the type of drawing required.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01066-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01066-111">Return value</span></span>

<span data-ttu-id="01066-112">Если приложение обрабатывает это сообщение, оно должно возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="01066-112">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="01066-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="01066-113">Remarks</span></span>

<span data-ttu-id="01066-114">Элемент **итемактион** структуры [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) указывает операцию рисования, которую должно выполнить приложение.</span><span class="sxs-lookup"><span data-stu-id="01066-114">The **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure specifies the drawing operation that an application should perform.</span></span>

<span data-ttu-id="01066-115">Перед возвратом из обработки этого сообщения приложение должно убедиться, что контекст устройства, определенный членом **HDC** структуры [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , находится в состоянии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="01066-115">Before returning from processing this message, an application should ensure that the device context identified by the **hDC** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure is in the default state.</span></span>

## <a name="requirements"></a><span data-ttu-id="01066-116">Требования</span><span class="sxs-lookup"><span data-stu-id="01066-116">Requirements</span></span>



| <span data-ttu-id="01066-117">Требование</span><span class="sxs-lookup"><span data-stu-id="01066-117">Requirement</span></span> | <span data-ttu-id="01066-118">Значение</span><span class="sxs-lookup"><span data-stu-id="01066-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="01066-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01066-119">Minimum supported client</span></span><br/> | <span data-ttu-id="01066-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01066-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="01066-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01066-121">Minimum supported server</span></span><br/> | <span data-ttu-id="01066-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="01066-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="01066-123">Header</span><span class="sxs-lookup"><span data-stu-id="01066-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="01066-124"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="01066-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
