---
title: Класс MicrosoftDNS_AType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись адреса узла (a).
ms.assetid: c7bd8a26-b0ac-49ef-9068-a0ecddeb6ef4
keywords:
- DNS класса MicrosoftDNS_AType
- DNS-MicrosoftDNS_AType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType
- MicrosoftDNS_AType.CreateInstanceFromPropertyData
- MicrosoftDNS_AType.Modify
- MicrosoftDNS_AType.IPAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e856968e2c3d4e581d69e0ac7bcbddc256424c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654491"
---
# <a name="microsoftdns_atype-class"></a><span data-ttu-id="7e690-105">\_Класс микрософтднс атипе</span><span class="sxs-lookup"><span data-stu-id="7e690-105">MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="7e690-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись адреса узла (a).</span><span class="sxs-lookup"><span data-stu-id="7e690-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a host Address (A) record.</span></span>

<span data-ttu-id="7e690-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="7e690-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e690-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e690-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_AType : MicrosoftDNS_ResourceRecord
{
  string IPAddress;
};
```

## <a name="members"></a><span data-ttu-id="7e690-109">Члены</span><span class="sxs-lookup"><span data-stu-id="7e690-109">Members</span></span>

<span data-ttu-id="7e690-110">Класс **микрософтднс \_ атипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7e690-110">The **MicrosoftDNS\_AType** class has these types of members:</span></span>

-   [<span data-ttu-id="7e690-111">Методы</span><span class="sxs-lookup"><span data-stu-id="7e690-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="7e690-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="7e690-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7e690-113">Методы</span><span class="sxs-lookup"><span data-stu-id="7e690-113">Methods</span></span>

<span data-ttu-id="7e690-114">Класс **микрософтднс \_ атипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7e690-114">The **MicrosoftDNS\_AType** class has these methods.</span></span>



| <span data-ttu-id="7e690-115">Метод</span><span class="sxs-lookup"><span data-stu-id="7e690-115">Method</span></span>                             | <span data-ttu-id="7e690-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7e690-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e690-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="7e690-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="7e690-118">Создает экземпляр RR с адресом узла (A) на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца, класс (по умолчанию — IN), значение срока жизни и IP-адрес узла.</span><span class="sxs-lookup"><span data-stu-id="7e690-118">Instantiates a Host Address (A) RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value and the IP address of the host.</span></span> <span data-ttu-id="7e690-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="7e690-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="7e690-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="7e690-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="7e690-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="7e690-121">**Modify**</span></span>                         | <span data-ttu-id="7e690-122">Обновляет значения TTL и IP-адреса значениями, указанными в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="7e690-122">Updates the TTL and IP address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="7e690-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="7e690-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="7e690-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="7e690-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="7e690-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="7e690-125">Qualifiers: Implemented</span></span><br/>             |



 

### <a name="properties"></a><span data-ttu-id="7e690-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="7e690-126">Properties</span></span>

<span data-ttu-id="7e690-127">Класс **микрософтднс \_ атипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7e690-127">The **MicrosoftDNS\_AType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e690-128">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="7e690-128">**IPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e690-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7e690-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e690-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7e690-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e690-131">Строка, представляющая IPv4-адрес узла.</span><span class="sxs-lookup"><span data-stu-id="7e690-131">String representing the IPv4 address of the host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e690-132">Требования</span><span class="sxs-lookup"><span data-stu-id="7e690-132">Requirements</span></span>



| <span data-ttu-id="7e690-133">Требование</span><span class="sxs-lookup"><span data-stu-id="7e690-133">Requirement</span></span> | <span data-ttu-id="7e690-134">Значение</span><span class="sxs-lookup"><span data-stu-id="7e690-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e690-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e690-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7e690-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7e690-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7e690-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e690-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7e690-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7e690-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7e690-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7e690-139">Namespace</span></span><br/>                | <span data-ttu-id="7e690-140">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="7e690-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="7e690-141">MOF</span><span class="sxs-lookup"><span data-stu-id="7e690-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e690-142"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e690-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e690-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e690-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e690-144">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="7e690-144">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="7e690-145">**Метод Креатеинстанцефромпропертидата \_ класса Атипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="7e690-145">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="7e690-146">**Метод Modify \_ класса микрософтднс атипе**</span><span class="sxs-lookup"><span data-stu-id="7e690-146">**Modify Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-modify.md)
</dt> </dl>

 

 





