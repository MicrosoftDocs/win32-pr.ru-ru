---
title: Метод Фетчрепортфаиледперусерентриес класса Win32_TSLicenseReport
description: Получение сведений о неудачных службы удаленных рабочих столов клиентских лицензиях для каждого пользователя (RDS \ 160; CAL на пользователя) из отчета.
ms.assetid: 2c16723c-1755-4ec1-a6db-55d769f8b6fd
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Фетчрепортфаиледперусерентриес
- Службы удаленных рабочих столов метода Фетчрепортфаиледперусерентриес, класс Win32_TSLicenseReport
- Класс Win32_TSLicenseReport службы удаленных рабочих столов, метод Фетчрепортфаиледперусерентриес
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 159f980944c70dbad4c6948a614d0c9964a5f0cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535231"
---
# <a name="fetchreportfailedperuserentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="4b9b9-106">Метод Фетчрепортфаиледперусерентриес \_ класса Win32 тслиценсерепорт</span><span class="sxs-lookup"><span data-stu-id="4b9b9-106">FetchReportFailedPerUserEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="4b9b9-107">Получает сведения о неудачных службы удаленных рабочих столов клиентских лицензиях на клиентские лицензии (RDS на пользователя) из отчета.</span><span class="sxs-lookup"><span data-stu-id="4b9b9-107">Retrieves details of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b9b9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b9b9-108">Syntax</span></span>


```mof
uint32 FetchReportFailedPerUserEntries(
  [in]      uint32                                  StartIndex,
  [in, out] uint32                                  Count,
  [out]     Win32_TSLicenseReportFailedPerUserEntry ReportFailedPerUserEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="4b9b9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b9b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b9b9-110">*StartIndex* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b9b9-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b9b9-111">Индекс первой записи отчета для извлечения.</span><span class="sxs-lookup"><span data-stu-id="4b9b9-111">The index of the first report entry to be retrieved.</span></span> <span data-ttu-id="4b9b9-112">Первая запись отчета имеет нулевой индекс.</span><span class="sxs-lookup"><span data-stu-id="4b9b9-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="4b9b9-113">*Количество* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="4b9b9-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b9b9-114">Число записей отчета, извлекаемых из объекта отчета.</span><span class="sxs-lookup"><span data-stu-id="4b9b9-114">The number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="4b9b9-115">Нулевое значение указывает, что необходимо извлечь все записи отчета, начиная с *startIndex* .</span><span class="sxs-lookup"><span data-stu-id="4b9b9-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="4b9b9-116">При возврате содержит количество записей в массиве *репортфаиледперусерентриес* .</span><span class="sxs-lookup"><span data-stu-id="4b9b9-116">On return, contains the number of entries in the *ReportFailedPerUserEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="4b9b9-117">*Репортфаиледперусерентриес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4b9b9-117">*ReportFailedPerUserEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b9b9-118">Массив классов [**Win32 \_ тслиценсерепортфаиледперусерентри**](win32-tslicensereportfailedperuserentry.md) , представляющих полученные записи лицензий.</span><span class="sxs-lookup"><span data-stu-id="4b9b9-118">An array of [**Win32\_TSLicenseReportFailedPerUserEntry**](win32-tslicensereportfailedperuserentry.md) classes that represent the license entries retrieved.</span></span> <span data-ttu-id="4b9b9-119">Параметр *Count* содержит количество элементов в этом массиве.</span><span class="sxs-lookup"><span data-stu-id="4b9b9-119">The *Count* parameter contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b9b9-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b9b9-120">Return value</span></span>

<span data-ttu-id="4b9b9-121">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="4b9b9-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4b9b9-122">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="4b9b9-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4b9b9-123">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4b9b9-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b9b9-124">Требования</span><span class="sxs-lookup"><span data-stu-id="4b9b9-124">Requirements</span></span>



| <span data-ttu-id="4b9b9-125">Требование</span><span class="sxs-lookup"><span data-stu-id="4b9b9-125">Requirement</span></span> | <span data-ttu-id="4b9b9-126">Значение</span><span class="sxs-lookup"><span data-stu-id="4b9b9-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b9b9-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b9b9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4b9b9-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4b9b9-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="4b9b9-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b9b9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4b9b9-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4b9b9-130">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="4b9b9-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4b9b9-131">Namespace</span></span><br/>                | <span data-ttu-id="4b9b9-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="4b9b9-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="4b9b9-133">MOF</span><span class="sxs-lookup"><span data-stu-id="4b9b9-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b9b9-134"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b9b9-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b9b9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4b9b9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b9b9-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b9b9-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b9b9-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b9b9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b9b9-138">**\_Тслиценсерепорт Win32**</span><span class="sxs-lookup"><span data-stu-id="4b9b9-138">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

 





