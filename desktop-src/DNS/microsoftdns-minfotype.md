---
title: Класс MicrosoftDNS_MINFOType
description: Подкласс Микрософтднс \_ ресаурцерекорд, который представляет запись почтовой информации (MINFO).
ms.assetid: 9c4b70b8-f9cf-4dea-8d2d-43e0de002d52
keywords:
- DNS класса MicrosoftDNS_MINFOType
- DNS-MicrosoftDNS_MINFOType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_MINFOType.Modify
- MicrosoftDNS_MINFOType.ResponsibleMailbox
- MicrosoftDNS_MINFOType.ErrorMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a7d230db9da32ce47cd4cfaf99c4978c4e63385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137403"
---
# <a name="microsoftdns_minfotype-class"></a><span data-ttu-id="7581a-105">\_Класс микрософтднс минфотипе</span><span class="sxs-lookup"><span data-stu-id="7581a-105">MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="7581a-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , который представляет запись почтовой информации (MINFO).</span><span class="sxs-lookup"><span data-stu-id="7581a-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Information (MINFO) record.</span></span>

<span data-ttu-id="7581a-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="7581a-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7581a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7581a-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MINFOType : MicrosoftDNS_ResourceRecord
{
  string ResponsibleMailbox;
  string ErrorMailbox;
};
```

## <a name="members"></a><span data-ttu-id="7581a-109">Члены</span><span class="sxs-lookup"><span data-stu-id="7581a-109">Members</span></span>

<span data-ttu-id="7581a-110">Класс **микрософтднс \_ минфотипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7581a-110">The **MicrosoftDNS\_MINFOType** class has these types of members:</span></span>

-   [<span data-ttu-id="7581a-111">Методы</span><span class="sxs-lookup"><span data-stu-id="7581a-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="7581a-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="7581a-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7581a-113">Методы</span><span class="sxs-lookup"><span data-stu-id="7581a-113">Methods</span></span>

<span data-ttu-id="7581a-114">Класс **микрософтднс \_ минфотипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7581a-114">The **MicrosoftDNS\_MINFOType** class has these methods.</span></span>



| <span data-ttu-id="7581a-115">Метод</span><span class="sxs-lookup"><span data-stu-id="7581a-115">Method</span></span>                             | <span data-ttu-id="7581a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7581a-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7581a-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="7581a-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="7581a-118">Создает экземпляр типа данных класса MINFO на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца почтового списка/Box, класс (по умолчанию = IN), значение срока жизни и ответственные и почтовые ящики ошибок.</span><span class="sxs-lookup"><span data-stu-id="7581a-118">Instantiates an MINFO Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mail list/box, class (default = IN), time-to-live value and the responsible and error mailboxes.</span></span> <span data-ttu-id="7581a-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="7581a-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="7581a-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="7581a-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="7581a-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="7581a-121">**Modify**</span></span>                         | <span data-ttu-id="7581a-122">Этот метод обновляет значения TTL, ответственного за почтовый ящик и почтовый ящик ошибок до значений, указанных в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="7581a-122">This method updates the TTL, Responsible Mailbox, and Error Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="7581a-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="7581a-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="7581a-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="7581a-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="7581a-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="7581a-125">Qualifiers: Implemented</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="7581a-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="7581a-126">Properties</span></span>

<span data-ttu-id="7581a-127">Класс **микрософтднс \_ минфотипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7581a-127">The **MicrosoftDNS\_MINFOType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7581a-128">**еррормаилбокс**</span><span class="sxs-lookup"><span data-stu-id="7581a-128">**ErrorMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7581a-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7581a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7581a-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7581a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7581a-131">Полное доменное имя, указывающее почтовый ящик для получения сообщений об ошибках, относящихся к списку рассылки, или к почтовому ящику, указанному именем владельца записи MINFO.</span><span class="sxs-lookup"><span data-stu-id="7581a-131">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="7581a-132">**респонсиблемаилбокс**</span><span class="sxs-lookup"><span data-stu-id="7581a-132">**ResponsibleMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7581a-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7581a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7581a-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7581a-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7581a-135">Полное доменное имя, указывающее почтовый ящик, отвечающий за список рассылки или почтовый ящик, указанный в имени владельца записи.</span><span class="sxs-lookup"><span data-stu-id="7581a-135">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7581a-136">Требования</span><span class="sxs-lookup"><span data-stu-id="7581a-136">Requirements</span></span>



| <span data-ttu-id="7581a-137">Требование</span><span class="sxs-lookup"><span data-stu-id="7581a-137">Requirement</span></span> | <span data-ttu-id="7581a-138">Значение</span><span class="sxs-lookup"><span data-stu-id="7581a-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7581a-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7581a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7581a-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7581a-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7581a-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7581a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7581a-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7581a-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7581a-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7581a-143">Namespace</span></span><br/>                | <span data-ttu-id="7581a-144">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="7581a-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="7581a-145">MOF</span><span class="sxs-lookup"><span data-stu-id="7581a-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7581a-146"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7581a-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7581a-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7581a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7581a-148">**Метод Креатеинстанцефромпропертидата \_ класса Минфотипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="7581a-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="7581a-149">**Метод Modify \_ класса микрософтднс минфотипе**</span><span class="sxs-lookup"><span data-stu-id="7581a-149">**Modify Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="7581a-150">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="7581a-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





