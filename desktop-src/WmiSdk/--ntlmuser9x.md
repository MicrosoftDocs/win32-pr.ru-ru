---
description: Управляет удаленным доступом к неподдерживаемым версиям Windows.
ms.assetid: eb326bba-a011-4b9c-b4ee-fc08ae364f6f
ms.tgt_platform: multiple
title: Класс __NTLMUser9X
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NTLMUser9X
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 79aa5153869c7337b6849e8c465dbbf8b36a0f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703011"
---
# <a name="__ntlmuser9x-class"></a><span data-ttu-id="35722-103">\_\_Класс NTLMUser9X</span><span class="sxs-lookup"><span data-stu-id="35722-103">\_\_NTLMUser9X class</span></span>

<span data-ttu-id="35722-104">Класс System **\_ \_ NTLMUser9X** управляет удаленным доступом к неподдерживаемым версиям Windows.</span><span class="sxs-lookup"><span data-stu-id="35722-104">The **\_\_NTLMUser9X** system class controls remote access to unsupported versions of Windows.</span></span> <span data-ttu-id="35722-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="35722-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="35722-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="35722-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="35722-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35722-107">Syntax</span></span>

``` syntax
class __NTLMUser9X : __SecurityRelatedClass
{
  string Authority;
  sint32 Flags;
  sint32 Mask;
  string Name;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="35722-108">Члены</span><span class="sxs-lookup"><span data-stu-id="35722-108">Members</span></span>

<span data-ttu-id="35722-109">Класс **\_ \_ NTLMUser9X** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="35722-109">The **\_\_NTLMUser9X** class has these types of members:</span></span>

-   [<span data-ttu-id="35722-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="35722-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35722-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="35722-111">Properties</span></span>

<span data-ttu-id="35722-112">Класс **\_ \_ NTLMUser9X** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="35722-112">The **\_\_NTLMUser9X** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35722-113">**Центр авторизации**</span><span class="sxs-lookup"><span data-stu-id="35722-113">**Authority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35722-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="35722-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35722-115">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35722-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35722-116">Домен, к которому применяется имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="35722-116">Domain to which a user name applies.</span></span>

</dd> <dt>

<span data-ttu-id="35722-117">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="35722-117">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35722-118">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="35722-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="35722-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35722-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35722-120">Флаги наследования.</span><span class="sxs-lookup"><span data-stu-id="35722-120">Inheritance flags.</span></span>

<dt>

<span data-ttu-id="35722-121">0</span><span class="sxs-lookup"><span data-stu-id="35722-121">0</span></span>
</dt> <dd>

<span data-ttu-id="35722-122">Без наследования.</span><span class="sxs-lookup"><span data-stu-id="35722-122">No inheritance.</span></span>

</dd> <dt>

<span data-ttu-id="35722-123">2</span><span class="sxs-lookup"><span data-stu-id="35722-123">2</span></span>
</dt> <dd>

<span data-ttu-id="35722-124">Применяется к дочерним пространствам имен в дополнение к текущему.</span><span class="sxs-lookup"><span data-stu-id="35722-124">Apply to child namespaces, in addition to the current one.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="35722-125">**Mask**</span><span class="sxs-lookup"><span data-stu-id="35722-125">**Mask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35722-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="35722-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="35722-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35722-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35722-128">Битовая маска, указывающая права доступа к пространству имен в репозитории инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="35722-128">Bitmask that specifies access rights to the namespace in the Windows Management Instrumentation (WMI) repository.</span></span> <span data-ttu-id="35722-129">Значения битов см. в разделе [**константы прав доступа к пространству имен**](namespace-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="35722-129">For bit values, see [**Namespace Access Rights Constants**](namespace-access-rights-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="35722-130">**Name**</span><span class="sxs-lookup"><span data-stu-id="35722-130">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35722-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="35722-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35722-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35722-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35722-133">Имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="35722-133">User name.</span></span>

</dd> <dt>

<span data-ttu-id="35722-134">**Тип**</span><span class="sxs-lookup"><span data-stu-id="35722-134">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35722-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="35722-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="35722-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35722-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35722-137">Доступ разрешен.</span><span class="sxs-lookup"><span data-stu-id="35722-137">Access allowed.</span></span>

<dt>

<span data-ttu-id="35722-138">0</span><span class="sxs-lookup"><span data-stu-id="35722-138">0</span></span>
</dt> <dd>

<span data-ttu-id="35722-139">Доступ разрешен.</span><span class="sxs-lookup"><span data-stu-id="35722-139">Access allowed.</span></span>

</dd> <dt>

<span data-ttu-id="35722-140">2</span><span class="sxs-lookup"><span data-stu-id="35722-140">2</span></span>
</dt> <dd>

<span data-ttu-id="35722-141">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="35722-141">Access denied.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35722-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35722-142">Remarks</span></span>

<span data-ttu-id="35722-143">Класс **\_ \_ NTLMUser9X** используется в качестве входного параметра для методов [**\_ \_ системсекурити:: Get9XUserList**](--systemsecurity-get9xuserlist.md) и [**\_ \_ системсекурити:: Set9XUserList**](--systemsecurity-set9xuserlist.md) .</span><span class="sxs-lookup"><span data-stu-id="35722-143">The **\_\_NTLMUser9X** class is used as an input parameter for the [**\_\_SystemSecurity::Get9XUserList**](--systemsecurity-get9xuserlist.md) and [**\_\_SystemSecurity::Set9XUserList**](--systemsecurity-set9xuserlist.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="35722-144">Требования</span><span class="sxs-lookup"><span data-stu-id="35722-144">Requirements</span></span>



| <span data-ttu-id="35722-145">Требование</span><span class="sxs-lookup"><span data-stu-id="35722-145">Requirement</span></span> | <span data-ttu-id="35722-146">Значение</span><span class="sxs-lookup"><span data-stu-id="35722-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="35722-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35722-147">Minimum supported client</span></span><br/> | <span data-ttu-id="35722-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35722-148">Windows Vista</span></span><br/>       |
| <span data-ttu-id="35722-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35722-149">Minimum supported server</span></span><br/> | <span data-ttu-id="35722-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35722-150">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="35722-151">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="35722-151">Namespace</span></span><br/>                | <span data-ttu-id="35722-152">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="35722-152">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="35722-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35722-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35722-154">**\_\_секуритирелатедкласс**</span><span class="sxs-lookup"><span data-stu-id="35722-154">**\_\_SecurityRelatedClass**</span></span>](/windows/desktop/WmiSdk/--securityrelatedclass)
</dt> <dt>

[<span data-ttu-id="35722-155">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="35722-155">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="35722-156">**\_\_системсекурити**</span><span class="sxs-lookup"><span data-stu-id="35722-156">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

