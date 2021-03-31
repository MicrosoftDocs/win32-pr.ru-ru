---
title: Сообщение MCM_SETUNICODEFORMAT (Коммктрл. h)
description: Задает флаг формата символов Юникода для элемента управления.
ms.assetid: 250789b5-694b-4502-9cc0-3bc260ea06e7
keywords:
- Элементы управления Windows для MCM_SETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- MCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0aee3318479f4e94b4d85f15fe7c58e4417a1bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490857"
---
# <a name="mcm_setunicodeformat-message"></a><span data-ttu-id="01fba-104">\_Сообщение MCM сетуникодеформат</span><span class="sxs-lookup"><span data-stu-id="01fba-104">MCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="01fba-105">Задает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="01fba-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="01fba-106">Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="01fba-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="01fba-107">Это сообщение можно отправить явным образом или использовать макрос [**монскал \_ сетуникодеформат**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="01fba-107">You can send this message explicitly or use the [**MonthCal\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="01fba-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="01fba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01fba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="01fba-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01fba-110">Определяет кодировку, используемую элементом управления.</span><span class="sxs-lookup"><span data-stu-id="01fba-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="01fba-111">Если это значение не равно нулю, элемент управления будет использовать символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="01fba-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="01fba-112">Если это значение равно нулю, элемент управления будет использовать символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="01fba-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="01fba-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01fba-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="01fba-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="01fba-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01fba-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01fba-115">Return value</span></span>

<span data-ttu-id="01fba-116">Возвращает предыдущий флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="01fba-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="01fba-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01fba-117">Remarks</span></span>

<span data-ttu-id="01fba-118">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ сетуникодеформат**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="01fba-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="01fba-119">Требования</span><span class="sxs-lookup"><span data-stu-id="01fba-119">Requirements</span></span>



| <span data-ttu-id="01fba-120">Требование</span><span class="sxs-lookup"><span data-stu-id="01fba-120">Requirement</span></span> | <span data-ttu-id="01fba-121">Значение</span><span class="sxs-lookup"><span data-stu-id="01fba-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01fba-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01fba-122">Minimum supported client</span></span><br/> | <span data-ttu-id="01fba-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01fba-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="01fba-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01fba-124">Minimum supported server</span></span><br/> | <span data-ttu-id="01fba-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01fba-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="01fba-126">Header</span><span class="sxs-lookup"><span data-stu-id="01fba-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="01fba-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="01fba-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01fba-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01fba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01fba-129">**MCM \_ жетуникодеформат**</span><span class="sxs-lookup"><span data-stu-id="01fba-129">**MCM\_GETUNICODEFORMAT**</span></span>](mcm-getunicodeformat.md)
</dt> </dl>

 

 





