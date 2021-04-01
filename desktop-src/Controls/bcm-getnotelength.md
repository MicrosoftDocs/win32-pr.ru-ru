---
title: Сообщение BCM_GETNOTELENGTH (Коммктрл. h)
description: Возвращает длину текста примечания, который может отображаться в описании кнопки ссылки на команду. Отправляйте это сообщение явным образом или с помощью \_ макроса кнопки жетнотеленгс.
ms.assetid: 62385485-b553-47e9-9f15-696cc4694752
keywords:
- Элементы управления Windows для BCM_GETNOTELENGTH сообщений
topic_type:
- apiref
api_name:
- BCM_GETNOTELENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b33c5245778481033bd97326c3d66a40bf03210
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071527"
---
# <a name="bcm_getnotelength-message"></a><span data-ttu-id="82ced-105">\_Сообщение ЖЕТНОТЕЛЕНГС BCM</span><span class="sxs-lookup"><span data-stu-id="82ced-105">BCM\_GETNOTELENGTH message</span></span>

<span data-ttu-id="82ced-106">Возвращает длину текста примечания, который может отображаться в описании кнопки ссылки на команду.</span><span class="sxs-lookup"><span data-stu-id="82ced-106">Gets the length of the note text that may be displayed in the description for a command link button.</span></span> <span data-ttu-id="82ced-107">Отправляйте это сообщение явным образом или с помощью макроса [**кнопки \_ жетнотеленгс**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) .</span><span class="sxs-lookup"><span data-stu-id="82ced-107">Send this message explicitly or by using the [**Button\_GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="82ced-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="82ced-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82ced-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="82ced-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82ced-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="82ced-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="82ced-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82ced-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82ced-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="82ced-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82ced-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82ced-113">Return value</span></span>

<span data-ttu-id="82ced-114">Возвращает длину текста примечания в **вчарс**, не включая завершающий **нуль**-символ, или нуль, если текст примечания отсутствует.</span><span class="sxs-lookup"><span data-stu-id="82ced-114">Returns the length of the note text in **WCHARs**, not including any terminating **NULL**, or zero if there is no note text.</span></span>

## <a name="remarks"></a><span data-ttu-id="82ced-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82ced-115">Remarks</span></span>

<span data-ttu-id="82ced-116">Начиная с Comctl32 DLL версии 6,01, кнопки ссылки на команды могут иметь Примечание.</span><span class="sxs-lookup"><span data-stu-id="82ced-116">Beginning with comctl32 DLL version 6.01, command link buttons may have a note.</span></span> <span data-ttu-id="82ced-117">Сведения о версиях DLL см. в разделе [общие версии элементов управления](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="82ced-117">For information on DLL versions, see [Common Control Versions](common-control-versions.md).</span></span>

<span data-ttu-id="82ced-118">Сообщение **BCM \_ жетнотеленгс** работает только с стилями кнопки [**BS \_ коммандлинк**](button-styles.md) и [**BS \_ дефкоммандлинк**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="82ced-118">The **BCM\_GETNOTELENGTH** message works only with the [**BS\_COMMANDLINK**](button-styles.md) and [**BS\_DEFCOMMANDLINK**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="82ced-119">Требования</span><span class="sxs-lookup"><span data-stu-id="82ced-119">Requirements</span></span>



| <span data-ttu-id="82ced-120">Требование</span><span class="sxs-lookup"><span data-stu-id="82ced-120">Requirement</span></span> | <span data-ttu-id="82ced-121">Значение</span><span class="sxs-lookup"><span data-stu-id="82ced-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82ced-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82ced-122">Minimum supported client</span></span><br/> | <span data-ttu-id="82ced-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="82ced-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="82ced-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82ced-124">Minimum supported server</span></span><br/> | <span data-ttu-id="82ced-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="82ced-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82ced-126">Header</span><span class="sxs-lookup"><span data-stu-id="82ced-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="82ced-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="82ced-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82ced-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82ced-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="82ced-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="82ced-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="82ced-130">Стили кнопок</span><span class="sxs-lookup"><span data-stu-id="82ced-130">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="82ced-131">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="82ced-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="82ced-132">Типы кнопок</span><span class="sxs-lookup"><span data-stu-id="82ced-132">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





