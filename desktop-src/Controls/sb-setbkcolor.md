---
title: Сообщение SB_SETBKCOLOR (Коммктрл. h)
description: Задает цвет фона в строке состояния.
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- Элементы управления Windows для SB_SETBKCOLOR сообщений
topic_type:
- apiref
api_name:
- SB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc08687c6d228074bc3e4dd7c8442a1c1e35a835
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415940"
---
# <a name="sb_setbkcolor-message"></a><span data-ttu-id="3c0f4-104">\_Сообщение SB сетбкколор</span><span class="sxs-lookup"><span data-stu-id="3c0f4-104">SB\_SETBKCOLOR message</span></span>

<span data-ttu-id="3c0f4-105">Задает цвет фона в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-105">Sets the background color in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c0f4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c0f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c0f4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c0f4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3c0f4-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3c0f4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c0f4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c0f4-110">Значение [**COLORREF**](/windows/desktop/gdi/colorref) , указывающее новый цвет фона.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that specifies the new background color.</span></span> <span data-ttu-id="3c0f4-111">Укажите \_ значение по умолчанию CLR, чтобы строка состояния использовала цвет фона по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-111">Specify the CLR\_DEFAULT value to cause the status bar to use its default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c0f4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c0f4-112">Return value</span></span>

<span data-ttu-id="3c0f4-113">Возвращает предыдущий цвет фона или \_ значение по умолчанию CLR, если цвет фона является цветом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-113">Returns the previous background color, or CLR\_DEFAULT if the background color is the default color.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c0f4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3c0f4-114">Requirements</span></span>



| <span data-ttu-id="3c0f4-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3c0f4-115">Requirement</span></span> | <span data-ttu-id="3c0f4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3c0f4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c0f4-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c0f4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3c0f4-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c0f4-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c0f4-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c0f4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3c0f4-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3c0f4-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c0f4-121">Header</span><span class="sxs-lookup"><span data-stu-id="3c0f4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c0f4-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c0f4-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

