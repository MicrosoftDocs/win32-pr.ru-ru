---
description: '\_Класс WMI взаимосвязей Win32 депендентсервице связывает две взаимозависимые базовые службы.'
ms.assetid: ba21fce3-f8f9-4886-b09d-a9e830376364
ms.tgt_platform: multiple
title: Класс Win32_DependentService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DependentService
- Win32_DependentService.TypeOfDependency
- Win32_DependentService.Antecedent
- Win32_DependentService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 047ec3411186f09f3d0e76da27158aa8ee91d4cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142862"
---
# <a name="win32_dependentservice-class"></a><span data-ttu-id="2f597-103">\_Класс Win32 депендентсервице</span><span class="sxs-lookup"><span data-stu-id="2f597-103">Win32\_DependentService class</span></span>

<span data-ttu-id="2f597-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ депендентсервице** связывает две взаимозависимые базовые службы.</span><span class="sxs-lookup"><span data-stu-id="2f597-104">The **Win32\_DependentService** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates two interdependent base services.</span></span>

<span data-ttu-id="2f597-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="2f597-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2f597-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="2f597-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f597-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f597-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DependentService : CIM_ServiceServiceDependency
{
  uint16                TypeOfDependency;
  Win32_BaseService REF Antecedent;
  Win32_BaseService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2f597-108">Члены</span><span class="sxs-lookup"><span data-stu-id="2f597-108">Members</span></span>

<span data-ttu-id="2f597-109">Класс **Win32 \_ депендентсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2f597-109">The **Win32\_DependentService** class has these types of members:</span></span>

-   [<span data-ttu-id="2f597-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2f597-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f597-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="2f597-111">Properties</span></span>

<span data-ttu-id="2f597-112">Класс **Win32 \_ депендентсервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2f597-112">The **Win32\_DependentService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f597-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="2f597-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f597-114">Тип данных: **Win32 \_ басесервице**</span><span class="sxs-lookup"><span data-stu-id="2f597-114">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="2f597-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2f597-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f597-116">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ басесервице")</span><span class="sxs-lookup"><span data-stu-id="2f597-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="2f597-117">[**\_ Басесервице Win32**](win32-baseservice.md) , представляющий базовую службу, **зависит от зависимого** свойства этого класса.</span><span class="sxs-lookup"><span data-stu-id="2f597-117">A [**Win32\_BaseService**](win32-baseservice.md) representing the base service relied upon by the **Dependent** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="2f597-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="2f597-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f597-119">Тип данных: **Win32 \_ басесервице**</span><span class="sxs-lookup"><span data-stu-id="2f597-119">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="2f597-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2f597-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f597-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ басесервице")</span><span class="sxs-lookup"><span data-stu-id="2f597-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="2f597-122">[**\_ Басесервице Win32**](win32-baseservice.md) , представляющий базовую службу, которая зависит от свойства **Antecedent** этого класса.</span><span class="sxs-lookup"><span data-stu-id="2f597-122">A [**Win32\_BaseService**](win32-baseservice.md) representing the base service that is dependent on the **Antecedent** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="2f597-123">**типеофдепенденци**</span><span class="sxs-lookup"><span data-stu-id="2f597-123">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f597-124">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2f597-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f597-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2f597-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f597-126">Природа зависимости между службами.</span><span class="sxs-lookup"><span data-stu-id="2f597-126">Nature of the service-to-service dependency.</span></span> <span data-ttu-id="2f597-127">Это свойство указывает, что связанная служба должна быть завершена, должна быть запущена или не должна запускаться для функционирования службы.</span><span class="sxs-lookup"><span data-stu-id="2f597-127">This property indicates that the associated service must have completed, must be started, or must not be started for the service to function.</span></span>

<span data-ttu-id="2f597-128">Это свойство наследуется от [**CIM \_ сервицесервицедепенденци**](cim-serviceservicedependency.md).</span><span class="sxs-lookup"><span data-stu-id="2f597-128">This property is inherited from [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2f597-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="2f597-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2f597-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="2f597-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>

<span data-ttu-id="2f597-131"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**Служба должна быть завершена** (2)</span><span class="sxs-lookup"><span data-stu-id="2f597-131"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**Service Must Have Completed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2f597-132">Служба должна быть завершена.</span><span class="sxs-lookup"><span data-stu-id="2f597-132">Service must have completed.</span></span>

</dd> <dt>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>

<span data-ttu-id="2f597-133"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**Служба должна быть запущена** (3)</span><span class="sxs-lookup"><span data-stu-id="2f597-133"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**Service Must Be Started** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2f597-134">Служба должна быть запущена.</span><span class="sxs-lookup"><span data-stu-id="2f597-134">Service must be started.</span></span>

</dd> <dt>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>

<span data-ttu-id="2f597-135"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**Служба не должна запускаться** (4)</span><span class="sxs-lookup"><span data-stu-id="2f597-135"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**Service Must Not Be Started** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2f597-136">Служба не должна быть запущена.</span><span class="sxs-lookup"><span data-stu-id="2f597-136">Service must not be started.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f597-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f597-137">Remarks</span></span>

<span data-ttu-id="2f597-138">Класс **Win32 \_ депендентсервице** является производным от [**CIM \_ сервицесервицедепенденци**](cim-serviceservicedependency.md).</span><span class="sxs-lookup"><span data-stu-id="2f597-138">The **Win32\_DependentService** class is derived from [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f597-139">Требования</span><span class="sxs-lookup"><span data-stu-id="2f597-139">Requirements</span></span>



| <span data-ttu-id="2f597-140">Требование</span><span class="sxs-lookup"><span data-stu-id="2f597-140">Requirement</span></span> | <span data-ttu-id="2f597-141">Значение</span><span class="sxs-lookup"><span data-stu-id="2f597-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f597-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f597-142">Minimum supported client</span></span><br/> | <span data-ttu-id="2f597-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f597-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2f597-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f597-144">Minimum supported server</span></span><br/> | <span data-ttu-id="2f597-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f597-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2f597-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2f597-146">Namespace</span></span><br/>                | <span data-ttu-id="2f597-147">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2f597-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2f597-148">MOF</span><span class="sxs-lookup"><span data-stu-id="2f597-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f597-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f597-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f597-150">DLL</span><span class="sxs-lookup"><span data-stu-id="2f597-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f597-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f597-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f597-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f597-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f597-153">**\_СЕРВИЦЕСЕРВИЦЕДЕПЕНДЕНЦИ CIM**</span><span class="sxs-lookup"><span data-stu-id="2f597-153">**CIM\_ServiceServiceDependency**</span></span>](cim-serviceservicedependency.md)
</dt> <dt>

<span data-ttu-id="2f597-154">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f597-154">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

