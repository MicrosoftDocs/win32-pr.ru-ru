---
title: Сообщение PSM_GETTABCONTROL (Пршт. h)
description: Получает маркер для элемента управления вкладки страницы свойств. Это сообщение можно отправить явно или с помощью \_ макроса пропшит.
ms.assetid: 5ddea541-c8e0-4357-b08e-3b5e64be377f
keywords:
- Элементы управления Windows для PSM_GETTABCONTROL сообщений
topic_type:
- apiref
api_name:
- PSM_GETTABCONTROL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab296159cac4dbfb4ef894d90d31bcd74d6ca2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534913"
---
# <a name="psm_gettabcontrol-message"></a><span data-ttu-id="64add-105">Сообщение ПСМ в \_ TabControl</span><span class="sxs-lookup"><span data-stu-id="64add-105">PSM\_GETTABCONTROL message</span></span>

<span data-ttu-id="64add-106">Получает маркер для элемента управления вкладки страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="64add-106">Retrieves the handle to the tab control of a property sheet.</span></span> <span data-ttu-id="64add-107">Это сообщение можно отправить явно или с помощью макроса [**пропшит \_**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) .</span><span class="sxs-lookup"><span data-stu-id="64add-107">You can send this message explicitly or by using the [**PropSheet\_GetTabControl**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="64add-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="64add-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64add-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64add-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64add-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="64add-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="64add-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64add-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64add-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="64add-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64add-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64add-113">Return value</span></span>

<span data-ttu-id="64add-114">Возвращает маркер для элемента управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="64add-114">Returns the handle to the tab control.</span></span>

## <a name="remarks"></a><span data-ttu-id="64add-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64add-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="64add-116">Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="64add-116">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="64add-117">Требования</span><span class="sxs-lookup"><span data-stu-id="64add-117">Requirements</span></span>



| <span data-ttu-id="64add-118">Требование</span><span class="sxs-lookup"><span data-stu-id="64add-118">Requirement</span></span> | <span data-ttu-id="64add-119">Значение</span><span class="sxs-lookup"><span data-stu-id="64add-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="64add-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64add-120">Minimum supported client</span></span><br/> | <span data-ttu-id="64add-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="64add-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="64add-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="64add-122">Minimum supported server</span></span><br/> | <span data-ttu-id="64add-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="64add-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="64add-124">Header</span><span class="sxs-lookup"><span data-stu-id="64add-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="64add-125"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="64add-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 





