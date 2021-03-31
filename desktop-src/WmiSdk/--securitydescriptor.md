---
description: Представляет дескриптор безопасности.
ms.assetid: 1ade1751-52a2-4ada-8255-323321111663
ms.tgt_platform: multiple
title: Класс __SecurityDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SecurityDescriptor
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
ms.openlocfilehash: 5f305387a29d1d1569addafd127f53c98246e1a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264801"
---
# <a name="__securitydescriptor-class"></a><span data-ttu-id="727c8-103">\_\_Класс SecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="727c8-103">\_\_SecurityDescriptor class</span></span>

<span data-ttu-id="727c8-104">Абстрактный системный класс **\_ \_ SecurityDescriptor** представляет [*дескриптор безопасности*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="727c8-104">The **\_\_SecurityDescriptor** abstract system class represents a [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span>

<span data-ttu-id="727c8-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="727c8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="727c8-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="727c8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="727c8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="727c8-107">Syntax</span></span>

``` syntax
class __SecurityDescriptor
{
  uint32 ControlFlags;
  __ACE  DACL[];
  __ACE  Group;
  __ACE  Owner;
  __ACE  SACL;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="727c8-108">Члены</span><span class="sxs-lookup"><span data-stu-id="727c8-108">Members</span></span>

<span data-ttu-id="727c8-109">Класс **\_ \_ SecurityDescriptor** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="727c8-109">The **\_\_SecurityDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="727c8-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="727c8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="727c8-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="727c8-111">Properties</span></span>

<span data-ttu-id="727c8-112">Класс **\_ \_ SecurityDescriptor** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="727c8-112">The **\_\_SecurityDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="727c8-113">**контролфлагс**</span><span class="sxs-lookup"><span data-stu-id="727c8-113">**ControlFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727c8-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="727c8-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="727c8-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="727c8-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727c8-116">Битовые флаги, предоставляющие сведения о содержимом и формате дескриптора.</span><span class="sxs-lookup"><span data-stu-id="727c8-116">Bit flags that provide information about the descriptor's contents and format.</span></span> <span data-ttu-id="727c8-117">Описание флагов см. в свойстве **контролфлагс** в классе [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="727c8-117">See the **ControlFlags** property in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class for a description of the flags.</span></span>

</dd> <dt>

<span data-ttu-id="727c8-118">**КОНТРОЛЯ**</span><span class="sxs-lookup"><span data-stu-id="727c8-118">**DACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727c8-119">Тип данных: массив **[**\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="727c8-119">Data type: **[**\_\_ACE**](--ace.md)** array</span></span>
</dt> <dt>

<span data-ttu-id="727c8-120">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="727c8-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727c8-121">Массив записей [**\_ \_ ACE**](--ace.md) , которые определяют доступ к объекту.</span><span class="sxs-lookup"><span data-stu-id="727c8-121">An array of [**\_\_ACE**](--ace.md) entries that specify access to the object.</span></span>

</dd> <dt>

<span data-ttu-id="727c8-122">**Группа**</span><span class="sxs-lookup"><span data-stu-id="727c8-122">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727c8-123">Тип данных: **[ **\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="727c8-123">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="727c8-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="727c8-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727c8-125">ACE, определяющий доверенное лицо, представляющее группу объекта.</span><span class="sxs-lookup"><span data-stu-id="727c8-125">ACE that identifies the trustee representing the group of the object.</span></span>

</dd> <dt>

<span data-ttu-id="727c8-126">**Владелец**</span><span class="sxs-lookup"><span data-stu-id="727c8-126">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727c8-127">Тип данных: **[ **\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="727c8-127">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="727c8-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="727c8-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727c8-129">ACE, определяющий доверенное лицо, представляющее владельца объекта.</span><span class="sxs-lookup"><span data-stu-id="727c8-129">ACE that identifies the trustee representing the owner of the object.</span></span>

</dd> <dt>

<span data-ttu-id="727c8-130">**СИСТЕМНЫЙ**</span><span class="sxs-lookup"><span data-stu-id="727c8-130">**SACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727c8-131">Тип данных: **[ **\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="727c8-131">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="727c8-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="727c8-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727c8-133">Массив записей [**\_ \_ ACE**](--ace.md) , определяющих пользователей и группы, для которых собираются данные аудита.</span><span class="sxs-lookup"><span data-stu-id="727c8-133">An array of [**\_\_ACE**](--ace.md) entries that identifies users and groups for which auditing information is gathered.</span></span>

</dd> <dt>

<span data-ttu-id="727c8-134">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="727c8-134">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727c8-135">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="727c8-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="727c8-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="727c8-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727c8-137">Время в формате [ \_ даты и времени CIM](cim-datetime.md) при создании дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="727c8-137">Time in the [CIM\_DATETIME](cim-datetime.md) format when the security descriptor was created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="727c8-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="727c8-138">Remarks</span></span>

<span data-ttu-id="727c8-139">Этот класс предоставляет свойства, наследуемые с помощью [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="727c8-139">This class provides properties inherited by [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="727c8-140">Дополнительные сведения см. в разделе [объекты дескрипторов безопасности WMI](wmi-security-descriptor-objects.md) и [изменение параметров безопасности доступа для защищаемых объектов](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="727c8-140">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="727c8-141">Дополнительные сведения об [элементах управления доступом](/windows/desktop/SecAuthZ/access-control-components)см. в разделе компоненты контроля доступа.</span><span class="sxs-lookup"><span data-stu-id="727c8-141">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="727c8-142">Требования</span><span class="sxs-lookup"><span data-stu-id="727c8-142">Requirements</span></span>



| <span data-ttu-id="727c8-143">Требование</span><span class="sxs-lookup"><span data-stu-id="727c8-143">Requirement</span></span> | <span data-ttu-id="727c8-144">Значение</span><span class="sxs-lookup"><span data-stu-id="727c8-144">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="727c8-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="727c8-145">Minimum supported client</span></span><br/> | <span data-ttu-id="727c8-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="727c8-146">Windows Vista</span></span><br/>       |
| <span data-ttu-id="727c8-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="727c8-147">Minimum supported server</span></span><br/> | <span data-ttu-id="727c8-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="727c8-148">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="727c8-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="727c8-149">Namespace</span></span><br/>                | <span data-ttu-id="727c8-150">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="727c8-150">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="727c8-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="727c8-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="727c8-152">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="727c8-152">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="727c8-153">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="727c8-153">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="727c8-154">Поддержание безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="727c8-154">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

