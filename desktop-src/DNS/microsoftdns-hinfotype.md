---
title: Класс MicrosoftDNS_HINFOType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись сведений об узле (HINFO).
ms.assetid: c6591010-0fe6-45b2-9032-9f847237ecf6
keywords:
- DNS класса MicrosoftDNS_HINFOType
- DNS-MicrosoftDNS_HINFOType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType
- MicrosoftDNS_HINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_HINFOType.Modify
- MicrosoftDNS_HINFOType.CPU
- MicrosoftDNS_HINFOType.OS
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3298e5a7f90dbaee24e5014b1a3aab76ad6997
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654563"
---
# <a name="microsoftdns_hinfotype-class"></a><span data-ttu-id="6fa48-105">\_Класс микрософтднс хинфотипе</span><span class="sxs-lookup"><span data-stu-id="6fa48-105">MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="6fa48-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись сведений об узле (HINFO).</span><span class="sxs-lookup"><span data-stu-id="6fa48-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Host Information (HINFO) record.</span></span>

<span data-ttu-id="6fa48-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="6fa48-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fa48-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6fa48-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_HINFOType : MicrosoftDNS_ResourceRecord
{
  string CPU;
  string OS;
};
```

## <a name="members"></a><span data-ttu-id="6fa48-109">Члены</span><span class="sxs-lookup"><span data-stu-id="6fa48-109">Members</span></span>

<span data-ttu-id="6fa48-110">Класс **микрософтднс \_ хинфотипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6fa48-110">The **MicrosoftDNS\_HINFOType** class has these types of members:</span></span>

-   [<span data-ttu-id="6fa48-111">Методы</span><span class="sxs-lookup"><span data-stu-id="6fa48-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="6fa48-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="6fa48-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6fa48-113">Методы</span><span class="sxs-lookup"><span data-stu-id="6fa48-113">Methods</span></span>

<span data-ttu-id="6fa48-114">Класс **микрософтднс \_ хинфотипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6fa48-114">The **MicrosoftDNS\_HINFOType** class has these methods.</span></span>



| <span data-ttu-id="6fa48-115">Метод</span><span class="sxs-lookup"><span data-stu-id="6fa48-115">Method</span></span>                             | <span data-ttu-id="6fa48-116">Описание</span><span class="sxs-lookup"><span data-stu-id="6fa48-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa48-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="6fa48-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="6fa48-118">Создает экземпляр ресурса RR на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца, класс (по умолчанию — IN), значение срока жизни, а также типы ресурсов ЦП и операционной системы узла.</span><span class="sxs-lookup"><span data-stu-id="6fa48-118">Instantiates an HINFO of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the host's CPU and operating system types.</span></span> <span data-ttu-id="6fa48-119">Он возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="6fa48-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="6fa48-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="6fa48-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="6fa48-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="6fa48-121">**Modify**</span></span>                         | <span data-ttu-id="6fa48-122">Обновляет значения TTL, CPU и операционной системы до значений, указанных в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="6fa48-122">Updates the TTL, CPU, and operating system to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="6fa48-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="6fa48-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="6fa48-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="6fa48-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="6fa48-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="6fa48-125">Qualifiers: Implemented</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="6fa48-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="6fa48-126">Properties</span></span>

<span data-ttu-id="6fa48-127">Класс **микрософтднс \_ хинфотипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6fa48-127">The **MicrosoftDNS\_HINFOType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6fa48-128">**ЦП**</span><span class="sxs-lookup"><span data-stu-id="6fa48-128">**CPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fa48-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6fa48-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fa48-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6fa48-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fa48-131">Тип ЦП владельца записи.</span><span class="sxs-lookup"><span data-stu-id="6fa48-131">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="6fa48-132">**ОС**</span><span class="sxs-lookup"><span data-stu-id="6fa48-132">**OS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fa48-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6fa48-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fa48-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6fa48-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fa48-135">Операционная система владельца записи.</span><span class="sxs-lookup"><span data-stu-id="6fa48-135">Operating system of the record owner.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6fa48-136">Требования</span><span class="sxs-lookup"><span data-stu-id="6fa48-136">Requirements</span></span>



| <span data-ttu-id="6fa48-137">Требование</span><span class="sxs-lookup"><span data-stu-id="6fa48-137">Requirement</span></span> | <span data-ttu-id="6fa48-138">Значение</span><span class="sxs-lookup"><span data-stu-id="6fa48-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa48-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6fa48-139">Minimum supported client</span></span><br/> | <span data-ttu-id="6fa48-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6fa48-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6fa48-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6fa48-141">Minimum supported server</span></span><br/> | <span data-ttu-id="6fa48-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6fa48-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6fa48-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6fa48-143">Namespace</span></span><br/>                | <span data-ttu-id="6fa48-144">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="6fa48-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6fa48-145">MOF</span><span class="sxs-lookup"><span data-stu-id="6fa48-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6fa48-146"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6fa48-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fa48-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6fa48-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fa48-148">**Метод Креатеинстанцефромпропертидата \_ класса Хинфотипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="6fa48-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="6fa48-149">**Метод Modify \_ класса микрософтднс хинфотипе**</span><span class="sxs-lookup"><span data-stu-id="6fa48-149">**Modify Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="6fa48-150">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="6fa48-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





