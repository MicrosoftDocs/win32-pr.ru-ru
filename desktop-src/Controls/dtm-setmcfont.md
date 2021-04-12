---
title: Сообщение DTM_SETMCFONT (Коммктрл. h)
description: Задает шрифт, используемый элементом управления "Календарь" элемента управления "Выбор даты и времени" (DTP). Это сообщение можно отправить явным образом или использовать \_ макрос Сетмонскалфонт DateTime.
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- Элементы управления Windows для DTM_SETMCFONT сообщений
topic_type:
- apiref
api_name:
- DTM_SETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b148ffb95acd82257265bf0bab53000b10803793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491823"
---
# <a name="dtm_setmcfont-message"></a><span data-ttu-id="48538-105">\_Сообщение DTM сетмкфонт</span><span class="sxs-lookup"><span data-stu-id="48538-105">DTM\_SETMCFONT message</span></span>

<span data-ttu-id="48538-106">Задает шрифт, используемый элементом управления "Календарь" элемента управления "Выбор даты и времени" (DTP).</span><span class="sxs-lookup"><span data-stu-id="48538-106">Sets the font to be used by the date and time picker (DTP) control's child month calendar control.</span></span> <span data-ttu-id="48538-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ сетмонскалфонт DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) .</span><span class="sxs-lookup"><span data-stu-id="48538-107">You can send this message explicitly or use the [**DateTime\_SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="48538-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="48538-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48538-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="48538-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48538-110">Описатель для шрифта, который будет задан.</span><span class="sxs-lookup"><span data-stu-id="48538-110">A handle to the font that will be set.</span></span>

</dd> <dt>

<span data-ttu-id="48538-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48538-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48538-112">Указывает, должен ли элемент управления перерисоваться сразу после установки шрифта.</span><span class="sxs-lookup"><span data-stu-id="48538-112">Specifies whether the control should be redrawn immediately upon setting the font.</span></span> <span data-ttu-id="48538-113">Если задать для этого параметра **значение true** , элемент управления будет перерисовываться самим собой.</span><span class="sxs-lookup"><span data-stu-id="48538-113">Setting this parameter to **TRUE** causes the control to redraw itself.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48538-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48538-114">Return value</span></span>

<span data-ttu-id="48538-115">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="48538-115">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="48538-116">Требования</span><span class="sxs-lookup"><span data-stu-id="48538-116">Requirements</span></span>



| <span data-ttu-id="48538-117">Требование</span><span class="sxs-lookup"><span data-stu-id="48538-117">Requirement</span></span> | <span data-ttu-id="48538-118">Значение</span><span class="sxs-lookup"><span data-stu-id="48538-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48538-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48538-119">Minimum supported client</span></span><br/> | <span data-ttu-id="48538-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48538-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48538-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48538-121">Minimum supported server</span></span><br/> | <span data-ttu-id="48538-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="48538-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="48538-123">Header</span><span class="sxs-lookup"><span data-stu-id="48538-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="48538-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="48538-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





