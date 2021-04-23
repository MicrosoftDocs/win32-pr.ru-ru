---
title: Сообщение PSM_CHANGED (Пршт. h)
description: Информирует страницу свойств о том, что информация на странице изменилась. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит Changed.
ms.assetid: b092969f-31dc-4e3c-9100-d15f1bdd5aa5
keywords:
- Элементы управления Windows для PSM_CHANGED сообщений
topic_type:
- apiref
api_name:
- PSM_CHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f931db5e25f816f7ea164ca5871a4e3e7757a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654632"
---
# <a name="psm_changed-message"></a><span data-ttu-id="510cc-105">ПСМ \_ измененное сообщение</span><span class="sxs-lookup"><span data-stu-id="510cc-105">PSM\_CHANGED message</span></span>

<span data-ttu-id="510cc-106">Информирует страницу свойств о том, что информация на странице изменилась.</span><span class="sxs-lookup"><span data-stu-id="510cc-106">Informs a property sheet that information in a page has changed.</span></span> <span data-ttu-id="510cc-107">Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ Changed**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) .</span><span class="sxs-lookup"><span data-stu-id="510cc-107">You can send this message explicitly or by using the [**PropSheet\_Changed**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="510cc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="510cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="510cc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="510cc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="510cc-110">Измененный обработчик на странице.</span><span class="sxs-lookup"><span data-stu-id="510cc-110">Handle to the page that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="510cc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="510cc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="510cc-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="510cc-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="510cc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="510cc-113">Return value</span></span>

<span data-ttu-id="510cc-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="510cc-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="510cc-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="510cc-115">Remarks</span></span>

<span data-ttu-id="510cc-116">На странице свойств будет активирована кнопка **Применить** .</span><span class="sxs-lookup"><span data-stu-id="510cc-116">The property sheet will enable the **Apply** button.</span></span>

> [!Note]  
> <span data-ttu-id="510cc-117">Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="510cc-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="510cc-118">Требования</span><span class="sxs-lookup"><span data-stu-id="510cc-118">Requirements</span></span>



| <span data-ttu-id="510cc-119">Требование</span><span class="sxs-lookup"><span data-stu-id="510cc-119">Requirement</span></span> | <span data-ttu-id="510cc-120">Значение</span><span class="sxs-lookup"><span data-stu-id="510cc-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="510cc-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="510cc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="510cc-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="510cc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="510cc-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="510cc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="510cc-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="510cc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="510cc-125">Header</span><span class="sxs-lookup"><span data-stu-id="510cc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="510cc-126"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="510cc-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





