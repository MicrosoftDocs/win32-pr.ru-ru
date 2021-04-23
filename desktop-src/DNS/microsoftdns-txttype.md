---
title: Класс MicrosoftDNS_TXTType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий текстовую запись (txt).
ms.assetid: e4bd445f-71c4-48dc-b210-e3ad4452d2e5
keywords:
- DNS класса MicrosoftDNS_TXTType
- DNS-MicrosoftDNS_TXTType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_TXTType.Modify
- MicrosoftDNS_TXTType.DescriptiveText
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d89563240b8e6d6bedb51cbe802180cd7577b57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654663"
---
# <a name="microsoftdns_txttype-class"></a><span data-ttu-id="b7f30-105">\_Класс микрософтднс тксттипе</span><span class="sxs-lookup"><span data-stu-id="b7f30-105">MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="b7f30-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий текстовую запись (txt).</span><span class="sxs-lookup"><span data-stu-id="b7f30-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Text (TXT) record.</span></span>

<span data-ttu-id="b7f30-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="b7f30-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7f30-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7f30-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_TXTType : MicrosoftDNS_ResourceRecord
{
  string DescriptiveText;
};
```

## <a name="members"></a><span data-ttu-id="b7f30-109">Члены</span><span class="sxs-lookup"><span data-stu-id="b7f30-109">Members</span></span>

<span data-ttu-id="b7f30-110">Класс **микрософтднс \_ тксттипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b7f30-110">The **MicrosoftDNS\_TXTType** class has these types of members:</span></span>

-   [<span data-ttu-id="b7f30-111">Методы</span><span class="sxs-lookup"><span data-stu-id="b7f30-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b7f30-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="b7f30-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b7f30-113">Методы</span><span class="sxs-lookup"><span data-stu-id="b7f30-113">Methods</span></span>

<span data-ttu-id="b7f30-114">Класс **микрософтднс \_ тксттипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b7f30-114">The **MicrosoftDNS\_TXTType** class has these methods.</span></span>



| <span data-ttu-id="b7f30-115">Метод</span><span class="sxs-lookup"><span data-stu-id="b7f30-115">Method</span></span>                             | <span data-ttu-id="b7f30-116">Описание</span><span class="sxs-lookup"><span data-stu-id="b7f30-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f30-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="b7f30-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="b7f30-118">Создает экземпляр типа RR на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца, класс (по умолчанию — IN), значение срока жизни и текст записи.</span><span class="sxs-lookup"><span data-stu-id="b7f30-118">Instantiates a TXT Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the record's text.</span></span> <span data-ttu-id="b7f30-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="b7f30-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="b7f30-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="b7f30-120">Qualifiers: Implemented, static</span></span><br/>        |
| <span data-ttu-id="b7f30-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="b7f30-121">**Modify**</span></span>                         | <span data-ttu-id="b7f30-122">Обновляет TTL и описательный текст на значения, указанные в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="b7f30-122">Updates the TTL and Descriptive Text to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="b7f30-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="b7f30-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="b7f30-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="b7f30-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="b7f30-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="b7f30-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b7f30-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="b7f30-126">Properties</span></span>

<span data-ttu-id="b7f30-127">Класс **микрософтднс \_ тксттипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b7f30-127">The **MicrosoftDNS\_TXTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7f30-128">**дескриптиветекст**</span><span class="sxs-lookup"><span data-stu-id="b7f30-128">**DescriptiveText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f30-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b7f30-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f30-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7f30-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f30-131">Описательный текст, семантика которого зависит от домена владельца.</span><span class="sxs-lookup"><span data-stu-id="b7f30-131">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7f30-132">Требования</span><span class="sxs-lookup"><span data-stu-id="b7f30-132">Requirements</span></span>



| <span data-ttu-id="b7f30-133">Требование</span><span class="sxs-lookup"><span data-stu-id="b7f30-133">Requirement</span></span> | <span data-ttu-id="b7f30-134">Значение</span><span class="sxs-lookup"><span data-stu-id="b7f30-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f30-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7f30-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b7f30-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b7f30-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b7f30-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7f30-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b7f30-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b7f30-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b7f30-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b7f30-139">Namespace</span></span><br/>                | <span data-ttu-id="b7f30-140">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="b7f30-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b7f30-141">MOF</span><span class="sxs-lookup"><span data-stu-id="b7f30-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7f30-142"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7f30-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7f30-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7f30-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7f30-144">**Метод Креатеинстанцефромпропертидата \_ класса Тксттипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="b7f30-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="b7f30-145">**Метод Modify \_ класса микрософтднс тксттипе**</span><span class="sxs-lookup"><span data-stu-id="b7f30-145">**Modify Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-modify.md)
</dt> <dt>

[<span data-ttu-id="b7f30-146">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="b7f30-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





