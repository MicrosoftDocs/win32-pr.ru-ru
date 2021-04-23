---
title: Класс MicrosoftDNS_MXType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись ресурса почтового обменника (MR).
ms.assetid: 7c147628-5bda-48dd-beb4-e630d1886da8
keywords:
- DNS класса MicrosoftDNS_MXType
- DNS-MicrosoftDNS_MXType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType
- MicrosoftDNS_MXType.CreateInstanceFromPropertyData
- MicrosoftDNS_MXType.Modify
- MicrosoftDNS_MXType.Preference
- MicrosoftDNS_MXType.MailExchange
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652743178b71b2f9fed296ecfa4427f85b5cf1c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988657"
---
# <a name="microsoftdns_mxtype-class"></a><span data-ttu-id="9ac21-105">\_Класс микрософтднс мкстипе</span><span class="sxs-lookup"><span data-stu-id="9ac21-105">MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="9ac21-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись ресурса почтового обменника (MR).</span><span class="sxs-lookup"><span data-stu-id="9ac21-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Exchanger (MR) RR.</span></span>

<span data-ttu-id="9ac21-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="9ac21-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ac21-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ac21-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MXType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string MailExchange;
};
```

## <a name="members"></a><span data-ttu-id="9ac21-109">Члены</span><span class="sxs-lookup"><span data-stu-id="9ac21-109">Members</span></span>

<span data-ttu-id="9ac21-110">Класс **микрософтднс \_ мкстипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9ac21-110">The **MicrosoftDNS\_MXType** class has these types of members:</span></span>

-   [<span data-ttu-id="9ac21-111">Методы</span><span class="sxs-lookup"><span data-stu-id="9ac21-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="9ac21-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ac21-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9ac21-113">Методы</span><span class="sxs-lookup"><span data-stu-id="9ac21-113">Methods</span></span>

<span data-ttu-id="9ac21-114">Класс **микрософтднс \_ мкстипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9ac21-114">The **MicrosoftDNS\_MXType** class has these methods.</span></span>



| <span data-ttu-id="9ac21-115">Метод</span><span class="sxs-lookup"><span data-stu-id="9ac21-115">Method</span></span>                             | <span data-ttu-id="9ac21-116">Описание</span><span class="sxs-lookup"><span data-stu-id="9ac21-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ac21-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="9ac21-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="9ac21-118">Создает объект MX типа RR на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца, класс (по умолчанию — IN), значение срока жизни, параметры записи и имя узла, которые должны быть обменом почтой.</span><span class="sxs-lookup"><span data-stu-id="9ac21-118">Instantiates an MX Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, record preference, and host name willing to be a mail exchange.</span></span> <span data-ttu-id="9ac21-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="9ac21-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="9ac21-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="9ac21-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="9ac21-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="9ac21-121">**Modify**</span></span>                         | <span data-ttu-id="9ac21-122">Обновляет параметры TTL, предпочтения и почтового обмена на значения, указанные в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="9ac21-122">Updates the TTL, Preference, and Mail Exchange to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="9ac21-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="9ac21-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="9ac21-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="9ac21-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="9ac21-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="9ac21-125">Qualifiers: Implemented</span></span><br/>                         |



 

### <a name="properties"></a><span data-ttu-id="9ac21-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ac21-126">Properties</span></span>

<span data-ttu-id="9ac21-127">Класс **микрософтднс \_ мкстипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9ac21-127">The **MicrosoftDNS\_MXType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ac21-128">**маилексчанже**</span><span class="sxs-lookup"><span data-stu-id="9ac21-128">**MailExchange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ac21-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ac21-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ac21-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ac21-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ac21-131">Полное доменное имя с указанием узла, который будет использоваться в качестве почтового обмена для имени владельца.</span><span class="sxs-lookup"><span data-stu-id="9ac21-131">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="9ac21-132">**Закрыт**</span><span class="sxs-lookup"><span data-stu-id="9ac21-132">**Preference**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ac21-133">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ac21-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9ac21-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ac21-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ac21-135">Предпочтение данной записи ресурса между другими пользователями того же владельца.</span><span class="sxs-lookup"><span data-stu-id="9ac21-135">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="9ac21-136">Более низкие значения являются предпочтительными.</span><span class="sxs-lookup"><span data-stu-id="9ac21-136">Lower values are preferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ac21-137">Требования</span><span class="sxs-lookup"><span data-stu-id="9ac21-137">Requirements</span></span>



| <span data-ttu-id="9ac21-138">Требование</span><span class="sxs-lookup"><span data-stu-id="9ac21-138">Requirement</span></span> | <span data-ttu-id="9ac21-139">Значение</span><span class="sxs-lookup"><span data-stu-id="9ac21-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ac21-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ac21-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9ac21-141">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9ac21-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9ac21-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ac21-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9ac21-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9ac21-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9ac21-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9ac21-144">Namespace</span></span><br/>                | <span data-ttu-id="9ac21-145">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="9ac21-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9ac21-146">MOF</span><span class="sxs-lookup"><span data-stu-id="9ac21-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ac21-147"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ac21-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ac21-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ac21-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ac21-149">**Метод Креатеинстанцефромпропертидата \_ класса Мкстипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="9ac21-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="9ac21-150">**Метод Modify \_ класса микрософтднс мкстипе**</span><span class="sxs-lookup"><span data-stu-id="9ac21-150">**Modify Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-modify.md)
</dt> <dt>

[<span data-ttu-id="9ac21-151">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="9ac21-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





