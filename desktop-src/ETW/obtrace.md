---
description: Представляет родительский класс, из которого производятся все классы трассировки событий диспетчера объектов.
ms.assetid: 07cfc4a2-c665-4080-bc4b-fe9ec7191fdc
title: Класс Обтраце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTrace
api_type:
- NA
api_location: ''
ms.openlocfilehash: ca89f58df9f5dd741da5b1fb8572b153c956cd43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815240"
---
# <a name="obtrace-class"></a><span data-ttu-id="784be-103">Класс Обтраце</span><span class="sxs-lookup"><span data-stu-id="784be-103">ObTrace class</span></span>

<span data-ttu-id="784be-104">Представляет родительский класс, из которого производятся все классы трассировки событий диспетчера объектов.</span><span class="sxs-lookup"><span data-stu-id="784be-104">Represents the parent class from which all object manager event trace classes are derived.</span></span>

<span data-ttu-id="784be-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="784be-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="784be-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="784be-106">Syntax</span></span>

``` syntax
[DisplayName("Object"), Dynamic, EventVersion(2), Guid("{89497f50-effe-4440-8cf2-ce6b1cdcaca7}")]
class ObTrace : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="784be-107">Участники</span><span class="sxs-lookup"><span data-stu-id="784be-107">Members</span></span>

<span data-ttu-id="784be-108">Класс **обтраце** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="784be-108">The **ObTrace** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="784be-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="784be-109">Remarks</span></span>

<span data-ttu-id="784be-110">Чтобы включить трассировку событий диспетчера объектов, вызовите функцию [**трацесетинформатион**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) с параметром *информатионкласс* , равным значению перечисления [**\_ \_ класса сведений о трассировке**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) **трацесистемтрацеенаблефлагсинфо** , а элемент **енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) — к **\_ \_ маркеру "PERF OB** " (0x80000040).</span><span class="sxs-lookup"><span data-stu-id="784be-110">To enable object manager event tracing, call the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function with the *InformationClass* parameter equal to the [**TRACE\_INFO\_CLASS**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) enumeration value **TraceSystemTraceEnableFlagsInfo** and the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure's **EnableFlags** member equal to **PERF\_OB\_HANDLE** (0x80000040).</span></span>

## <a name="requirements"></a><span data-ttu-id="784be-111">Требования</span><span class="sxs-lookup"><span data-stu-id="784be-111">Requirements</span></span>



| <span data-ttu-id="784be-112">Требование</span><span class="sxs-lookup"><span data-stu-id="784be-112">Requirement</span></span> | <span data-ttu-id="784be-113">Значение</span><span class="sxs-lookup"><span data-stu-id="784be-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="784be-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="784be-114">Minimum supported client</span></span><br/> | <span data-ttu-id="784be-115">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="784be-115">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="784be-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="784be-116">Minimum supported server</span></span><br/> | <span data-ttu-id="784be-117">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="784be-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="784be-118">MOF</span><span class="sxs-lookup"><span data-stu-id="784be-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="784be-119"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="784be-119"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 
