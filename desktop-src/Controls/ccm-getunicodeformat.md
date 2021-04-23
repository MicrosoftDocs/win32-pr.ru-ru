---
title: Сообщение CCM_GETUNICODEFORMAT (Коммктрл. h)
description: Возвращает флаг формата символов Юникода для элемента управления.
ms.assetid: 8a23cd1c-549e-4d48-891a-b37dbf5c524b
keywords:
- Элементы управления Windows для CCM_GETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- CCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 095d49ccc57faa05e86d12df130b12ce3d542bf6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136455"
---
# <a name="ccm_getunicodeformat-message"></a><span data-ttu-id="84ab9-104">\_Сообщение ЖЕТУНИКОДЕФОРМАТ CCM</span><span class="sxs-lookup"><span data-stu-id="84ab9-104">CCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="84ab9-105">Возвращает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="84ab9-105">Gets the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="84ab9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="84ab9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84ab9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="84ab9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="84ab9-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="84ab9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="84ab9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84ab9-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="84ab9-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="84ab9-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84ab9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84ab9-111">Return value</span></span>

<span data-ttu-id="84ab9-112">Возвращает флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="84ab9-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="84ab9-113">Если это значение не равно нулю, то элемент управления использует символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="84ab9-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="84ab9-114">Если это значение равно нулю, то элемент управления использует символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="84ab9-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="84ab9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="84ab9-115">Requirements</span></span>



| <span data-ttu-id="84ab9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="84ab9-116">Requirement</span></span> | <span data-ttu-id="84ab9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="84ab9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84ab9-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84ab9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="84ab9-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84ab9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84ab9-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84ab9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="84ab9-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="84ab9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84ab9-122">Header</span><span class="sxs-lookup"><span data-stu-id="84ab9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="84ab9-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="84ab9-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84ab9-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84ab9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84ab9-125">**\_СЕТУНИКОДЕФОРМАТ CCM**</span><span class="sxs-lookup"><span data-stu-id="84ab9-125">**CCM\_SETUNICODEFORMAT**</span></span>](ccm-setunicodeformat.md)
</dt> </dl>

 

 





