---
title: Код уведомления TBN_MAPACCELERATOR (Коммктрл. h)
description: Запрашивает индекс кнопки на панели инструментов, соответствующей указанному символу ускорителя. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- TBN_MAPACCELERATOR кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_MAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b20f1908f441c38e23aa7428f8c8edb8a192c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988186"
---
# <a name="tbn_mapaccelerator-notification-code"></a><span data-ttu-id="e3a46-105">\_Код уведомления ТБН мапакцелератор</span><span class="sxs-lookup"><span data-stu-id="e3a46-105">TBN\_MAPACCELERATOR notification code</span></span>

<span data-ttu-id="e3a46-106">Запрашивает индекс кнопки на панели инструментов, соответствующей указанному символу ускорителя.</span><span class="sxs-lookup"><span data-stu-id="e3a46-106">Requests the index of the button in the toolbar corresponding to the specified accelerator character.</span></span> <span data-ttu-id="e3a46-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e3a46-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_MAPACCELERATOR

    lpnmtb = (NMCHAR*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e3a46-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3a46-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3a46-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3a46-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3a46-110">Указатель на структуру [**нмчар**](/windows/win32/api/commctrl/ns-commctrl-nmchar) , содержащую символ клавиши быстрого вызова и принимающий индекс соответствующей кнопки.</span><span class="sxs-lookup"><span data-stu-id="e3a46-110">A pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains the accelerator key character and that receives the index of the corresponding button.</span></span> <span data-ttu-id="e3a46-111">Поле **двитемнекст** имеет значение-1, если ускоритель не соответствует команде.</span><span class="sxs-lookup"><span data-stu-id="e3a46-111">The **dwItemNext** field is -1 if the accelerator does not correspond to a command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3a46-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3a46-112">Return value</span></span>

<span data-ttu-id="e3a46-113">Значение TRUE, если для **нмчар. двитемнекст** задано значение.</span><span class="sxs-lookup"><span data-stu-id="e3a46-113">TRUE if **NMCHAR.dwItemNext** is set to a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a46-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e3a46-114">Requirements</span></span>



| <span data-ttu-id="e3a46-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e3a46-115">Requirement</span></span> | <span data-ttu-id="e3a46-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e3a46-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a46-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3a46-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e3a46-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3a46-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e3a46-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3a46-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e3a46-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e3a46-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e3a46-121">Header</span><span class="sxs-lookup"><span data-stu-id="e3a46-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3a46-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3a46-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





