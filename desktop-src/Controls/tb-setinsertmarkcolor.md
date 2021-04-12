---
title: Сообщение TB_SETINSERTMARKCOLOR (Коммктрл. h)
description: Задает цвет, используемый для отображения метки вставки для панели инструментов.
ms.assetid: 09a04449-9a1f-4f9a-b09f-9f22f930d735
keywords:
- Элементы управления Windows для TB_SETINSERTMARKCOLOR сообщений
topic_type:
- apiref
api_name:
- TB_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 954654d71a3e3b7bba9af287d3e92fb2362e8711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135099"
---
# <a name="tb_setinsertmarkcolor-message"></a><span data-ttu-id="9af58-104">\_Сообщение СЕТИНСЕРТМАРККОЛОР ТБ</span><span class="sxs-lookup"><span data-stu-id="9af58-104">TB\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="9af58-105">Задает цвет, используемый для отображения метки вставки для панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="9af58-105">Sets the color used to draw the insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="9af58-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9af58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9af58-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9af58-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9af58-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9af58-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9af58-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9af58-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9af58-110">Значение **COLORREF** , содержащее новый цвет метки вставки.</span><span class="sxs-lookup"><span data-stu-id="9af58-110">**COLORREF** value that contains the new insertion mark color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9af58-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9af58-111">Return value</span></span>

<span data-ttu-id="9af58-112">Возвращает значение **COLORREF** , содержащее предыдущий цвет отметки вставки.</span><span class="sxs-lookup"><span data-stu-id="9af58-112">Returns a **COLORREF** value that contains the previous insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="9af58-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9af58-113">Requirements</span></span>



| <span data-ttu-id="9af58-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9af58-114">Requirement</span></span> | <span data-ttu-id="9af58-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9af58-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9af58-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9af58-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9af58-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9af58-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9af58-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9af58-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9af58-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9af58-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9af58-120">Header</span><span class="sxs-lookup"><span data-stu-id="9af58-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9af58-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9af58-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9af58-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9af58-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9af58-123">**\_ЖЕТИНСЕРТМАРККОЛОР ТБ**</span><span class="sxs-lookup"><span data-stu-id="9af58-123">**TB\_GETINSERTMARKCOLOR**</span></span>](tb-getinsertmarkcolor.md)
</dt> </dl>

 

 





