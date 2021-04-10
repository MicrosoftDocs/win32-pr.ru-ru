---
title: Класс MicrosoftDNS_Statistic
description: '\_Класс статистики микрософтднс представляет собой отдельную статистику DNS-сервера.'
ms.assetid: 49ee79d6-b93f-4a9b-8054-1ad290d092d6
keywords:
- DNS класса MicrosoftDNS_Statistic
- DNS-MicrosoftDNS_Statistic класса, описание
topic_type:
- apiref
api_name:
- MicrosoftDNS_Statistic
- MicrosoftDNS_Statistic.DnsServerName
- MicrosoftDNS_Statistic.CollectionName
- MicrosoftDNS_Statistic.CollectionId
- MicrosoftDNS_Statistic.Name
- MicrosoftDNS_Statistic.Value
- MicrosoftDNS_Statistic.StringValue
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77e26f1738c046e446fa898c4fdff2f6e8855730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071900"
---
# <a name="microsoftdns_statistic-class"></a><span data-ttu-id="9ba7c-105">\_Класс статистики микрософтднс</span><span class="sxs-lookup"><span data-stu-id="9ba7c-105">MicrosoftDNS\_Statistic class</span></span>

<span data-ttu-id="9ba7c-106">Класс **\_ статистики микрософтднс** представляет собой ОТДЕЛЬНУЮ статистику DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-106">The **MicrosoftDNS\_Statistic** class represents a single DNS Server statistic.</span></span>

<span data-ttu-id="9ba7c-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ba7c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ba7c-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_Statistic
{
  string DnsServerName;
  string CollectionName;
  uint32 CollectionId;
  string Name;
  uint32 Value;
  string StringValue;
};
```

## <a name="members"></a><span data-ttu-id="9ba7c-109">Члены</span><span class="sxs-lookup"><span data-stu-id="9ba7c-109">Members</span></span>

<span data-ttu-id="9ba7c-110">Класс **\_ статистики микрософтднс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9ba7c-110">The **MicrosoftDNS\_Statistic** class has these types of members:</span></span>

-   [<span data-ttu-id="9ba7c-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ba7c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ba7c-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ba7c-112">Properties</span></span>

<span data-ttu-id="9ba7c-113">Класс **\_ статистики микрософтднс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-113">The **MicrosoftDNS\_Statistic** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ba7c-114">**CollectionId**</span><span class="sxs-lookup"><span data-stu-id="9ba7c-114">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba7c-115">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ba7c-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba7c-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba7c-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba7c-117">Числовое представление **CollectionName**.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-117">Numeric representation of **CollectionName**.</span></span>

</dd> <dt>

<span data-ttu-id="9ba7c-118">**CollectionName**</span><span class="sxs-lookup"><span data-stu-id="9ba7c-118">**CollectionName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba7c-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ba7c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ba7c-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba7c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba7c-121">Имя коллекции, которой принадлежит статистика.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-121">Name of the collection to which the statistic belongs.</span></span>

</dd> <dt>

<span data-ttu-id="9ba7c-122">**днссервернаме**</span><span class="sxs-lookup"><span data-stu-id="9ba7c-122">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba7c-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ba7c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ba7c-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba7c-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba7c-125">Указывает полное доменное имя (FQDN) или IP-адрес DNS-сервера, содержащего статистику.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-125">Indicates the FQDN or IP address of the DNS Server that contains the statistic.</span></span>

</dd> <dt>

<span data-ttu-id="9ba7c-126">**Name**</span><span class="sxs-lookup"><span data-stu-id="9ba7c-126">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba7c-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ba7c-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ba7c-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba7c-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba7c-129">Имя статистики.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-129">Name of the statistic.</span></span>

</dd> <dt>

<span data-ttu-id="9ba7c-130">**StringValue**</span><span class="sxs-lookup"><span data-stu-id="9ba7c-130">**StringValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba7c-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ba7c-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ba7c-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba7c-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba7c-133">Строковое значение статистики, используемое только в том случае, если значение статистики не представлено в виде DWORD.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-133">String value of the statistic, used only when the statistic value is not represented as a DWORD.</span></span>

</dd> <dt>

<span data-ttu-id="9ba7c-134">**Значение**</span><span class="sxs-lookup"><span data-stu-id="9ba7c-134">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba7c-135">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ba7c-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba7c-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba7c-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba7c-137">Числовое значение статистики, представленное в виде типа DWORD.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-137">Numeric value of the statistic, represented as a DWORD.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ba7c-138">Требования</span><span class="sxs-lookup"><span data-stu-id="9ba7c-138">Requirements</span></span>



| <span data-ttu-id="9ba7c-139">Требование</span><span class="sxs-lookup"><span data-stu-id="9ba7c-139">Requirement</span></span> | <span data-ttu-id="9ba7c-140">Значение</span><span class="sxs-lookup"><span data-stu-id="9ba7c-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ba7c-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ba7c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="9ba7c-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9ba7c-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9ba7c-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ba7c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="9ba7c-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9ba7c-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9ba7c-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9ba7c-145">Namespace</span></span><br/>                | <span data-ttu-id="9ba7c-146">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="9ba7c-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9ba7c-147">MOF</span><span class="sxs-lookup"><span data-stu-id="9ba7c-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ba7c-148"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ba7c-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ba7c-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ba7c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ba7c-150">Микрософтднс \_ статистикколлектион</span><span class="sxs-lookup"><span data-stu-id="9ba7c-150">MicrosoftDNS\_StatisticCollection</span></span>](microsoftdns-statisticcollection.md)
</dt> </dl>

 

 





