---
title: Класс MicrosoftDNS_SRVType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись службы (SRV).
ms.assetid: 4b36246d-4466-46d9-9267-180e43547ae6
keywords:
- DNS класса MicrosoftDNS_SRVType
- DNS-MicrosoftDNS_SRVType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
- MicrosoftDNS_SRVType.Modify
- MicrosoftDNS_SRVType.Priority
- MicrosoftDNS_SRVType.Weight
- MicrosoftDNS_SRVType.Port
- MicrosoftDNS_SRVType.SRVDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea955cad281e9361b4fa1ca5b033a4ca0d39719
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491157"
---
# <a name="microsoftdns_srvtype-class"></a><span data-ttu-id="afae7-105">\_Класс микрософтднс срвтипе</span><span class="sxs-lookup"><span data-stu-id="afae7-105">MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="afae7-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись службы (SRV).</span><span class="sxs-lookup"><span data-stu-id="afae7-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Service (SRV) record.</span></span>

<span data-ttu-id="afae7-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="afae7-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="afae7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="afae7-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SRVType : MicrosoftDNS_ResourceRecord
{
  uint16 Priority;
  uint16 Weight;
  uint16 Port;
  string SRVDomainName;
};
```

## <a name="members"></a><span data-ttu-id="afae7-109">Члены</span><span class="sxs-lookup"><span data-stu-id="afae7-109">Members</span></span>

<span data-ttu-id="afae7-110">Класс **микрософтднс \_ срвтипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="afae7-110">The **MicrosoftDNS\_SRVType** class has these types of members:</span></span>

-   [<span data-ttu-id="afae7-111">Методы</span><span class="sxs-lookup"><span data-stu-id="afae7-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="afae7-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="afae7-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="afae7-113">Методы</span><span class="sxs-lookup"><span data-stu-id="afae7-113">Methods</span></span>

<span data-ttu-id="afae7-114">Класс **микрософтднс \_ срвтипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="afae7-114">The **MicrosoftDNS\_SRVType** class has these methods.</span></span>



| <span data-ttu-id="afae7-115">Метод</span><span class="sxs-lookup"><span data-stu-id="afae7-115">Method</span></span>                             | <span data-ttu-id="afae7-116">Описание</span><span class="sxs-lookup"><span data-stu-id="afae7-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afae7-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="afae7-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="afae7-118">Создает экземпляр SRV типа RR на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца/целевого объекта, класс (по умолчанию — IN), значение срока жизни и приоритет целевого узла, вес, порт и имя домена.</span><span class="sxs-lookup"><span data-stu-id="afae7-118">Instantiates an SRV Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/target Name, class (default = IN), time-to-live value, and target host's priority, weight, port, and domain name.</span></span> <span data-ttu-id="afae7-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="afae7-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="afae7-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="afae7-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="afae7-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="afae7-121">**Modify**</span></span>                         | <span data-ttu-id="afae7-122">Обновляет значения срока жизни, приоритета, веса, порта и доменного имени до значений, указанных в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="afae7-122">Updates the TTL, Priority, Weight, Port, and Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="afae7-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="afae7-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="afae7-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="afae7-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="afae7-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="afae7-125">Qualifiers: Implemented</span></span><br/>                  |



 

### <a name="properties"></a><span data-ttu-id="afae7-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="afae7-126">Properties</span></span>

<span data-ttu-id="afae7-127">Класс **микрософтднс \_ срвтипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="afae7-127">The **MicrosoftDNS\_SRVType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="afae7-128">**порт**.</span><span class="sxs-lookup"><span data-stu-id="afae7-128">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afae7-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="afae7-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="afae7-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="afae7-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afae7-131">Порт, используемый на целевом узле службы протокола.</span><span class="sxs-lookup"><span data-stu-id="afae7-131">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="afae7-132">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="afae7-132">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afae7-133">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="afae7-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="afae7-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="afae7-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afae7-135">Приоритет целевого узла, указанного в имени владельца.</span><span class="sxs-lookup"><span data-stu-id="afae7-135">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="afae7-136">Более низкие значения подразумевают более высокие приоритеты.</span><span class="sxs-lookup"><span data-stu-id="afae7-136">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="afae7-137">**срвдомаиннаме**</span><span class="sxs-lookup"><span data-stu-id="afae7-137">**SRVDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afae7-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="afae7-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afae7-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="afae7-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afae7-140">Полное доменное имя целевого узла.</span><span class="sxs-lookup"><span data-stu-id="afae7-140">FQDN of the target host.</span></span> <span data-ttu-id="afae7-141">Целевой объект \\ . \\ означает, что служба не будет доступна в этом домене.</span><span class="sxs-lookup"><span data-stu-id="afae7-141">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="afae7-142">**Weight**</span><span class="sxs-lookup"><span data-stu-id="afae7-142">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afae7-143">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="afae7-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="afae7-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="afae7-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afae7-145">Вес целевого узла.</span><span class="sxs-lookup"><span data-stu-id="afae7-145">Weight of the target host.</span></span> <span data-ttu-id="afae7-146">Это полезно при выборе между узлами с одинаковым приоритетом.</span><span class="sxs-lookup"><span data-stu-id="afae7-146">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="afae7-147">Вероятность использования этого узла должна быть пропорциональна его весу.</span><span class="sxs-lookup"><span data-stu-id="afae7-147">The chances of using this host should be proportional to its weight.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="afae7-148">Требования</span><span class="sxs-lookup"><span data-stu-id="afae7-148">Requirements</span></span>



| <span data-ttu-id="afae7-149">Требование</span><span class="sxs-lookup"><span data-stu-id="afae7-149">Requirement</span></span> | <span data-ttu-id="afae7-150">Значение</span><span class="sxs-lookup"><span data-stu-id="afae7-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="afae7-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="afae7-151">Minimum supported client</span></span><br/> | <span data-ttu-id="afae7-152">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="afae7-152">None supported</span></span><br/>                                                              |
| <span data-ttu-id="afae7-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="afae7-153">Minimum supported server</span></span><br/> | <span data-ttu-id="afae7-154">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="afae7-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="afae7-155">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="afae7-155">Namespace</span></span><br/>                | <span data-ttu-id="afae7-156">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="afae7-156">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="afae7-157">MOF</span><span class="sxs-lookup"><span data-stu-id="afae7-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afae7-158"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="afae7-158"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afae7-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="afae7-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afae7-160">**Метод Креатеинстанцефромпропертидата \_ класса Срвтипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="afae7-160">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="afae7-161">**Метод Modify \_ класса микрософтднс срвтипе**</span><span class="sxs-lookup"><span data-stu-id="afae7-161">**Modify Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-modify.md)
</dt> <dt>

[<span data-ttu-id="afae7-162">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="afae7-162">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





