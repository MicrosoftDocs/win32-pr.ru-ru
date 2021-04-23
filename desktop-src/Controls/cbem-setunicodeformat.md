---
title: Сообщение CBEM_SETUNICODEFORMAT (Коммктрл. h)
description: Задает флаг формата символов Юникода для элемента управления. Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления.
ms.assetid: 4811709b-1639-4468-8598-97d9dc8d9057
keywords:
- Элементы управления Windows для CBEM_SETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- CBEM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89540d4e942b8b705685c13addeeb17adf0b4f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137287"
---
# <a name="cbem_setunicodeformat-message"></a><span data-ttu-id="8d24c-105">\_Сообщение кбем сетуникодеформат</span><span class="sxs-lookup"><span data-stu-id="8d24c-105">CBEM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="8d24c-106">Задает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="8d24c-106">Sets the UNICODE character format flag for the control.</span></span> <span data-ttu-id="8d24c-107">Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="8d24c-107">This message enables you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d24c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d24c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d24c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d24c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d24c-110">Определяет кодировку, используемую элементом управления.</span><span class="sxs-lookup"><span data-stu-id="8d24c-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="8d24c-111">Если это значение не равно нулю, элемент управления будет использовать символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="8d24c-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="8d24c-112">Если это значение равно нулю, элемент управления будет использовать символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="8d24c-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="8d24c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d24c-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8d24c-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8d24c-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d24c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d24c-115">Return value</span></span>

<span data-ttu-id="8d24c-116">Возвращает предыдущий флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="8d24c-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d24c-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d24c-117">Remarks</span></span>

<span data-ttu-id="8d24c-118">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ сетуникодеформат**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="8d24c-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d24c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8d24c-119">Requirements</span></span>



| <span data-ttu-id="8d24c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8d24c-120">Requirement</span></span> | <span data-ttu-id="8d24c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8d24c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d24c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d24c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8d24c-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8d24c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d24c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d24c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8d24c-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8d24c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d24c-126">Header</span><span class="sxs-lookup"><span data-stu-id="8d24c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d24c-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d24c-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d24c-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d24c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d24c-129">**КБЕМ \_ жетуникодеформат**</span><span class="sxs-lookup"><span data-stu-id="8d24c-129">**CBEM\_GETUNICODEFORMAT**</span></span>](cbem-getunicodeformat.md)
</dt> </dl>

 

 





