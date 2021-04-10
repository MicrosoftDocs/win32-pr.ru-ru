---
description: Определяет стандартные, конкретные и универсальные права. Эти права используются в записях управления доступом (ACE) и являются основным средством указания запрошенного или предоставленного доступа к объекту.
ms.assetid: f115ee54-3333-4109-8004-d71904a7a943
title: ACCESS_MASK (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d10d9e8db246c2705911cc57221400f40da014d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156295"
---
# <a name="access_mask"></a><span data-ttu-id="c7aca-104">\_Маска доступа</span><span class="sxs-lookup"><span data-stu-id="c7aca-104">ACCESS\_MASK</span></span>

<span data-ttu-id="c7aca-105">Тип **данных \_ Mask доступа** — это значение типа **DWORD** , определяющее стандартные, конкретные и универсальные права.</span><span class="sxs-lookup"><span data-stu-id="c7aca-105">The **ACCESS\_MASK** data type is a **DWORD** value that defines standard, specific, and generic rights.</span></span> <span data-ttu-id="c7aca-106">Эти права используются в [*записях управления доступом*](/windows/desktop/SecGloss/a-gly) (ACE) и являются основным средством указания запрошенного или предоставленного доступа к объекту.</span><span class="sxs-lookup"><span data-stu-id="c7aca-106">These rights are used in [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) and are the primary means of specifying the requested or granted access to an object.</span></span>


```C++
typedef DWORD ACCESS_MASK;
typedef ACCESS_MASK* PACCESS_MASK;
```



## <a name="remarks"></a><span data-ttu-id="c7aca-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7aca-107">Remarks</span></span>

<span data-ttu-id="c7aca-108">Биты в этом значении выделяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="c7aca-108">The bits in this value are allocated as follows.</span></span>



| <span data-ttu-id="c7aca-109">Bits</span><span class="sxs-lookup"><span data-stu-id="c7aca-109">Bits</span></span>             | <span data-ttu-id="c7aca-110">Значение</span><span class="sxs-lookup"><span data-stu-id="c7aca-110">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7aca-111">0 15</span><span class="sxs-lookup"><span data-stu-id="c7aca-111">0 15</span></span><br/>  | <span data-ttu-id="c7aca-112">Определенные права.</span><span class="sxs-lookup"><span data-stu-id="c7aca-112">Specific rights.</span></span> <span data-ttu-id="c7aca-113">Содержит маску доступа, относящуюся к типу объекта, связанному с маской.</span><span class="sxs-lookup"><span data-stu-id="c7aca-113">Contains the access mask specific to the object type associated with the mask.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="c7aca-114">16 23</span><span class="sxs-lookup"><span data-stu-id="c7aca-114">16 23</span></span><br/> | <span data-ttu-id="c7aca-115">Стандартные права.</span><span class="sxs-lookup"><span data-stu-id="c7aca-115">Standard rights.</span></span> <span data-ttu-id="c7aca-116">Содержит стандартные права доступа объекта.</span><span class="sxs-lookup"><span data-stu-id="c7aca-116">Contains the object's standard access rights.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="c7aca-117">24</span><span class="sxs-lookup"><span data-stu-id="c7aca-117">24</span></span><br/>    | <span data-ttu-id="c7aca-118">Доступ к безопасности системы (**доступ к \_ системе \_ безопасности системы**).</span><span class="sxs-lookup"><span data-stu-id="c7aca-118">Access system security (**ACCESS\_SYSTEM\_SECURITY**).</span></span> <span data-ttu-id="c7aca-119">Он используется для указания доступа к [*системному списку управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="c7aca-119">It is used to indicate access to a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="c7aca-120">Этот тип доступа требует, чтобы вызывающий процесс имел привилегии **\_ безопасности \_ SE** (Управление аудитом и журналом безопасности).</span><span class="sxs-lookup"><span data-stu-id="c7aca-120">This type of access requires the calling process to have the **SE\_SECURITY\_NAME** (Manage auditing and security log) privilege.</span></span> <span data-ttu-id="c7aca-121">Если этот флаг установлен в маске доступа ACE аудита доступа (успешный или неуспешный доступ), аудит доступа к SACL будет проводиться.</span><span class="sxs-lookup"><span data-stu-id="c7aca-121">If this flag is set in the access mask of an audit access ACE (successful or unsuccessful access), the SACL access will be audited.</span></span><br/> |
| <span data-ttu-id="c7aca-122">25</span><span class="sxs-lookup"><span data-stu-id="c7aca-122">25</span></span><br/>    | <span data-ttu-id="c7aca-123">Максимально допустимое (максимально допустимое).**\_**</span><span class="sxs-lookup"><span data-stu-id="c7aca-123">Maximum allowed (**MAXIMUM\_ALLOWED**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c7aca-124">26 27</span><span class="sxs-lookup"><span data-stu-id="c7aca-124">26 27</span></span><br/> | <span data-ttu-id="c7aca-125">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="c7aca-125">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="c7aca-126">28</span><span class="sxs-lookup"><span data-stu-id="c7aca-126">28</span></span><br/>    | <span data-ttu-id="c7aca-127">Универсальные все (**универсальные \_ все**).</span><span class="sxs-lookup"><span data-stu-id="c7aca-127">Generic all (**GENERIC\_ALL**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="c7aca-128">29</span><span class="sxs-lookup"><span data-stu-id="c7aca-128">29</span></span><br/>    | <span data-ttu-id="c7aca-129">Универсальное выполнение (**универсальное \_ выполнение**).</span><span class="sxs-lookup"><span data-stu-id="c7aca-129">Generic execute (**GENERIC\_EXECUTE**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c7aca-130">30</span><span class="sxs-lookup"><span data-stu-id="c7aca-130">30</span></span><br/>    | <span data-ttu-id="c7aca-131">Универсальная запись (**Универсальная \_ запись**).</span><span class="sxs-lookup"><span data-stu-id="c7aca-131">Generic write (**GENERIC\_WRITE**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="c7aca-132">31</span><span class="sxs-lookup"><span data-stu-id="c7aca-132">31</span></span><br/>    | <span data-ttu-id="c7aca-133">Универсальное чтение (**универсальное \_ Чтение**).</span><span class="sxs-lookup"><span data-stu-id="c7aca-133">Generic read (**GENERIC\_READ**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

<span data-ttu-id="c7aca-134">Биты стандартных прав, 16 – 23, содержат стандартные права доступа объекта и могут быть сочетанием следующих предопределенных флагов.</span><span class="sxs-lookup"><span data-stu-id="c7aca-134">Standard rights bits, 16 to 23, contain the object's standard access rights and can be a combination of the following predefined flags.</span></span>



| <span data-ttu-id="c7aca-135">bit</span><span class="sxs-lookup"><span data-stu-id="c7aca-135">Bit</span></span>           | <span data-ttu-id="c7aca-136">Flag</span><span class="sxs-lookup"><span data-stu-id="c7aca-136">Flag</span></span>                         | <span data-ttu-id="c7aca-137">Значение</span><span class="sxs-lookup"><span data-stu-id="c7aca-137">Meaning</span></span>                                                                                                                                                                                                                                  |
|---------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7aca-138">16</span><span class="sxs-lookup"><span data-stu-id="c7aca-138">16</span></span><br/> | <span data-ttu-id="c7aca-139">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="c7aca-139">**DELETE**</span></span><br/>        | <span data-ttu-id="c7aca-140">Удаление доступа.</span><span class="sxs-lookup"><span data-stu-id="c7aca-140">Delete access.</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="c7aca-141">17</span><span class="sxs-lookup"><span data-stu-id="c7aca-141">17</span></span><br/> | <span data-ttu-id="c7aca-142">**\_Контроль чтения**</span><span class="sxs-lookup"><span data-stu-id="c7aca-142">**READ\_CONTROL**</span></span><br/> | <span data-ttu-id="c7aca-143">Доступ на чтение для владельца, группы и [*списка управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="c7aca-143">Read access to the owner, group, and [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of the security descriptor.</span></span><br/> |
| <span data-ttu-id="c7aca-144">18</span><span class="sxs-lookup"><span data-stu-id="c7aca-144">18</span></span><br/> | <span data-ttu-id="c7aca-145">**ЗАПИСЬ \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="c7aca-145">**WRITE\_DAC**</span></span><br/>    | <span data-ttu-id="c7aca-146">Доступ на запись к DACL.</span><span class="sxs-lookup"><span data-stu-id="c7aca-146">Write access to the DACL.</span></span><br/>                                                                                                                                                                                                     |
| <span data-ttu-id="c7aca-147">19</span><span class="sxs-lookup"><span data-stu-id="c7aca-147">19</span></span><br/> | <span data-ttu-id="c7aca-148">**\_владелец записи**</span><span class="sxs-lookup"><span data-stu-id="c7aca-148">**WRITE\_OWNER**</span></span><br/>  | <span data-ttu-id="c7aca-149">Доступ на запись для владельца.</span><span class="sxs-lookup"><span data-stu-id="c7aca-149">Write access to owner.</span></span><br/>                                                                                                                                                                                                        |
| <span data-ttu-id="c7aca-150">20</span><span class="sxs-lookup"><span data-stu-id="c7aca-150">20</span></span><br/> | <span data-ttu-id="c7aca-151">**SYNCHRONIZE**</span><span class="sxs-lookup"><span data-stu-id="c7aca-151">**SYNCHRONIZE**</span></span><br/>   | <span data-ttu-id="c7aca-152">Синхронизация доступа.</span><span class="sxs-lookup"><span data-stu-id="c7aca-152">Synchronize access.</span></span><br/>                                                                                                                                                                                                           |



 

<span data-ttu-id="c7aca-153">Следующие константы, определенные в Winnt. h, представляют конкретные и стандартные права доступа.</span><span class="sxs-lookup"><span data-stu-id="c7aca-153">The following constants defined in Winnt.h represent the specific and standard access rights.</span></span>


```C++
#define DELETE                           (0x00010000L)
#define READ_CONTROL                     (0x00020000L)
#define WRITE_DAC                        (0x00040000L)
#define WRITE_OWNER                      (0x00080000L)
#define SYNCHRONIZE                      (0x00100000L)

#define STANDARD_RIGHTS_REQUIRED         (0x000F0000L)

#define STANDARD_RIGHTS_READ             (READ_CONTROL)
#define STANDARD_RIGHTS_WRITE            (READ_CONTROL)
#define STANDARD_RIGHTS_EXECUTE          (READ_CONTROL)

#define STANDARD_RIGHTS_ALL              (0x001F0000L)

#define SPECIFIC_RIGHTS_ALL              (0x0000FFFFL)
```



## <a name="requirements"></a><span data-ttu-id="c7aca-154">Требования</span><span class="sxs-lookup"><span data-stu-id="c7aca-154">Requirements</span></span>



| <span data-ttu-id="c7aca-155">Требование</span><span class="sxs-lookup"><span data-stu-id="c7aca-155">Requirement</span></span> | <span data-ttu-id="c7aca-156">Значение</span><span class="sxs-lookup"><span data-stu-id="c7aca-156">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7aca-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7aca-157">Minimum supported client</span></span><br/> | <span data-ttu-id="c7aca-158">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c7aca-158">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c7aca-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7aca-159">Minimum supported server</span></span><br/> | <span data-ttu-id="c7aca-160">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c7aca-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c7aca-161">Header</span><span class="sxs-lookup"><span data-stu-id="c7aca-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7aca-162"><dt>Файл Winnt. h (включая Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7aca-162"><dt>Winnt.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7aca-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7aca-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7aca-164">Управление доступом</span><span class="sxs-lookup"><span data-stu-id="c7aca-164">Access Control</span></span>](access-control.md)
</dt> <dt>

[<span data-ttu-id="c7aca-165">Основные структуры управления доступом</span><span class="sxs-lookup"><span data-stu-id="c7aca-165">Basic Access Control Structures</span></span>](authorization-structures.md)
</dt> <dt>

[<span data-ttu-id="c7aca-166">Права доступа и маски доступа</span><span class="sxs-lookup"><span data-stu-id="c7aca-166">Access Rights and Access Masks</span></span>](access-rights-and-access-masks.md)
</dt> <dt>

[<span data-ttu-id="c7aca-167">**УНИВЕРСАЛЬНое \_ сопоставление**</span><span class="sxs-lookup"><span data-stu-id="c7aca-167">**GENERIC\_MAPPING**</span></span>](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)
</dt> </dl>

 

