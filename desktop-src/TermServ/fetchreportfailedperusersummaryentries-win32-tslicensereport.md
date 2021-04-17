---
title: Метод Фетчрепортфаиледперусерсуммарентриес класса Win32_TSLicenseReport
description: Получение сводных данных о неудачных службы удаленных рабочих столов клиентских лицензиях для каждого пользователя (RDS \ 160; CAL на пользователя) из отчета.
ms.assetid: dc9c4a36-b2a8-407e-b902-ee9d51227909
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Фетчрепортфаиледперусерсуммарентриес
- Службы удаленных рабочих столов метода Фетчрепортфаиледперусерсуммарентриес, класс Win32_TSLicenseReport
- Класс Win32_TSLicenseReport службы удаленных рабочих столов, метод Фетчрепортфаиледперусерсуммарентриес
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5219c2c854e04dabf8b5bfe0b5b70a07bbc3c57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682089"
---
# <a name="fetchreportfailedperusersummaryentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="2bb8a-106">Метод Фетчрепортфаиледперусерсуммарентриес \_ класса Win32 тслиценсерепорт</span><span class="sxs-lookup"><span data-stu-id="2bb8a-106">FetchReportFailedPerUserSummaryEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="2bb8a-107">Получение сводных данных о неудачных службы удаленных рабочих столов клиентских лицензиях на клиентские лицензии (RDS на пользователя) из отчета.</span><span class="sxs-lookup"><span data-stu-id="2bb8a-107">Retrieves summary information of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bb8a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2bb8a-108">Syntax</span></span>


```mof
uint32 FetchReportFailedPerUserSummaryEntries(
  [in]      uint32                                         StartIndex,
  [in, out] uint32                                         Count,
  [out]     Win32_TSLicenseReportFailedPerUserSummaryEntry ReportFailedPerUserSummaryEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="2bb8a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2bb8a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bb8a-110">*StartIndex* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2bb8a-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bb8a-111">Индекс первой записи отчета для извлечения.</span><span class="sxs-lookup"><span data-stu-id="2bb8a-111">The index of the first report entry to be retrieved.</span></span> <span data-ttu-id="2bb8a-112">Первая запись отчета имеет нулевой индекс.</span><span class="sxs-lookup"><span data-stu-id="2bb8a-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="2bb8a-113">*Количество* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="2bb8a-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2bb8a-114">Число записей отчета, извлекаемых из объекта отчета.</span><span class="sxs-lookup"><span data-stu-id="2bb8a-114">The number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="2bb8a-115">Нулевое значение указывает, что необходимо извлечь все записи отчета, начиная с *startIndex* .</span><span class="sxs-lookup"><span data-stu-id="2bb8a-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="2bb8a-116">При возврате содержит количество записей в массиве *репортфаиледперусерсуммарентриес* .</span><span class="sxs-lookup"><span data-stu-id="2bb8a-116">On return, contains the number of entries in the *ReportFailedPerUserSummaryEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="2bb8a-117">*Репортфаиледперусерсуммарентриес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2bb8a-117">*ReportFailedPerUserSummaryEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2bb8a-118">Массив классов [**Win32 \_ тслиценсерепортфаиледперусерсуммарентри**](win32-tslicensereportfailedperusersummaryentry.md) , представляющих полученные записи лицензий.</span><span class="sxs-lookup"><span data-stu-id="2bb8a-118">An array of [**Win32\_TSLicenseReportFailedPerUserSummaryEntry**](win32-tslicensereportfailedperusersummaryentry.md) classes that represent the license entries retrieved.</span></span> <span data-ttu-id="2bb8a-119">Параметр *Count* содержит количество элементов в этом массиве.</span><span class="sxs-lookup"><span data-stu-id="2bb8a-119">The *Count* parameter contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bb8a-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2bb8a-120">Return value</span></span>

<span data-ttu-id="2bb8a-121">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="2bb8a-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2bb8a-122">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="2bb8a-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2bb8a-123">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2bb8a-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2bb8a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="2bb8a-124">Requirements</span></span>



| <span data-ttu-id="2bb8a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="2bb8a-125">Requirement</span></span> | <span data-ttu-id="2bb8a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2bb8a-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bb8a-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2bb8a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2bb8a-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2bb8a-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="2bb8a-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2bb8a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2bb8a-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2bb8a-130">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="2bb8a-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2bb8a-131">Namespace</span></span><br/>                | <span data-ttu-id="2bb8a-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="2bb8a-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="2bb8a-133">MOF</span><span class="sxs-lookup"><span data-stu-id="2bb8a-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2bb8a-134"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2bb8a-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2bb8a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2bb8a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bb8a-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bb8a-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bb8a-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2bb8a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bb8a-138">**\_Тслиценсерепорт Win32**</span><span class="sxs-lookup"><span data-stu-id="2bb8a-138">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

 





