---
title: Сообщение TB_BUTTONSTRUCTSIZE (Коммктрл. h)
description: Задает размер структуры ТББУТТОН.
ms.assetid: 4e63a075-4191-44c1-8df6-38fce51d4be5
keywords:
- Элементы управления Windows для TB_BUTTONSTRUCTSIZE сообщений
topic_type:
- apiref
api_name:
- TB_BUTTONSTRUCTSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7187c1f4cb45306fd293c7eb74ef8807f395ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072031"
---
# <a name="tb_buttonstructsize-message"></a><span data-ttu-id="e8736-104">\_Сообщение БУТТОНСТРУКТСИЗЕ ТБ</span><span class="sxs-lookup"><span data-stu-id="e8736-104">TB\_BUTTONSTRUCTSIZE message</span></span>

<span data-ttu-id="e8736-105">Задает размер структуры [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) .</span><span class="sxs-lookup"><span data-stu-id="e8736-105">Specifies the size of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8736-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8736-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8736-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8736-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8736-108">Размер (в байтах) структуры [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) .</span><span class="sxs-lookup"><span data-stu-id="e8736-108">Size, in bytes, of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e8736-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8736-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e8736-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e8736-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8736-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8736-111">Return value</span></span>

<span data-ttu-id="e8736-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="e8736-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8736-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8736-113">Remarks</span></span>

<span data-ttu-id="e8736-114">Система использует размер для определения используемой версии библиотеки динамической компоновки (DLL) общего элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e8736-114">The system uses the size to determine which version of the common control dynamic-link library (DLL) is being used.</span></span>

<span data-ttu-id="e8736-115">Если приложение использует функцию [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) для создания панели инструментов, приложение должно отправить это сообщение на панель инструментов перед отправкой сообщения [**ТБ \_ аддбитмап**](tb-addbitmap.md) или [**ТБ \_ аддбуттонс**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="e8736-115">If an application uses the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create the toolbar, the application must send this message to the toolbar before sending the [**TB\_ADDBITMAP**](tb-addbitmap.md) or [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span> <span data-ttu-id="e8736-116">Функция [**креатетулбарекс**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) автоматически отправляет **ТБ \_ буттонструктсизе**, а размер структуры [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) является параметром функции.</span><span class="sxs-lookup"><span data-stu-id="e8736-116">The [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) function automatically sends **TB\_BUTTONSTRUCTSIZE**, and the size of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure is a parameter of the function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8736-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e8736-117">Requirements</span></span>



| <span data-ttu-id="e8736-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e8736-118">Requirement</span></span> | <span data-ttu-id="e8736-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e8736-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8736-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8736-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e8736-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8736-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8736-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8736-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e8736-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e8736-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8736-124">Header</span><span class="sxs-lookup"><span data-stu-id="e8736-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8736-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8736-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

