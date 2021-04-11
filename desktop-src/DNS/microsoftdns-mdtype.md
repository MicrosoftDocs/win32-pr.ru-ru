---
title: Класс MicrosoftDNS_MDType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись почтового агента для домена (MD).
ms.assetid: 11242372-65fe-44ee-845b-2430aec59127
keywords:
- DNS класса MicrosoftDNS_MDType
- DNS-MicrosoftDNS_MDType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType
- MicrosoftDNS_MDType.CreateInstanceFromPropertyData
- MicrosoftDNS_MDType.Modify
- MicrosoftDNS_MDType.MDHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7641fda7a223fed7c2dc9229c5a3449c575e84ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891889"
---
# <a name="microsoftdns_mdtype-class"></a><span data-ttu-id="12af3-105">\_Класс микрософтднс мдтипе</span><span class="sxs-lookup"><span data-stu-id="12af3-105">MicrosoftDNS\_MDType class</span></span>

<span data-ttu-id="12af3-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись почтового агента для домена (MD).</span><span class="sxs-lookup"><span data-stu-id="12af3-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Agent for Domain (MD) record.</span></span>

<span data-ttu-id="12af3-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="12af3-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="12af3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12af3-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MDType : MicrosoftDNS_ResourceRecord
{
  string MDHost;
};
```

## <a name="members"></a><span data-ttu-id="12af3-109">Члены</span><span class="sxs-lookup"><span data-stu-id="12af3-109">Members</span></span>

<span data-ttu-id="12af3-110">Класс **микрософтднс \_ мдтипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="12af3-110">The **MicrosoftDNS\_MDType** class has these types of members:</span></span>

-   [<span data-ttu-id="12af3-111">Методы</span><span class="sxs-lookup"><span data-stu-id="12af3-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="12af3-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="12af3-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="12af3-113">Методы</span><span class="sxs-lookup"><span data-stu-id="12af3-113">Methods</span></span>

<span data-ttu-id="12af3-114">Класс **микрософтднс \_ мдтипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="12af3-114">The **MicrosoftDNS\_MDType** class has these methods.</span></span>



| <span data-ttu-id="12af3-115">Метод</span><span class="sxs-lookup"><span data-stu-id="12af3-115">Method</span></span>                             | <span data-ttu-id="12af3-116">Описание</span><span class="sxs-lookup"><span data-stu-id="12af3-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12af3-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="12af3-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="12af3-118">Создает экземпляр DNS-записи ресурса MD на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца домена, класс (по умолчанию — IN), значение срока жизни и узел почтового агента.</span><span class="sxs-lookup"><span data-stu-id="12af3-118">Instantiates a DNS MD Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the domain, class (default = IN), time-to-live value and the host of the mail agent.</span></span> <span data-ttu-id="12af3-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="12af3-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="12af3-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="12af3-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="12af3-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="12af3-121">**Modify**</span></span>                         | <span data-ttu-id="12af3-122">Обновляет узел TTL и MD на значения, указанные в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="12af3-122">Updates the TTL and MD host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="12af3-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="12af3-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="12af3-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="12af3-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="12af3-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="12af3-125">Qualifiers: Implemented</span></span><br/>                                 |



 

### <a name="properties"></a><span data-ttu-id="12af3-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="12af3-126">Properties</span></span>

<span data-ttu-id="12af3-127">Класс **микрософтднс \_ мдтипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="12af3-127">The **MicrosoftDNS\_MDType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12af3-128">**мдхост**</span><span class="sxs-lookup"><span data-stu-id="12af3-128">**MDHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12af3-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="12af3-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12af3-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="12af3-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12af3-131">Полное доменное имя, указывающее узел с почтовым агентом, который может доставлять почту для указанного домена.</span><span class="sxs-lookup"><span data-stu-id="12af3-131">FQDN that specifies a host with a mail agent capable of delivering mail for the specified domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12af3-132">Требования</span><span class="sxs-lookup"><span data-stu-id="12af3-132">Requirements</span></span>



| <span data-ttu-id="12af3-133">Требование</span><span class="sxs-lookup"><span data-stu-id="12af3-133">Requirement</span></span> | <span data-ttu-id="12af3-134">Значение</span><span class="sxs-lookup"><span data-stu-id="12af3-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12af3-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12af3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="12af3-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="12af3-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="12af3-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12af3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="12af3-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="12af3-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="12af3-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="12af3-139">Namespace</span></span><br/>                | <span data-ttu-id="12af3-140">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="12af3-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="12af3-141">MOF</span><span class="sxs-lookup"><span data-stu-id="12af3-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12af3-142"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12af3-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12af3-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12af3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12af3-144">**Метод Креатеинстанцефромпропертидата \_ класса Мдтипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="12af3-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="12af3-145">**Метод Modify \_ класса микрософтднс мдтипе**</span><span class="sxs-lookup"><span data-stu-id="12af3-145">**Modify Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-modify.md)
</dt> <dt>

[<span data-ttu-id="12af3-146">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="12af3-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





