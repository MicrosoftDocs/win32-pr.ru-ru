---
title: Метод Фетчрепортсуммарентриес класса Win32_TSLicenseReport
description: Извлекает сводные данные по клиентским лицензиям службы удаленных рабочих столов на пользователя (RDS \ 160; CAL на пользователя) из отчета.
ms.assetid: 0312B787-83E9-42FC-B21B-904B804C5C94
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Фетчрепортсуммарентриес
- Службы удаленных рабочих столов метода Фетчрепортсуммарентриес, класс Win32_TSLicenseReport
- Класс Win32_TSLicenseReport службы удаленных рабочих столов, метод Фетчрепортсуммарентриес
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e47100c71e195cacb6a1004975955eae778765a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135243"
---
# <a name="fetchreportsummaryentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="fac82-106">Метод Фетчрепортсуммарентриес \_ класса Win32 тслиценсерепорт</span><span class="sxs-lookup"><span data-stu-id="fac82-106">FetchReportSummaryEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="fac82-107">Возвращает сводные данные о лицензиях на клиентский доступ службы удаленных рабочих столов на пользователя (клиентские лицензии RDS на пользователя) из отчета.</span><span class="sxs-lookup"><span data-stu-id="fac82-107">Retrieves summaries of Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="fac82-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fac82-108">Syntax</span></span>


```mof
uint32 FetchReportSummaryEntries(
  [in]      uint32                            StartIndex,
  [in, out] uint32                            Count,
  [out]     Win32_TSLicenseReportSummaryEntry ReportSummaryEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="fac82-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fac82-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fac82-110">*StartIndex* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fac82-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fac82-111">Индекс первой записи отчета, которая должна быть получена.</span><span class="sxs-lookup"><span data-stu-id="fac82-111">Index of the first report entry to be received.</span></span> <span data-ttu-id="fac82-112">Первая запись отчета имеет нулевой индекс.</span><span class="sxs-lookup"><span data-stu-id="fac82-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="fac82-113">*Количество* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="fac82-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fac82-114">Число записей отчета, извлекаемых из объекта отчета.</span><span class="sxs-lookup"><span data-stu-id="fac82-114">Number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="fac82-115">Нулевое значение указывает, что необходимо извлечь все записи отчета, начиная с *startIndex* .</span><span class="sxs-lookup"><span data-stu-id="fac82-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="fac82-116">При возврате содержит количество записей в массиве *репортсуммарентриес* .</span><span class="sxs-lookup"><span data-stu-id="fac82-116">On return, contains the number of entries in the *ReportSummaryEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="fac82-117">*Репортсуммарентриес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fac82-117">*ReportSummaryEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fac82-118">Возвращает массив классов [**Win32 \_ тслиценсерепортсуммарентри**](win32-tslicensereportsummaryentry.md) .</span><span class="sxs-lookup"><span data-stu-id="fac82-118">Returns an array of [**Win32\_TSLicenseReportSummaryEntry**](win32-tslicensereportsummaryentry.md) classes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fac82-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fac82-119">Return value</span></span>

<span data-ttu-id="fac82-120">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="fac82-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fac82-121">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="fac82-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fac82-122">Значение **лсервер \_ I \_ \_ unmore \_ Data** (0x4001) означает, что больше нет записей отчетов.</span><span class="sxs-lookup"><span data-stu-id="fac82-122">A value of **LSERVER\_I\_NO\_MORE\_DATA** (0x4001) indicates that there are no more report entries.</span></span>

## <a name="remarks"></a><span data-ttu-id="fac82-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fac82-123">Remarks</span></span>

<span data-ttu-id="fac82-124">Это не статический метод.</span><span class="sxs-lookup"><span data-stu-id="fac82-124">This is not a static method.</span></span> <span data-ttu-id="fac82-125">Этот метод должен вызываться из объекта отчета об использовании лицензий на пользователя.</span><span class="sxs-lookup"><span data-stu-id="fac82-125">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="fac82-126">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="fac82-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fac82-127">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="fac82-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fac82-128">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="fac82-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fac82-129">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="fac82-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fac82-130">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fac82-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fac82-131">Требования</span><span class="sxs-lookup"><span data-stu-id="fac82-131">Requirements</span></span>



| <span data-ttu-id="fac82-132">Требование</span><span class="sxs-lookup"><span data-stu-id="fac82-132">Requirement</span></span> | <span data-ttu-id="fac82-133">Значение</span><span class="sxs-lookup"><span data-stu-id="fac82-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fac82-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fac82-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fac82-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fac82-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="fac82-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fac82-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fac82-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fac82-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="fac82-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fac82-138">Namespace</span></span><br/>                | <span data-ttu-id="fac82-139">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="fac82-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="fac82-140">MOF</span><span class="sxs-lookup"><span data-stu-id="fac82-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fac82-141"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fac82-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fac82-142">DLL</span><span class="sxs-lookup"><span data-stu-id="fac82-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fac82-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fac82-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fac82-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fac82-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac82-145">**\_Тслиценсерепорт Win32**</span><span class="sxs-lookup"><span data-stu-id="fac82-145">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="fac82-146">**\_Тслиценсерепортсуммарентри Win32**</span><span class="sxs-lookup"><span data-stu-id="fac82-146">**Win32\_TSLicenseReportSummaryEntry**</span></span>](win32-tslicensereportsummaryentry.md)
</dt> </dl>

 

