---
title: Класс MicrosoftDNS_RTType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись маршрутизации через (RT).
ms.assetid: 986e2bbf-4f45-4611-906e-66079fda7f4c
keywords:
- DNS класса MicrosoftDNS_RTType
- DNS-MicrosoftDNS_RTType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
- MicrosoftDNS_RTType.Modify
- MicrosoftDNS_RTType.Preference
- MicrosoftDNS_RTType.IntermediateHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d867185d8ce07a54a47eb5ea7591ec8d68a11059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988806"
---
# <a name="microsoftdns_rttype-class"></a><span data-ttu-id="72e8e-105">\_Класс микрософтднс рттипе</span><span class="sxs-lookup"><span data-stu-id="72e8e-105">MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="72e8e-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись МАРШРУТИЗАЦИИ через (RT).</span><span class="sxs-lookup"><span data-stu-id="72e8e-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Route Through (RT) record.</span></span>

<span data-ttu-id="72e8e-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="72e8e-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="72e8e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72e8e-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_RTType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string IntermediateHost;
};
```

## <a name="members"></a><span data-ttu-id="72e8e-109">Члены</span><span class="sxs-lookup"><span data-stu-id="72e8e-109">Members</span></span>

<span data-ttu-id="72e8e-110">Класс **микрософтднс \_ рттипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="72e8e-110">The **MicrosoftDNS\_RTType** class has these types of members:</span></span>

-   [<span data-ttu-id="72e8e-111">Методы</span><span class="sxs-lookup"><span data-stu-id="72e8e-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="72e8e-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="72e8e-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="72e8e-113">Методы</span><span class="sxs-lookup"><span data-stu-id="72e8e-113">Methods</span></span>

<span data-ttu-id="72e8e-114">Класс **микрософтднс \_ рттипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="72e8e-114">The **MicrosoftDNS\_RTType** class has these methods.</span></span>



| <span data-ttu-id="72e8e-115">Метод</span><span class="sxs-lookup"><span data-stu-id="72e8e-115">Method</span></span>                             | <span data-ttu-id="72e8e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="72e8e-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72e8e-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="72e8e-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="72e8e-118">Создает экземпляр типа ресурса RR на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца/узла, класс (по умолчанию — IN), значение срока жизни, параметры записи и имя промежуточного узла.</span><span class="sxs-lookup"><span data-stu-id="72e8e-118">Instantiates an RT Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/host Name, class (default = IN), time-to-live value, record preference and intermediate host name.</span></span> <span data-ttu-id="72e8e-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="72e8e-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="72e8e-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="72e8e-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="72e8e-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="72e8e-121">**Modify**</span></span>                         | <span data-ttu-id="72e8e-122">Обновляет параметры TTL, предпочтение и промежуточный узел на значения, указанные в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="72e8e-122">Updates the TTL, Preference, and Intermediate Host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="72e8e-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="72e8e-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="72e8e-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="72e8e-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="72e8e-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="72e8e-125">Qualifiers: Implemented</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="72e8e-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="72e8e-126">Properties</span></span>

<span data-ttu-id="72e8e-127">Класс **микрософтднс \_ рттипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="72e8e-127">The **MicrosoftDNS\_RTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72e8e-128">**интермедиатехост**</span><span class="sxs-lookup"><span data-stu-id="72e8e-128">**IntermediateHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72e8e-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="72e8e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72e8e-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="72e8e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72e8e-131">Полное доменное имя, указывающее узел, который будет выступать в качестве промежуточного в достижение узла, указанного владельцем.</span><span class="sxs-lookup"><span data-stu-id="72e8e-131">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="72e8e-132">**Закрыт**</span><span class="sxs-lookup"><span data-stu-id="72e8e-132">**Preference**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72e8e-133">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72e8e-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72e8e-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="72e8e-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72e8e-135">Предпочтение данной записи ресурса между другими пользователями того же владельца.</span><span class="sxs-lookup"><span data-stu-id="72e8e-135">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="72e8e-136">Более низкие значения являются предпочтительными.</span><span class="sxs-lookup"><span data-stu-id="72e8e-136">Lower values are preferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72e8e-137">Требования</span><span class="sxs-lookup"><span data-stu-id="72e8e-137">Requirements</span></span>



| <span data-ttu-id="72e8e-138">Требование</span><span class="sxs-lookup"><span data-stu-id="72e8e-138">Requirement</span></span> | <span data-ttu-id="72e8e-139">Значение</span><span class="sxs-lookup"><span data-stu-id="72e8e-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72e8e-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="72e8e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="72e8e-141">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="72e8e-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="72e8e-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="72e8e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="72e8e-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="72e8e-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="72e8e-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="72e8e-144">Namespace</span></span><br/>                | <span data-ttu-id="72e8e-145">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="72e8e-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="72e8e-146">MOF</span><span class="sxs-lookup"><span data-stu-id="72e8e-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72e8e-147"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72e8e-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72e8e-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72e8e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72e8e-149">**Метод Креатеинстанцефромпропертидата \_ класса Рттипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="72e8e-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="72e8e-150">**Метод Modify \_ класса микрософтднс рттипе**</span><span class="sxs-lookup"><span data-stu-id="72e8e-150">**Modify Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-modify.md)
</dt> <dt>

[<span data-ttu-id="72e8e-151">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="72e8e-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





