---
description: Представляет элемент управления доступом.
ms.assetid: 47daffd0-b9db-4367-b0b8-654a2da30fed
ms.tgt_platform: multiple
title: Класс __ACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ACE
- All
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
ms.openlocfilehash: ea2a765225145ce3d44e0aff89aeaca0a7563e0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498069"
---
# <a name="__ace-class"></a><span data-ttu-id="0f5ea-103">\_\_Класс ACE</span><span class="sxs-lookup"><span data-stu-id="0f5ea-103">\_\_ACE class</span></span>

<span data-ttu-id="0f5ea-104">Абстрактный системный класс **\_ \_ ACE** представляет запись управления доступом ([*ACE*](/windows/desktop/SecGloss/a-gly)).</span><span class="sxs-lookup"><span data-stu-id="0f5ea-104">The **\_\_ACE** abstract system class represents an access control entry ([*ACE*](/windows/desktop/SecGloss/a-gly)).</span></span>

<span data-ttu-id="0f5ea-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="0f5ea-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0f5ea-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="0f5ea-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f5ea-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f5ea-107">Syntax</span></span>

``` syntax
class  __ACE : __SecurityRelatedClass
{
            AceFlags;
            AccessMask;
            AceType;
            GuidInheritedObjectType;
            GuidObjectType;
  uint64    TIME_CREATED;
  __Trustee Trustee;
};
```

## <a name="members"></a><span data-ttu-id="0f5ea-108">Члены</span><span class="sxs-lookup"><span data-stu-id="0f5ea-108">Members</span></span>

<span data-ttu-id="0f5ea-109">Класс **\_ \_ ACE** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0f5ea-109">The **\_\_ACE** class has these types of members:</span></span>

-   [<span data-ttu-id="0f5ea-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0f5ea-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0f5ea-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="0f5ea-111">Properties</span></span>

<span data-ttu-id="0f5ea-112">Класс **\_ \_ ACE** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0f5ea-112">The **\_\_ACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f5ea-113">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="0f5ea-113">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f5ea-114">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0f5ea-114">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="0f5ea-115">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0f5ea-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0f5ea-116">Битовые флаги, представляющие права, которые предоставляются или запрещают доверенному лицу.</span><span class="sxs-lookup"><span data-stu-id="0f5ea-116">Bit flags representing rights that are granted or denied to the trustee.</span></span> <span data-ttu-id="0f5ea-117">Дополнительные сведения и описание флагов см. в разделе свойство **AccessMask** в классе [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="0f5ea-117">For more information and a description of the flags, see **AccessMask** property in the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ea-118">**AceFlags**</span><span class="sxs-lookup"><span data-stu-id="0f5ea-118">**AceFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f5ea-119">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0f5ea-119">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="0f5ea-120">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0f5ea-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0f5ea-121">Битовые флаги, определяющие наследование ACE.</span><span class="sxs-lookup"><span data-stu-id="0f5ea-121">Bit flags specifying the inheritance of the ACE.</span></span> <span data-ttu-id="0f5ea-122">Дополнительные сведения и описание флагов см. в разделе свойство **AceFlags** в классе [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="0f5ea-122">For more information and a description of the flags, see **AceFlags** property in the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ea-123">**AceType**</span><span class="sxs-lookup"><span data-stu-id="0f5ea-123">**AceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f5ea-124">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0f5ea-124">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="0f5ea-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0f5ea-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0f5ea-126">Тип записи ACE, представляемой этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="0f5ea-126">The type of ACE entry that this instance represents.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ea-127">**гуидинхеритедобжекттипе**</span><span class="sxs-lookup"><span data-stu-id="0f5ea-127">**GuidInheritedObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f5ea-128">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0f5ea-128">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="0f5ea-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0f5ea-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0f5ea-130">Идентификатор GUID родителя объекта, к которому применяются права доступа в свойстве **AccessMask** .</span><span class="sxs-lookup"><span data-stu-id="0f5ea-130">The GUID of the parent of the object to which the access rights in the **AccessMask** property apply.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ea-131">**гуидобжекттипе**</span><span class="sxs-lookup"><span data-stu-id="0f5ea-131">**GuidObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f5ea-132">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0f5ea-132">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="0f5ea-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0f5ea-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0f5ea-134">Идентификатор GUID, указывающий тип объекта, к которому применяются права в свойстве **AccessMask** .</span><span class="sxs-lookup"><span data-stu-id="0f5ea-134">The GUID that indicates the type of object to which the rights in the **AccessMask** property apply.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ea-135">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="0f5ea-135">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f5ea-136">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0f5ea-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0f5ea-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f5ea-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f5ea-138">Время создания дескриптора безопасности в формате [ \_ даты и времени CIM](cim-datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="0f5ea-138">The time, in the [CIM\_DATETIME](cim-datetime.md) format, when the security descriptor was created.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ea-139">**Доверенное лицо**</span><span class="sxs-lookup"><span data-stu-id="0f5ea-139">**Trustee**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f5ea-140">Тип данных: **[ **\_ \_ доверенное лицо**](--trustee.md)**</span><span class="sxs-lookup"><span data-stu-id="0f5ea-140">Data type: **[**\_\_Trustee**](--trustee.md)**</span></span>
</dt> <dt>

<span data-ttu-id="0f5ea-141">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0f5ea-141">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0f5ea-142">Доверенное лицо записи ACE, представленной этим экземпляром класса **\_ \_ ACE** .</span><span class="sxs-lookup"><span data-stu-id="0f5ea-142">The trustee of the ACE entry represented by this instance of the **\_\_ACE** class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f5ea-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f5ea-143">Remarks</span></span>

<span data-ttu-id="0f5ea-144">Этот класс предоставляет свойства, наследуемые классом [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) , который является членом класса [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="0f5ea-144">This class provides the properties that are inherited by the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class, which is a member of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="0f5ea-145">Дополнительные сведения см. в разделе [объекты дескрипторов безопасности WMI](wmi-security-descriptor-objects.md) и [изменение параметров безопасности доступа для защищаемых объектов](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="0f5ea-145">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="0f5ea-146">Дополнительные сведения об [элементах управления доступом](/windows/desktop/SecAuthZ/access-control-components)см. в разделе компоненты контроля доступа.</span><span class="sxs-lookup"><span data-stu-id="0f5ea-146">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f5ea-147">Требования</span><span class="sxs-lookup"><span data-stu-id="0f5ea-147">Requirements</span></span>



| <span data-ttu-id="0f5ea-148">Требование</span><span class="sxs-lookup"><span data-stu-id="0f5ea-148">Requirement</span></span> | <span data-ttu-id="0f5ea-149">Значение</span><span class="sxs-lookup"><span data-stu-id="0f5ea-149">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0f5ea-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f5ea-150">Minimum supported client</span></span><br/> | <span data-ttu-id="0f5ea-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f5ea-151">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0f5ea-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f5ea-152">Minimum supported server</span></span><br/> | <span data-ttu-id="0f5ea-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f5ea-153">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="0f5ea-154">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0f5ea-154">Namespace</span></span><br/>                | <span data-ttu-id="0f5ea-155">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="0f5ea-155">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="0f5ea-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f5ea-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f5ea-157">**\_\_секуритирелатедкласс**</span><span class="sxs-lookup"><span data-stu-id="0f5ea-157">**\_\_SecurityRelatedClass**</span></span>](--securityrelatedclass.md)
</dt> <dt>

[<span data-ttu-id="0f5ea-158">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="0f5ea-158">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="0f5ea-159">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="0f5ea-159">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="0f5ea-160">Поддержание безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="0f5ea-160">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

