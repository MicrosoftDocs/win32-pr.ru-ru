---
title: Класс MicrosoftDNS_WINSType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись службы Windows Internet Name Service (WINS).
ms.assetid: 8f891d80-ee4d-4641-8a6c-159c78e5cf86
keywords:
- DNS класса MicrosoftDNS_WINSType
- DNS-MicrosoftDNS_WINSType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSType.Modify
- MicrosoftDNS_WINSType.MappingFlag
- MicrosoftDNS_WINSType.LookupTimeout
- MicrosoftDNS_WINSType.CacheTimeout
- MicrosoftDNS_WINSType.WinsServers
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce23132073305142948518327ea5b6c7e46f1289
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892217"
---
# <a name="microsoftdns_winstype-class"></a><span data-ttu-id="27353-105">\_Класс микрософтднс винстипе</span><span class="sxs-lookup"><span data-stu-id="27353-105">MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="27353-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись службы Windows Internet Name Service (WINS).</span><span class="sxs-lookup"><span data-stu-id="27353-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Windows Internet Name Service (WINS) record.</span></span>

<span data-ttu-id="27353-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="27353-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="27353-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27353-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WINSType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string WinsServers;
};
```

## <a name="members"></a><span data-ttu-id="27353-109">Члены</span><span class="sxs-lookup"><span data-stu-id="27353-109">Members</span></span>

<span data-ttu-id="27353-110">Класс **микрософтднс \_ винстипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="27353-110">The **MicrosoftDNS\_WINSType** class has these types of members:</span></span>

-   [<span data-ttu-id="27353-111">Методы</span><span class="sxs-lookup"><span data-stu-id="27353-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="27353-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="27353-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="27353-113">Методы</span><span class="sxs-lookup"><span data-stu-id="27353-113">Methods</span></span>

<span data-ttu-id="27353-114">Класс **микрософтднс \_ винстипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="27353-114">The **MicrosoftDNS\_WINSType** class has these methods.</span></span>



| <span data-ttu-id="27353-115">Метод</span><span class="sxs-lookup"><span data-stu-id="27353-115">Method</span></span>                             | <span data-ttu-id="27353-116">Описание</span><span class="sxs-lookup"><span data-stu-id="27353-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27353-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="27353-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="27353-118">Создает экземпляр типа ресурса RR на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца, класс (по умолчанию — IN), значение срока жизни и флаг сопоставления WINS, время ожидания кэша и список IP-адресов для поиска.</span><span class="sxs-lookup"><span data-stu-id="27353-118">Instantiates a WINS Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, look-up time out, cache time out and list of IP addresses for look up.</span></span> <span data-ttu-id="27353-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="27353-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="27353-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="27353-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="27353-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="27353-121">**Modify**</span></span>                         | <span data-ttu-id="27353-122">Обновляет значения TTL, флага сопоставления, времени ожидания при поиске, времени ожидания кэша и WINS-серверов до значений, указанных в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="27353-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Wins Servers to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="27353-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="27353-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="27353-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="27353-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="27353-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="27353-125">Qualifiers: Implemented</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="27353-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="27353-126">Properties</span></span>

<span data-ttu-id="27353-127">Класс **микрософтднс \_ винстипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="27353-127">The **MicrosoftDNS\_WINSType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="27353-128">**CacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="27353-128">**CacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27353-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27353-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27353-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27353-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27353-131">Время в секундах, в течение которого DNS-сервер, использующий поиск WINS, может кэшировать ответ WINS-сервера.</span><span class="sxs-lookup"><span data-stu-id="27353-131">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="27353-132">**лукуптимеаут**</span><span class="sxs-lookup"><span data-stu-id="27353-132">**LookupTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27353-133">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27353-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27353-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27353-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27353-135">Время в секундах, в течение которого DNS-сервер пытается выполнить разрешение с помощью поиска WINS.</span><span class="sxs-lookup"><span data-stu-id="27353-135">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="27353-136">**маппингфлаг**</span><span class="sxs-lookup"><span data-stu-id="27353-136">**MappingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27353-137">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27353-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27353-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27353-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27353-139">Флаг сопоставления WINS, указывающий, следует ли включать запись в репликацию зоны.</span><span class="sxs-lookup"><span data-stu-id="27353-139">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="27353-140">Он может иметь только два значения: 0x80000000 и 0x00010000, соответствующие флагам репликации и без репликации (локальная запись) соответственно.</span><span class="sxs-lookup"><span data-stu-id="27353-140">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="27353-141">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="27353-141">The following values are valid.</span></span>



| <span data-ttu-id="27353-142">Значение</span><span class="sxs-lookup"><span data-stu-id="27353-142">Value</span></span>                                                                                                                                               | <span data-ttu-id="27353-143">Значение</span><span class="sxs-lookup"><span data-stu-id="27353-143">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="27353-144"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="27353-144"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="27353-145">Флаг репликации</span><span class="sxs-lookup"><span data-stu-id="27353-145">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="27353-146"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="27353-146"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="27353-147">Флаг отсутствия репликации (локальная запись)</span><span class="sxs-lookup"><span data-stu-id="27353-147">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="27353-148">**винссерверс**</span><span class="sxs-lookup"><span data-stu-id="27353-148">**WinsServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27353-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="27353-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27353-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27353-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27353-151">Список разделенных запятыми IP-адресов WINS-серверов, используемых при поиске WINS.</span><span class="sxs-lookup"><span data-stu-id="27353-151">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27353-152">Требования</span><span class="sxs-lookup"><span data-stu-id="27353-152">Requirements</span></span>



| <span data-ttu-id="27353-153">Требование</span><span class="sxs-lookup"><span data-stu-id="27353-153">Requirement</span></span> | <span data-ttu-id="27353-154">Значение</span><span class="sxs-lookup"><span data-stu-id="27353-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27353-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27353-155">Minimum supported client</span></span><br/> | <span data-ttu-id="27353-156">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="27353-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="27353-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27353-157">Minimum supported server</span></span><br/> | <span data-ttu-id="27353-158">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="27353-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="27353-159">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="27353-159">Namespace</span></span><br/>                | <span data-ttu-id="27353-160">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="27353-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="27353-161">MOF</span><span class="sxs-lookup"><span data-stu-id="27353-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27353-162"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27353-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27353-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27353-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27353-164">**Метод Креатеинстанцефромпропертидата \_ класса Винстипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="27353-164">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="27353-165">**Метод Modify \_ класса микрософтднс винстипе**</span><span class="sxs-lookup"><span data-stu-id="27353-165">**Modify Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-modify.md)
</dt> <dt>

[<span data-ttu-id="27353-166">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="27353-166">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





