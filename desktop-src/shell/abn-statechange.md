---
description: Уведомляет панель приложений о том, что состояние автоскрытия или Always on панели задач изменилось&\# 8212; то есть пользователь выбрал или очистил &\# 0034; Always On Top&\# 0034; или &\# 0034; Автоматически скрывать&\# 0034; флажок на странице свойств панели задач.
title: Сообщение ABN_STATECHANGE (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ac2c00a2-ac20-40a5-947e-6b75a2620a0b
api_name:
- ABN_STATECHANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 33879fcb5e9435e2245bc3d00a9fab75bf1cbdc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896902"
---
# <a name="abn_statechange-message"></a><span data-ttu-id="fdc7f-103">\_Сообщение АБН STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="fdc7f-103">ABN\_STATECHANGE message</span></span>

<span data-ttu-id="fdc7f-104">Уведомляет панель приложений о том, что состояние автоскрытия или Always on панели задач было изменено, т. е. пользователь выбрал или снял флажок "Always On Top" или "автоматически скрывать" на странице свойств панели задач.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-104">Notifies an appbar that the taskbar's autohide or always-on-top state has changed that is, the user has selected or cleared the "Always on top" or "Auto hide" check box on the taskbar's property sheet.</span></span>


```C++
ABN_STATECHANGE 
```



## <a name="parameters"></a><span data-ttu-id="fdc7f-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="fdc7f-105">Parameters</span></span>

<span data-ttu-id="fdc7f-106">Это сообщение не содержит параметров.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fdc7f-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fdc7f-107">Return value</span></span>

<span data-ttu-id="fdc7f-108">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="fdc7f-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdc7f-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="fdc7f-109">Remarks</span></span>

<span data-ttu-id="fdc7f-110">Панель приложений может использовать это сообщение уведомления, чтобы установить его состояние в соответствии с соответствующими настройками панели задач (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="fdc7f-110">An appbar can use this notification message to set its state to conform to that of the taskbar, if desired.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdc7f-111">Требования</span><span class="sxs-lookup"><span data-stu-id="fdc7f-111">Requirements</span></span>



| <span data-ttu-id="fdc7f-112">Требование</span><span class="sxs-lookup"><span data-stu-id="fdc7f-112">Requirement</span></span> | <span data-ttu-id="fdc7f-113">Значение</span><span class="sxs-lookup"><span data-stu-id="fdc7f-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc7f-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fdc7f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fdc7f-115">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fdc7f-115">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fdc7f-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fdc7f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fdc7f-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fdc7f-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fdc7f-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fdc7f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdc7f-119"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdc7f-119"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




