---
title: Сообщение DTM_GETMCFONT (Коммктрл. h)
description: Возвращает шрифт, который в настоящее время используется элементом управления "Календарь" элемента управления "Выбор даты и времени" (DTP). Это сообщение можно отправить явным образом или использовать \_ макрос Жетмонскалфонт DateTime.
ms.assetid: 6687a1dc-6f6d-4684-80b2-f726b08d2f3a
keywords:
- Элементы управления Windows для DTM_GETMCFONT сообщений
topic_type:
- apiref
api_name:
- DTM_GETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d799d5dbbe5e3a4cdf7eede871f9aeac451d17a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892493"
---
# <a name="dtm_getmcfont-message"></a><span data-ttu-id="b8219-105">\_Сообщение DTM жетмкфонт</span><span class="sxs-lookup"><span data-stu-id="b8219-105">DTM\_GETMCFONT message</span></span>

<span data-ttu-id="b8219-106">Возвращает шрифт, который в настоящее время используется элементом управления "Календарь" элемента управления "Выбор даты и времени" (DTP).</span><span class="sxs-lookup"><span data-stu-id="b8219-106">Gets the font that the date and time picker (DTP) control's child month calendar control is currently using.</span></span> <span data-ttu-id="b8219-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ жетмонскалфонт DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) .</span><span class="sxs-lookup"><span data-stu-id="b8219-107">You can send this message explicitly or use the [**DateTime\_GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8219-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8219-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8219-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8219-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b8219-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b8219-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b8219-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8219-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b8219-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b8219-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8219-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8219-113">Return value</span></span>

<span data-ttu-id="b8219-114">Возвращает значение ХФОНТ, которое является маркером текущего шрифта.</span><span class="sxs-lookup"><span data-stu-id="b8219-114">Returns an HFONT value that is the handle to the current font.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8219-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b8219-115">Requirements</span></span>



| <span data-ttu-id="b8219-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b8219-116">Requirement</span></span> | <span data-ttu-id="b8219-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b8219-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8219-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8219-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b8219-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8219-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8219-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8219-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b8219-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b8219-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8219-122">Header</span><span class="sxs-lookup"><span data-stu-id="b8219-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8219-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8219-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





