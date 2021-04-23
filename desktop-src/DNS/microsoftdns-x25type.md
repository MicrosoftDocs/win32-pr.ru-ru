---
title: Класс MicrosoftDNS_X25Type
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись X. 25 (X25).
ms.assetid: 1213dfd7-30b3-413e-b723-f4284fa0b416
keywords:
- DNS класса MicrosoftDNS_X25Type
- DNS-MicrosoftDNS_X25Type класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type
- MicrosoftDNS_X25Type.CreateInstanceFromPropertyData
- MicrosoftDNS_X25Type.Modify
- MicrosoftDNS_X25Type.PSDNAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e584119dbd45d5d6c7fae347c506c42fcda4fff7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654561"
---
# <a name="microsoftdns_x25type-class"></a><span data-ttu-id="10290-105">\_Класс микрософтднс X25Type</span><span class="sxs-lookup"><span data-stu-id="10290-105">MicrosoftDNS\_X25Type class</span></span>

<span data-ttu-id="10290-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись X. 25 (X25).</span><span class="sxs-lookup"><span data-stu-id="10290-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an X.25 (X25) record.</span></span>

<span data-ttu-id="10290-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="10290-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="10290-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10290-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_X25Type : MicrosoftDNS_ResourceRecord
{
  string PSDNAddress;
};
```

## <a name="members"></a><span data-ttu-id="10290-109">Члены</span><span class="sxs-lookup"><span data-stu-id="10290-109">Members</span></span>

<span data-ttu-id="10290-110">Класс **микрософтднс \_ X25Type** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="10290-110">The **MicrosoftDNS\_X25Type** class has these types of members:</span></span>

-   [<span data-ttu-id="10290-111">Методы</span><span class="sxs-lookup"><span data-stu-id="10290-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="10290-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="10290-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="10290-113">Методы</span><span class="sxs-lookup"><span data-stu-id="10290-113">Methods</span></span>

<span data-ttu-id="10290-114">Класс **микрософтднс \_ X25Type** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="10290-114">The **MicrosoftDNS\_X25Type** class has these methods.</span></span>



| <span data-ttu-id="10290-115">Метод</span><span class="sxs-lookup"><span data-stu-id="10290-115">Method</span></span>                             | <span data-ttu-id="10290-116">Описание</span><span class="sxs-lookup"><span data-stu-id="10290-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10290-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="10290-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="10290-118">Создает экземпляр типа RR на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца, класс (по умолчанию — IN), значение срока жизни и адрес PSDN.</span><span class="sxs-lookup"><span data-stu-id="10290-118">Instantiates an 'X25' Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the PSDN address.</span></span> <span data-ttu-id="10290-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="10290-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="10290-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="10290-120">Qualifiers: Implemented, static</span></span><br/>              |
| <span data-ttu-id="10290-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="10290-121">**Modify**</span></span>                         | <span data-ttu-id="10290-122">Этот метод обновляет TTL и адрес PSDN значениями, указанными в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="10290-122">This method updates the TTL and PSDN Address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="10290-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="10290-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="10290-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="10290-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="10290-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="10290-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="10290-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="10290-126">Properties</span></span>

<span data-ttu-id="10290-127">Класс **микрософтднс \_ X25Type** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="10290-127">The **MicrosoftDNS\_X25Type** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10290-128">**псднаддресс**</span><span class="sxs-lookup"><span data-stu-id="10290-128">**PSDNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10290-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10290-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10290-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10290-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10290-131">Адрес PSDN владельца записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="10290-131">PSDN address of the owner of the RR.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10290-132">Требования</span><span class="sxs-lookup"><span data-stu-id="10290-132">Requirements</span></span>



| <span data-ttu-id="10290-133">Требование</span><span class="sxs-lookup"><span data-stu-id="10290-133">Requirement</span></span> | <span data-ttu-id="10290-134">Значение</span><span class="sxs-lookup"><span data-stu-id="10290-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10290-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10290-135">Minimum supported client</span></span><br/> | <span data-ttu-id="10290-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="10290-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="10290-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10290-137">Minimum supported server</span></span><br/> | <span data-ttu-id="10290-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="10290-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="10290-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="10290-139">Namespace</span></span><br/>                | <span data-ttu-id="10290-140">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="10290-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="10290-141">MOF</span><span class="sxs-lookup"><span data-stu-id="10290-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10290-142"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10290-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10290-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10290-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10290-144">**Метод Креатеинстанцефромпропертидата \_ класса X25Type микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="10290-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="10290-145">**Метод Modify \_ класса микрософтднс X25Type**</span><span class="sxs-lookup"><span data-stu-id="10290-145">**Modify Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-modify.md)
</dt> <dt>

[<span data-ttu-id="10290-146">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="10290-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





