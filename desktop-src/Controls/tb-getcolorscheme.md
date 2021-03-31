---
title: Сообщение TB_GETCOLORSCHEME (Коммктрл. h)
description: Извлекает сведения о цветовой схеме из элемента управления ToolBar.
ms.assetid: af172631-309e-4181-a690-05946cd6e143
keywords:
- Элементы управления Windows для TB_GETCOLORSCHEME сообщений
topic_type:
- apiref
api_name:
- TB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61344439ae8bc2b3a9ecd47472174577d652aa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490998"
---
# <a name="tb_getcolorscheme-message"></a><span data-ttu-id="38776-104">\_Сообщение ЖЕТКОЛОРСЧЕМЕ ТБ</span><span class="sxs-lookup"><span data-stu-id="38776-104">TB\_GETCOLORSCHEME message</span></span>

<span data-ttu-id="38776-105">Извлекает сведения о цветовой схеме из элемента управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="38776-105">Retrieves the color scheme information from the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="38776-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="38776-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38776-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38776-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="38776-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="38776-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="38776-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38776-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38776-110">Указатель на структуру [**колорсчеме**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) , которая получит сведения о цветовой схеме.</span><span class="sxs-lookup"><span data-stu-id="38776-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that will receive the color scheme information.</span></span> <span data-ttu-id="38776-111">Перед отправкой этого сообщения необходимо задать для элемента **кбсизе** этой структуры значение **sizeof**(колорсчеме).</span><span class="sxs-lookup"><span data-stu-id="38776-111">You must set the **cbSize** member of this structure to **sizeof**(COLORSCHEME) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38776-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38776-112">Return value</span></span>

<span data-ttu-id="38776-113">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="38776-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="38776-114">Требования</span><span class="sxs-lookup"><span data-stu-id="38776-114">Requirements</span></span>



| <span data-ttu-id="38776-115">Требование</span><span class="sxs-lookup"><span data-stu-id="38776-115">Requirement</span></span> | <span data-ttu-id="38776-116">Значение</span><span class="sxs-lookup"><span data-stu-id="38776-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38776-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38776-117">Minimum supported client</span></span><br/> | <span data-ttu-id="38776-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38776-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="38776-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38776-119">Minimum supported server</span></span><br/> | <span data-ttu-id="38776-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="38776-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="38776-121">Header</span><span class="sxs-lookup"><span data-stu-id="38776-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="38776-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="38776-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38776-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38776-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38776-124">**\_СЕТКОЛОРСЧЕМЕ ТБ**</span><span class="sxs-lookup"><span data-stu-id="38776-124">**TB\_SETCOLORSCHEME**</span></span>](tb-setcolorscheme.md)
</dt> </dl>

 

 





