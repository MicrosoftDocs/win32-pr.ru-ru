---
title: Сообщение TCM_SETCURSEL (Коммктрл. h)
description: Выбирает вкладку в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл сеткурсел.
ms.assetid: cf709d8c-c522-47c8-8ff3-463dc8e924b5
keywords:
- Элементы управления Windows для TCM_SETCURSEL сообщений
topic_type:
- apiref
api_name:
- TCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90033c5a19b0eb7b73f9ed886e8dad8d1ca4c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988683"
---
# <a name="tcm_setcursel-message"></a><span data-ttu-id="af380-105">\_Сообщение СЕТКУРСЕЛ TCM</span><span class="sxs-lookup"><span data-stu-id="af380-105">TCM\_SETCURSEL message</span></span>

<span data-ttu-id="af380-106">Выбирает вкладку в элементе управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="af380-106">Selects a tab in a tab control.</span></span> <span data-ttu-id="af380-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ сеткурсел**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) .</span><span class="sxs-lookup"><span data-stu-id="af380-107">You can send this message explicitly or by using the [**TabCtrl\_SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="af380-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="af380-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af380-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af380-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af380-110">Индекс выбираемой вкладки.</span><span class="sxs-lookup"><span data-stu-id="af380-110">Index of the tab to select.</span></span>

</dd> <dt>

<span data-ttu-id="af380-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af380-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="af380-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="af380-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af380-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af380-113">Return value</span></span>

<span data-ttu-id="af380-114">Возвращает индекс ранее выбранной вкладки в случае успеха, или-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="af380-114">Returns the index of the previously selected tab if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="af380-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af380-115">Remarks</span></span>

<span data-ttu-id="af380-116">Элемент управления "Вкладка" не отправляет код уведомления [ТКН \_ Селчангинг](tcn-selchanging.md) или [ТКН \_ селчанже](tcn-selchange.md) , когда вкладка выбрана с помощью этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="af380-116">A tab control does not send a [TCN\_SELCHANGING](tcn-selchanging.md) or [TCN\_SELCHANGE](tcn-selchange.md) notification code when a tab is selected using this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="af380-117">Требования</span><span class="sxs-lookup"><span data-stu-id="af380-117">Requirements</span></span>



| <span data-ttu-id="af380-118">Требование</span><span class="sxs-lookup"><span data-stu-id="af380-118">Requirement</span></span> | <span data-ttu-id="af380-119">Значение</span><span class="sxs-lookup"><span data-stu-id="af380-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af380-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af380-120">Minimum supported client</span></span><br/> | <span data-ttu-id="af380-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af380-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af380-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af380-122">Minimum supported server</span></span><br/> | <span data-ttu-id="af380-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af380-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af380-124">Header</span><span class="sxs-lookup"><span data-stu-id="af380-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="af380-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="af380-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





