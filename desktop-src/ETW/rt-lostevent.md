---
description: Этот класс типа событий используется для указания того, что события были потеряны в сеансе в режиме реального времени. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 19c747c0-2d9f-49c5-81e4-06a870371bac
title: Класс RT_LostEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RT_LostEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: b689dd95aa1e078572d33de64f245e4844698d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541871"
---
# <a name="rt_lostevent-class"></a><span data-ttu-id="1c399-104">\_Класс ЛОСТЕВЕНТ RT</span><span class="sxs-lookup"><span data-stu-id="1c399-104">RT\_LostEvent class</span></span>

<span data-ttu-id="1c399-105">Этот класс типа событий используется для указания того, что события были потеряны в сеансе в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="1c399-105">This event type class is used to indicate that events were lost in a real-time session.</span></span>

<span data-ttu-id="1c399-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="1c399-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c399-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c399-107">Syntax</span></span>

``` syntax
[EventType{32, 33, 34}, EventTypeName{"RTLostEvent", "RTLostBuffer", "RTLostFile"}]
class RT_LostEvent : Lost_Event
{
};
```

## <a name="members"></a><span data-ttu-id="1c399-108">Участники</span><span class="sxs-lookup"><span data-stu-id="1c399-108">Members</span></span>

<span data-ttu-id="1c399-109">Класс **RT \_ лостевент** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="1c399-109">The **RT\_LostEvent** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c399-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="1c399-110">Remarks</span></span>

<span data-ttu-id="1c399-111">Тип события Ртлостевент указывает на потерю одного или нескольких событий.</span><span class="sxs-lookup"><span data-stu-id="1c399-111">The RTLostEvent event type indicates that one or more events were lost.</span></span> <span data-ttu-id="1c399-112">Тип события Ртлостбуффер указывает, что один или несколько буферов были потеряны.</span><span class="sxs-lookup"><span data-stu-id="1c399-112">The RTLostBuffer event type indicates that one or more buffers were lost.</span></span> <span data-ttu-id="1c399-113">Типы событий Ртлостевент и Ртлостбуффер доставляются перед обработкой событий из буфера.</span><span class="sxs-lookup"><span data-stu-id="1c399-113">The RTLostEvent and RTLostBuffer event types are delivered before processing events from the buffer.</span></span>

<span data-ttu-id="1c399-114">Ртлостфиле указывает, что резервный файл, используемый авторегистратором для отслеживания событий, был потерян.</span><span class="sxs-lookup"><span data-stu-id="1c399-114">The RTLostFile indicates that the backing file used by the AutoLogger to capture events was lost.</span></span>

<span data-ttu-id="1c399-115">События разрыва зависят от частоты, с которой регистрируются события, а также от того, сколько времени потребитель тратит на обработку событий.</span><span class="sxs-lookup"><span data-stu-id="1c399-115">Loosing events depends on the frequency with which the events are logged and how much time the consumer spends processing the events.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c399-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1c399-116">Requirements</span></span>



| <span data-ttu-id="1c399-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1c399-117">Requirement</span></span> | <span data-ttu-id="1c399-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1c399-118">Value</span></span> |
|-------------------------------------|------------------------------------------------|
| <span data-ttu-id="1c399-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c399-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1c399-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1c399-120">Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1c399-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c399-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1c399-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1c399-122">None supported</span></span><br/>                      |



## <a name="see-also"></a><span data-ttu-id="1c399-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c399-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c399-124">**Потерянное \_ событие**</span><span class="sxs-lookup"><span data-stu-id="1c399-124">**Lost\_Event**</span></span>](lost-event.md)
</dt> </dl>

 

 




