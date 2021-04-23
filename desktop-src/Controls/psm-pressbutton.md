---
title: Сообщение PSM_PRESSBUTTON (Пршт. h)
description: Имитирует выбор кнопки страницы свойств. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит прессбуттон.
ms.assetid: 82a55a29-d916-47ee-b0a0-f685a3a386d9
keywords:
- Элементы управления Windows для PSM_PRESSBUTTON сообщений
topic_type:
- apiref
api_name:
- PSM_PRESSBUTTON
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b54b04dcc7b1263019f49ff8c1de0d2c21a12a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493302"
---
# <a name="psm_pressbutton-message"></a><span data-ttu-id="b3f4f-105">\_Сообщение ПСМ прессбуттон</span><span class="sxs-lookup"><span data-stu-id="b3f4f-105">PSM\_PRESSBUTTON message</span></span>

<span data-ttu-id="b3f4f-106">Имитирует выбор кнопки страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="b3f4f-106">Simulates the selection of a property sheet button.</span></span> <span data-ttu-id="b3f4f-107">Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ прессбуттон**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) .</span><span class="sxs-lookup"><span data-stu-id="b3f4f-107">You can send this message explicitly or by using the [**PropSheet\_PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b3f4f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3f4f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3f4f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b3f4f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3f4f-110">Индекс кнопки для выбора.</span><span class="sxs-lookup"><span data-stu-id="b3f4f-110">Index of the button to select.</span></span> <span data-ttu-id="b3f4f-111">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="b3f4f-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="b3f4f-112">Значение</span><span class="sxs-lookup"><span data-stu-id="b3f4f-112">Value</span></span>                                                                                                                                                            | <span data-ttu-id="b3f4f-113">Значение</span><span class="sxs-lookup"><span data-stu-id="b3f4f-113">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PSBTN_APPLYNOW"></span><span id="psbtn_applynow"></span><dl> <span data-ttu-id="b3f4f-114"><dt>**ПСБТН \_ апплинов**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f4f-114"><dt>**PSBTN\_APPLYNOW**</dt></span></span> </dl> | <span data-ttu-id="b3f4f-115">Нажмите кнопку **Применить** .</span><span class="sxs-lookup"><span data-stu-id="b3f4f-115">Selects the **Apply** button.</span></span> <span data-ttu-id="b3f4f-116">Это значение недопустимо при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="b3f4f-116">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/> |
| <span id="PSBTN_BACK"></span><span id="psbtn_back"></span><dl> <span data-ttu-id="b3f4f-117"><dt>**ПСБТН \_ назад**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f4f-117"><dt>**PSBTN\_BACK**</dt></span></span> </dl>             | <span data-ttu-id="b3f4f-118">Нажмите кнопку **назад** .</span><span class="sxs-lookup"><span data-stu-id="b3f4f-118">Selects the **Back** button.</span></span><br/>                                                                                                         |
| <span id="PSBTN_CANCEL"></span><span id="psbtn_cancel"></span><dl> <span data-ttu-id="b3f4f-119"><dt>**ПСБТН \_ Отмена**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f4f-119"><dt>**PSBTN\_CANCEL**</dt></span></span> </dl>       | <span data-ttu-id="b3f4f-120">Нажмите кнопку **Отмена** .</span><span class="sxs-lookup"><span data-stu-id="b3f4f-120">Selects the **Cancel** button.</span></span><br/>                                                                                                       |
| <span id="PSBTN_FINISH"></span><span id="psbtn_finish"></span><dl> <span data-ttu-id="b3f4f-121"><dt>**\_Завершение псбтн**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f4f-121"><dt>**PSBTN\_FINISH**</dt></span></span> </dl>       | <span data-ttu-id="b3f4f-122">Выбирает кнопку **Готово** .</span><span class="sxs-lookup"><span data-stu-id="b3f4f-122">Selects the **Finish** button.</span></span><br/>                                                                                                       |
| <span id="PSBTN_HELP"></span><span id="psbtn_help"></span><dl> <span data-ttu-id="b3f4f-123"><dt>**\_Справка псбтн**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f4f-123"><dt>**PSBTN\_HELP**</dt></span></span> </dl>             | <span data-ttu-id="b3f4f-124">Выбор кнопки " **Справка** ".</span><span class="sxs-lookup"><span data-stu-id="b3f4f-124">Selects the **Help** button.</span></span> <span data-ttu-id="b3f4f-125">Это значение недопустимо при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="b3f4f-125">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/>  |
| <span id="PSBTN_NEXT"></span><span id="psbtn_next"></span><dl> <span data-ttu-id="b3f4f-126"><dt>**ПСБТН \_ Далее**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f4f-126"><dt>**PSBTN\_NEXT**</dt></span></span> </dl>             | <span data-ttu-id="b3f4f-127">Нажмите кнопку **Далее** .</span><span class="sxs-lookup"><span data-stu-id="b3f4f-127">Selects the **Next** button.</span></span><br/>                                                                                                         |
| <span id="PSBTN_OK"></span><span id="psbtn_ok"></span><dl> <span data-ttu-id="b3f4f-128"><dt>**ПСБТН \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f4f-128"><dt>**PSBTN\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="b3f4f-129">Нажмите кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="b3f4f-129">Selects the **OK** button.</span></span> <span data-ttu-id="b3f4f-130">Это значение недопустимо при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="b3f4f-130">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="b3f4f-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b3f4f-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3f4f-132">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b3f4f-132">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3f4f-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3f4f-133">Return value</span></span>

<span data-ttu-id="b3f4f-134">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="b3f4f-134">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3f4f-135">Требования</span><span class="sxs-lookup"><span data-stu-id="b3f4f-135">Requirements</span></span>



| <span data-ttu-id="b3f4f-136">Требование</span><span class="sxs-lookup"><span data-stu-id="b3f4f-136">Requirement</span></span> | <span data-ttu-id="b3f4f-137">Значение</span><span class="sxs-lookup"><span data-stu-id="b3f4f-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3f4f-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b3f4f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b3f4f-139">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3f4f-139">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b3f4f-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b3f4f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b3f4f-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b3f4f-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b3f4f-142">Header</span><span class="sxs-lookup"><span data-stu-id="b3f4f-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3f4f-143"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3f4f-143"><dt>Prsht.h</dt></span></span> </dl> |



 

 





