---
title: Класс MicrosoftDNS_MGType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись почтовой группы (MG).
ms.assetid: ce5795d1-e575-46ef-ad82-62b329e261d6
keywords:
- DNS класса MicrosoftDNS_MGType
- DNS-MicrosoftDNS_MGType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
- MicrosoftDNS_MGType.Modify
- MicrosoftDNS_MGType.MGMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4772f8841977fbeae1f0bf609a65a9511bc704a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535357"
---
# <a name="microsoftdns_mgtype-class"></a><span data-ttu-id="e1d77-105">\_Класс микрософтднс мгтипе</span><span class="sxs-lookup"><span data-stu-id="e1d77-105">MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="e1d77-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись почтовой группы (MG).</span><span class="sxs-lookup"><span data-stu-id="e1d77-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Group (MG) record.</span></span>

<span data-ttu-id="e1d77-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="e1d77-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d77-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1d77-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MGType : MicrosoftDNS_ResourceRecord
{
  string MGMailbox;
};
```

## <a name="members"></a><span data-ttu-id="e1d77-109">Члены</span><span class="sxs-lookup"><span data-stu-id="e1d77-109">Members</span></span>

<span data-ttu-id="e1d77-110">Класс **микрософтднс \_ мгтипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e1d77-110">The **MicrosoftDNS\_MGType** class has these types of members:</span></span>

-   [<span data-ttu-id="e1d77-111">Методы</span><span class="sxs-lookup"><span data-stu-id="e1d77-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e1d77-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="e1d77-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e1d77-113">Методы</span><span class="sxs-lookup"><span data-stu-id="e1d77-113">Methods</span></span>

<span data-ttu-id="e1d77-114">Класс **микрософтднс \_ мгтипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e1d77-114">The **MicrosoftDNS\_MGType** class has these methods.</span></span>



| <span data-ttu-id="e1d77-115">Метод</span><span class="sxs-lookup"><span data-stu-id="e1d77-115">Method</span></span>                             | <span data-ttu-id="e1d77-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e1d77-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d77-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="e1d77-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="e1d77-118">Этот метод создает тип записи ресурса MG на основе данных в входных параметрах метода: имя DNS-сервера записей, имя контейнера, имя владельца почтовой группы, класс (по умолчанию — IN), значение срока жизни и имя почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="e1d77-118">This method instantiates an MG Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mail group, class (default = IN), time-to-live value and the mailbox name.</span></span> <span data-ttu-id="e1d77-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="e1d77-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="e1d77-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="e1d77-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="e1d77-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="e1d77-121">**Modify**</span></span>                         | <span data-ttu-id="e1d77-122">Этот метод обновляет почтовый ящик TTL и MG значениями, указанными в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="e1d77-122">This method updates the TTL and MG Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="e1d77-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="e1d77-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="e1d77-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="e1d77-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="e1d77-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="e1d77-125">Qualifiers: Implemented</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="e1d77-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="e1d77-126">Properties</span></span>

<span data-ttu-id="e1d77-127">Класс **микрософтднс \_ мгтипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e1d77-127">The **MicrosoftDNS\_MGType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e1d77-128">**мгмаилбокс**</span><span class="sxs-lookup"><span data-stu-id="e1d77-128">**MGMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1d77-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e1d77-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1d77-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e1d77-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1d77-131">Полное доменное имя, указывающее почтовый ящик, который является членом почтовой группы, указанной в имени владельца записи.</span><span class="sxs-lookup"><span data-stu-id="e1d77-131">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1d77-132">Требования</span><span class="sxs-lookup"><span data-stu-id="e1d77-132">Requirements</span></span>



| <span data-ttu-id="e1d77-133">Требование</span><span class="sxs-lookup"><span data-stu-id="e1d77-133">Requirement</span></span> | <span data-ttu-id="e1d77-134">Значение</span><span class="sxs-lookup"><span data-stu-id="e1d77-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d77-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e1d77-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e1d77-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e1d77-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e1d77-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e1d77-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e1d77-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e1d77-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e1d77-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e1d77-139">Namespace</span></span><br/>                | <span data-ttu-id="e1d77-140">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="e1d77-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e1d77-141">MOF</span><span class="sxs-lookup"><span data-stu-id="e1d77-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1d77-142"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1d77-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1d77-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1d77-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d77-144">**Метод Креатеинстанцефромпропертидата \_ класса Мгтипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="e1d77-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="e1d77-145">**Метод Modify \_ класса микрософтднс мгтипе**</span><span class="sxs-lookup"><span data-stu-id="e1d77-145">**Modify Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-modify.md)
</dt> <dt>

[<span data-ttu-id="e1d77-146">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="e1d77-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





