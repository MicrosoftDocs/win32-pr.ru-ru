---
title: Класс MicrosoftDNS_MBType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись ресурса почтового ящика (МБ).
ms.assetid: b8f3b106-58f4-44b8-b2db-b00f1a495641
keywords:
- DNS класса MicrosoftDNS_MBType
- DNS-MicrosoftDNS_MBType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
- MicrosoftDNS_MBType.Modify
- MicrosoftDNS_MBType.MBHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89ad6599ad058f65beba961f00c1bd6c43663487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988812"
---
# <a name="microsoftdns_mbtype-class"></a><span data-ttu-id="4e01d-105">\_Класс микрософтднс мбтипе</span><span class="sxs-lookup"><span data-stu-id="4e01d-105">MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="4e01d-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись ресурса почтового ящика (МБ).</span><span class="sxs-lookup"><span data-stu-id="4e01d-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mailbox (MB) resource record.</span></span>

<span data-ttu-id="4e01d-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="4e01d-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e01d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e01d-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MBType : MicrosoftDNS_ResourceRecord
{
  string MBHost;
};
```

## <a name="members"></a><span data-ttu-id="4e01d-109">Члены</span><span class="sxs-lookup"><span data-stu-id="4e01d-109">Members</span></span>

<span data-ttu-id="4e01d-110">Класс **микрософтднс \_ мбтипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4e01d-110">The **MicrosoftDNS\_MBType** class has these types of members:</span></span>

-   [<span data-ttu-id="4e01d-111">Методы</span><span class="sxs-lookup"><span data-stu-id="4e01d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="4e01d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="4e01d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4e01d-113">Методы</span><span class="sxs-lookup"><span data-stu-id="4e01d-113">Methods</span></span>

<span data-ttu-id="4e01d-114">Класс **микрософтднс \_ мбтипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4e01d-114">The **MicrosoftDNS\_MBType** class has these methods.</span></span>



| <span data-ttu-id="4e01d-115">Метод</span><span class="sxs-lookup"><span data-stu-id="4e01d-115">Method</span></span>                             | <span data-ttu-id="4e01d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4e01d-116">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e01d-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="4e01d-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="4e01d-118">Создает экземпляр RR в МБ на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца почтового ящика, класс (по умолчанию — IN), значение срока жизни и узел почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="4e01d-118">Instantiates an MB RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mailbox, class (default = IN), time-to-live value and the mailbox host.</span></span> <span data-ttu-id="4e01d-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="4e01d-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="4e01d-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="4e01d-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="4e01d-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="4e01d-121">**Modify**</span></span>                         | <span data-ttu-id="4e01d-122">Обновляет узлы TTL и MB до значений, указанных в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="4e01d-122">Updates the TTL and MB host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="4e01d-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="4e01d-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="4e01d-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="4e01d-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="4e01d-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="4e01d-125">Qualifiers: Implemented</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="4e01d-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="4e01d-126">Properties</span></span>

<span data-ttu-id="4e01d-127">Класс **микрософтднс \_ мбтипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4e01d-127">The **MicrosoftDNS\_MBType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e01d-128">**мбхост**</span><span class="sxs-lookup"><span data-stu-id="4e01d-128">**MBHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e01d-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4e01d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e01d-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4e01d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e01d-131">Полное доменное имя, указывающее узел почтового ящика, указанный в имени владельца записи.</span><span class="sxs-lookup"><span data-stu-id="4e01d-131">FQDN that specifies a host of the mailbox specified in the record's Owner Name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e01d-132">Требования</span><span class="sxs-lookup"><span data-stu-id="4e01d-132">Requirements</span></span>



| <span data-ttu-id="4e01d-133">Требование</span><span class="sxs-lookup"><span data-stu-id="4e01d-133">Requirement</span></span> | <span data-ttu-id="4e01d-134">Значение</span><span class="sxs-lookup"><span data-stu-id="4e01d-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e01d-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e01d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4e01d-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4e01d-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4e01d-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e01d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4e01d-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4e01d-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4e01d-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4e01d-139">Namespace</span></span><br/>                | <span data-ttu-id="4e01d-140">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="4e01d-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4e01d-141">MOF</span><span class="sxs-lookup"><span data-stu-id="4e01d-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e01d-142"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e01d-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e01d-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e01d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e01d-144">**Метод Креатеинстанцефромпропертидата \_ класса Мбтипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="4e01d-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="4e01d-145">**Метод Modify \_ класса микрософтднс мбтипе**</span><span class="sxs-lookup"><span data-stu-id="4e01d-145">**Modify Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="4e01d-146">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="4e01d-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





