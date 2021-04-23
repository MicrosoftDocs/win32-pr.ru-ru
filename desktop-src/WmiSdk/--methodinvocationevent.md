---
description: '\_ \_ Системный класс месодинвокатионевент определен, но не реализован.'
ms.assetid: ea736e44-a6bc-41e5-abc5-9e21a5504f44
ms.tgt_platform: multiple
title: Класс __MethodInvocationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodInvocationEvent
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: bc7e8d70d027caf31a90d49abc490c2de2d52fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265615"
---
# <a name="__methodinvocationevent-class"></a><span data-ttu-id="5dd6f-103">\_\_Класс Месодинвокатионевент</span><span class="sxs-lookup"><span data-stu-id="5dd6f-103">\_\_MethodInvocationEvent class</span></span>

<span data-ttu-id="5dd6f-104">Системный класс **\_ \_ месодинвокатионевент** определен, но не реализован.</span><span class="sxs-lookup"><span data-stu-id="5dd6f-104">The **\_\_MethodInvocationEvent** system class is defined but is not implemented.</span></span>

<span data-ttu-id="5dd6f-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="5dd6f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5dd6f-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="5dd6f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dd6f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5dd6f-107">Syntax</span></span>

``` syntax
class __MethodInvocationEvent : __InstanceOperationEvent
{
  string       Method;
  __Parameters Parameters;
  boolean      PreCall;
  uint8        SECURITY_DESCRIPTOR[];
  object       TargetInstance;
  uint64       TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="5dd6f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="5dd6f-108">Members</span></span>

<span data-ttu-id="5dd6f-109">Класс **\_ \_ месодинвокатионевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5dd6f-109">The **\_\_MethodInvocationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="5dd6f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="5dd6f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5dd6f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="5dd6f-111">Properties</span></span>

<span data-ttu-id="5dd6f-112">Класс **\_ \_ месодинвокатионевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5dd6f-112">The **\_\_MethodInvocationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5dd6f-113">**Метод**</span><span class="sxs-lookup"><span data-stu-id="5dd6f-113">**Method**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dd6f-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5dd6f-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5dd6f-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5dd6f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5dd6f-116">Метод, вызываемый для активации события.</span><span class="sxs-lookup"><span data-stu-id="5dd6f-116">Method invoked to trigger the event.</span></span>

</dd> <dt>

<span data-ttu-id="5dd6f-117">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="5dd6f-117">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dd6f-118">Тип данных: **\_ \_ Параметры**</span><span class="sxs-lookup"><span data-stu-id="5dd6f-118">Data type: **\_\_Parameters**</span></span>
</dt> <dt>

<span data-ttu-id="5dd6f-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5dd6f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5dd6f-120">Ссылка на экземпляр, представляющий входные и выходные параметры вызова метода.</span><span class="sxs-lookup"><span data-stu-id="5dd6f-120">Reference to an instance that represents the input and output parameters of the method call.</span></span>

</dd> <dt>

<span data-ttu-id="5dd6f-121">**Предвызов**</span><span class="sxs-lookup"><span data-stu-id="5dd6f-121">**PreCall**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dd6f-122">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="5dd6f-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5dd6f-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5dd6f-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5dd6f-124">Если **значение — true**, событие возникает перед вызовом метода.</span><span class="sxs-lookup"><span data-stu-id="5dd6f-124">If **TRUE**, the event is raised before the method is called.</span></span>

</dd> <dt>

<span data-ttu-id="5dd6f-125">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="5dd6f-125">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dd6f-126">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="5dd6f-126">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5dd6f-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5dd6f-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5dd6f-128">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="5dd6f-128">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="5dd6f-129">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="5dd6f-129">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="5dd6f-130">Дополнительные сведения см. в разделе [дескрипторы безопасности](/windows/desktop/SecAuthZ/security-descriptors).</span><span class="sxs-lookup"><span data-stu-id="5dd6f-130">For more information, see [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors).</span></span>

</dd> <dt>

<span data-ttu-id="5dd6f-131">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="5dd6f-131">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dd6f-132">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="5dd6f-132">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5dd6f-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5dd6f-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5dd6f-134">Экземпляр метода, для которого вызывается метод.</span><span class="sxs-lookup"><span data-stu-id="5dd6f-134">Instance the method is invoked on.</span></span> <span data-ttu-id="5dd6f-135">Это свойство наследуется от [**\_ \_ инстанцеоператионевент**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="5dd6f-135">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dd6f-136">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="5dd6f-136">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dd6f-137">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5dd6f-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5dd6f-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5dd6f-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5dd6f-139">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="5dd6f-139">Unique value that indicates the time an event is generated.</span></span> <span data-ttu-id="5dd6f-140">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="5dd6f-140">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="5dd6f-141">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="5dd6f-141">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="5dd6f-142">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="5dd6f-142">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="5dd6f-143">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5dd6f-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5dd6f-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5dd6f-144">Remarks</span></span>

<span data-ttu-id="5dd6f-145">Класс **\_ \_ месодинвокатионевент** является производным от [**\_ \_ инстанцеоператионевент**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="5dd6f-145">The **\_\_MethodInvocationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5dd6f-146">Требования</span><span class="sxs-lookup"><span data-stu-id="5dd6f-146">Requirements</span></span>



| <span data-ttu-id="5dd6f-147">Требование</span><span class="sxs-lookup"><span data-stu-id="5dd6f-147">Requirement</span></span> | <span data-ttu-id="5dd6f-148">Значение</span><span class="sxs-lookup"><span data-stu-id="5dd6f-148">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5dd6f-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5dd6f-149">Minimum supported client</span></span><br/> | <span data-ttu-id="5dd6f-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5dd6f-150">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5dd6f-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5dd6f-151">Minimum supported server</span></span><br/> | <span data-ttu-id="5dd6f-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5dd6f-152">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="5dd6f-153">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5dd6f-153">Namespace</span></span><br/>                | <span data-ttu-id="5dd6f-154">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="5dd6f-154">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5dd6f-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5dd6f-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dd6f-156">**\_\_инстанцеоператионевент**</span><span class="sxs-lookup"><span data-stu-id="5dd6f-156">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="5dd6f-157">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="5dd6f-157">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

