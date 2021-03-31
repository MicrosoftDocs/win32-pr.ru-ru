---
title: Сообщение TB_GETEXTENDEDSTYLE (Коммктрл. h)
description: Извлекает расширенные стили для элемента управления ToolBar.
ms.assetid: d9e31a8e-5e5a-4d2d-bc3b-65ac40e8592f
keywords:
- Элементы управления Windows для TB_GETEXTENDEDSTYLE сообщений
topic_type:
- apiref
api_name:
- TB_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80bc4f4ad45e5c1c75366e0890f3fd76ec1fa74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802057"
---
# <a name="tb_getextendedstyle-message"></a><span data-ttu-id="d2e48-104">\_Сообщение ЖЕТЕКСТЕНДЕДСТИЛЕ ТБ</span><span class="sxs-lookup"><span data-stu-id="d2e48-104">TB\_GETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="d2e48-105">Извлекает расширенные стили для элемента управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="d2e48-105">Retrieves the extended styles for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2e48-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2e48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2e48-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2e48-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d2e48-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d2e48-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d2e48-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2e48-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d2e48-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d2e48-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2e48-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2e48-111">Return value</span></span>

<span data-ttu-id="d2e48-112">Возвращает **DWORD** , представляющий стили, используемые в данный момент для элемента управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="d2e48-112">Returns a **DWORD** that represents the styles currently in use for the toolbar control.</span></span> <span data-ttu-id="d2e48-113">Это значение может быть сочетанием [расширенных стилей](toolbar-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="d2e48-113">This value can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2e48-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d2e48-114">Requirements</span></span>



| <span data-ttu-id="d2e48-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d2e48-115">Requirement</span></span> | <span data-ttu-id="d2e48-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d2e48-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2e48-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2e48-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d2e48-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2e48-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2e48-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2e48-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d2e48-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2e48-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2e48-121">Header</span><span class="sxs-lookup"><span data-stu-id="d2e48-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2e48-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2e48-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2e48-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2e48-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2e48-124">**\_СЕТЕКСТЕНДЕДСТИЛЕ ТБ**</span><span class="sxs-lookup"><span data-stu-id="d2e48-124">**TB\_SETEXTENDEDSTYLE**</span></span>](tb-setextendedstyle.md)
</dt> </dl>

 

 





