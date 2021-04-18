---
title: Метод Фетчрепортпердевицеентриес класса Win32_TSLicenseReport
description: Получение сведений о выданных лицензиях на клиентский доступ службы удаленных рабочих столов на устройство (RDS \ 160; CAL "на устройство") из отчета.
ms.assetid: 3f632a65-d6e0-4efd-9498-d04a05f9ddec
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Фетчрепортпердевицеентриес
- Службы удаленных рабочих столов метода Фетчрепортпердевицеентриес, класс Win32_TSLicenseReport
- Класс Win32_TSLicenseReport службы удаленных рабочих столов, метод Фетчрепортпердевицеентриес
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportPerDeviceEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce77fce941dd0a24fb6ee17e0aeb67b4e78bdae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672843"
---
# <a name="fetchreportperdeviceentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="8dc80-106">Метод Фетчрепортпердевицеентриес \_ класса Win32 тслиценсерепорт</span><span class="sxs-lookup"><span data-stu-id="8dc80-106">FetchReportPerDeviceEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="8dc80-107">Получение сведений о выданных лицензиях на клиентский доступ службы удаленных рабочих столов для каждого устройства (клиентские лицензии служб удаленных рабочих столов на устройство) из отчета.</span><span class="sxs-lookup"><span data-stu-id="8dc80-107">Retrieves information of issued Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dc80-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8dc80-108">Syntax</span></span>


```mof
uint32 FetchReportPerDeviceEntries(
  [in]      uint32                              StartIndex,
  [in, out] uint32                              Count,
  [out]     Win32_TSLicenseReportPerDeviceEntry ReportPerDeviceEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="8dc80-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8dc80-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dc80-110">*StartIndex* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8dc80-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dc80-111">Индекс первой записи отчета для извлечения.</span><span class="sxs-lookup"><span data-stu-id="8dc80-111">The index of the first report entry to be retrieved.</span></span> <span data-ttu-id="8dc80-112">Первая запись отчета имеет нулевой индекс.</span><span class="sxs-lookup"><span data-stu-id="8dc80-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="8dc80-113">*Количество* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="8dc80-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8dc80-114">Число записей отчета, извлекаемых из объекта отчета.</span><span class="sxs-lookup"><span data-stu-id="8dc80-114">The number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="8dc80-115">Нулевое значение указывает, что необходимо извлечь все записи отчета, начиная с *startIndex* .</span><span class="sxs-lookup"><span data-stu-id="8dc80-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="8dc80-116">При возврате содержит количество записей в массиве *репортпердевицеентриес* .</span><span class="sxs-lookup"><span data-stu-id="8dc80-116">On return, contains the number of entries in the *ReportPerDeviceEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="8dc80-117">*Репортпердевицеентриес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8dc80-117">*ReportPerDeviceEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8dc80-118">Массив классов [**Win32 \_ тслиценсерепортпердевицеентри**](win32-tslicensereportperdeviceentry.md) , представляющих полученные записи лицензий.</span><span class="sxs-lookup"><span data-stu-id="8dc80-118">An array of [**Win32\_TSLicenseReportPerDeviceEntry**](win32-tslicensereportperdeviceentry.md) classes the represent the license entries retrieved.</span></span> <span data-ttu-id="8dc80-119">Параметр *Count* содержит количество элементов в этом массиве.</span><span class="sxs-lookup"><span data-stu-id="8dc80-119">The *Count* parameter contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dc80-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8dc80-120">Return value</span></span>

<span data-ttu-id="8dc80-121">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="8dc80-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8dc80-122">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8dc80-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8dc80-123">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8dc80-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8dc80-124">Требования</span><span class="sxs-lookup"><span data-stu-id="8dc80-124">Requirements</span></span>



| <span data-ttu-id="8dc80-125">Требование</span><span class="sxs-lookup"><span data-stu-id="8dc80-125">Requirement</span></span> | <span data-ttu-id="8dc80-126">Значение</span><span class="sxs-lookup"><span data-stu-id="8dc80-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dc80-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8dc80-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8dc80-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8dc80-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="8dc80-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8dc80-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8dc80-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8dc80-130">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="8dc80-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8dc80-131">Namespace</span></span><br/>                | <span data-ttu-id="8dc80-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="8dc80-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="8dc80-133">MOF</span><span class="sxs-lookup"><span data-stu-id="8dc80-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8dc80-134"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8dc80-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8dc80-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8dc80-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8dc80-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8dc80-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dc80-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8dc80-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dc80-138">**\_Тслиценсерепорт Win32**</span><span class="sxs-lookup"><span data-stu-id="8dc80-138">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

 





