---
title: Класс MicrosoftDNS_AAAAType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись IPv6-адреса (AAAA). Запись AAAA обычно прописывается \ 0034; с записью \ 0034;.
ms.assetid: e16a7a69-18df-43dc-add9-700a702724ce
keywords:
- DNS класса MicrosoftDNS_AAAAType
- DNS-MicrosoftDNS_AAAAType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType
- MicrosoftDNS_AAAAType.CreateInstanceFromPropertyData
- MicrosoftDNS_AAAAType.Modify
- MicrosoftDNS_AAAAType.IPv6Address
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0131177c342730c08868946c29356554cbfb9cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654495"
---
# <a name="microsoftdns_aaaatype-class"></a><span data-ttu-id="e721e-106">\_Класс микрософтднс аааатипе</span><span class="sxs-lookup"><span data-stu-id="e721e-106">MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="e721e-107">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись IPv6-адреса (AAAA).</span><span class="sxs-lookup"><span data-stu-id="e721e-107">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an IPv6 Address (AAAA) record.</span></span> <span data-ttu-id="e721e-108">Запись AAAA обычно произносится как «четыре» записи.</span><span class="sxs-lookup"><span data-stu-id="e721e-108">The AAAA record is commonly pronounced "quad-a record".</span></span>

<span data-ttu-id="e721e-109">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="e721e-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e721e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e721e-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_AAAAType : MicrosoftDNS_ResourceRecord
{
  string IPv6Address;
};
```

## <a name="members"></a><span data-ttu-id="e721e-111">Члены</span><span class="sxs-lookup"><span data-stu-id="e721e-111">Members</span></span>

<span data-ttu-id="e721e-112">Класс **микрософтднс \_ аааатипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e721e-112">The **MicrosoftDNS\_AAAAType** class has these types of members:</span></span>

-   [<span data-ttu-id="e721e-113">Методы</span><span class="sxs-lookup"><span data-stu-id="e721e-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="e721e-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="e721e-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e721e-115">Методы</span><span class="sxs-lookup"><span data-stu-id="e721e-115">Methods</span></span>

<span data-ttu-id="e721e-116">Класс **микрософтднс \_ аааатипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e721e-116">The **MicrosoftDNS\_AAAAType** class has these methods.</span></span>



| <span data-ttu-id="e721e-117">Метод</span><span class="sxs-lookup"><span data-stu-id="e721e-117">Method</span></span>                             | <span data-ttu-id="e721e-118">Описание</span><span class="sxs-lookup"><span data-stu-id="e721e-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e721e-119">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="e721e-119">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="e721e-120">Создает экземпляр типа ресурса RR на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца/узла, класс (по умолчанию — IN), значение срока жизни и IPv6-адрес.</span><span class="sxs-lookup"><span data-stu-id="e721e-120">Instantiates an 'AAAA' type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Host Name, class (default = IN), time-to-live value, and the IPv6 address.</span></span> <span data-ttu-id="e721e-121">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="e721e-121">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="e721e-122">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="e721e-122">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="e721e-123">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="e721e-123">**Modify**</span></span>                         | <span data-ttu-id="e721e-124">Обновляет значения TTL и IPv6 до значений, указанных в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="e721e-124">Updates the TTL and IPv6 address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="e721e-125">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="e721e-125">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="e721e-126">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="e721e-126">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="e721e-127">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="e721e-127">Qualifiers: Implemented</span></span><br/>      |



 

### <a name="properties"></a><span data-ttu-id="e721e-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="e721e-128">Properties</span></span>

<span data-ttu-id="e721e-129">Класс **микрософтднс \_ аааатипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e721e-129">The **MicrosoftDNS\_AAAAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e721e-130">**IPv6Address**</span><span class="sxs-lookup"><span data-stu-id="e721e-130">**IPv6Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e721e-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e721e-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e721e-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e721e-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e721e-133">IPv6-адрес узла.</span><span class="sxs-lookup"><span data-stu-id="e721e-133">IPv6 address for the host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e721e-134">Требования</span><span class="sxs-lookup"><span data-stu-id="e721e-134">Requirements</span></span>



| <span data-ttu-id="e721e-135">Требование</span><span class="sxs-lookup"><span data-stu-id="e721e-135">Requirement</span></span> | <span data-ttu-id="e721e-136">Значение</span><span class="sxs-lookup"><span data-stu-id="e721e-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e721e-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e721e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e721e-138">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e721e-138">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e721e-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e721e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e721e-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e721e-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e721e-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e721e-141">Namespace</span></span><br/>                | <span data-ttu-id="e721e-142">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="e721e-142">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e721e-143">MOF</span><span class="sxs-lookup"><span data-stu-id="e721e-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e721e-144"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e721e-144"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e721e-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e721e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e721e-146">**Метод Креатеинстанцефромпропертидата \_ класса Аааатипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="e721e-146">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="e721e-147">**Метод Modify \_ класса микрософтднс аааатипе**</span><span class="sxs-lookup"><span data-stu-id="e721e-147">**Modify Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[<span data-ttu-id="e721e-148">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="e721e-148">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





