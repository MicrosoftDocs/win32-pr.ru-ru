---
description: Получает состояния автоскрытия и постоянного верхнего уровня для панели задач Windows.
title: Сообщение ABM_GETSTATE (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 18e16752-16be-492b-a4fa-c951e18dc86c
api_name:
- ABM_GETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 71225cd8d93de09a07cb0049066e52be08c18a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342872"
---
# <a name="abm_getstate-message"></a><span data-ttu-id="424b1-103">Сообщение АБМ о \_ состоянии</span><span class="sxs-lookup"><span data-stu-id="424b1-103">ABM\_GETSTATE message</span></span>

<span data-ttu-id="424b1-104">Получает состояния автоскрытия и постоянного верхнего уровня для панели задач Windows.</span><span class="sxs-lookup"><span data-stu-id="424b1-104">Retrieves the autohide and always-on-top states of the Windows taskbar.</span></span>


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a><span data-ttu-id="424b1-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="424b1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="424b1-106">*пабд*</span><span class="sxs-lookup"><span data-stu-id="424b1-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="424b1-107">Указатель на структуру [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="424b1-107">Pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="424b1-108">При отправке этого сообщения необходимо указать элемент **кбсизе** . все остальные элементы игнорируются.</span><span class="sxs-lookup"><span data-stu-id="424b1-108">You must specify the **cbSize** member when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="424b1-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="424b1-109">Return value</span></span>

<span data-ttu-id="424b1-110">Возвращает нуль, если панель задач не находится ни в режиме автоскрытия, ни в состоянии Always On (верхнее).</span><span class="sxs-lookup"><span data-stu-id="424b1-110">Returns zero if the taskbar is neither in the autohide nor always-on-top state.</span></span> <span data-ttu-id="424b1-111">В противном случае возвращаемое значение будет одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="424b1-111">Otherwise, the return value is one or both of the following:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="424b1-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="424b1-112">Return code</span></span></th>
<th><span data-ttu-id="424b1-113">Описание</span><span class="sxs-lookup"><span data-stu-id="424b1-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="424b1-114"><dt><strong>ABS_ALWAYSONTOP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="424b1-114"><dt><strong>ABS_ALWAYSONTOP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="424b1-115">Панель задач находится в состоянии Always On (верхнее).</span><span class="sxs-lookup"><span data-stu-id="424b1-115">The taskbar is in the always-on-top state.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="424b1-116">Начиная с Windows 7 ABS_ALWAYSONTOP больше не возвращается, так как панель задач всегда находится в этом состоянии.</span><span class="sxs-lookup"><span data-stu-id="424b1-116">As of Windows 7, ABS_ALWAYSONTOP is no longer returned because the taskbar is always in that state.</span></span> <span data-ttu-id="424b1-117">Старый код следует обновлять, чтобы не учитывать отсутствие этого значения, если это значение не предполагает, что возвращаемое значение означает, что панель задач не находится в состоянии Always On (верхнее).</span><span class="sxs-lookup"><span data-stu-id="424b1-117">Older code should be updated to ignore the absence of this value in not assume that return value to mean that the taskbar is not in the always-on-top state.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="424b1-118"><dt><strong>ABS_AUTOHIDE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="424b1-118"><dt><strong>ABS_AUTOHIDE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="424b1-119">Панель задач находится в состоянии автоскрытия.</span><span class="sxs-lookup"><span data-stu-id="424b1-119">The taskbar is in the autohide state.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="424b1-120">Требования</span><span class="sxs-lookup"><span data-stu-id="424b1-120">Requirements</span></span>



| <span data-ttu-id="424b1-121">Требование</span><span class="sxs-lookup"><span data-stu-id="424b1-121">Requirement</span></span> | <span data-ttu-id="424b1-122">Значение</span><span class="sxs-lookup"><span data-stu-id="424b1-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="424b1-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="424b1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="424b1-124">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="424b1-124">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="424b1-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="424b1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="424b1-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="424b1-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="424b1-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="424b1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="424b1-128"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="424b1-128"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




