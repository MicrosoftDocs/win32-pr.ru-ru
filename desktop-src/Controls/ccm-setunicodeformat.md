---
title: Сообщение CCM_SETUNICODEFORMAT (Коммктрл. h)
description: Задает флаг формата символов Юникода для элемента управления. Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления.
ms.assetid: 8028b7d7-30d2-4154-81c7-ba1ed095ef02
keywords:
- Элементы управления Windows для CCM_SETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- CCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffbe9f5032c193cb612f68ca8ed6ec6b04ce8094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491520"
---
# <a name="ccm_setunicodeformat-message"></a><span data-ttu-id="61d84-105">\_Сообщение СЕТУНИКОДЕФОРМАТ CCM</span><span class="sxs-lookup"><span data-stu-id="61d84-105">CCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="61d84-106">Задает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="61d84-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="61d84-107">Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="61d84-107">This message enables you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="61d84-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="61d84-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61d84-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="61d84-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61d84-110">Значение, определяющее кодировку, используемую элементом управления.</span><span class="sxs-lookup"><span data-stu-id="61d84-110">A value that determines the character set that is used by the control.</span></span> <span data-ttu-id="61d84-111">Если это значение равно **true**, элемент управления будет использовать символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="61d84-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="61d84-112">Если это значение равно **false**, элемент управления будет использовать символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="61d84-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="61d84-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61d84-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="61d84-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="61d84-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61d84-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="61d84-115">Return value</span></span>

<span data-ttu-id="61d84-116">Возвращает предыдущий флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="61d84-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="61d84-117">Требования</span><span class="sxs-lookup"><span data-stu-id="61d84-117">Requirements</span></span>



| <span data-ttu-id="61d84-118">Требование</span><span class="sxs-lookup"><span data-stu-id="61d84-118">Requirement</span></span> | <span data-ttu-id="61d84-119">Значение</span><span class="sxs-lookup"><span data-stu-id="61d84-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61d84-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61d84-120">Minimum supported client</span></span><br/> | <span data-ttu-id="61d84-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61d84-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61d84-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61d84-122">Minimum supported server</span></span><br/> | <span data-ttu-id="61d84-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="61d84-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61d84-124">Header</span><span class="sxs-lookup"><span data-stu-id="61d84-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="61d84-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="61d84-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61d84-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61d84-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61d84-127">**\_ЖЕТУНИКОДЕФОРМАТ CCM**</span><span class="sxs-lookup"><span data-stu-id="61d84-127">**CCM\_GETUNICODEFORMAT**</span></span>](ccm-getunicodeformat.md)
</dt> </dl>

 

 





