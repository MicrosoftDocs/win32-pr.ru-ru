---
title: Сообщение PSM_UNCHANGED (Пршт. h)
description: Информирует страницу свойств о том, что данные на странице возвращены к ранее сохраненному состоянию. Это сообщение можно отправить явно или с помощью \_ неизмененного макроса пропшит.
ms.assetid: 61c15dec-40d0-4720-a117-4eed765c8819
keywords:
- Элементы управления Windows для PSM_UNCHANGED сообщений
topic_type:
- apiref
api_name:
- PSM_UNCHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d6216f94afd610bb49710a3e84b4c21a673f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262219"
---
# <a name="psm_unchanged-message"></a><span data-ttu-id="3d5d6-105">ПСМ \_ НЕизмененное сообщение</span><span class="sxs-lookup"><span data-stu-id="3d5d6-105">PSM\_UNCHANGED message</span></span>

<span data-ttu-id="3d5d6-106">Информирует страницу свойств о том, что данные на странице возвращены к ранее сохраненному состоянию.</span><span class="sxs-lookup"><span data-stu-id="3d5d6-106">Informs a property sheet that information in a page has reverted to the previously saved state.</span></span> <span data-ttu-id="3d5d6-107">Это сообщение можно отправить явно или с помощью [**\_ неизмененного**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) макроса пропшит.</span><span class="sxs-lookup"><span data-stu-id="3d5d6-107">You can send this message explicitly or by using the [**PropSheet\_UnChanged**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3d5d6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d5d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d5d6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d5d6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d5d6-110">Обработчик для страницы, которая возвращена в ранее сохраненное состояние.</span><span class="sxs-lookup"><span data-stu-id="3d5d6-110">Handle to the page that has reverted to the previously saved state.</span></span>

</dd> <dt>

<span data-ttu-id="3d5d6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d5d6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d5d6-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3d5d6-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d5d6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d5d6-113">Return value</span></span>

<span data-ttu-id="3d5d6-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="3d5d6-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d5d6-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d5d6-115">Remarks</span></span>

<span data-ttu-id="3d5d6-116">Страница свойств отключает кнопку **Применить** , если на странице свойств не зарегистрированы изменения других страниц.</span><span class="sxs-lookup"><span data-stu-id="3d5d6-116">The property sheet disables the **Apply** button if no other pages have registered changes with the property sheet.</span></span>

> [!Note]  
> <span data-ttu-id="3d5d6-117">Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="3d5d6-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3d5d6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="3d5d6-118">Requirements</span></span>



| <span data-ttu-id="3d5d6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="3d5d6-119">Requirement</span></span> | <span data-ttu-id="3d5d6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3d5d6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5d6-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d5d6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3d5d6-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3d5d6-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3d5d6-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d5d6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3d5d6-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3d5d6-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3d5d6-125">Header</span><span class="sxs-lookup"><span data-stu-id="3d5d6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d5d6-126"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d5d6-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





