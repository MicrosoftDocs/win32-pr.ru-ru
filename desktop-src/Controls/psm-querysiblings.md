---
title: Сообщение PSM_QUERYSIBLINGS (Пршт. h)
description: Отправляется на страницу свойств, которая затем пересылает сообщение каждой из страниц. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит куерисиблингс.
ms.assetid: 96f48847-b7b8-4d6f-8bde-ada915b7c962
keywords:
- Элементы управления Windows для PSM_QUERYSIBLINGS сообщений
topic_type:
- apiref
api_name:
- PSM_QUERYSIBLINGS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5943fefa906475e34d1cc7acc7f8a86cd99252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534352"
---
# <a name="psm_querysiblings-message"></a><span data-ttu-id="13b73-105">\_Сообщение ПСМ куерисиблингс</span><span class="sxs-lookup"><span data-stu-id="13b73-105">PSM\_QUERYSIBLINGS message</span></span>

<span data-ttu-id="13b73-106">Отправляется на страницу свойств, которая затем пересылает сообщение каждой из страниц.</span><span class="sxs-lookup"><span data-stu-id="13b73-106">Sent to a property sheet, which then forwards the message to each of its pages.</span></span> <span data-ttu-id="13b73-107">Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ куерисиблингс**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) .</span><span class="sxs-lookup"><span data-stu-id="13b73-107">You can send this message explicitly or by using the [**PropSheet\_QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="13b73-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="13b73-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13b73-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="13b73-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13b73-110">Первый определяемый приложением параметр.</span><span class="sxs-lookup"><span data-stu-id="13b73-110">First application-defined parameter.</span></span>

</dd> <dt>

<span data-ttu-id="13b73-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13b73-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13b73-112">Второй параметр, определяемый приложением.</span><span class="sxs-lookup"><span data-stu-id="13b73-112">Second application-defined parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13b73-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13b73-113">Return value</span></span>

<span data-ttu-id="13b73-114">Возвращает ненулевое значение со страницы на странице свойств или нуль, если ни одна страница не возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="13b73-114">Returns the nonzero value from a page in the property sheet, or zero if no page returns a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13b73-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13b73-115">Remarks</span></span>

<span data-ttu-id="13b73-116">Если страница возвращает ненулевое значение, вкладка свойств не отправляет сообщение на последующие страницы.</span><span class="sxs-lookup"><span data-stu-id="13b73-116">If a page returns a nonzero value, the property sheet does not send the message to subsequent pages.</span></span>

## <a name="requirements"></a><span data-ttu-id="13b73-117">Требования</span><span class="sxs-lookup"><span data-stu-id="13b73-117">Requirements</span></span>



| <span data-ttu-id="13b73-118">Требование</span><span class="sxs-lookup"><span data-stu-id="13b73-118">Requirement</span></span> | <span data-ttu-id="13b73-119">Значение</span><span class="sxs-lookup"><span data-stu-id="13b73-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="13b73-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13b73-120">Minimum supported client</span></span><br/> | <span data-ttu-id="13b73-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="13b73-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="13b73-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13b73-122">Minimum supported server</span></span><br/> | <span data-ttu-id="13b73-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="13b73-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="13b73-124">Header</span><span class="sxs-lookup"><span data-stu-id="13b73-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="13b73-125"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="13b73-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 





