---
title: Класс MicrosoftDNS_WKSType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись Well-Known Services (WKS).
ms.assetid: 7bbfd518-d473-4127-949b-9133a43ac7a7
keywords:
- DNS класса MicrosoftDNS_WKSType
- DNS-MicrosoftDNS_WKSType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WKSType.Modify
- MicrosoftDNS_WKSType.InternetAddress
- MicrosoftDNS_WKSType.IPProtocol
- MicrosoftDNS_WKSType.Services
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f7fde08721bb8bb62b93f72b792060b06c15dad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988894"
---
# <a name="microsoftdns_wkstype-class"></a><span data-ttu-id="08718-105">\_Класс микрософтднс вкстипе</span><span class="sxs-lookup"><span data-stu-id="08718-105">MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="08718-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись Well-Known Services (WKS).</span><span class="sxs-lookup"><span data-stu-id="08718-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Well-Known Services (WKS) record.</span></span>

<span data-ttu-id="08718-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="08718-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="08718-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08718-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WKSType : MicrosoftDNS_ResourceRecord
{
  string InternetAddress;
  string IPProtocol;
  string Services;
};
```

## <a name="members"></a><span data-ttu-id="08718-109">Члены</span><span class="sxs-lookup"><span data-stu-id="08718-109">Members</span></span>

<span data-ttu-id="08718-110">Класс **микрософтднс \_ вкстипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="08718-110">The **MicrosoftDNS\_WKSType** class has these types of members:</span></span>

-   [<span data-ttu-id="08718-111">Методы</span><span class="sxs-lookup"><span data-stu-id="08718-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="08718-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="08718-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="08718-113">Методы</span><span class="sxs-lookup"><span data-stu-id="08718-113">Methods</span></span>

<span data-ttu-id="08718-114">Класс **микрософтднс \_ вкстипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="08718-114">The **MicrosoftDNS\_WKSType** class has these methods.</span></span>



| <span data-ttu-id="08718-115">Метод</span><span class="sxs-lookup"><span data-stu-id="08718-115">Method</span></span>                             | <span data-ttu-id="08718-116">Описание</span><span class="sxs-lookup"><span data-stu-id="08718-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08718-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="08718-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="08718-118">Создает экземпляр типа WKS, основанный на данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца, класс (по умолчанию — IN), значение срока жизни и адрес в Интернете владельца, IP-протокол и битовая маска порта.</span><span class="sxs-lookup"><span data-stu-id="08718-118">Instantiates a WKS Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the owner's Internet Address, IP protocol and port bit mask.</span></span> <span data-ttu-id="08718-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="08718-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="08718-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="08718-120">Qualifiers: Implemented, static</span></span><br/>  |
| <span data-ttu-id="08718-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="08718-121">**Modify**</span></span>                         | <span data-ttu-id="08718-122">Этот метод обновляет значения TTL, адрес Интернета, IP-протокол и службы до значений, указанных в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="08718-122">This method updates the TTL, Internet Address, IP Protocol, and Services to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="08718-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="08718-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="08718-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="08718-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="08718-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="08718-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="08718-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="08718-126">Properties</span></span>

<span data-ttu-id="08718-127">Класс **микрософтднс \_ вкстипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="08718-127">The **MicrosoftDNS\_WKSType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08718-128">**интернетаддресс**</span><span class="sxs-lookup"><span data-stu-id="08718-128">**InternetAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08718-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08718-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08718-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08718-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08718-131">IP-адрес владельца записи.</span><span class="sxs-lookup"><span data-stu-id="08718-131">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="08718-132">**IPProtocol**</span><span class="sxs-lookup"><span data-stu-id="08718-132">**IPProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08718-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08718-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08718-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08718-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08718-135">Строка, представляющая протокол IP для этой записи.</span><span class="sxs-lookup"><span data-stu-id="08718-135">String representing the IP protocol for this record.</span></span> <span data-ttu-id="08718-136">Допустимые значения: UDP или TCP.</span><span class="sxs-lookup"><span data-stu-id="08718-136">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="08718-137">**Службы**</span><span class="sxs-lookup"><span data-stu-id="08718-137">**Services**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08718-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08718-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08718-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08718-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08718-140">Строка, содержащая все службы, используемые записью службы хорошо известных служб (WKS).</span><span class="sxs-lookup"><span data-stu-id="08718-140">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08718-141">Требования</span><span class="sxs-lookup"><span data-stu-id="08718-141">Requirements</span></span>



| <span data-ttu-id="08718-142">Требование</span><span class="sxs-lookup"><span data-stu-id="08718-142">Requirement</span></span> | <span data-ttu-id="08718-143">Значение</span><span class="sxs-lookup"><span data-stu-id="08718-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08718-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08718-144">Minimum supported client</span></span><br/> | <span data-ttu-id="08718-145">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="08718-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="08718-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08718-146">Minimum supported server</span></span><br/> | <span data-ttu-id="08718-147">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="08718-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="08718-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="08718-148">Namespace</span></span><br/>                | <span data-ttu-id="08718-149">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="08718-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="08718-150">MOF</span><span class="sxs-lookup"><span data-stu-id="08718-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08718-151"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08718-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08718-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08718-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08718-153">**Метод Креатеинстанцефромпропертидата \_ класса Вкстипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="08718-153">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="08718-154">**Метод Modify \_ класса микрософтднс вкстипе**</span><span class="sxs-lookup"><span data-stu-id="08718-154">**Modify Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-modify.md)
</dt> <dt>

[<span data-ttu-id="08718-155">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="08718-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





