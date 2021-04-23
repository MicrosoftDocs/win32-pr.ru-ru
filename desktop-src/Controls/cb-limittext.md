---
title: Сообщение CB_LIMITTEXT (Winuser. h)
description: Ограничивает длину текста, который пользователь может ввести в поле ввода поля со списком.
ms.assetid: 95b7d07a-594b-4096-afbb-4dab77bdc41d
keywords:
- Элементы управления Windows для CB_LIMITTEXT сообщений
topic_type:
- apiref
api_name:
- CB_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ea9ccd63bb1503e73aebdd584a53bc32bcb8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071611"
---
# <a name="cb_limittext-message"></a><span data-ttu-id="084b8-104">\_Сообщение ЛИМИТТЕКСТ CB</span><span class="sxs-lookup"><span data-stu-id="084b8-104">CB\_LIMITTEXT message</span></span>

<span data-ttu-id="084b8-105">Ограничивает длину текста, который пользователь может ввести в поле ввода поля со списком.</span><span class="sxs-lookup"><span data-stu-id="084b8-105">Limits the length of the text the user may type into the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="084b8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="084b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="084b8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="084b8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="084b8-108">Максимальное число **тчарс** , которое может ввести пользователь, не включая завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="084b8-108">The maximum number of **TCHARs** the user can enter, not including the terminating null character.</span></span> <span data-ttu-id="084b8-109">Если этот параметр равен нулю, длина текста ограничена 0x7FFFFFFE символами.</span><span class="sxs-lookup"><span data-stu-id="084b8-109">If this parameter is zero, the text length is limited to 0x7FFFFFFE characters.</span></span>

</dd> <dt>

<span data-ttu-id="084b8-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="084b8-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="084b8-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="084b8-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="084b8-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="084b8-112">Return value</span></span>

<span data-ttu-id="084b8-113">Возвращаемое значение всегда равно **true**.</span><span class="sxs-lookup"><span data-stu-id="084b8-113">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="084b8-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="084b8-114">Remarks</span></span>

<span data-ttu-id="084b8-115">Если поле со списком не имеет стиля [**CBS \_ аутохскролл**](combo-box-styles.md) , Установка предельного размера текста больше, чем размер элемента управления "поле ввода", не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="084b8-115">If the combo box does not have the [**CBS\_AUTOHSCROLL**](combo-box-styles.md) style, setting the text limit to be larger than the size of the edit control has no effect.</span></span>

<span data-ttu-id="084b8-116">Сообщение **\_ лимиттекст CB** ограничивает только текст, который может ввести пользователь.</span><span class="sxs-lookup"><span data-stu-id="084b8-116">The **CB\_LIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="084b8-117">Он не влияет на любой текст, уже находящиеся в элементе управления "поле ввода" при отправке сообщения, и на длину текста, скопированного в элемент управления "поле ввода", при выборе строки в списке.</span><span class="sxs-lookup"><span data-stu-id="084b8-117">It has no effect on any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control when a string in the list box is selected.</span></span>

<span data-ttu-id="084b8-118">Ограничение по умолчанию для текста, которое пользователь может ввести в поле ввода, — 30 000 **тчарс**.</span><span class="sxs-lookup"><span data-stu-id="084b8-118">The default limit to the text a user can enter in the edit control is 30,000 **TCHARs**.</span></span>

## <a name="requirements"></a><span data-ttu-id="084b8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="084b8-119">Requirements</span></span>



| <span data-ttu-id="084b8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="084b8-120">Requirement</span></span> | <span data-ttu-id="084b8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="084b8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="084b8-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="084b8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="084b8-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="084b8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="084b8-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="084b8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="084b8-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="084b8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="084b8-126">Header</span><span class="sxs-lookup"><span data-stu-id="084b8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="084b8-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="084b8-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





