---
title: Сообщение LVM_GETSTRINGWIDTH (Коммктрл. h)
description: Определяет ширину указанной строки с использованием текущего шрифта указанного элемента управления "список-представление". Это сообщение можно отправить явно или с помощью \_ макроса Жетстрингвидс ListView.
ms.assetid: ffe97640-d4b6-45ae-be5d-71fed69c2026
keywords:
- Элементы управления Windows для LVM_GETSTRINGWIDTH сообщений
topic_type:
- apiref
api_name:
- LVM_GETSTRINGWIDTH
- LVM_GETSTRINGWIDTHA
- LVM_GETSTRINGWIDTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e27512eb7a2a260976356ed2a128b48975f9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535039"
---
# <a name="lvm_getstringwidth-message"></a><span data-ttu-id="0ca27-105">\_Сообщение LVM жетстрингвидс</span><span class="sxs-lookup"><span data-stu-id="0ca27-105">LVM\_GETSTRINGWIDTH message</span></span>

<span data-ttu-id="0ca27-106">Определяет ширину указанной строки с использованием текущего шрифта указанного элемента управления "список-представление".</span><span class="sxs-lookup"><span data-stu-id="0ca27-106">Determines the width of a specified string using the specified list-view control's current font.</span></span> <span data-ttu-id="0ca27-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетстрингвидс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) .</span><span class="sxs-lookup"><span data-stu-id="0ca27-107">You can send this message explicitly or by using the [**ListView\_GetStringWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ca27-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ca27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ca27-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0ca27-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0ca27-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="0ca27-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0ca27-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ca27-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ca27-112">Указатель на строку, завершающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="0ca27-112">Pointer to a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ca27-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ca27-113">Return value</span></span>

<span data-ttu-id="0ca27-114">Возвращает ширину строки в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0ca27-114">Returns the string width if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ca27-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ca27-115">Remarks</span></span>

<span data-ttu-id="0ca27-116">Сообщение LVM \_ жетстрингвидс возвращает точную ширину (в пикселях) указанной строки.</span><span class="sxs-lookup"><span data-stu-id="0ca27-116">The LVM\_GETSTRINGWIDTH message returns the exact width, in pixels, of the specified string.</span></span> <span data-ttu-id="0ca27-117">При использовании возвращаемой ширины строки в качестве ширины столбца в сообщении [**LVM \_ сетколумнвидс**](lvm-setcolumnwidth.md) строка будет обрезана.</span><span class="sxs-lookup"><span data-stu-id="0ca27-117">If you use the returned string width as the column width in the [**LVM\_SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) message, the string will be truncated.</span></span> <span data-ttu-id="0ca27-118">Чтобы получить ширину столбца, которая может содержать строку без усечения, необходимо добавить заполнение к возвращаемой ширине строки.</span><span class="sxs-lookup"><span data-stu-id="0ca27-118">To retrieve the column width that can contain the string without truncating it, you must add padding to the returned string width.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ca27-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0ca27-119">Requirements</span></span>



| <span data-ttu-id="0ca27-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0ca27-120">Requirement</span></span> | <span data-ttu-id="0ca27-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0ca27-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ca27-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ca27-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0ca27-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0ca27-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ca27-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ca27-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0ca27-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0ca27-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ca27-126">Header</span><span class="sxs-lookup"><span data-stu-id="0ca27-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ca27-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ca27-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0ca27-128">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="0ca27-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0ca27-129">**LVM \_ ЖЕТСТРИНГВИДСВ** (Юникод) и **LVM \_ жетстрингвидса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0ca27-129">**LVM\_GETSTRINGWIDTHW** (Unicode) and **LVM\_GETSTRINGWIDTHA** (ANSI)</span></span><br/>     |



 

 





