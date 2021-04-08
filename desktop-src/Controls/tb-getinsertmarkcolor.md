---
title: Сообщение TB_GETINSERTMARKCOLOR (Коммктрл. h)
description: Получает цвет, используемый для рисования метки вставки панели инструментов.
ms.assetid: 52915dc6-a45c-4f3b-aa9b-99a23d423e59
keywords:
- Элементы управления Windows для TB_GETINSERTMARKCOLOR сообщений
topic_type:
- apiref
api_name:
- TB_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104ceebd5f3989ed870cf70ccad819300d85c05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891961"
---
# <a name="tb_getinsertmarkcolor-message"></a><span data-ttu-id="07d96-104">\_Сообщение ЖЕТИНСЕРТМАРККОЛОР ТБ</span><span class="sxs-lookup"><span data-stu-id="07d96-104">TB\_GETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="07d96-105">Получает цвет, используемый для рисования метки вставки панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="07d96-105">Retrieves the color used to draw the insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="07d96-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="07d96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07d96-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="07d96-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="07d96-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="07d96-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="07d96-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07d96-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="07d96-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="07d96-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07d96-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07d96-111">Return value</span></span>

<span data-ttu-id="07d96-112">Возвращает значение [**COLORREF**](/windows/desktop/gdi/colorref) , содержащее текущий цвет отметки вставки.</span><span class="sxs-lookup"><span data-stu-id="07d96-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that contains the current insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="07d96-113">Требования</span><span class="sxs-lookup"><span data-stu-id="07d96-113">Requirements</span></span>



| <span data-ttu-id="07d96-114">Требование</span><span class="sxs-lookup"><span data-stu-id="07d96-114">Requirement</span></span> | <span data-ttu-id="07d96-115">Значение</span><span class="sxs-lookup"><span data-stu-id="07d96-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07d96-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07d96-116">Minimum supported client</span></span><br/> | <span data-ttu-id="07d96-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="07d96-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="07d96-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07d96-118">Minimum supported server</span></span><br/> | <span data-ttu-id="07d96-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="07d96-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="07d96-120">Header</span><span class="sxs-lookup"><span data-stu-id="07d96-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="07d96-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="07d96-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07d96-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07d96-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d96-123">**\_СЕТИНСЕРТМАРККОЛОР ТБ**</span><span class="sxs-lookup"><span data-stu-id="07d96-123">**TB\_SETINSERTMARKCOLOR**</span></span>](tb-setinsertmarkcolor.md)
</dt> </dl>

 

