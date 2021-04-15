---
title: Класс MicrosoftDNS_PTRType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись указателя (PTR).
ms.assetid: 2cb0f13b-e683-473b-9cdd-bc5d805b919d
keywords:
- DNS класса MicrosoftDNS_PTRType
- DNS-MicrosoftDNS_PTRType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType
- MicrosoftDNS_PTRType.CreateInstanceFromPropertyData
- MicrosoftDNS_PTRType.Modify
- MicrosoftDNS_PTRType.PTRDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65dc434eb751ed925ab9efcdaf29f04741b749ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534337"
---
# <a name="microsoftdns_ptrtype-class"></a><span data-ttu-id="6a6c6-105">\_Класс микрософтднс птртипе</span><span class="sxs-lookup"><span data-stu-id="6a6c6-105">MicrosoftDNS\_PTRType class</span></span>

<span data-ttu-id="6a6c6-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись указателя (PTR).</span><span class="sxs-lookup"><span data-stu-id="6a6c6-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Pointer (PTR) record.</span></span>

<span data-ttu-id="6a6c6-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="6a6c6-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a6c6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a6c6-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_PTRType : MicrosoftDNS_ResourceRecord
{
  string PTRDomainName;
};
```

## <a name="members"></a><span data-ttu-id="6a6c6-109">Члены</span><span class="sxs-lookup"><span data-stu-id="6a6c6-109">Members</span></span>

<span data-ttu-id="6a6c6-110">Класс **микрософтднс \_ птртипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6a6c6-110">The **MicrosoftDNS\_PTRType** class has these types of members:</span></span>

-   [<span data-ttu-id="6a6c6-111">Методы</span><span class="sxs-lookup"><span data-stu-id="6a6c6-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="6a6c6-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="6a6c6-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6a6c6-113">Методы</span><span class="sxs-lookup"><span data-stu-id="6a6c6-113">Methods</span></span>

<span data-ttu-id="6a6c6-114">Класс **микрософтднс \_ птртипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6a6c6-114">The **MicrosoftDNS\_PTRType** class has these methods.</span></span>



| <span data-ttu-id="6a6c6-115">Метод</span><span class="sxs-lookup"><span data-stu-id="6a6c6-115">Method</span></span>                             | <span data-ttu-id="6a6c6-116">Описание</span><span class="sxs-lookup"><span data-stu-id="6a6c6-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a6c6-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="6a6c6-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="6a6c6-118">Создает экземпляр записи ресурса PTR DNS на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца, класс (по умолчанию — IN), значение срока жизни и полное доменное имя записи PTR.</span><span class="sxs-lookup"><span data-stu-id="6a6c6-118">Instantiates a DNS PTR Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value and the FQDN of the PTR record.</span></span> <span data-ttu-id="6a6c6-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="6a6c6-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="6a6c6-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="6a6c6-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="6a6c6-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="6a6c6-121">**Modify**</span></span>                         | <span data-ttu-id="6a6c6-122">Обновляет имя домена TTL и PTR на значения, указанные в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="6a6c6-122">Updates the TTL and PTR Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="6a6c6-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="6a6c6-123">If a new value for a parameter is not specified, the current value for the parameter is not changed.</span></span> <span data-ttu-id="6a6c6-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="6a6c6-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="6a6c6-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="6a6c6-125">Qualifiers: Implemented</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="6a6c6-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="6a6c6-126">Properties</span></span>

<span data-ttu-id="6a6c6-127">Класс **микрософтднс \_ птртипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6a6c6-127">The **MicrosoftDNS\_PTRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6a6c6-128">**птрдомаиннаме**</span><span class="sxs-lookup"><span data-stu-id="6a6c6-128">**PTRDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a6c6-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6a6c6-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a6c6-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6a6c6-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a6c6-131">Полное доменное имя данных записи PTR.</span><span class="sxs-lookup"><span data-stu-id="6a6c6-131">FQDN of the PTR record data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6a6c6-132">Требования</span><span class="sxs-lookup"><span data-stu-id="6a6c6-132">Requirements</span></span>



| <span data-ttu-id="6a6c6-133">Требование</span><span class="sxs-lookup"><span data-stu-id="6a6c6-133">Requirement</span></span> | <span data-ttu-id="6a6c6-134">Значение</span><span class="sxs-lookup"><span data-stu-id="6a6c6-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a6c6-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a6c6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6a6c6-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6a6c6-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6a6c6-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a6c6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6a6c6-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6a6c6-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6a6c6-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6a6c6-139">Namespace</span></span><br/>                | <span data-ttu-id="6a6c6-140">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="6a6c6-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6a6c6-141">MOF</span><span class="sxs-lookup"><span data-stu-id="6a6c6-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a6c6-142"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a6c6-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a6c6-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a6c6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a6c6-144">**Метод Креатеинстанцефромпропертидата \_ класса Птртипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="6a6c6-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="6a6c6-145">**Метод Modify \_ класса микрософтднс птртипе**</span><span class="sxs-lookup"><span data-stu-id="6a6c6-145">**Modify Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="6a6c6-146">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="6a6c6-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





