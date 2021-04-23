---
title: Сообщение PSM_SETFINISHTEXT (Пршт. h)
description: Задает текст кнопки "Готово" в мастере, показывает и включает кнопку, а также скрывает кнопки "Далее" и "назад". Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит сетфиништекст.
ms.assetid: fa89c6d7-9ab7-4e7c-ba08-d665420492a3
keywords:
- Элементы управления Windows для PSM_SETFINISHTEXT сообщений
topic_type:
- apiref
api_name:
- PSM_SETFINISHTEXT
- PSM_SETFINISHTEXTA
- PSM_SETFINISHTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08195cddc96c8b92f403be6940f31099e21151f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801223"
---
# <a name="psm_setfinishtext-message"></a><span data-ttu-id="d5db6-105">\_Сообщение ПСМ сетфиништекст</span><span class="sxs-lookup"><span data-stu-id="d5db6-105">PSM\_SETFINISHTEXT message</span></span>

<span data-ttu-id="d5db6-106">Задает текст кнопки **"Готово"** в мастере, показывает и включает кнопку, а также скрывает кнопки " **Далее** " и " **назад** ".</span><span class="sxs-lookup"><span data-stu-id="d5db6-106">Sets the text of the **Finish** button in a wizard, shows and enables the button, and hides the **Next** and **Back** buttons.</span></span> <span data-ttu-id="d5db6-107">Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ сетфиништекст**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) .</span><span class="sxs-lookup"><span data-stu-id="d5db6-107">You can send this message explicitly or by using the [**PropSheet\_SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d5db6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5db6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5db6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5db6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5db6-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d5db6-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d5db6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5db6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5db6-112">Указатель на новый текст для кнопки **"Готово"** .</span><span class="sxs-lookup"><span data-stu-id="d5db6-112">Pointer to the new text for the **Finish** button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5db6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5db6-113">Return value</span></span>

<span data-ttu-id="d5db6-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="d5db6-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5db6-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5db6-115">Remarks</span></span>

<span data-ttu-id="d5db6-116">По умолчанию кнопка **"Готово"** не имеет сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="d5db6-116">By default, the **Finish** button does not have a keyboard accelerator.</span></span> <span data-ttu-id="d5db6-117">Вы можете создать сочетание клавиш с помощью этого сообщения, включив амперсанд (&) в текстовую строку, назначенную для *lParam*.</span><span class="sxs-lookup"><span data-stu-id="d5db6-117">You can create a keyboard accelerator with this message by including an ampersand (&) in the text string that you assign to *lParam*.</span></span> <span data-ttu-id="d5db6-118">Например, "&Finish" определяет F в качестве сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="d5db6-118">For example, "&Finish" defines F as the accelerator key.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5db6-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d5db6-119">Requirements</span></span>



| <span data-ttu-id="d5db6-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d5db6-120">Requirement</span></span> | <span data-ttu-id="d5db6-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d5db6-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d5db6-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5db6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d5db6-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5db6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d5db6-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5db6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d5db6-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d5db6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d5db6-126">Header</span><span class="sxs-lookup"><span data-stu-id="d5db6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5db6-127"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5db6-127"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="d5db6-128">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="d5db6-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d5db6-129">**ПСМ \_ СЕТФИНИШТЕКСТВ** (Юникод) и **ПСМ \_ сетфиништекста** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d5db6-129">**PSM\_SETFINISHTEXTW** (Unicode) and **PSM\_SETFINISHTEXTA** (ANSI)</span></span><br/>    |



 

 





