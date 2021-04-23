---
description: Уведомляет панель приложений, когда произошло событие, которое может повлиять на размер и расположение панель приложений.
ms.assetid: 1016a362-4d2b-410e-aec9-c1cc8f497778
title: Сообщение ABN_POSCHANGED (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b0a800b1c112cba18fbadbba79a999ec83c77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984373"
---
# <a name="abn_poschanged-message"></a><span data-ttu-id="7f2fe-103">\_Сообщение АБН посчанжед</span><span class="sxs-lookup"><span data-stu-id="7f2fe-103">ABN\_POSCHANGED message</span></span>

<span data-ttu-id="7f2fe-104">Уведомляет панель приложений, когда произошло событие, которое может повлиять на размер и расположение панель приложений.</span><span class="sxs-lookup"><span data-stu-id="7f2fe-104">Notifies an appbar when an event has occurred that may affect the appbar's size and position.</span></span> <span data-ttu-id="7f2fe-105">События включают изменения размера, расположения и видимости панели задач, а также добавление, удаление или изменение размера другого панель приложений на той же стороне экрана.</span><span class="sxs-lookup"><span data-stu-id="7f2fe-105">Events include changes in the taskbar's size, position, and visibility state, as well as the addition, removal, or resizing of another appbar on the same side of the screen.</span></span>


```C++
ABN_POSCHANGED
```



## <a name="parameters"></a><span data-ttu-id="7f2fe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f2fe-106">Parameters</span></span>

<span data-ttu-id="7f2fe-107">Это сообщение не содержит параметров.</span><span class="sxs-lookup"><span data-stu-id="7f2fe-107">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7f2fe-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f2fe-108">Return value</span></span>

<span data-ttu-id="7f2fe-109">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="7f2fe-109">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f2fe-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="7f2fe-110">Remarks</span></span>

<span data-ttu-id="7f2fe-111">Панель приложений должен ответить на это сообщение уведомления, отправив сообщения [**АБМ \_ Куерипос**](abm-querypos.md) и [**АБМ \_ сетпос**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="7f2fe-111">An appbar should respond to this notification message by sending the [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages.</span></span> <span data-ttu-id="7f2fe-112">Если его положение изменилось, панель приложений должен вызвать функцию [**мовевиндов**](/windows/desktop/api/winuser/nf-winuser-movewindow) , чтобы переместить себя в новое положение.</span><span class="sxs-lookup"><span data-stu-id="7f2fe-112">If its position has changed, the appbar should call the [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) function to move itself to the new position.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f2fe-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7f2fe-113">Requirements</span></span>



| <span data-ttu-id="7f2fe-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7f2fe-114">Requirement</span></span> | <span data-ttu-id="7f2fe-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7f2fe-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f2fe-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f2fe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7f2fe-117">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7f2fe-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7f2fe-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f2fe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7f2fe-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7f2fe-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7f2fe-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7f2fe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f2fe-121"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f2fe-121"><dt>Shellapi.h</dt></span></span> </dl> |



 

