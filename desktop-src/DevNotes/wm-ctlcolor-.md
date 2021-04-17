---
description: Сообщение WM \_ ктлколор используется в 16-разрядных версиях Windows для изменения цветовой схемы списков, списков полей со списками, окон сообщений, элементов управления "Кнопка", "Правка", статических элементов управления и диалоговых окон. Примечание. сведения, относящиеся к этому сообщению и 32-разрядным версиям Windows, см. в разделе Примечания.
ms.assetid: e654cf48-550f-4210-9952-20470b9a397a
title: Сообщение WM_CTLCOLOR (Виндовскс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8166979c17b7d2eef50af062e5df13712e9d32ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657439"
---
# <a name="wm_ctlcolor-message"></a><span data-ttu-id="1a787-103">\_Сообщение КТЛКОЛОР WM</span><span class="sxs-lookup"><span data-stu-id="1a787-103">WM\_CTLCOLOR message</span></span>

<span data-ttu-id="1a787-104">Сообщение **WM \_ ктлколор** используется в 16-разрядных версиях Windows для изменения цветовой схемы списков, списков полей со списками, окон сообщений, элементов управления "Кнопка", "Правка", статических элементов управления и диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="1a787-104">The **WM\_CTLCOLOR** message is used in 16-bit versions of Windows to change the color scheme of list boxes, the list boxes of combo boxes, message boxes, button controls, edit controls, static controls, and dialog boxes.</span></span>

> [!Note]  
> <span data-ttu-id="1a787-105">Сведения, относящиеся к этому сообщению и 32-разрядным версиям Windows, см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="1a787-105">For information related to this message and 32-bit versions of Windows, see Remarks.</span></span>

 


```C++
  WM_CTLCOLOR

  WPARAM wParam;
  LPARAM lParam;
    
```



## <a name="parameters"></a><span data-ttu-id="1a787-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a787-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a787-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="1a787-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="1a787-108">Маркер окна назначения.</span><span class="sxs-lookup"><span data-stu-id="1a787-108">A handle to destination window.</span></span>

</dd> <dt>

<span data-ttu-id="1a787-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a787-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a787-110">Маркер контекстного интерфейса (DC).</span><span class="sxs-lookup"><span data-stu-id="1a787-110">A handle to a display context (DC).</span></span>

</dd> <dt>

<span data-ttu-id="1a787-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a787-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a787-112">Маркер дочернего окна (элемента управления).</span><span class="sxs-lookup"><span data-stu-id="1a787-112">A handle to a child window (control).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a787-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a787-113">Return value</span></span>

<span data-ttu-id="1a787-114">Если приложение обрабатывает это сообщение, оно возвращает дескриптор кисти.</span><span class="sxs-lookup"><span data-stu-id="1a787-114">If an application processes this message, it returns a handle to a brush.</span></span> <span data-ttu-id="1a787-115">Система использует кисть для рисования фона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1a787-115">The system uses the brush to paint the background of the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a787-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a787-116">Remarks</span></span>

<span data-ttu-id="1a787-117">Сообщение **WM \_ ктлколор** из 16-разрядной версии Windows заменено более конкретными уведомлениями.</span><span class="sxs-lookup"><span data-stu-id="1a787-117">The **WM\_CTLCOLOR** message from 16-bit Windows has been replaced by more specific notifications.</span></span> <span data-ttu-id="1a787-118">В число этих замен входят следующие.</span><span class="sxs-lookup"><span data-stu-id="1a787-118">These replacements include the following:</span></span>

-   [<span data-ttu-id="1a787-119">**WM \_ ктлколорбтн**</span><span class="sxs-lookup"><span data-stu-id="1a787-119">**WM\_CTLCOLORBTN**</span></span>](../controls/wm-ctlcolorbtn.md)
-   [<span data-ttu-id="1a787-120">**WM \_ ктлколоредит**</span><span class="sxs-lookup"><span data-stu-id="1a787-120">**WM\_CTLCOLOREDIT**</span></span>](../controls/wm-ctlcoloredit.md)
-   [<span data-ttu-id="1a787-121">**WM \_ ктлколордлг**</span><span class="sxs-lookup"><span data-stu-id="1a787-121">**WM\_CTLCOLORDLG**</span></span>](../dlgbox/wm-ctlcolordlg.md)
-   [<span data-ttu-id="1a787-122">**WM \_ ктлколорлистбокс**</span><span class="sxs-lookup"><span data-stu-id="1a787-122">**WM\_CTLCOLORLISTBOX**</span></span>](../controls/wm-ctlcolorlistbox.md)
-   [<span data-ttu-id="1a787-123">**WM \_ ктлколорскроллбар**</span><span class="sxs-lookup"><span data-stu-id="1a787-123">**WM\_CTLCOLORSCROLLBAR**</span></span>](../controls/wm-ctlcolorscrollbar.md)
-   [<span data-ttu-id="1a787-124">**WM \_ ктлколорстатик**</span><span class="sxs-lookup"><span data-stu-id="1a787-124">**WM\_CTLCOLORSTATIC**</span></span>](../controls/wm-ctlcolorstatic.md)

## <a name="requirements"></a><span data-ttu-id="1a787-125">Требования</span><span class="sxs-lookup"><span data-stu-id="1a787-125">Requirements</span></span>



| <span data-ttu-id="1a787-126">Требование</span><span class="sxs-lookup"><span data-stu-id="1a787-126">Requirement</span></span> | <span data-ttu-id="1a787-127">Значение</span><span class="sxs-lookup"><span data-stu-id="1a787-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a787-128">Header</span><span class="sxs-lookup"><span data-stu-id="1a787-128">Header</span></span><br/> | <dl> <span data-ttu-id="1a787-129"><dt>Виндовскс. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a787-129"><dt>WindowsX.h</dt></span></span> </dl> |



 

 
