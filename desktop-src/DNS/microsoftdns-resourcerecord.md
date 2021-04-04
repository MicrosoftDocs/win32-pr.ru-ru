---
title: Класс MicrosoftDNS_ResourceRecord
description: Класс Микрософтднс \_ ресаурцерекорд представляет общие свойства записи ресурса DNS. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 84d6d106-fcc9-44ae-8db2-181c60489aec
keywords:
- DNS класса MicrosoftDNS_ResourceRecord
- DNS-MicrosoftDNS_ResourceRecord класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
- MicrosoftDNS_ResourceRecord.DnsServerName
- MicrosoftDNS_ResourceRecord.ContainerName
- MicrosoftDNS_ResourceRecord.DomainName
- MicrosoftDNS_ResourceRecord.OwnerName
- MicrosoftDNS_ResourceRecord.RecordClass 1
- MicrosoftDNS_ResourceRecord.TTL
- MicrosoftDNS_ResourceRecord.TimeStamp
- MicrosoftDNS_ResourceRecord.RecordData
- MicrosoftDNS_ResourceRecord.TextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe546ceabb5590ccd4907448af5efd5e2d4fe2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988809"
---
# <a name="microsoftdns_resourcerecord-class"></a><span data-ttu-id="a9ea3-105">\_Класс микрософтднс ресаурцерекорд</span><span class="sxs-lookup"><span data-stu-id="a9ea3-105">MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="a9ea3-106">Класс **микрософтднс \_ ресаурцерекорд** представляет общие свойства записи ресурса DNS.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-106">The **MicrosoftDNS\_ResourceRecord** class represents the general properties of a DNS RR.</span></span>

<span data-ttu-id="a9ea3-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9ea3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9ea3-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ResourceRecord : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string DomainName;
  string OwnerName;
  uint16 RecordClass=1;
  uint32 TTL;
  uint32 TimeStamp;
  string RecordData;
  string TextRepresentation;
};
```

## <a name="members"></a><span data-ttu-id="a9ea3-109">Члены</span><span class="sxs-lookup"><span data-stu-id="a9ea3-109">Members</span></span>

<span data-ttu-id="a9ea3-110">Класс **микрософтднс \_ ресаурцерекорд** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a9ea3-110">The **MicrosoftDNS\_ResourceRecord** class has these types of members:</span></span>

-   [<span data-ttu-id="a9ea3-111">Методы</span><span class="sxs-lookup"><span data-stu-id="a9ea3-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a9ea3-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="a9ea3-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a9ea3-113">Методы</span><span class="sxs-lookup"><span data-stu-id="a9ea3-113">Methods</span></span>

<span data-ttu-id="a9ea3-114">Класс **микрософтднс \_ ресаурцерекорд** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-114">The **MicrosoftDNS\_ResourceRecord** class has these methods.</span></span>



| <span data-ttu-id="a9ea3-115">Метод</span><span class="sxs-lookup"><span data-stu-id="a9ea3-115">Method</span></span>                                   | <span data-ttu-id="a9ea3-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a9ea3-116">Description</span></span>                                                                                                                                                                                                                                                            |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ea3-117">**креатеинстанцефромтекстрепресентатион**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-117">**CreateInstanceFromTextRepresentation**</span></span> | <span data-ttu-id="a9ea3-118">Анализирует запись ресурса в строке Текстрепресентатион, а также с входными DNS-сервером и именами контейнеров, определяет и создает объект Ресаурцерекорд.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-118">Parses the RR in the TextRepresentation string, and with the input DNS Server and Container Names, defines, and instantiates a ResourceRecord object.</span></span> <span data-ttu-id="a9ea3-119">Метод возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-119">The method returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="a9ea3-120">Квалификаторы: нет</span><span class="sxs-lookup"><span data-stu-id="a9ea3-120">Qualifiers: None</span></span><br/> |
| <span data-ttu-id="a9ea3-121">**жетобжектбитекстрепресентатион**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-121">**GetObjectByTextRepresentation**</span></span>        | <span data-ttu-id="a9ea3-122">Извлекает существующий экземпляр \_ подкласса микрософтднс ресаурцерекорд, представленный строкой текстрепресентатион вместе с DNS-сервером и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-122">Retrieves an existing instance of the MicrosoftDns\_ResourceRecord subclass, represented by the TextRepresentation string along with the DNS Server and Container Name.</span></span> <br/> <span data-ttu-id="a9ea3-123">Квалификаторы: нет</span><span class="sxs-lookup"><span data-stu-id="a9ea3-123">Qualifiers: None</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="a9ea3-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="a9ea3-124">Properties</span></span>

<span data-ttu-id="a9ea3-125">Класс **микрософтднс \_ ресаурцерекорд** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-125">The **MicrosoftDNS\_ResourceRecord** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9ea3-126">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-126">**ContainerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ea3-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ea3-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9ea3-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ea3-129">Указывает имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-129">Indicates the name of the Container for the Zone, Cache, or RootHints instance that contains the RR.</span></span>

</dd> <dt>

<span data-ttu-id="a9ea3-130">**днссервернаме**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-130">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ea3-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ea3-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9ea3-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ea3-133">Указывает полное доменное имя (FQDN) или IP-адрес DNS-сервера, содержащего запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-133">Indicates the FQDN or IP address of the DNS Server that contains the RR.</span></span>

</dd> <dt>

<span data-ttu-id="a9ea3-134">**Имя_домена**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-134">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ea3-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ea3-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9ea3-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ea3-137">Представляет полное доменное имя домена, содержащего запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-137">Represents the FQDN of the Domain that contains the RR.</span></span> <span data-ttu-id="a9ea3-138">Это свойство может содержать строки \\ .. Кэш \\ или \\ .. Русинтс \\ , если внутренний кэш или русинтс содержит запись ресурса соответственно.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-138">This property may contain the strings \\..Cache\\ or \\..RootHints\\ if the internal cache or RootHints contain the RR, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="a9ea3-139">**OwnerName**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-139">**OwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ea3-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ea3-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9ea3-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ea3-142">Имя владельца для записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-142">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="a9ea3-143">**Рекордкласс = 1**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-143">**RecordClass=1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ea3-144">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9ea3-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9ea3-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ea3-146">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="a9ea3-146">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="a9ea3-147">Эта строка представляет класс записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-147">This string represents the class of the Resource Record.</span></span> <span data-ttu-id="a9ea3-148">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="a9ea3-148">Valid values include:</span></span>

<span data-ttu-id="a9ea3-149">1: в (Интернет)</span><span class="sxs-lookup"><span data-stu-id="a9ea3-149">1: IN (Internet)</span></span>

<span data-ttu-id="a9ea3-150">2: CS (КСНЕТ)</span><span class="sxs-lookup"><span data-stu-id="a9ea3-150">2: CS (CSNET)</span></span>

<span data-ttu-id="a9ea3-151">3: CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="a9ea3-151">3: CH (CHAOS)</span></span>

<span data-ttu-id="a9ea3-152">4: HS (Хесиод)</span><span class="sxs-lookup"><span data-stu-id="a9ea3-152">4: HS (Hesiod)</span></span>

</dd> <dt>

<span data-ttu-id="a9ea3-153">**рекорддата**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-153">**RecordData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ea3-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ea3-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9ea3-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ea3-156">Данные записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-156">Resource record data.</span></span>

</dd> <dt>

<span data-ttu-id="a9ea3-157">**текстрепресентатион**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-157">**TextRepresentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ea3-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9ea3-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9ea3-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ea3-160">Текстовое представление всей записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-160">Text representation of the entire RR.</span></span>

</dd> <dt>

<span data-ttu-id="a9ea3-161">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-161">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ea3-162">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9ea3-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9ea3-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ea3-164">Время последнего обновления записи ресурса, выраженное в прошедшем времени с 1 января 1601 г., среднее время по Гринвичу (GMT).</span><span class="sxs-lookup"><span data-stu-id="a9ea3-164">Time at which the RR was last refreshed, expressed in elapsed hours since January 1, 1601, Greenwich Mean Time (GMT).</span></span>

</dd> <dt>

<span data-ttu-id="a9ea3-165">**Срок жизни**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-165">**TTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9ea3-166">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9ea3-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9ea3-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9ea3-168">Время в секундах, в течение которого запись ресурса может быть кэширована [*распознавателем*](r-gly.md)DNS.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-168">Time, in seconds, that the RR can be cached by a DNS [*resolver*](r-gly.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9ea3-169">Требования</span><span class="sxs-lookup"><span data-stu-id="a9ea3-169">Requirements</span></span>



| <span data-ttu-id="a9ea3-170">Требование</span><span class="sxs-lookup"><span data-stu-id="a9ea3-170">Requirement</span></span> | <span data-ttu-id="a9ea3-171">Значение</span><span class="sxs-lookup"><span data-stu-id="a9ea3-171">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ea3-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9ea3-172">Minimum supported client</span></span><br/> | <span data-ttu-id="a9ea3-173">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a9ea3-173">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a9ea3-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9ea3-174">Minimum supported server</span></span><br/> | <span data-ttu-id="a9ea3-175">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a9ea3-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a9ea3-176">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a9ea3-176">Namespace</span></span><br/>                | <span data-ttu-id="a9ea3-177">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="a9ea3-177">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a9ea3-178">MOF</span><span class="sxs-lookup"><span data-stu-id="a9ea3-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9ea3-179"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9ea3-179"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9ea3-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9ea3-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9ea3-181">**Метод Креатеинстанцефромтекстрепресентатион \_ класса Ресаурцерекорд микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-181">**CreateInstanceFromTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> <dt>

[<span data-ttu-id="a9ea3-182">**Метод Жетобжектбитекстрепресентатион \_ класса Ресаурцерекорд микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="a9ea3-182">**GetObjectByTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





