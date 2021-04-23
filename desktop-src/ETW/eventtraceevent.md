---
description: Родительский класс для событий заголовка журнала. Этот класс всегда является первым классом трассировки событий, отправляемым потребителю (это событие не отправляется потребителям реального времени). Следующий синтаксис упрощен из MOF-кода.
ms.assetid: fb507d9a-6ed2-4cb1-8cea-85c0a3832e51
title: Класс Евенттрацеевент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTraceEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0036ee0a49225568aac066735824fe55ce8f0fa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984496"
---
# <a name="eventtraceevent-class"></a><span data-ttu-id="d0129-105">Класс Евенттрацеевент</span><span class="sxs-lookup"><span data-stu-id="d0129-105">EventTraceEvent class</span></span>

<span data-ttu-id="d0129-106">Родительский класс для событий заголовка журнала.</span><span class="sxs-lookup"><span data-stu-id="d0129-106">The parent class for log header events.</span></span> <span data-ttu-id="d0129-107">Этот класс всегда является первым классом трассировки событий, отправляемым потребителю (это событие не отправляется потребителям реального времени).</span><span class="sxs-lookup"><span data-stu-id="d0129-107">This class is always the first event trace class sent to a consumer (this event is not sent to real-time consumers).</span></span>

<span data-ttu-id="d0129-108">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="d0129-108">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0129-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0129-109">Syntax</span></span>

``` syntax
[Guid("{68fdd900-4a3e-11d1-84f4-0000f80464e3}")]
class EventTraceEvent : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="d0129-110">Участники</span><span class="sxs-lookup"><span data-stu-id="d0129-110">Members</span></span>

<span data-ttu-id="d0129-111">Класс **евенттрацеевент** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="d0129-111">The **EventTraceEvent** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0129-112">Требования</span><span class="sxs-lookup"><span data-stu-id="d0129-112">Requirements</span></span>



| <span data-ttu-id="d0129-113">Требование</span><span class="sxs-lookup"><span data-stu-id="d0129-113">Requirement</span></span> | <span data-ttu-id="d0129-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d0129-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d0129-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0129-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d0129-116">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d0129-116">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d0129-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0129-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d0129-118">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d0129-118">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d0129-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0129-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0129-120">**МСНТ \_ системтраце**</span><span class="sxs-lookup"><span data-stu-id="d0129-120">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="d0129-121">**\_Заголовок евенттраце**</span><span class="sxs-lookup"><span data-stu-id="d0129-121">**EventTrace\_Header**</span></span>](eventtrace-header.md)
</dt> </dl>

 

 




