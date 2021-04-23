---
description: Отменяет регистрацию панель приложений, удаляя ее из внутреннего списка системы. Система больше не отправляет сообщения уведомления панель приложений или не позволяет другим приложениям использовать область экрана, используемую панель приложений.
title: Сообщение ABM_REMOVE (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3da73a52-3dbb-4133-a9bd-86540e1c4154
api_name:
- ABM_REMOVE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7f4530869b9f68772c28fefd6130ff8e4b6ffbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896906"
---
# <a name="abm_remove-message"></a><span data-ttu-id="43a05-104">АБМ \_ Удалить сообщение</span><span class="sxs-lookup"><span data-stu-id="43a05-104">ABM\_REMOVE message</span></span>

<span data-ttu-id="43a05-105">Отменяет регистрацию панель приложений, удаляя ее из внутреннего списка системы.</span><span class="sxs-lookup"><span data-stu-id="43a05-105">Unregisters an appbar by removing it from the system's internal list.</span></span> <span data-ttu-id="43a05-106">Система больше не отправляет сообщения уведомления панель приложений или не позволяет другим приложениям использовать область экрана, используемую панель приложений.</span><span class="sxs-lookup"><span data-stu-id="43a05-106">The system no longer sends notification messages to the appbar or prevents other applications from using the screen area used by the appbar.</span></span>


```C++
                SHAppBarMessage(ABM_REMOVE, pabd); 
            
```



## <a name="parameters"></a><span data-ttu-id="43a05-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="43a05-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a05-108">*пабд*</span><span class="sxs-lookup"><span data-stu-id="43a05-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="43a05-109">Указатель на структуру [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) , содержащую маркер для панель приложений, для которого отменяется регистрация.</span><span class="sxs-lookup"><span data-stu-id="43a05-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that contains the handle to the appbar to unregister.</span></span> <span data-ttu-id="43a05-110">При отправке этого сообщения необходимо указать элементы **кбсизе** и **HWND** . все остальные элементы игнорируются.</span><span class="sxs-lookup"><span data-stu-id="43a05-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43a05-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43a05-111">Return value</span></span>

<span data-ttu-id="43a05-112">Всегда возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="43a05-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="43a05-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="43a05-113">Remarks</span></span>

<span data-ttu-id="43a05-114">Это сообщение приводит к тому, что система отправляет сообщение уведомления [**АБН \_ посчанжед**](abn-poschanged.md) всем AppBar.</span><span class="sxs-lookup"><span data-stu-id="43a05-114">This message causes the system to send the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message to all appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a05-115">Требования</span><span class="sxs-lookup"><span data-stu-id="43a05-115">Requirements</span></span>



| <span data-ttu-id="43a05-116">Требование</span><span class="sxs-lookup"><span data-stu-id="43a05-116">Requirement</span></span> | <span data-ttu-id="43a05-117">Значение</span><span class="sxs-lookup"><span data-stu-id="43a05-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43a05-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43a05-118">Minimum supported client</span></span><br/> | <span data-ttu-id="43a05-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="43a05-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="43a05-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43a05-120">Minimum supported server</span></span><br/> | <span data-ttu-id="43a05-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="43a05-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43a05-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="43a05-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="43a05-123"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="43a05-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




