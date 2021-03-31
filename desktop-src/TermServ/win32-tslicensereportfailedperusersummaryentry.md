---
title: Класс Win32_TSLicenseReportFailedPerUserSummaryEntry
description: Содержит сведения о доменах, для которых не удалось выдачу на пользователя.
ms.assetid: f7265734-ac4d-439f-ae8b-3694e6f81f2a
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSLicenseReportFailedPerUserSummaryEntry службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSLicenseReportFailedPerUserSummaryEntry, описание
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserSummaryEntry
- Win32_TSLicenseReportFailedPerUserSummaryEntry.DomainName
- Win32_TSLicenseReportFailedPerUserSummaryEntry.FailedIssuanceCount
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f086d275c064f5df18ee01a3a38639a40913f3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988254"
---
# <a name="win32_tslicensereportfailedperusersummaryentry-class"></a><span data-ttu-id="faaa4-105">\_Класс Win32 тслиценсерепортфаиледперусерсуммарентри</span><span class="sxs-lookup"><span data-stu-id="faaa4-105">Win32\_TSLicenseReportFailedPerUserSummaryEntry class</span></span>

<span data-ttu-id="faaa4-106">Содержит сведения о доменах, для которых не удалось выдачу на пользователя.</span><span class="sxs-lookup"><span data-stu-id="faaa4-106">Provides details of the domains to which Per User Issuance was failed.</span></span>

<span data-ttu-id="faaa4-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="faaa4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="faaa4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="faaa4-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserSummaryEntry
{
  string DomainName;
  uint32 FailedIssuanceCount;
};
```

## <a name="members"></a><span data-ttu-id="faaa4-109">Члены</span><span class="sxs-lookup"><span data-stu-id="faaa4-109">Members</span></span>

<span data-ttu-id="faaa4-110">Класс **Win32 \_ тслиценсерепортфаиледперусерсуммарентри** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="faaa4-110">The **Win32\_TSLicenseReportFailedPerUserSummaryEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="faaa4-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="faaa4-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="faaa4-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="faaa4-112">Properties</span></span>

<span data-ttu-id="faaa4-113">Класс **Win32 \_ тслиценсерепортфаиледперусерсуммарентри** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="faaa4-113">The **Win32\_TSLicenseReportFailedPerUserSummaryEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="faaa4-114">**Имя_домена**</span><span class="sxs-lookup"><span data-stu-id="faaa4-114">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faaa4-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="faaa4-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="faaa4-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="faaa4-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="faaa4-117">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="faaa4-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="faaa4-118">Указывает имя домена, в котором произошел сбой при выдаче лицензии.</span><span class="sxs-lookup"><span data-stu-id="faaa4-118">Specifies the domain name to which the license issuance failed.</span></span>

</dd> <dt>

<span data-ttu-id="faaa4-119">**фаиледиссуанцекаунт**</span><span class="sxs-lookup"><span data-stu-id="faaa4-119">**FailedIssuanceCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faaa4-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="faaa4-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="faaa4-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="faaa4-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="faaa4-122">Количество неудачных выдачи.</span><span class="sxs-lookup"><span data-stu-id="faaa4-122">The number of failed issuances.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="faaa4-123">Требования</span><span class="sxs-lookup"><span data-stu-id="faaa4-123">Requirements</span></span>



| <span data-ttu-id="faaa4-124">Требование</span><span class="sxs-lookup"><span data-stu-id="faaa4-124">Requirement</span></span> | <span data-ttu-id="faaa4-125">Значение</span><span class="sxs-lookup"><span data-stu-id="faaa4-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="faaa4-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="faaa4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="faaa4-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="faaa4-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="faaa4-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="faaa4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="faaa4-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="faaa4-129">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="faaa4-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="faaa4-130">Namespace</span></span><br/>                | <span data-ttu-id="faaa4-131">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="faaa4-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="faaa4-132">MOF</span><span class="sxs-lookup"><span data-stu-id="faaa4-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="faaa4-133"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="faaa4-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="faaa4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="faaa4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="faaa4-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="faaa4-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faaa4-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="faaa4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faaa4-137">**фетчрепортфаиледперусерсуммарентриес**</span><span class="sxs-lookup"><span data-stu-id="faaa4-137">**FetchReportFailedPerUserSummaryEntries**</span></span>](fetchreportfailedperusersummaryentries-win32-tslicensereport.md)
</dt> </dl>

 

