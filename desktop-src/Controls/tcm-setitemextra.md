---
title: Сообщение TCM_SETITEMEXTRA (Коммктрл. h)
description: Задает число байтов на вкладку, зарезервированную для определяемых приложением данных в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл сетитемекстра.
ms.assetid: 8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4
keywords:
- Элементы управления Windows для TCM_SETITEMEXTRA сообщений
topic_type:
- apiref
api_name:
- TCM_SETITEMEXTRA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6c7fdb47483ae0ddc841ae5f79b8f913e6a4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135090"
---
# <a name="tcm_setitemextra-message"></a><span data-ttu-id="a7c24-105">\_Сообщение СЕТИТЕМЕКСТРА TCM</span><span class="sxs-lookup"><span data-stu-id="a7c24-105">TCM\_SETITEMEXTRA message</span></span>

<span data-ttu-id="a7c24-106">Задает число байтов на вкладку, зарезервированную для определяемых приложением данных в элементе управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="a7c24-106">Sets the number of bytes per tab reserved for application-defined data in a tab control.</span></span> <span data-ttu-id="a7c24-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ сетитемекстра**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) .</span><span class="sxs-lookup"><span data-stu-id="a7c24-107">You can send this message explicitly or by using the [**TabCtrl\_SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a7c24-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7c24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7c24-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a7c24-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7c24-110">Количество дополнительных байтов.</span><span class="sxs-lookup"><span data-stu-id="a7c24-110">Number of extra bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a7c24-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a7c24-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a7c24-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a7c24-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7c24-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7c24-113">Return value</span></span>

<span data-ttu-id="a7c24-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a7c24-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7c24-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7c24-115">Remarks</span></span>

<span data-ttu-id="a7c24-116">По умолчанию количество дополнительных байтов равно четырем.</span><span class="sxs-lookup"><span data-stu-id="a7c24-116">By default, the number of extra bytes is four.</span></span> <span data-ttu-id="a7c24-117">Приложение, которое изменяет число дополнительных байтов, не может использовать структуру [**тЦитем**](/windows/win32/api/commctrl/ns-commctrl-tcitema) для получения и задания определяемых приложением данных для вкладки. Вместо этого необходимо определить новую структуру, состоящую из структуры [**тЦитемхеадер**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) , за которой следуют элементы, определяемые приложением.</span><span class="sxs-lookup"><span data-stu-id="a7c24-117">An application that changes the number of extra bytes cannot use the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure to retrieve and set the application-defined data for a tab. Instead, you must define a new structure that consists of the [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) structure followed by application-defined members.</span></span>

<span data-ttu-id="a7c24-118">Приложение должно изменять только количество дополнительных байтов, если элемент управления "Вкладка" не содержит ни одной вкладки.</span><span class="sxs-lookup"><span data-stu-id="a7c24-118">An application should only change the number of extra bytes when a tab control does not contain any tabs.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7c24-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a7c24-119">Requirements</span></span>



| <span data-ttu-id="a7c24-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a7c24-120">Requirement</span></span> | <span data-ttu-id="a7c24-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a7c24-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7c24-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7c24-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a7c24-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a7c24-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a7c24-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7c24-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a7c24-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a7c24-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a7c24-126">Header</span><span class="sxs-lookup"><span data-stu-id="a7c24-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7c24-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7c24-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





