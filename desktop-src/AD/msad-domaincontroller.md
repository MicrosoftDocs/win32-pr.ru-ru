---
title: Класс MSAD_DomainController
description: Представляет контроллер домена (DC), на котором работает поставщик WMI.
ms.assetid: a7671967-79d7-48f8-8869-dd65272e2ed2
ms.tgt_platform: multiple
keywords:
- Класс MSAD_DomainController Active Directory
- Active Directory класса MSAD_DomainController, описание
topic_type:
- apiref
api_name:
- MSAD_DomainController
- MSAD_DomainController.DistinguishedName
- MSAD_DomainController.CommonName
- MSAD_DomainController.SiteName
- MSAD_DomainController.NTDsaGUID
- MSAD_DomainController.IsGC
- MSAD_DomainController.TimeOfOldestReplSync
- MSAD_DomainController.TimeOfOldestReplAdd
- MSAD_DomainController.TimeOfOldestReplDel
- MSAD_DomainController.TimeOfOldestReplMod
- MSAD_DomainController.TimeOfOldestReplUpdRefs
- MSAD_DomainController.IsNextRIDPoolAvailable
- MSAD_DomainController.PercentOfRIDsLeft
- MSAD_DomainController.IsRegisteredInDNS
- MSAD_DomainController.IsAdvertisingToLocator
- MSAD_DomainController.IsSysVolReady
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303071d3d268953687bc387709c74531f8b40584
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490740"
---
# <a name="msad_domaincontroller-class"></a><span data-ttu-id="3fce3-105">Класс МСАДного \_ класса (DomainController)</span><span class="sxs-lookup"><span data-stu-id="3fce3-105">MSAD\_DomainController class</span></span>

<span data-ttu-id="3fce3-106">Представляет контроллер домена (DC), на котором работает поставщик WMI.</span><span class="sxs-lookup"><span data-stu-id="3fce3-106">Represents the domain controller (DC) on which the WMI provider is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fce3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3fce3-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class  MSAD_DomainController
{
  String   DistinguishedName;
  String   CommonName;
  String   SiteName;
  String   NTDsaGUID;
  boolean  IsGC = FALSE;
  datetime TimeOfOldestReplSync;
  datetime TimeOfOldestReplAdd;
  datetime TimeOfOldestReplDel;
  datetime TimeOfOldestReplMod;
  datetime TimeOfOldestReplUpdRefs;
  boolean  IsNextRIDPoolAvailable = FALSE;
  uint32   PercentOfRIDsLeft;
  boolean  IsRegisteredInDNS;
  boolean  IsAdvertisingToLocator = FALSE;
  boolean  IsSysVolReady = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="3fce3-108">Члены</span><span class="sxs-lookup"><span data-stu-id="3fce3-108">Members</span></span>

<span data-ttu-id="3fce3-109">Класс **\_ DomainController МСАД** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3fce3-109">The **MSAD\_DomainController** class has these types of members:</span></span>

-   [<span data-ttu-id="3fce3-110">Методы</span><span class="sxs-lookup"><span data-stu-id="3fce3-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="3fce3-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="3fce3-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3fce3-112">Методы</span><span class="sxs-lookup"><span data-stu-id="3fce3-112">Methods</span></span>

<span data-ttu-id="3fce3-113">Класс **\_ DomainController МСАД** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="3fce3-113">The **MSAD\_DomainController** class has these methods.</span></span>



| <span data-ttu-id="3fce3-114">Метод</span><span class="sxs-lookup"><span data-stu-id="3fce3-114">Method</span></span>                                                 | <span data-ttu-id="3fce3-115">Описание</span><span class="sxs-lookup"><span data-stu-id="3fce3-115">Description</span></span>                                                                              |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fce3-116">**ексекутеккк**</span><span class="sxs-lookup"><span data-stu-id="3fce3-116">**ExecuteKCC**</span></span>](executekcc-msad-domaincontroller.md) | <span data-ttu-id="3fce3-117">Вызывает средство проверки согласованности знаний для проверки топологии репликации.</span><span class="sxs-lookup"><span data-stu-id="3fce3-117">Invokes the Knowledge Consistency Checker to verify the replication topology.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3fce3-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="3fce3-118">Properties</span></span>

<span data-ttu-id="3fce3-119">Класс **\_ DomainController МСАД** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3fce3-119">The **MSAD\_DomainController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3fce3-120">**CommonName**</span><span class="sxs-lookup"><span data-stu-id="3fce3-120">**CommonName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fce3-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3fce3-121">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="3fce3-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fce3-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fce3-123">Возвращает общее имя объекта сервера.</span><span class="sxs-lookup"><span data-stu-id="3fce3-123">Gets the common name of the server object.</span></span>

</dd> <dt>

<span data-ttu-id="3fce3-124">**DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="3fce3-124">**DistinguishedName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fce3-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3fce3-125">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="3fce3-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fce3-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fce3-127">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3fce3-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3fce3-128">Возвращает путь X. 500 объекта [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) .</span><span class="sxs-lookup"><span data-stu-id="3fce3-128">Gets the X.500 path of the [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) object.</span></span>

</dd> <dt>

<span data-ttu-id="3fce3-129">**исадвертисингтолокатор**</span><span class="sxs-lookup"><span data-stu-id="3fce3-129">**IsAdvertisingToLocator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fce3-130">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3fce3-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3fce3-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fce3-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fce3-132">Возвращает значение, указывающее, правильно ли объявлена служба локатора на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="3fce3-132">Gets the value that indicates whether the locator service on the DC is advertising correctly.</span></span> <span data-ttu-id="3fce3-133">**Значение true** , если служба локатора на КОНТРОЛЛЕРе домена объявляется правильно; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3fce3-133">**TRUE** if the locator service on the DC is advertising correctly; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="3fce3-134">**исгк**</span><span class="sxs-lookup"><span data-stu-id="3fce3-134">**IsGC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fce3-135">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3fce3-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3fce3-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fce3-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fce3-137">Возвращает значение, указывающее, является ли контроллер домена сервером глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="3fce3-137">Gets the value that indicates whether the DC is a Global Catalog server.</span></span> <span data-ttu-id="3fce3-138">**Значение true** , если контроллер домена является сервером глобального каталога; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3fce3-138">**TRUE** if the DC is a Global Catalog server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="3fce3-139">**иснекстридпулаваилабле**</span><span class="sxs-lookup"><span data-stu-id="3fce3-139">**IsNextRIDPoolAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fce3-140">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3fce3-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3fce3-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fce3-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fce3-142">Возвращает значение, указывающее, получил ли контроллер домена другой пул RID.</span><span class="sxs-lookup"><span data-stu-id="3fce3-142">Gets the value that indicates whether the DC has obtained another RID pool.</span></span> <span data-ttu-id="3fce3-143">**Значение true** , если контроллер домена получил другой пул RID и выделение идентификаторов RID на этом контроллере домена может продолжаться даже в том случае, если текущий пул идентификаторов RID исчерпан. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3fce3-143">**TRUE** if the DC has obtained another RID pool and allocation of RIDs on this DC can continue even if the current pool of RIDs is exhausted; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="3fce3-144">**исрегистерединднс**</span><span class="sxs-lookup"><span data-stu-id="3fce3-144">**IsRegisteredInDNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fce3-145">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3fce3-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3fce3-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fce3-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fce3-147">Возвращает значение, указывающее, правильно ли зарегистрирован контроллер домена в DNS.</span><span class="sxs-lookup"><span data-stu-id="3fce3-147">Gets the value that indicates whether the DC is registered correctly in DNS.</span></span> <span data-ttu-id="3fce3-148">**Значение true** , если контроллер домена правильно зарегистрирован в DNS; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3fce3-148">**TRUE** if the DC is registered correctly in DNS; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="3fce3-149">**иссисволреади**</span><span class="sxs-lookup"><span data-stu-id="3fce3-149">**IsSysVolReady**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fce3-150">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3fce3-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3fce3-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fce3-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fce3-152">Возвращает значение, указывающее, правильно ли Опубликовано SysVol.</span><span class="sxs-lookup"><span data-stu-id="3fce3-152">Gets the value that indicates whether the SysVol has published correctly.</span></span> <span data-ttu-id="3fce3-153">**Значение true** , если SYSVOL опубликован правильно; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3fce3-153">**TRUE** if the SysVol has published correctly; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="3fce3-154">**нтдсагуид**</span><span class="sxs-lookup"><span data-stu-id="3fce3-154">**NTDsaGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fce3-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3fce3-155">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="3fce3-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fce3-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fce3-157">Возвращает идентификатор GUID, связанный с объектом [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) в контейнере конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3fce3-157">Gets the GUID that is associated with the [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) object in the configuration container.</span></span> <span data-ttu-id="3fce3-158">Объект **NTDS-DSA** представляет процесс домен Active Directory службы DSA на сервере.</span><span class="sxs-lookup"><span data-stu-id="3fce3-158">The **NTDS-DSA** object represents the Active Directory Domain Service DSA process on the server.</span></span>

</dd> <dt>

<span data-ttu-id="3fce3-159">**перцентофридслефт**</span><span class="sxs-lookup"><span data-stu-id="3fce3-159">**PercentOfRIDsLeft**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fce3-160">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3fce3-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3fce3-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fce3-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fce3-162">Возвращает процент идентификаторов RID, оставшихся в текущем пуле RID на этом контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="3fce3-162">Gets the percentage of RIDs that are left in the current RID pool on this DC.</span></span>

</dd> <dt>

<span data-ttu-id="3fce3-163">**Значением**</span><span class="sxs-lookup"><span data-stu-id="3fce3-163">**SiteName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fce3-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3fce3-164">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="3fce3-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fce3-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fce3-166">Возвращает сайт, на котором существует контроллер домена.</span><span class="sxs-lookup"><span data-stu-id="3fce3-166">Gets the site in which the DC exists.</span></span>

</dd> <dt>

<span data-ttu-id="3fce3-167">**тимеофолдестрепладд**</span><span class="sxs-lookup"><span data-stu-id="3fce3-167">**TimeOfOldestReplAdd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fce3-168">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3fce3-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3fce3-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fce3-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fce3-170">Получает метку времени самой старой операции добавления репликации, которая все еще находится в очереди на этом контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="3fce3-170">Gets the timestamp of the oldest replication add operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="3fce3-171">**тимеофолдестреплдел**</span><span class="sxs-lookup"><span data-stu-id="3fce3-171">**TimeOfOldestReplDel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fce3-172">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3fce3-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3fce3-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fce3-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fce3-174">Получает метку времени самой старой операции удаления репликации, которая все еще находится в очереди на этом контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="3fce3-174">Gets the timestamp of the oldest replication delete operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="3fce3-175">**тимеофолдестреплмод**</span><span class="sxs-lookup"><span data-stu-id="3fce3-175">**TimeOfOldestReplMod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fce3-176">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3fce3-176">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3fce3-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fce3-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fce3-178">Получает метку времени самой старой операции изменения репликации, которая все еще находится в очереди на этом контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="3fce3-178">Gets the timestamp of the oldest replication modify operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="3fce3-179">**тимеофолдестреплсинк**</span><span class="sxs-lookup"><span data-stu-id="3fce3-179">**TimeOfOldestReplSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fce3-180">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3fce3-180">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3fce3-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fce3-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fce3-182">Получает метку времени самой старой операции синхронизации репликации, которая все еще находится в очереди на этом контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="3fce3-182">Gets the timestamp of the oldest replication sync operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="3fce3-183">**тимеофолдестреплупдрефс**</span><span class="sxs-lookup"><span data-stu-id="3fce3-183">**TimeOfOldestReplUpdRefs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fce3-184">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3fce3-184">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3fce3-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fce3-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fce3-186">Получает метку времени самой старой операции обновления репликации, которая все еще находится в очереди на этом контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="3fce3-186">Gets the timestamp of the oldest replication update operation that is still in the queue on this domain controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3fce3-187">Требования</span><span class="sxs-lookup"><span data-stu-id="3fce3-187">Requirements</span></span>



| <span data-ttu-id="3fce3-188">Требование</span><span class="sxs-lookup"><span data-stu-id="3fce3-188">Requirement</span></span> | <span data-ttu-id="3fce3-189">Значение</span><span class="sxs-lookup"><span data-stu-id="3fce3-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fce3-190">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3fce3-190">Minimum supported client</span></span><br/> | <span data-ttu-id="3fce3-191">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3fce3-191">None supported</span></span><br/>                                                               |
| <span data-ttu-id="3fce3-192">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3fce3-192">Minimum supported server</span></span><br/> | <span data-ttu-id="3fce3-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3fce3-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3fce3-194">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3fce3-194">Namespace</span></span><br/>                | <span data-ttu-id="3fce3-195">Корневой \\ микрософтактиведиректори</span><span class="sxs-lookup"><span data-stu-id="3fce3-195">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="3fce3-196">MOF</span><span class="sxs-lookup"><span data-stu-id="3fce3-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fce3-197"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3fce3-197"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fce3-198">DLL</span><span class="sxs-lookup"><span data-stu-id="3fce3-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fce3-199"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fce3-199"><dt>Replprov.dll</dt></span></span> </dl> |



 

