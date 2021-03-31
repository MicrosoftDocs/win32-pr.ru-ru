---
title: Сообщение PSM_SETBUTTONTEXT (Пршт. h)
description: Задает текст на кнопке в мастере Aero. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит сетбуттонтекст.
ms.assetid: 30b7afd1-5094-430f-9c48-d87832d96050
keywords:
- Элементы управления Windows для PSM_SETBUTTONTEXT сообщений
topic_type:
- apiref
api_name:
- PSM_SETBUTTONTEXT
- PSM_SETBUTTONTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a0b55f73fc7084e89f54c1e741d12000b0f949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071516"
---
# <a name="psm_setbuttontext-message"></a><span data-ttu-id="f1de9-105">\_Сообщение ПСМ сетбуттонтекст</span><span class="sxs-lookup"><span data-stu-id="f1de9-105">PSM\_SETBUTTONTEXT message</span></span>

<span data-ttu-id="f1de9-106">Задает текст на кнопке в мастере Aero.</span><span class="sxs-lookup"><span data-stu-id="f1de9-106">Sets the text on a button in an Aero wizard.</span></span> <span data-ttu-id="f1de9-107">Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ сетбуттонтекст**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) .</span><span class="sxs-lookup"><span data-stu-id="f1de9-107">You can send this message explicitly or by using the [**PropSheet\_SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f1de9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1de9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1de9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f1de9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1de9-110">Одно из следующих значений, задающее кнопку, для которой задан текст.</span><span class="sxs-lookup"><span data-stu-id="f1de9-110">One of the following values specifying the button whose text is set.</span></span>



| <span data-ttu-id="f1de9-111">Значение</span><span class="sxs-lookup"><span data-stu-id="f1de9-111">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="f1de9-112">Значение</span><span class="sxs-lookup"><span data-stu-id="f1de9-112">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="f1de9-113"><dt>**ПСВИЗБ \_ назад**</dt></span><span class="sxs-lookup"><span data-stu-id="f1de9-113"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="f1de9-114">Кнопка " **назад** ".</span><span class="sxs-lookup"><span data-stu-id="f1de9-114">The **Back** button.</span></span><br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="f1de9-115"><dt>**ПСВИЗБ \_ Отмена**</dt></span><span class="sxs-lookup"><span data-stu-id="f1de9-115"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="f1de9-116">Кнопка **Отмена** .</span><span class="sxs-lookup"><span data-stu-id="f1de9-116">The **Cancel** button.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="f1de9-117"><dt>**ПСВИЗБ \_ дисабледфиниш**</dt></span><span class="sxs-lookup"><span data-stu-id="f1de9-117"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="f1de9-118">Кнопка **"Готово"** .</span><span class="sxs-lookup"><span data-stu-id="f1de9-118">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="f1de9-119"><dt>**\_Завершение псвизб**</dt></span><span class="sxs-lookup"><span data-stu-id="f1de9-119"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="f1de9-120">Кнопка **"Готово"** .</span><span class="sxs-lookup"><span data-stu-id="f1de9-120">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="f1de9-121"><dt>**ПСВИЗБ \_ Далее**</dt></span><span class="sxs-lookup"><span data-stu-id="f1de9-121"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="f1de9-122">Кнопка **Далее** .</span><span class="sxs-lookup"><span data-stu-id="f1de9-122">The **Next** button.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="f1de9-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1de9-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1de9-124">Заданный текст.</span><span class="sxs-lookup"><span data-stu-id="f1de9-124">The text to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1de9-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1de9-125">Return value</span></span>

<span data-ttu-id="f1de9-126">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="f1de9-126">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1de9-127">Требования</span><span class="sxs-lookup"><span data-stu-id="f1de9-127">Requirements</span></span>



| <span data-ttu-id="f1de9-128">Требование</span><span class="sxs-lookup"><span data-stu-id="f1de9-128">Requirement</span></span> | <span data-ttu-id="f1de9-129">Значение</span><span class="sxs-lookup"><span data-stu-id="f1de9-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f1de9-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1de9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f1de9-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f1de9-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f1de9-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1de9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f1de9-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f1de9-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f1de9-134">Header</span><span class="sxs-lookup"><span data-stu-id="f1de9-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1de9-135"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1de9-135"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="f1de9-136">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f1de9-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f1de9-137">**ПСМ \_ СЕТБУТТОНТЕКСТВ** (Юникод)</span><span class="sxs-lookup"><span data-stu-id="f1de9-137">**PSM\_SETBUTTONTEXTW** (Unicode)</span></span><br/>                                       |



 

 





