---
title: Класс MicrosoftDNS_RPType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись ответственного лица (RP).
ms.assetid: 2b1c1bbc-a69f-4480-a7f2-6420240d4ad8
keywords:
- DNS класса MicrosoftDNS_RPType
- DNS-MicrosoftDNS_RPType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
- MicrosoftDNS_RPType.Modify
- MicrosoftDNS_RPType.RPMailbox
- MicrosoftDNS_RPType.TXTDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9aae8686016d26cb9007b21a06c125d56ed5207f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892117"
---
# <a name="microsoftdns_rptype-class"></a><span data-ttu-id="fd624-105">\_Класс микрософтднс рптипе</span><span class="sxs-lookup"><span data-stu-id="fd624-105">MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="fd624-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись ответственного лица (RP).</span><span class="sxs-lookup"><span data-stu-id="fd624-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Responsible Person (RP) record.</span></span>

<span data-ttu-id="fd624-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="fd624-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd624-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd624-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_RPType : MicrosoftDNS_ResourceRecord
{
  string RPMailbox;
  string TXTDomainName;
};
```

## <a name="members"></a><span data-ttu-id="fd624-109">Члены</span><span class="sxs-lookup"><span data-stu-id="fd624-109">Members</span></span>

<span data-ttu-id="fd624-110">Класс **микрософтднс \_ рптипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fd624-110">The **MicrosoftDNS\_RPType** class has these types of members:</span></span>

-   [<span data-ttu-id="fd624-111">Методы</span><span class="sxs-lookup"><span data-stu-id="fd624-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fd624-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="fd624-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fd624-113">Методы</span><span class="sxs-lookup"><span data-stu-id="fd624-113">Methods</span></span>

<span data-ttu-id="fd624-114">Класс **микрософтднс \_ рптипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="fd624-114">The **MicrosoftDNS\_RPType** class has these methods.</span></span>



| <span data-ttu-id="fd624-115">Метод</span><span class="sxs-lookup"><span data-stu-id="fd624-115">Method</span></span>                             | <span data-ttu-id="fd624-116">Описание</span><span class="sxs-lookup"><span data-stu-id="fd624-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd624-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="fd624-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="fd624-118">Создает экземпляр типа ресурса RP на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца/ответственного лица, класс (по умолчанию — IN), значение срока жизни и имена доменов для местоположения RR пользователя и TXT-файла.</span><span class="sxs-lookup"><span data-stu-id="fd624-118">Instantiates an RP Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/responsible person Name, class (default = IN), time-to-live value and the domain names for the person's mailbox and TXT RR locations.</span></span> <span data-ttu-id="fd624-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="fd624-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="fd624-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="fd624-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="fd624-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="fd624-121">**Modify**</span></span>                         | <span data-ttu-id="fd624-122">Этот метод обновляет имя домена "TTL", "почтовый ящик RP" и "TXT" на значения, указанные в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="fd624-122">This method updates the TTL, RP Mailbox and TXT Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="fd624-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="fd624-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="fd624-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="fd624-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="fd624-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="fd624-125">Qualifiers: Implemented</span></span><br/>                                  |



 

### <a name="properties"></a><span data-ttu-id="fd624-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="fd624-126">Properties</span></span>

<span data-ttu-id="fd624-127">Класс **микрософтднс \_ рптипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fd624-127">The **MicrosoftDNS\_RPType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd624-128">**рпмаилбокс**</span><span class="sxs-lookup"><span data-stu-id="fd624-128">**RPMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd624-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fd624-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd624-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fd624-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd624-131">Полное доменное имя, указывающее почтовый ящик ответственного лица.</span><span class="sxs-lookup"><span data-stu-id="fd624-131">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="fd624-132">**ткстдомаиннаме**</span><span class="sxs-lookup"><span data-stu-id="fd624-132">**TXTDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd624-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fd624-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd624-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fd624-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd624-135">Полное доменное имя, для которого существуют записи ресурсов TXT.</span><span class="sxs-lookup"><span data-stu-id="fd624-135">FQDN for which TXT Resource Records exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd624-136">Требования</span><span class="sxs-lookup"><span data-stu-id="fd624-136">Requirements</span></span>



| <span data-ttu-id="fd624-137">Требование</span><span class="sxs-lookup"><span data-stu-id="fd624-137">Requirement</span></span> | <span data-ttu-id="fd624-138">Значение</span><span class="sxs-lookup"><span data-stu-id="fd624-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd624-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd624-139">Minimum supported client</span></span><br/> | <span data-ttu-id="fd624-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fd624-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fd624-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd624-141">Minimum supported server</span></span><br/> | <span data-ttu-id="fd624-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fd624-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fd624-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fd624-143">Namespace</span></span><br/>                | <span data-ttu-id="fd624-144">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="fd624-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fd624-145">MOF</span><span class="sxs-lookup"><span data-stu-id="fd624-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd624-146"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd624-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd624-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd624-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd624-148">**Метод Креатеинстанцефромпропертидата \_ класса Рптипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="fd624-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="fd624-149">**Метод Modify \_ класса микрософтднс рптипе**</span><span class="sxs-lookup"><span data-stu-id="fd624-149">**Modify Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-modify.md)
</dt> <dt>

[<span data-ttu-id="fd624-150">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="fd624-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





