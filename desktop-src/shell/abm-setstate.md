---
description: Задает состояния автоскрытия и Always On в верхней части панели задач Windows.
title: Сообщение ABM_SETSTATE (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a60e156d-19ef-49b9-83fc-138d1a2169f2
api_name:
- ABM_SETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cd21ca49d1a57d870c26e010420f978f1d9b88a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984381"
---
# <a name="abm_setstate-message"></a><span data-ttu-id="b09a7-103">\_Сообщение АБМ SETSTATE</span><span class="sxs-lookup"><span data-stu-id="b09a7-103">ABM\_SETSTATE message</span></span>

<span data-ttu-id="b09a7-104">Задает состояния автоскрытия и Always On в верхней части панели задач Windows.</span><span class="sxs-lookup"><span data-stu-id="b09a7-104">Sets the autohide and always-on-top states of the Windows taskbar.</span></span>


```C++
SHAppBarMessage(ABM_SETSTATE, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="b09a7-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="b09a7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b09a7-106">*пабд*</span><span class="sxs-lookup"><span data-stu-id="b09a7-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="b09a7-107">Указатель на структуру [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="b09a7-107">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="b09a7-108">При отправке этого сообщения необходимо указать элементы **кбсизе** и **HWND** .</span><span class="sxs-lookup"><span data-stu-id="b09a7-108">You must specify the **cbSize** and **hWnd** members when sending this message.</span></span> <span data-ttu-id="b09a7-109">Данные для требуемого состояния отправляются в член **lParam** с помощью одного из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b09a7-109">Data for the desired state is sent in the **lParam** member using one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="b09a7-110"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="b09a7-110"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="b09a7-111">Автоскрытие и постоянное выключение в начало</span><span class="sxs-lookup"><span data-stu-id="b09a7-111">Autohide and always-on-top both off</span></span>

</dd> <dt>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>

<span data-ttu-id="b09a7-112"><span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**ABS \_ алвайсонтоп**</span><span class="sxs-lookup"><span data-stu-id="b09a7-112"><span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**ABS\_ALWAYSONTOP**</span></span>


</dt> <dd>

<span data-ttu-id="b09a7-113">Always On-On — Автоскрытие отключено</span><span class="sxs-lookup"><span data-stu-id="b09a7-113">Always-on-top on, autohide off</span></span>

</dd> <dt>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>

<span data-ttu-id="b09a7-114"><span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**Автоскрытие ABS \_**</span><span class="sxs-lookup"><span data-stu-id="b09a7-114"><span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**ABS\_AUTOHIDE**</span></span>


</dt> <dd>

<span data-ttu-id="b09a7-115">Автоматическое скрытие вкл., всегда включено — сверху</span><span class="sxs-lookup"><span data-stu-id="b09a7-115">Autohide on, always-on-top off</span></span>

</dd> <dt>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>

<span data-ttu-id="b09a7-116"><span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**\_АВТОскрытие ABS \| \_ алвайсонтоп**</span><span class="sxs-lookup"><span data-stu-id="b09a7-116"><span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS\_AUTOHIDE \| ABS\_ALWAYSONTOP**</span></span>


</dt> <dd>

<span data-ttu-id="b09a7-117">Автоскрытие и постоянное включение в начало</span><span class="sxs-lookup"><span data-stu-id="b09a7-117">Autohide and always-on-top both on</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b09a7-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b09a7-118">Return value</span></span>

<span data-ttu-id="b09a7-119">Всегда возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="b09a7-119">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b09a7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b09a7-120">Requirements</span></span>



| <span data-ttu-id="b09a7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b09a7-121">Requirement</span></span> | <span data-ttu-id="b09a7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b09a7-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b09a7-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b09a7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b09a7-124">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b09a7-124">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b09a7-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b09a7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b09a7-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b09a7-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b09a7-127">Header</span><span class="sxs-lookup"><span data-stu-id="b09a7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b09a7-128"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="b09a7-128"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




