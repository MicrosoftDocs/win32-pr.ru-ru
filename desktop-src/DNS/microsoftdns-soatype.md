---
title: Класс MicrosoftDNS_SOAType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий начальную запись зоны (SOA).
ms.assetid: a5e6b6d3-7f5d-42e2-b3ed-2786f7aafb14
keywords:
- DNS класса MicrosoftDNS_SOAType
- DNS-MicrosoftDNS_SOAType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType
- MicrosoftDNS_SOAType.Modify
- MicrosoftDNS_SOAType.SerialNumber
- MicrosoftDNS_SOAType.PrimaryServer
- MicrosoftDNS_SOAType.ResponsibleParty
- MicrosoftDNS_SOAType.RefreshInterval
- MicrosoftDNS_SOAType.RetryDelay
- MicrosoftDNS_SOAType.ExpireLimit
- MicrosoftDNS_SOAType.MinimumTTL
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a3e7cb617514e2ed7c8692a866cc80dfc639391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071242"
---
# <a name="microsoftdns_soatype-class"></a><span data-ttu-id="51456-105">\_Класс микрософтднс соатипе</span><span class="sxs-lookup"><span data-stu-id="51456-105">MicrosoftDNS\_SOAType class</span></span>

<span data-ttu-id="51456-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий начальную запись зоны (SOA).</span><span class="sxs-lookup"><span data-stu-id="51456-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Start Of Authority (SOA) record.</span></span>

<span data-ttu-id="51456-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="51456-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="51456-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51456-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SOAType : MicrosoftDNS_ResourceRecord
{
  uint32 SerialNumber;
  string PrimaryServer;
  string ResponsibleParty;
  uint32 RefreshInterval;
  uint32 RetryDelay;
  uint32 ExpireLimit;
  uint32 MinimumTTL;
};
```

## <a name="members"></a><span data-ttu-id="51456-109">Члены</span><span class="sxs-lookup"><span data-stu-id="51456-109">Members</span></span>

<span data-ttu-id="51456-110">Класс **микрософтднс \_ соатипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="51456-110">The **MicrosoftDNS\_SOAType** class has these types of members:</span></span>

-   [<span data-ttu-id="51456-111">Методы</span><span class="sxs-lookup"><span data-stu-id="51456-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="51456-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="51456-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="51456-113">Методы</span><span class="sxs-lookup"><span data-stu-id="51456-113">Methods</span></span>

<span data-ttu-id="51456-114">Класс **микрософтднс \_ соатипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="51456-114">The **MicrosoftDNS\_SOAType** class has these methods.</span></span>



| <span data-ttu-id="51456-115">Метод</span><span class="sxs-lookup"><span data-stu-id="51456-115">Method</span></span>     | <span data-ttu-id="51456-116">Описание</span><span class="sxs-lookup"><span data-stu-id="51456-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51456-117">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="51456-117">**Modify**</span></span> | <span data-ttu-id="51456-118">Обновляет значение TTL, серийный номер SOA, сервер-источник, ответственный субъект, интервал обновления, задержку повтора, ограничение срока действия и минимальный срок жизни (для зоны) на значения, указанные в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="51456-118">Updates the TTL, SOA Serial Number, Primary Server, Responsible Party, Refresh Interval, Retry Delay, Expire Limit and Minimum TTL (for the zone) to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="51456-119">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="51456-119">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="51456-120">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="51456-120">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="51456-121">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="51456-121">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="51456-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="51456-122">Properties</span></span>

<span data-ttu-id="51456-123">Класс **микрософтднс \_ соатипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="51456-123">The **MicrosoftDNS\_SOAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51456-124">**експирелимит**</span><span class="sxs-lookup"><span data-stu-id="51456-124">**ExpireLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51456-125">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51456-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51456-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="51456-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51456-127">Время в секундах перед неотвечающей зоной больше не является полномочным.</span><span class="sxs-lookup"><span data-stu-id="51456-127">Time, in seconds, before an unresponsive zone is no longer authoritative.</span></span>

</dd> <dt>

<span data-ttu-id="51456-128">**минимумттл**</span><span class="sxs-lookup"><span data-stu-id="51456-128">**MinimumTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51456-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51456-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51456-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="51456-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51456-131">Нижний предел времени в секундах, в течение которого DNS-сервер или сопоставитель кэширования могут кэшировать любую запись ресурса из зоны, к которой принадлежит эта запись.</span><span class="sxs-lookup"><span data-stu-id="51456-131">Lower limit on the time, in seconds, that a DNS Server or Caching resolver are allowed to cache any resource record from the zone to which this record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="51456-132">**Сервер**</span><span class="sxs-lookup"><span data-stu-id="51456-132">**PrimaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51456-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="51456-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51456-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="51456-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51456-135">Полномочный DNS-сервер для зоны, к которой принадлежит запись.</span><span class="sxs-lookup"><span data-stu-id="51456-135">Authoritative DNS Server for the zone to which the record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="51456-136">**RefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="51456-136">**RefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51456-137">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51456-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51456-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="51456-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51456-139">Время в секундах до обновления зоны, содержащей эту запись.</span><span class="sxs-lookup"><span data-stu-id="51456-139">Time, in seconds, before the zone containing this record should be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="51456-140">**респонсиблепарти**</span><span class="sxs-lookup"><span data-stu-id="51456-140">**ResponsibleParty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51456-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="51456-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51456-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="51456-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51456-143">Имя ответственного лица для зоны, к которой принадлежит запись.</span><span class="sxs-lookup"><span data-stu-id="51456-143">Name of the responsible party for the zone to which the record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="51456-144">**ретриделай**</span><span class="sxs-lookup"><span data-stu-id="51456-144">**RetryDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51456-145">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51456-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51456-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="51456-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51456-147">Время в секундах перед повторной попыткой неудачного обновления зоны, к которой принадлежит эта запись.</span><span class="sxs-lookup"><span data-stu-id="51456-147">Time, in seconds, before retrying a failed refresh of the zone to which this record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="51456-148">**Номер**</span><span class="sxs-lookup"><span data-stu-id="51456-148">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51456-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51456-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51456-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="51456-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51456-151">Серийный номер записи SOA.</span><span class="sxs-lookup"><span data-stu-id="51456-151">Serial number of the SOA record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51456-152">Требования</span><span class="sxs-lookup"><span data-stu-id="51456-152">Requirements</span></span>



| <span data-ttu-id="51456-153">Требование</span><span class="sxs-lookup"><span data-stu-id="51456-153">Requirement</span></span> | <span data-ttu-id="51456-154">Значение</span><span class="sxs-lookup"><span data-stu-id="51456-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51456-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51456-155">Minimum supported client</span></span><br/> | <span data-ttu-id="51456-156">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="51456-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="51456-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51456-157">Minimum supported server</span></span><br/> | <span data-ttu-id="51456-158">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="51456-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="51456-159">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="51456-159">Namespace</span></span><br/>                | <span data-ttu-id="51456-160">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="51456-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="51456-161">MOF</span><span class="sxs-lookup"><span data-stu-id="51456-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51456-162"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51456-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51456-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51456-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51456-164">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="51456-164">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="51456-165">**Метод Modify \_ класса микрософтднс соатипе**</span><span class="sxs-lookup"><span data-stu-id="51456-165">**Modify Method of the MicrosoftDNS\_SOAType Class**</span></span>](microsoftdns-soatype-modify.md)
</dt> </dl>

 

 





