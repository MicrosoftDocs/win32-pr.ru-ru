---
description: '\_ \_ Абстрактный системный класс доверенного лица представляет доверенное лицо. Можно использовать либо имя, либо идентификатор безопасности (массив байтов).'
ms.assetid: 92d17c7c-ebca-4dd0-80d8-6edd999ca394
ms.tgt_platform: multiple
title: Класс __Trustee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Trustee
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
ms.openlocfilehash: 5c6ba04760e924ffe9d86916cffdb82ea2488219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547183"
---
# <a name="__trustee-class"></a><span data-ttu-id="2be6d-104">\_\_Класс доверенного лица</span><span class="sxs-lookup"><span data-stu-id="2be6d-104">\_\_Trustee class</span></span>

<span data-ttu-id="2be6d-105">Абстрактный системный класс [**\_ \_ доверенного лица**](--securitydescriptor.md) представляет [*доверенное лицо*](/windows/desktop/SecGloss/t-gly).</span><span class="sxs-lookup"><span data-stu-id="2be6d-105">The [**\_\_Trustee**](--securitydescriptor.md) abstract system class represents a [*trustee*](/windows/desktop/SecGloss/t-gly).</span></span> <span data-ttu-id="2be6d-106">Можно использовать либо имя, либо идентификатор безопасности (массив байтов).</span><span class="sxs-lookup"><span data-stu-id="2be6d-106">Either a name or an SID (byte array) can be used.</span></span>

<span data-ttu-id="2be6d-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="2be6d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2be6d-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="2be6d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2be6d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2be6d-109">Syntax</span></span>

``` syntax
class __Trustee
{
  string Domain;
  string Name;
  uint8  SID[];
  uint32 SidLength;
  string SidString;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="2be6d-110">Члены</span><span class="sxs-lookup"><span data-stu-id="2be6d-110">Members</span></span>

<span data-ttu-id="2be6d-111">Класс **\_ \_ доверенного лица** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2be6d-111">The **\_\_Trustee** class has these types of members:</span></span>

-   [<span data-ttu-id="2be6d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="2be6d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2be6d-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="2be6d-113">Properties</span></span>

<span data-ttu-id="2be6d-114">Класс **\_ \_ доверенного лица** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="2be6d-114">The **\_\_Trustee** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2be6d-115">**Доменная**</span><span class="sxs-lookup"><span data-stu-id="2be6d-115">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be6d-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2be6d-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be6d-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2be6d-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2be6d-118">Доменная часть учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2be6d-118">Domain portion of the account.</span></span>

</dd> <dt>

<span data-ttu-id="2be6d-119">**Name**</span><span class="sxs-lookup"><span data-stu-id="2be6d-119">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be6d-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2be6d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be6d-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2be6d-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2be6d-122">Имя части учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2be6d-122">Name portion of the account.</span></span>

</dd> <dt>

<span data-ttu-id="2be6d-123">**SID**</span><span class="sxs-lookup"><span data-stu-id="2be6d-123">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be6d-124">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="2be6d-124">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2be6d-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2be6d-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2be6d-126">Идентификатор безопасности доверенного лица в двоичном формате байтового массива.</span><span class="sxs-lookup"><span data-stu-id="2be6d-126">The SID of the trustee in the binary byte array form.</span></span>

</dd> <dt>

<span data-ttu-id="2be6d-127">**сидленгс**</span><span class="sxs-lookup"><span data-stu-id="2be6d-127">**SidLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be6d-128">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2be6d-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2be6d-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2be6d-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2be6d-130">Длина SID в байтах.</span><span class="sxs-lookup"><span data-stu-id="2be6d-130">The length of the SID in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2be6d-131">**сидстринг**</span><span class="sxs-lookup"><span data-stu-id="2be6d-131">**SidString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be6d-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2be6d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be6d-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2be6d-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2be6d-134">Идентификатор безопасности доверенного лица в строковом формате, например "S-1-1-0".</span><span class="sxs-lookup"><span data-stu-id="2be6d-134">The SID of the trustee in the string format, for example, "S-1-1-0".</span></span>

</dd> <dt>

<span data-ttu-id="2be6d-135">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="2be6d-135">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be6d-136">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2be6d-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2be6d-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2be6d-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2be6d-138">Время в формате [ \_ даты и времени CIM](cim-datetime.md) при создании дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="2be6d-138">Time in the [CIM\_DATETIME](cim-datetime.md) format when the security descriptor was created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2be6d-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2be6d-139">Remarks</span></span>

<span data-ttu-id="2be6d-140">Этот класс предоставляет свойства, наследуемые классом [**\_ доверенного лица Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , который является членом класса [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="2be6d-140">This class provides properties that are inherited by the [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) class, which is a member of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="2be6d-141">Дополнительные сведения см. в разделе [объекты дескрипторов безопасности WMI](wmi-security-descriptor-objects.md) и [изменение параметров безопасности доступа для защищаемых объектов](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2be6d-141">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="2be6d-142">Дополнительные сведения об [элементах управления доступом](/windows/desktop/SecAuthZ/access-control-components)см. в разделе компоненты контроля доступа.</span><span class="sxs-lookup"><span data-stu-id="2be6d-142">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="2be6d-143">Требования</span><span class="sxs-lookup"><span data-stu-id="2be6d-143">Requirements</span></span>



| <span data-ttu-id="2be6d-144">Требование</span><span class="sxs-lookup"><span data-stu-id="2be6d-144">Requirement</span></span> | <span data-ttu-id="2be6d-145">Значение</span><span class="sxs-lookup"><span data-stu-id="2be6d-145">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="2be6d-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2be6d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="2be6d-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2be6d-147">Windows Vista</span></span><br/>       |
| <span data-ttu-id="2be6d-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2be6d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="2be6d-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2be6d-149">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="2be6d-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2be6d-150">Namespace</span></span><br/>                | <span data-ttu-id="2be6d-151">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="2be6d-151">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="2be6d-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2be6d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2be6d-153">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="2be6d-153">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="2be6d-154">**\_Доверенное лицо Win32**</span><span class="sxs-lookup"><span data-stu-id="2be6d-154">**Win32\_Trustee**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
</dt> <dt>

[<span data-ttu-id="2be6d-155">Поддержание безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="2be6d-155">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

