---
title: Класс MicrosoftDNS_MRType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись переименования почтового ящика (MR).
ms.assetid: fa5da18f-121b-477b-8876-6e337382e9b8
keywords:
- DNS класса MicrosoftDNS_MRType
- DNS-MicrosoftDNS_MRType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType
- MicrosoftDNS_MRType.CreateInstanceFromPropertyData
- MicrosoftDNS_MRType.Modify
- MicrosoftDNS_MRType.MRMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 732f0e6f51963f5ae810e4730406a94264fdde47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136950"
---
# <a name="microsoftdns_mrtype-class"></a><span data-ttu-id="6689e-105">\_Класс микрософтднс мртипе</span><span class="sxs-lookup"><span data-stu-id="6689e-105">MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="6689e-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись переименования почтового ящика (MR).</span><span class="sxs-lookup"><span data-stu-id="6689e-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mailbox Rename (MR) record.</span></span>

<span data-ttu-id="6689e-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="6689e-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6689e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6689e-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MRType : MicrosoftDNS_ResourceRecord
{
  string MRMailbox;
};
```

## <a name="members"></a><span data-ttu-id="6689e-109">Члены</span><span class="sxs-lookup"><span data-stu-id="6689e-109">Members</span></span>

<span data-ttu-id="6689e-110">Класс **микрософтднс \_ мртипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6689e-110">The **MicrosoftDNS\_MRType** class has these types of members:</span></span>

-   [<span data-ttu-id="6689e-111">Методы</span><span class="sxs-lookup"><span data-stu-id="6689e-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="6689e-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="6689e-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6689e-113">Методы</span><span class="sxs-lookup"><span data-stu-id="6689e-113">Methods</span></span>

<span data-ttu-id="6689e-114">Класс **микрософтднс \_ мртипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6689e-114">The **MicrosoftDNS\_MRType** class has these methods.</span></span>



| <span data-ttu-id="6689e-115">Метод</span><span class="sxs-lookup"><span data-stu-id="6689e-115">Method</span></span>                             | <span data-ttu-id="6689e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="6689e-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6689e-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="6689e-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="6689e-118">Этот метод создает тип RR типа "MR" на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца почтового ящика, класс (по умолчанию — IN), значение срока жизни и переименование почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="6689e-118">This method instantiates an 'MR' Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mailbox, class (default = IN), time-to-live value and the mailbox rename.</span></span> <span data-ttu-id="6689e-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="6689e-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="6689e-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="6689e-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="6689e-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="6689e-121">**Modify**</span></span>                         | <span data-ttu-id="6689e-122">Этот метод обновляет в почтовом ящике TTL и MR значения, указанные в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="6689e-122">This method updates the TTL and MR Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="6689e-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="6689e-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="6689e-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="6689e-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="6689e-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="6689e-125">Qualifiers: Implemented</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="6689e-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="6689e-126">Properties</span></span>

<span data-ttu-id="6689e-127">Класс **микрософтднс \_ мртипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6689e-127">The **MicrosoftDNS\_MRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6689e-128">**мрмаилбокс**</span><span class="sxs-lookup"><span data-stu-id="6689e-128">**MRMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6689e-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6689e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6689e-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6689e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6689e-131">Полное доменное имя, указывающее почтовый ящик, который является правильным именем почтового ящика, указанного в имени владельца записи.</span><span class="sxs-lookup"><span data-stu-id="6689e-131">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's owner name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6689e-132">Требования</span><span class="sxs-lookup"><span data-stu-id="6689e-132">Requirements</span></span>



| <span data-ttu-id="6689e-133">Требование</span><span class="sxs-lookup"><span data-stu-id="6689e-133">Requirement</span></span> | <span data-ttu-id="6689e-134">Значение</span><span class="sxs-lookup"><span data-stu-id="6689e-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6689e-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6689e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6689e-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6689e-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6689e-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6689e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6689e-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6689e-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6689e-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6689e-139">Namespace</span></span><br/>                | <span data-ttu-id="6689e-140">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="6689e-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6689e-141">MOF</span><span class="sxs-lookup"><span data-stu-id="6689e-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6689e-142"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6689e-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6689e-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6689e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6689e-144">**Метод Креатеинстанцефромпропертидата \_ класса Мртипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="6689e-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="6689e-145">**Метод Modify \_ класса микрософтднс мртипе**</span><span class="sxs-lookup"><span data-stu-id="6689e-145">**Modify Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="6689e-146">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="6689e-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





