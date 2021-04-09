---
title: Сообщение PSM_ENABLEWIZBUTTONS (Пршт. h)
description: Включает или отключает любые стандартные кнопки в мастере Aero. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ енаблевизбуттонс.
ms.assetid: 9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4
keywords:
- Элементы управления Windows для PSM_ENABLEWIZBUTTONS сообщений
topic_type:
- apiref
api_name:
- PSM_ENABLEWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01fb30fa3337aed369c2cd24a1296785bd6b3a79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988905"
---
# <a name="psm_enablewizbuttons-message"></a><span data-ttu-id="adf64-105">\_Сообщение ПСМ енаблевизбуттонс</span><span class="sxs-lookup"><span data-stu-id="adf64-105">PSM\_ENABLEWIZBUTTONS message</span></span>

<span data-ttu-id="adf64-106">Включает или отключает любые стандартные кнопки в мастере Aero.</span><span class="sxs-lookup"><span data-stu-id="adf64-106">Enables or disables any of the standard buttons in an Aero wizard.</span></span> <span data-ttu-id="adf64-107">Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ енаблевизбуттонс**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) .</span><span class="sxs-lookup"><span data-stu-id="adf64-107">You can send this message explicitly or use the [**PropSheet\_EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="adf64-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="adf64-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adf64-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="adf64-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="adf64-110">Одно или несколько из следующих значений, указывающих, какие кнопки страницы свойств должны быть включены.</span><span class="sxs-lookup"><span data-stu-id="adf64-110">One or more of the following values that specify which property sheet buttons are to be enabled.</span></span> <span data-ttu-id="adf64-111">Если значение кнопки включено и для этого параметра, и для *lParam*, оно включено.</span><span class="sxs-lookup"><span data-stu-id="adf64-111">If a button value is included in both this parameter and *lParam*, it is enabled.</span></span>



| <span data-ttu-id="adf64-112">Значение</span><span class="sxs-lookup"><span data-stu-id="adf64-112">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="adf64-113">Значение</span><span class="sxs-lookup"><span data-stu-id="adf64-113">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="adf64-114"><dt>**ПСВИЗБ \_ назад**</dt></span><span class="sxs-lookup"><span data-stu-id="adf64-114"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="adf64-115">Кнопка " **назад** ".</span><span class="sxs-lookup"><span data-stu-id="adf64-115">The **Back** button.</span></span><br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="adf64-116"><dt>**ПСВИЗБ \_ Отмена**</dt></span><span class="sxs-lookup"><span data-stu-id="adf64-116"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="adf64-117">Кнопка **Отмена** .</span><span class="sxs-lookup"><span data-stu-id="adf64-117">The **Cancel** button.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="adf64-118"><dt>**ПСВИЗБ \_ дисабледфиниш**</dt></span><span class="sxs-lookup"><span data-stu-id="adf64-118"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="adf64-119">Кнопка **"Готово"** .</span><span class="sxs-lookup"><span data-stu-id="adf64-119">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="adf64-120"><dt>**\_Завершение псвизб**</dt></span><span class="sxs-lookup"><span data-stu-id="adf64-120"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="adf64-121">Кнопка **"Готово"** .</span><span class="sxs-lookup"><span data-stu-id="adf64-121">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="adf64-122"><dt>**ПСВИЗБ \_ Далее**</dt></span><span class="sxs-lookup"><span data-stu-id="adf64-122"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="adf64-123">Кнопка **Далее** .</span><span class="sxs-lookup"><span data-stu-id="adf64-123">The **Next** button.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="adf64-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="adf64-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="adf64-125">Одно или несколько из тех же значений, которые используются в параметре *wParam*, указывая, какие кнопки затрагиваются этим вызовом.</span><span class="sxs-lookup"><span data-stu-id="adf64-125">One or more of the same values used in *wParam*, specifying which buttons are affected by this call.</span></span> <span data-ttu-id="adf64-126">Если значение кнопки отображается в этом параметре, но не в *wParam*, это означает, что кнопка должна быть отключена.</span><span class="sxs-lookup"><span data-stu-id="adf64-126">If a button value appears in this parameter but not in *wParam*, it indicates that the button should be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adf64-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="adf64-127">Return value</span></span>

<span data-ttu-id="adf64-128">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="adf64-128">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="adf64-129">Требования</span><span class="sxs-lookup"><span data-stu-id="adf64-129">Requirements</span></span>



| <span data-ttu-id="adf64-130">Требование</span><span class="sxs-lookup"><span data-stu-id="adf64-130">Requirement</span></span> | <span data-ttu-id="adf64-131">Значение</span><span class="sxs-lookup"><span data-stu-id="adf64-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="adf64-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="adf64-132">Minimum supported client</span></span><br/> | <span data-ttu-id="adf64-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="adf64-133">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="adf64-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="adf64-134">Minimum supported server</span></span><br/> | <span data-ttu-id="adf64-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="adf64-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="adf64-136">Header</span><span class="sxs-lookup"><span data-stu-id="adf64-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="adf64-137"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="adf64-137"><dt>Prsht.h</dt></span></span> </dl> |



 

 





