---
title: Класс MicrosoftDNS_WINSRType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись WINS Reverse (WINSR).
ms.assetid: e611dc63-838f-4a79-baca-febd27612111
keywords:
- DNS класса MicrosoftDNS_WINSRType
- DNS-MicrosoftDNS_WINSRType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSRType.Modify
- MicrosoftDNS_WINSRType.MappingFlag
- MicrosoftDNS_WINSRType.LookupTimeout
- MicrosoftDNS_WINSRType.CacheTimeout
- MicrosoftDNS_WINSRType.ResultDomain
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9500c6a36a1c3a7cc243f1cbcfbc0edca6cecf2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416077"
---
# <a name="microsoftdns_winsrtype-class"></a><span data-ttu-id="a249b-105">\_Класс микрософтднс винсртипе</span><span class="sxs-lookup"><span data-stu-id="a249b-105">MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="a249b-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись WINS Reverse (WINSR).</span><span class="sxs-lookup"><span data-stu-id="a249b-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a WINS Reverse Look-up (WINSR) record.</span></span>

<span data-ttu-id="a249b-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="a249b-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a249b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a249b-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WINSRType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string ResultDomain;
};
```

## <a name="members"></a><span data-ttu-id="a249b-109">Члены</span><span class="sxs-lookup"><span data-stu-id="a249b-109">Members</span></span>

<span data-ttu-id="a249b-110">Класс **микрософтднс \_ винсртипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a249b-110">The **MicrosoftDNS\_WINSRType** class has these types of members:</span></span>

-   [<span data-ttu-id="a249b-111">Методы</span><span class="sxs-lookup"><span data-stu-id="a249b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a249b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="a249b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a249b-113">Методы</span><span class="sxs-lookup"><span data-stu-id="a249b-113">Methods</span></span>

<span data-ttu-id="a249b-114">Класс **микрософтднс \_ винсртипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a249b-114">The **MicrosoftDNS\_WINSRType** class has these methods.</span></span>



| <span data-ttu-id="a249b-115">Метод</span><span class="sxs-lookup"><span data-stu-id="a249b-115">Method</span></span>                             | <span data-ttu-id="a249b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a249b-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a249b-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="a249b-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="a249b-118">Создает экземпляр типа ресурса WINSR на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца, класс (по умолчанию — IN), значение срока жизни и флаг сопоставления WINS, время ожидания для отмены просмотра, время ожидания кэша WINS и имя домена для добавления.</span><span class="sxs-lookup"><span data-stu-id="a249b-118">Instantiates a WINSR Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="a249b-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="a249b-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="a249b-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="a249b-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="a249b-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="a249b-121">**Modify**</span></span>                         | <span data-ttu-id="a249b-122">Обновляет значения TTL, флага сопоставления, времени ожидания при поиске, истечения времени ожидания кэша и домена результата до значений, указанных в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="a249b-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="a249b-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="a249b-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="a249b-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="a249b-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="a249b-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="a249b-125">Qualifiers: Implemented</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="a249b-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="a249b-126">Properties</span></span>

<span data-ttu-id="a249b-127">Класс **микрософтднс \_ винсртипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a249b-127">The **MicrosoftDNS\_WINSRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a249b-128">**CacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="a249b-128">**CacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a249b-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a249b-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a249b-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a249b-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a249b-131">Время в секундах, в течение которого DNS-сервер, использующий поиск WINS, может кэшировать ответ WINS-сервера.</span><span class="sxs-lookup"><span data-stu-id="a249b-131">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="a249b-132">**лукуптимеаут**</span><span class="sxs-lookup"><span data-stu-id="a249b-132">**LookupTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a249b-133">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a249b-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a249b-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a249b-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a249b-135">Время ожидания (в секундах) для DNS-сервера, использующего обратный поиск WINS.</span><span class="sxs-lookup"><span data-stu-id="a249b-135">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="a249b-136">**маппингфлаг**</span><span class="sxs-lookup"><span data-stu-id="a249b-136">**MappingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a249b-137">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a249b-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a249b-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a249b-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a249b-139">Флаг сопоставления WINSR, указывающий, следует ли включать запись в репликацию зоны.</span><span class="sxs-lookup"><span data-stu-id="a249b-139">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="a249b-140">Он может иметь только два значения: 0x80000000 и 0x00010000, соответствующие флагам репликации и без репликации (локальная запись) соответственно.</span><span class="sxs-lookup"><span data-stu-id="a249b-140">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="a249b-141">**ресултдомаин**</span><span class="sxs-lookup"><span data-stu-id="a249b-141">**ResultDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a249b-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a249b-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a249b-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a249b-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a249b-144">Имя домена, добавляемое к возвращенным NetBIOS-именам.</span><span class="sxs-lookup"><span data-stu-id="a249b-144">Domain name to append to returned NetBIOS names.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a249b-145">Требования</span><span class="sxs-lookup"><span data-stu-id="a249b-145">Requirements</span></span>



| <span data-ttu-id="a249b-146">Требование</span><span class="sxs-lookup"><span data-stu-id="a249b-146">Requirement</span></span> | <span data-ttu-id="a249b-147">Значение</span><span class="sxs-lookup"><span data-stu-id="a249b-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a249b-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a249b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a249b-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a249b-149">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a249b-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a249b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a249b-151">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a249b-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a249b-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a249b-152">Namespace</span></span><br/>                | <span data-ttu-id="a249b-153">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="a249b-153">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a249b-154">MOF</span><span class="sxs-lookup"><span data-stu-id="a249b-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a249b-155"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a249b-155"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a249b-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a249b-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a249b-157">**Метод Креатеинстанцефромпропертидата \_ класса Винсртипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="a249b-157">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="a249b-158">**Метод Modify \_ класса микрософтднс винсртипе**</span><span class="sxs-lookup"><span data-stu-id="a249b-158">**Modify Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="a249b-159">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="a249b-159">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





