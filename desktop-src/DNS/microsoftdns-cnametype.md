---
title: Класс MicrosoftDNS_CNAMEType
description: Подкласс Микрософтднс \_ ресаурцерекорд, который представляет запись канонического имени (CNAME).
ms.assetid: 93a972e3-abb1-425f-beb7-32abe7d0b485
keywords:
- DNS класса MicrosoftDNS_CNAMEType
- DNS-MicrosoftDNS_CNAMEType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType
- MicrosoftDNS_CNAMEType.CreateInstanceFromPropertyData
- MicrosoftDNS_CNAMEType.Modify
- MicrosoftDNS_CNAMEType.PrimaryName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dca8729c2c750e1cef774b5f0f3eadc3e2f6fbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891945"
---
# <a name="microsoftdns_cnametype-class"></a><span data-ttu-id="187b7-105">\_Класс микрософтднс кнаметипе</span><span class="sxs-lookup"><span data-stu-id="187b7-105">MicrosoftDNS\_CNAMEType class</span></span>

<span data-ttu-id="187b7-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , который представляет запись канонического имени (CNAME).</span><span class="sxs-lookup"><span data-stu-id="187b7-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Canonical Name (CNAME) record.</span></span>

<span data-ttu-id="187b7-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="187b7-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="187b7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="187b7-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_CNAMEType : MicrosoftDNS_ResourceRecord
{
  string PrimaryName;
};
```

## <a name="members"></a><span data-ttu-id="187b7-109">Члены</span><span class="sxs-lookup"><span data-stu-id="187b7-109">Members</span></span>

<span data-ttu-id="187b7-110">Класс **микрософтднс \_ кнаметипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="187b7-110">The **MicrosoftDNS\_CNAMEType** class has these types of members:</span></span>

-   [<span data-ttu-id="187b7-111">Методы</span><span class="sxs-lookup"><span data-stu-id="187b7-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="187b7-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="187b7-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="187b7-113">Методы</span><span class="sxs-lookup"><span data-stu-id="187b7-113">Methods</span></span>

<span data-ttu-id="187b7-114">Класс **микрософтднс \_ кнаметипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="187b7-114">The **MicrosoftDNS\_CNAMEType** class has these methods.</span></span>



| <span data-ttu-id="187b7-115">Метод</span><span class="sxs-lookup"><span data-stu-id="187b7-115">Method</span></span>                             | <span data-ttu-id="187b7-116">Описание</span><span class="sxs-lookup"><span data-stu-id="187b7-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="187b7-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="187b7-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="187b7-118">Создает экземпляр записи ресурса CNAME на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца, класс (по умолчанию — IN), значение срока жизни и первичное имя записи CNAME.</span><span class="sxs-lookup"><span data-stu-id="187b7-118">Instantiates a CNAME Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the primary name of the CNAME record.</span></span> <span data-ttu-id="187b7-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="187b7-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="187b7-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="187b7-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="187b7-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="187b7-121">**Modify**</span></span>                         | <span data-ttu-id="187b7-122">Обновляет значения TTL и PRIMARY до значений, указанных в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="187b7-122">Updates the TTL and Primary Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="187b7-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="187b7-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="187b7-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="187b7-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="187b7-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="187b7-125">Qualifiers: Implemented</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="187b7-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="187b7-126">Properties</span></span>

<span data-ttu-id="187b7-127">Класс **микрософтднс \_ кнаметипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="187b7-127">The **MicrosoftDNS\_CNAMEType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="187b7-128">**примаринаме**</span><span class="sxs-lookup"><span data-stu-id="187b7-128">**PrimaryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="187b7-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="187b7-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="187b7-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="187b7-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="187b7-131">Каноническое или основное имя владельца записи CNAME.</span><span class="sxs-lookup"><span data-stu-id="187b7-131">Canonical, or primary name for the owner of the CNAME record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="187b7-132">Требования</span><span class="sxs-lookup"><span data-stu-id="187b7-132">Requirements</span></span>



| <span data-ttu-id="187b7-133">Требование</span><span class="sxs-lookup"><span data-stu-id="187b7-133">Requirement</span></span> | <span data-ttu-id="187b7-134">Значение</span><span class="sxs-lookup"><span data-stu-id="187b7-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="187b7-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="187b7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="187b7-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="187b7-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="187b7-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="187b7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="187b7-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="187b7-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="187b7-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="187b7-139">Namespace</span></span><br/>                | <span data-ttu-id="187b7-140">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="187b7-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="187b7-141">MOF</span><span class="sxs-lookup"><span data-stu-id="187b7-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="187b7-142"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="187b7-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="187b7-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="187b7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="187b7-144">**Метод Креатеинстанцефромпропертидата \_ класса Кнаметипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="187b7-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="187b7-145">**Метод Modify \_ класса микрософтднс кнаметипе**</span><span class="sxs-lookup"><span data-stu-id="187b7-145">**Modify Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-modify.md)
</dt> <dt>

[<span data-ttu-id="187b7-146">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="187b7-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





