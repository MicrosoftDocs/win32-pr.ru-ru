---
title: Сообщение UDM_SETUNICODEFORMAT (Коммктрл. h)
description: Задает флаг формата символов Юникода для элемента управления. Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления.
ms.assetid: abe882db-bf32-40b0-a1c0-3e89cdc93fe7
keywords:
- Элементы управления Windows для UDM_SETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- UDM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db3f9dbc1e19fdb43aa0b7d5e6de6fdddd308eb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071678"
---
# <a name="udm_setunicodeformat-message"></a><span data-ttu-id="28973-105">\_Сообщение СЕТУНИКОДЕФОРМАТ UDM</span><span class="sxs-lookup"><span data-stu-id="28973-105">UDM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="28973-106">Задает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="28973-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="28973-107">Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="28973-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="28973-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="28973-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28973-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="28973-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28973-110">Определяет кодировку, используемую элементом управления.</span><span class="sxs-lookup"><span data-stu-id="28973-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="28973-111">Если это значение равно **true**, элемент управления будет использовать символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="28973-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="28973-112">Если это значение равно **false**, элемент управления будет использовать символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="28973-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="28973-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28973-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="28973-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="28973-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28973-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28973-115">Return value</span></span>

<span data-ttu-id="28973-116">Возвращает предыдущий флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="28973-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="28973-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28973-117">Remarks</span></span>

<span data-ttu-id="28973-118">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ сетуникодеформат**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="28973-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="28973-119">Требования</span><span class="sxs-lookup"><span data-stu-id="28973-119">Requirements</span></span>



| <span data-ttu-id="28973-120">Требование</span><span class="sxs-lookup"><span data-stu-id="28973-120">Requirement</span></span> | <span data-ttu-id="28973-121">Значение</span><span class="sxs-lookup"><span data-stu-id="28973-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28973-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28973-122">Minimum supported client</span></span><br/> | <span data-ttu-id="28973-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28973-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="28973-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28973-124">Minimum supported server</span></span><br/> | <span data-ttu-id="28973-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="28973-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="28973-126">Header</span><span class="sxs-lookup"><span data-stu-id="28973-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="28973-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="28973-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28973-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28973-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28973-129">**\_ЖЕТУНИКОДЕФОРМАТ UDM**</span><span class="sxs-lookup"><span data-stu-id="28973-129">**UDM\_GETUNICODEFORMAT**</span></span>](udm-getunicodeformat.md)
</dt> </dl>

 

 





