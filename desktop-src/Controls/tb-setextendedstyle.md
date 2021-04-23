---
title: Сообщение TB_SETEXTENDEDSTYLE (Коммктрл. h)
description: Задает расширенные стили для элемента управления ToolBar.
ms.assetid: aec64bc7-74b4-4efc-9864-2c8a9fbd35c2
keywords:
- Элементы управления Windows для TB_SETEXTENDEDSTYLE сообщений
topic_type:
- apiref
api_name:
- TB_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a540aaeff61bd81b649f0509e064a29282f598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136806"
---
# <a name="tb_setextendedstyle-message"></a><span data-ttu-id="2e537-104">\_Сообщение СЕТЕКСТЕНДЕДСТИЛЕ ТБ</span><span class="sxs-lookup"><span data-stu-id="2e537-104">TB\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="2e537-105">Задает расширенные стили для элемента управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="2e537-105">Sets the extended styles for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e537-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e537-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e537-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e537-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2e537-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="2e537-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2e537-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e537-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e537-110">Значение, указывающее новые расширенные стили.</span><span class="sxs-lookup"><span data-stu-id="2e537-110">Value specifying the new extended styles.</span></span> <span data-ttu-id="2e537-111">Этот параметр может быть сочетанием [расширенных стилей](toolbar-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="2e537-111">This parameter can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e537-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e537-112">Return value</span></span>

<span data-ttu-id="2e537-113">Возвращает значение **типа DWORD** , представляющее предыдущие расширенные стили.</span><span class="sxs-lookup"><span data-stu-id="2e537-113">Returns a **DWORD** that represents the previous extended styles.</span></span> <span data-ttu-id="2e537-114">Это значение может быть сочетанием [расширенных стилей](toolbar-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="2e537-114">This value can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e537-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2e537-115">Requirements</span></span>



| <span data-ttu-id="2e537-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2e537-116">Requirement</span></span> | <span data-ttu-id="2e537-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2e537-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e537-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e537-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2e537-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e537-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e537-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e537-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2e537-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2e537-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e537-122">Header</span><span class="sxs-lookup"><span data-stu-id="2e537-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e537-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e537-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e537-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e537-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e537-125">**\_ЖЕТЕКСТЕНДЕДСТИЛЕ ТБ**</span><span class="sxs-lookup"><span data-stu-id="2e537-125">**TB\_GETEXTENDEDSTYLE**</span></span>](tb-getextendedstyle.md)
</dt> </dl>

 

 





