---
title: Класс MicrosoftDNS_ATMAType
description: Подкласс Микрософтднс \_ ресаурцерекорд, представляющий запись адреса ATM в имя (ATMA).
ms.assetid: 3e9e4032-08a0-4a2e-bcff-f461b69a44d4
keywords:
- DNS класса MicrosoftDNS_ATMAType
- DNS-MicrosoftDNS_ATMAType класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
- MicrosoftDNS_ATMAType.Modify
- MicrosoftDNS_ATMAType.Format
- MicrosoftDNS_ATMAType.ATMAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 237dc4ecb657e79e835abcfdacf90844fb05c5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988661"
---
# <a name="microsoftdns_atmatype-class"></a><span data-ttu-id="dd4cb-105">\_Класс микрософтднс атматипе</span><span class="sxs-lookup"><span data-stu-id="dd4cb-105">MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="dd4cb-106">Подкласс [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) , представляющий запись адреса ATM в имя (ATMA).</span><span class="sxs-lookup"><span data-stu-id="dd4cb-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an ATM Address to Name (ATMA) record.</span></span>

<span data-ttu-id="dd4cb-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="dd4cb-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd4cb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd4cb-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ATMAType : MicrosoftDNS_ResourceRecord
{
  uint16 Format;
  string ATMAddress;
};
```

## <a name="members"></a><span data-ttu-id="dd4cb-109">Члены</span><span class="sxs-lookup"><span data-stu-id="dd4cb-109">Members</span></span>

<span data-ttu-id="dd4cb-110">Класс **микрософтднс \_ атматипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dd4cb-110">The **MicrosoftDNS\_ATMAType** class has these types of members:</span></span>

-   [<span data-ttu-id="dd4cb-111">Методы</span><span class="sxs-lookup"><span data-stu-id="dd4cb-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="dd4cb-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="dd4cb-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dd4cb-113">Методы</span><span class="sxs-lookup"><span data-stu-id="dd4cb-113">Methods</span></span>

<span data-ttu-id="dd4cb-114">Класс **микрософтднс \_ атматипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="dd4cb-114">The **MicrosoftDNS\_ATMAType** class has these methods.</span></span>



| <span data-ttu-id="dd4cb-115">Метод</span><span class="sxs-lookup"><span data-stu-id="dd4cb-115">Method</span></span>                             | <span data-ttu-id="dd4cb-116">Описание</span><span class="sxs-lookup"><span data-stu-id="dd4cb-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd4cb-117">**креатеинстанцефромпропертидата**</span><span class="sxs-lookup"><span data-stu-id="dd4cb-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="dd4cb-118">Создает экземпляр записи ресурса ATMA на основе данных в входных параметрах метода: имя DNS-сервера записи, имя контейнера, имя владельца или узла, класс (по умолчанию — IN), значение срока жизни и формат ATM и адрес.</span><span class="sxs-lookup"><span data-stu-id="dd4cb-118">Instantiates an ATMA Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Node Name, class (default = IN), time-to-live value, and ATM format and address.</span></span> <span data-ttu-id="dd4cb-119">Возвращает ссылку на новый объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="dd4cb-119">Returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="dd4cb-120">Квалификаторы: реализованные, статические</span><span class="sxs-lookup"><span data-stu-id="dd4cb-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="dd4cb-121">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="dd4cb-121">**Modify**</span></span>                         | <span data-ttu-id="dd4cb-122">Обновляет параметры TTL, Format и ATMA на значения, указанные в качестве входных параметров этого метода.</span><span class="sxs-lookup"><span data-stu-id="dd4cb-122">Updates the TTL, Format and ATMA Address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="dd4cb-123">Если новое значение параметра не указано, текущее значение параметра не изменяется.</span><span class="sxs-lookup"><span data-stu-id="dd4cb-123">If a new value for a parameter is not specified, the current value for the parameter is not changed.</span></span> <span data-ttu-id="dd4cb-124">Метод возвращает ссылку на измененный объект в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="dd4cb-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="dd4cb-125">Квалификаторы: Реализовано</span><span class="sxs-lookup"><span data-stu-id="dd4cb-125">Qualifiers: Implemented</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="dd4cb-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="dd4cb-126">Properties</span></span>

<span data-ttu-id="dd4cb-127">Класс **микрософтднс \_ атматипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dd4cb-127">The **MicrosoftDNS\_ATMAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd4cb-128">**атмаддресс**</span><span class="sxs-lookup"><span data-stu-id="dd4cb-128">**ATMAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd4cb-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd4cb-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd4cb-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd4cb-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd4cb-131">Строка переменной длины октетов, содержащая ATM-адрес узла или владельца, к которому относится эта запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd4cb-131">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="dd4cb-132">Первые 4 байта массива используются для хранения размера строки октета.</span><span class="sxs-lookup"><span data-stu-id="dd4cb-132">The first 4 bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="dd4cb-133">Наиболее значимый байт хранится в байте 0.</span><span class="sxs-lookup"><span data-stu-id="dd4cb-133">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="dd4cb-134">**Формат**</span><span class="sxs-lookup"><span data-stu-id="dd4cb-134">**Format**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd4cb-135">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd4cb-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd4cb-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd4cb-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd4cb-137">Формат адреса ATM.</span><span class="sxs-lookup"><span data-stu-id="dd4cb-137">ATM address format.</span></span> <span data-ttu-id="dd4cb-138">Допустимые значения: 0, указывающий формат адреса конечной системы (АЕСА) ATM, а 1 — формат E. 164.</span><span class="sxs-lookup"><span data-stu-id="dd4cb-138">Valid values are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd4cb-139">Требования</span><span class="sxs-lookup"><span data-stu-id="dd4cb-139">Requirements</span></span>



| <span data-ttu-id="dd4cb-140">Требование</span><span class="sxs-lookup"><span data-stu-id="dd4cb-140">Requirement</span></span> | <span data-ttu-id="dd4cb-141">Значение</span><span class="sxs-lookup"><span data-stu-id="dd4cb-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd4cb-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd4cb-142">Minimum supported client</span></span><br/> | <span data-ttu-id="dd4cb-143">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dd4cb-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dd4cb-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd4cb-144">Minimum supported server</span></span><br/> | <span data-ttu-id="dd4cb-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dd4cb-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dd4cb-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dd4cb-146">Namespace</span></span><br/>                | <span data-ttu-id="dd4cb-147">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="dd4cb-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="dd4cb-148">MOF</span><span class="sxs-lookup"><span data-stu-id="dd4cb-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd4cb-149"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd4cb-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd4cb-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd4cb-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd4cb-151">**Метод Креатеинстанцефромпропертидата \_ класса Атматипе микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="dd4cb-151">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="dd4cb-152">**Метод Modify \_ класса микрософтднс атматипе**</span><span class="sxs-lookup"><span data-stu-id="dd4cb-152">**Modify Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-modify.md)
</dt> <dt>

[<span data-ttu-id="dd4cb-153">**Микрософтднс \_ ресаурцерекорд**</span><span class="sxs-lookup"><span data-stu-id="dd4cb-153">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





