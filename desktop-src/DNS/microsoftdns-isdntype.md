---
title: Класс MicrosoftDNS_ISDNType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись ISDN.
ms.assetid: 8925042c-65d3-465f-aedd-9f7c862620b5
keywords:
- DNS класса MicrosoftDNS_ISDNType
- DNS-MicrosoftDNS_ISDNType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
- MicrosoftDNS_ISDNType.Modify
- MicrosoftDNS_ISDNType.ISDNNumber
- MicrosoftDNS_ISDNType.SubAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4e8b50d75f7b6d57226247c978ced45e07b1acc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135191"
---
# <a name="microsoftdns_isdntype-class"></a><span data-ttu-id="ffe63-105">\_Класс микрософтднс исднтипе</span><span class="sxs-lookup"><span data-stu-id="ffe63-105">MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="ffe63-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись ISDN.</span><span class="sxs-lookup"><span data-stu-id="ffe63-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an ISDN record.</span></span>

<span data-ttu-id="ffe63-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="ffe63-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffe63-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffe63-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ISDNType : MicrosoftDNS_ResourceRecord
{
  string ISDNNumber;
  string SubAddress;
};
```

## <a name="members"></a><span data-ttu-id="ffe63-109">Члены</span><span class="sxs-lookup"><span data-stu-id="ffe63-109">Members</span></span>

<span data-ttu-id="ffe63-110">Класс **микрософтднс \_ исднтипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ffe63-110">The **MicrosoftDNS\_ISDNType** class has these types of members:</span></span>

-   [<span data-ttu-id="ffe63-111">Методы</span><span class="sxs-lookup"><span data-stu-id="ffe63-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ffe63-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="ffe63-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ffe63-113">Методы</span><span class="sxs-lookup"><span data-stu-id="ffe63-113">Methods</span></span>

<span data-ttu-id="ffe63-114">Класс **микрософтднс \_ исднтипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ffe63-114">The **MicrosoftDNS\_ISDNType** class has these methods.</span></span>



| <span data-ttu-id="ffe63-115">Метод</span><span class="sxs-lookup"><span data-stu-id="ffe63-115">Method</span></span>                             | <span data-ttu-id="ffe63-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ffe63-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffe63-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="ffe63-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="ffe63-118">Создает экземпляр записи ресурса ISDN на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца, класс (по умолчанию — IN), значение срока жизни, а также номер ISDN и дополнительный адрес владельца.</span><span class="sxs-lookup"><span data-stu-id="ffe63-118">Instantiates an ISDN Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the ISDN number and subaddress of the owner.</span></span> <span data-ttu-id="ffe63-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="ffe63-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="ffe63-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="ffe63-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="ffe63-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="ffe63-121">**Modify**</span></span>                         | <span data-ttu-id="ffe63-122">Обновляет значения TTL, номер ISDN и подадрес для значений, указанных в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="ffe63-122">Updates the TTL, ISDN Number, and Subaddress to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="ffe63-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="ffe63-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="ffe63-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="ffe63-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="ffe63-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="ffe63-125">Qualifiers: Implemented</span></span><br/>                   |



 

### <a name="properties"></a><span data-ttu-id="ffe63-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="ffe63-126">Properties</span></span>

<span data-ttu-id="ffe63-127">Класс **микрософтднс \_ исднтипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ffe63-127">The **MicrosoftDNS\_ISDNType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ffe63-128">**исдннумбер**</span><span class="sxs-lookup"><span data-stu-id="ffe63-128">**ISDNNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffe63-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ffe63-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffe63-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffe63-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffe63-131">Номер ISDN и DDI владельца записи.</span><span class="sxs-lookup"><span data-stu-id="ffe63-131">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="ffe63-132">**Подадрес**</span><span class="sxs-lookup"><span data-stu-id="ffe63-132">**SubAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffe63-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ffe63-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffe63-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffe63-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffe63-135">Подадрес владельца, если он определен.</span><span class="sxs-lookup"><span data-stu-id="ffe63-135">Subaddress of the owner, if defined.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ffe63-136">Требования</span><span class="sxs-lookup"><span data-stu-id="ffe63-136">Requirements</span></span>



| <span data-ttu-id="ffe63-137">Требование</span><span class="sxs-lookup"><span data-stu-id="ffe63-137">Requirement</span></span> | <span data-ttu-id="ffe63-138">Значение</span><span class="sxs-lookup"><span data-stu-id="ffe63-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffe63-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ffe63-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ffe63-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ffe63-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ffe63-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ffe63-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ffe63-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ffe63-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ffe63-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ffe63-143">Namespace</span></span><br/>                | <span data-ttu-id="ffe63-144">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="ffe63-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ffe63-145">MOF</span><span class="sxs-lookup"><span data-stu-id="ffe63-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffe63-146"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffe63-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffe63-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ffe63-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffe63-148">**Метод Креатеинстанцефромпропертидата \_ класса Исднтипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="ffe63-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ffe63-149">**Метод Modify \_ класса микрософтднс исднтипе**</span><span class="sxs-lookup"><span data-stu-id="ffe63-149">**Modify Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-modify.md)
</dt> <dt>

[<span data-ttu-id="ffe63-150">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="ffe63-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





