---
title: Класс MicrosoftDNS_NSType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись сервера имен (NS).
ms.assetid: 8d229acd-bc47-4a32-b6f1-b784a48dc91a
keywords:
- DNS класса MicrosoftDNS_NSType
- DNS-MicrosoftDNS_NSType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_NSType
- MicrosoftDNS_NSType.CreateInstanceFromPropertyData
- MicrosoftDNS_NSType.Modify
- MicrosoftDNS_NSType.NSHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07155c36089e60b12aeea214b19cb8aca146005a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989428"
---
# <a name="microsoftdns_nstype-class"></a><span data-ttu-id="7949a-105">\_Класс микрософтднс нстипе</span><span class="sxs-lookup"><span data-stu-id="7949a-105">MicrosoftDNS\_NSType class</span></span>

<span data-ttu-id="7949a-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись сервера имен (NS).</span><span class="sxs-lookup"><span data-stu-id="7949a-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Name Server (NS) record.</span></span>

<span data-ttu-id="7949a-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="7949a-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7949a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7949a-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_NSType : MicrosoftDNS_ResourceRecord
{
  string NSHost;
};
```

## <a name="members"></a><span data-ttu-id="7949a-109">Члены</span><span class="sxs-lookup"><span data-stu-id="7949a-109">Members</span></span>

<span data-ttu-id="7949a-110">Класс **микрософтднс \_ нстипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7949a-110">The **MicrosoftDNS\_NSType** class has these types of members:</span></span>

-   [<span data-ttu-id="7949a-111">Методы</span><span class="sxs-lookup"><span data-stu-id="7949a-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="7949a-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="7949a-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7949a-113">Методы</span><span class="sxs-lookup"><span data-stu-id="7949a-113">Methods</span></span>

<span data-ttu-id="7949a-114">Класс **микрософтднс \_ нстипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7949a-114">The **MicrosoftDNS\_NSType** class has these methods.</span></span>



| <span data-ttu-id="7949a-115">Метод</span><span class="sxs-lookup"><span data-stu-id="7949a-115">Method</span></span>                             | <span data-ttu-id="7949a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7949a-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7949a-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="7949a-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="7949a-118">Создает экземпляр записи ресурса NS DNS на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца, класс (по умолчанию — IN), значение срока жизни и узел с полномочиями для домена.</span><span class="sxs-lookup"><span data-stu-id="7949a-118">Instantiates a DNS NS Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value and the host with authority for the domain.</span></span> <span data-ttu-id="7949a-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="7949a-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="7949a-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="7949a-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="7949a-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="7949a-121">**Modify**</span></span>                         | <span data-ttu-id="7949a-122">Обновляет значения TTL и узла NS значениями, указанными в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="7949a-122">Updates the TTL and NS Host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="7949a-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="7949a-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="7949a-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="7949a-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="7949a-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="7949a-125">Qualifiers: Implemented</span></span><br/>                               |



 

### <a name="properties"></a><span data-ttu-id="7949a-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="7949a-126">Properties</span></span>

<span data-ttu-id="7949a-127">Класс **микрософтднс \_ нстипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7949a-127">The **MicrosoftDNS\_NSType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7949a-128">**ншост**</span><span class="sxs-lookup"><span data-stu-id="7949a-128">**NSHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7949a-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7949a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7949a-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7949a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7949a-131">Полномочный узел для домена.</span><span class="sxs-lookup"><span data-stu-id="7949a-131">Authoritative host for the domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7949a-132">Требования</span><span class="sxs-lookup"><span data-stu-id="7949a-132">Requirements</span></span>



| <span data-ttu-id="7949a-133">Требование</span><span class="sxs-lookup"><span data-stu-id="7949a-133">Requirement</span></span> | <span data-ttu-id="7949a-134">Значение</span><span class="sxs-lookup"><span data-stu-id="7949a-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7949a-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7949a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7949a-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7949a-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7949a-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7949a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7949a-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7949a-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7949a-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7949a-139">Namespace</span></span><br/>                | <span data-ttu-id="7949a-140">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="7949a-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="7949a-141">MOF</span><span class="sxs-lookup"><span data-stu-id="7949a-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7949a-142"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7949a-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7949a-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7949a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7949a-144">**Метод Креатеинстанцефромпропертидата \_ класса Нстипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="7949a-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_NSType Class**</span></span>](microsoftdns-nstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="7949a-145">**Метод Modify \_ класса микрософтднс нстипе**</span><span class="sxs-lookup"><span data-stu-id="7949a-145">**Modify Method of the MicrosoftDNS\_NSType Class**</span></span>](microsoftdns-nstype-modify.md)
</dt> <dt>

[<span data-ttu-id="7949a-146">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="7949a-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





