---
title: Класс MicrosoftDNS_MFType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись агента переадресации почты для домена (MF).
ms.assetid: 0ba0fddd-c316-4a5b-ad65-6344dbe949c1
keywords:
- DNS класса MicrosoftDNS_MFType
- DNS-MicrosoftDNS_MFType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType
- MicrosoftDNS_MFType.CreateInstanceFromPropertyData
- MicrosoftDNS_MFType.Modify
- MicrosoftDNS_MFType.MFHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e030f695e95ee736b1c53a345201e0bd1addfe3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136606"
---
# <a name="microsoftdns_mftype-class"></a><span data-ttu-id="87594-105">\_Класс микрософтднс мфтипе</span><span class="sxs-lookup"><span data-stu-id="87594-105">MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="87594-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись агента переадресации почты для домена (MF).</span><span class="sxs-lookup"><span data-stu-id="87594-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Forwarding Agent for Domain (MF) record.</span></span>

<span data-ttu-id="87594-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="87594-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="87594-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87594-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MFType : MicrosoftDNS_ResourceRecord
{
  string MFHost;
};
```

## <a name="members"></a><span data-ttu-id="87594-109">Члены</span><span class="sxs-lookup"><span data-stu-id="87594-109">Members</span></span>

<span data-ttu-id="87594-110">Класс **микрософтднс \_ мфтипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="87594-110">The **MicrosoftDNS\_MFType** class has these types of members:</span></span>

-   [<span data-ttu-id="87594-111">Методы</span><span class="sxs-lookup"><span data-stu-id="87594-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="87594-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="87594-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="87594-113">Методы</span><span class="sxs-lookup"><span data-stu-id="87594-113">Methods</span></span>

<span data-ttu-id="87594-114">Класс **микрософтднс \_ мфтипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="87594-114">The **MicrosoftDNS\_MFType** class has these methods.</span></span>



| <span data-ttu-id="87594-115">Метод</span><span class="sxs-lookup"><span data-stu-id="87594-115">Method</span></span>                             | <span data-ttu-id="87594-116">Описание</span><span class="sxs-lookup"><span data-stu-id="87594-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87594-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="87594-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="87594-118">Этот метод создает тип записей записи типа MF на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца домена, класс (по умолчанию — IN), значение срока жизни и узел почтового агента.</span><span class="sxs-lookup"><span data-stu-id="87594-118">This method instantiates an MF Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the domain, class (default = IN), time-to-live value and the host of the mail agent.</span></span> <span data-ttu-id="87594-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="87594-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="87594-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="87594-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="87594-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="87594-121">**Modify**</span></span>                         | <span data-ttu-id="87594-122">Этот метод обновляет узел TTL и MF на значения, указанные в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="87594-122">This method updates the TTL and MF Host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="87594-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="87594-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="87594-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="87594-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="87594-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="87594-125">Qualifiers: Implemented</span></span><br/>                         |



 

### <a name="properties"></a><span data-ttu-id="87594-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="87594-126">Properties</span></span>

<span data-ttu-id="87594-127">Класс **микрософтднс \_ мфтипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="87594-127">The **MicrosoftDNS\_MFType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87594-128">**мфхост**</span><span class="sxs-lookup"><span data-stu-id="87594-128">**MFHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87594-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="87594-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87594-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87594-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87594-131">Полное доменное имя, указывающее узел с почтовым агентом, который будет принимать почту для перенаправления в указанный домен.</span><span class="sxs-lookup"><span data-stu-id="87594-131">FQDN specifying a host with a mail agent that will accept mail for forwarding to the specified domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87594-132">Требования</span><span class="sxs-lookup"><span data-stu-id="87594-132">Requirements</span></span>



| <span data-ttu-id="87594-133">Требование</span><span class="sxs-lookup"><span data-stu-id="87594-133">Requirement</span></span> | <span data-ttu-id="87594-134">Значение</span><span class="sxs-lookup"><span data-stu-id="87594-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87594-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87594-135">Minimum supported client</span></span><br/> | <span data-ttu-id="87594-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="87594-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="87594-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87594-137">Minimum supported server</span></span><br/> | <span data-ttu-id="87594-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="87594-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="87594-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="87594-139">Namespace</span></span><br/>                | <span data-ttu-id="87594-140">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="87594-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="87594-141">MOF</span><span class="sxs-lookup"><span data-stu-id="87594-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87594-142"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87594-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87594-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87594-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87594-144">**Метод Креатеинстанцефромпропертидата \_ класса Мфтипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="87594-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="87594-145">**Метод Modify \_ класса микрософтднс мфтипе**</span><span class="sxs-lookup"><span data-stu-id="87594-145">**Modify Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-modify.md)
</dt> <dt>

[<span data-ttu-id="87594-146">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="87594-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





