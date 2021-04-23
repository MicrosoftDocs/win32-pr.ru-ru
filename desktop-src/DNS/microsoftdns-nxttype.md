---
title: Класс MicrosoftDNS_NXTType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий следующую запись ресурса (NXT).
ms.assetid: bb24509e-083b-4432-89e3-501167f12299
keywords:
- DNS класса MicrosoftDNS_NXTType
- DNS-MicrosoftDNS_NXTType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_NXTType.Modify
- MicrosoftDNS_NXTType.NextDomainName
- MicrosoftDNS_NXTType.Types
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79db82b3ae760c31d4e6fef80eb01469cb2bb41d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136222"
---
# <a name="microsoftdns_nxttype-class"></a><span data-ttu-id="e4bae-105">\_Класс микрософтднс нксттипе</span><span class="sxs-lookup"><span data-stu-id="e4bae-105">MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="e4bae-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий следующую запись ресурса (NXT).</span><span class="sxs-lookup"><span data-stu-id="e4bae-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Next (NXT) RR.</span></span>

<span data-ttu-id="e4bae-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="e4bae-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4bae-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4bae-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_NXTType : MicrosoftDNS_ResourceRecord
{
  string NextDomainName;
  string Types;
};
```

## <a name="members"></a><span data-ttu-id="e4bae-109">Члены</span><span class="sxs-lookup"><span data-stu-id="e4bae-109">Members</span></span>

<span data-ttu-id="e4bae-110">Класс **микрософтднс \_ нксттипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e4bae-110">The **MicrosoftDNS\_NXTType** class has these types of members:</span></span>

-   [<span data-ttu-id="e4bae-111">Методы</span><span class="sxs-lookup"><span data-stu-id="e4bae-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e4bae-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="e4bae-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e4bae-113">Методы</span><span class="sxs-lookup"><span data-stu-id="e4bae-113">Methods</span></span>

<span data-ttu-id="e4bae-114">Класс **микрософтднс \_ нксттипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e4bae-114">The **MicrosoftDNS\_NXTType** class has these methods.</span></span>



| <span data-ttu-id="e4bae-115">Метод</span><span class="sxs-lookup"><span data-stu-id="e4bae-115">Method</span></span>                             | <span data-ttu-id="e4bae-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e4bae-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4bae-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="e4bae-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="e4bae-118">Создает экземпляр записи ресурса NXT на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца, класс (по умолчанию — IN), значение срока жизни и флаг сопоставления WINS, время ожидания для отмены просмотра, время ожидания кэша WINS и имя домена для добавления.</span><span class="sxs-lookup"><span data-stu-id="e4bae-118">Instantiates an NXT Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out, and domain name to append.</span></span> <span data-ttu-id="e4bae-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="e4bae-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="e4bae-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="e4bae-120">Qualifiers: Implemented, static</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="e4bae-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="e4bae-121">**Modify**</span></span>                         | <span data-ttu-id="e4bae-122">Обновляет значения TTL, флага сопоставления, времени ожидания при поиске, истечения времени ожидания кэша и домена результата до значений, указанных в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="e4bae-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="e4bae-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="e4bae-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="e4bae-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="e4bae-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="e4bae-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="e4bae-125">Qualifiers: Implemented</span></span><br/> <span data-ttu-id="e4bae-126">**Windows Server 2003:** Этот метод также обновляет Некстдомаиннаме и типы значениями, указанными в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="e4bae-126">**Windows Server 2003:** This method also updates the NextDomainName and Types to the values specified as the input parameters of this method.</span></span><br/> <br/> |



 

### <a name="properties"></a><span data-ttu-id="e4bae-127">Свойства</span><span class="sxs-lookup"><span data-stu-id="e4bae-127">Properties</span></span>

<span data-ttu-id="e4bae-128">Класс **микрософтднс \_ нксттипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e4bae-128">The **MicrosoftDNS\_NXTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e4bae-129">**некстдомаиннаме**</span><span class="sxs-lookup"><span data-stu-id="e4bae-129">**NextDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4bae-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e4bae-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4bae-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e4bae-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4bae-132">Следующее имя домена.</span><span class="sxs-lookup"><span data-stu-id="e4bae-132">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="e4bae-133">**Типы**</span><span class="sxs-lookup"><span data-stu-id="e4bae-133">**Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4bae-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e4bae-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4bae-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e4bae-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4bae-136">Разделенный пробелами список назначенных пространств имен для имени владельца записи ресурса NXT.</span><span class="sxs-lookup"><span data-stu-id="e4bae-136">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4bae-137">Требования</span><span class="sxs-lookup"><span data-stu-id="e4bae-137">Requirements</span></span>



| <span data-ttu-id="e4bae-138">Требование</span><span class="sxs-lookup"><span data-stu-id="e4bae-138">Requirement</span></span> | <span data-ttu-id="e4bae-139">Значение</span><span class="sxs-lookup"><span data-stu-id="e4bae-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4bae-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4bae-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e4bae-141">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e4bae-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e4bae-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4bae-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e4bae-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e4bae-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e4bae-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e4bae-144">Namespace</span></span><br/>                | <span data-ttu-id="e4bae-145">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="e4bae-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e4bae-146">MOF</span><span class="sxs-lookup"><span data-stu-id="e4bae-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4bae-147"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4bae-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4bae-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4bae-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4bae-149">**Метод Креатеинстанцефромпропертидата \_ класса Нксттипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="e4bae-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="e4bae-150">**Метод Modify \_ класса микрософтднс нксттипе**</span><span class="sxs-lookup"><span data-stu-id="e4bae-150">**Modify Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-modify.md)
</dt> <dt>

[<span data-ttu-id="e4bae-151">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="e4bae-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





