---
title: Код уведомления HDN_ITEMCHANGING (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка, что атрибуты элемента заголовка будут изменены. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: c3361f88-69d4-425f-b548-0ad3b2a00af4
keywords:
- HDN_ITEMCHANGING кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGING
- HDN_ITEMCHANGINGA
- HDN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c803f9bde466b524b2ca1cb89062f5fc89d6865f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891501"
---
# <a name="hdn_itemchanging-notification-code"></a><span data-ttu-id="77014-105">\_Код уведомления ХДН итемчангинг</span><span class="sxs-lookup"><span data-stu-id="77014-105">HDN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="77014-106">Сообщает родительскому окну элемента управления заголовка, что атрибуты элемента заголовка будут изменены.</span><span class="sxs-lookup"><span data-stu-id="77014-106">Notifies a header control's parent window that the attributes of a header item are about to change.</span></span> <span data-ttu-id="77014-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="77014-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCHANGING

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="77014-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="77014-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77014-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77014-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77014-110">Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую сведения о элементе управления заголовка и элементе заголовка, включая атрибуты, которые необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="77014-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the header item, including the attributes that are about to change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77014-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77014-111">Return value</span></span>

<span data-ttu-id="77014-112">Возвращает **значение false** , чтобы разрешить изменения, или **true** , чтобы предотвратить их.</span><span class="sxs-lookup"><span data-stu-id="77014-112">Returns **FALSE** to allow the changes, or **TRUE** to prevent them.</span></span>

## <a name="requirements"></a><span data-ttu-id="77014-113">Требования</span><span class="sxs-lookup"><span data-stu-id="77014-113">Requirements</span></span>



| <span data-ttu-id="77014-114">Требование</span><span class="sxs-lookup"><span data-stu-id="77014-114">Requirement</span></span> | <span data-ttu-id="77014-115">Значение</span><span class="sxs-lookup"><span data-stu-id="77014-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77014-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77014-116">Minimum supported client</span></span><br/> | <span data-ttu-id="77014-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77014-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77014-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77014-118">Minimum supported server</span></span><br/> | <span data-ttu-id="77014-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77014-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77014-120">Header</span><span class="sxs-lookup"><span data-stu-id="77014-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="77014-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="77014-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="77014-122">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="77014-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="77014-123">**ХДН \_ ИТЕМЧАНГИНГВ** (Юникод) и **ХДН \_ итемчангинга** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="77014-123">**HDN\_ITEMCHANGINGW** (Unicode) and **HDN\_ITEMCHANGINGA** (ANSI)</span></span><br/>         |



 

 





