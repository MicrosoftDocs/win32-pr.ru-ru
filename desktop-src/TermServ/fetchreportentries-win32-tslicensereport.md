---
title: Метод Фетчрепортентриес класса Win32_TSLicenseReport
description: Получение сведений о лицензиях на клиентский доступ службы удаленных рабочих столов на пользователя (RDS \ 160; CAL на пользователя) из отчета. Каждая запись представляет собой RDS \ 160; Клиентская лицензия "на пользователя", используемая в данный момент.
ms.assetid: 151ff95c-4ad3-4d19-936d-1cb08b4d5056
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Фетчрепортентриес
- Службы удаленных рабочих столов метода Фетчрепортентриес, класс Win32_TSLicenseReport
- Класс Win32_TSLicenseReport службы удаленных рабочих столов, метод Фетчрепортентриес
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc64c9591444307ba0519da02cf9c6f13d20252e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535234"
---
# <a name="fetchreportentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="7d473-107">Метод Фетчрепортентриес \_ класса Win32 тслиценсерепорт</span><span class="sxs-lookup"><span data-stu-id="7d473-107">FetchReportEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="7d473-108">Получение сведений о клиентских лицензиях службы удаленных рабочих столов на пользователя (клиентские лицензии RDS на пользователя) из отчета.</span><span class="sxs-lookup"><span data-stu-id="7d473-108">Retrieves details of Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span> <span data-ttu-id="7d473-109">Каждая запись представляет собой клиентскую лицензию RDS "на пользователя", которая используется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="7d473-109">Each entry represents a RDS Per User CAL that is currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d473-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d473-110">Syntax</span></span>


```mof
uint32 FetchReportEntries(
  [in]      uint32                     StartIndex,
  [in, out] uint32                     Count,
  [out]     Win32_TSLicenseReportEntry ReportEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="7d473-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d473-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d473-112">*StartIndex* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7d473-112">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d473-113">Индекс первой записи отчета, которая должна быть получена.</span><span class="sxs-lookup"><span data-stu-id="7d473-113">Index of the first report entry to be received.</span></span> <span data-ttu-id="7d473-114">Первая запись отчета имеет нулевой индекс.</span><span class="sxs-lookup"><span data-stu-id="7d473-114">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="7d473-115">*Количество* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="7d473-115">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d473-116">Число записей отчета, извлекаемых из объекта отчета.</span><span class="sxs-lookup"><span data-stu-id="7d473-116">Number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="7d473-117">Нулевое значение указывает, что необходимо извлечь все записи отчета, начиная с *startIndex* .</span><span class="sxs-lookup"><span data-stu-id="7d473-117">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="7d473-118">При возврате содержит количество записей в массиве *репортентриес* .</span><span class="sxs-lookup"><span data-stu-id="7d473-118">On return, contains the number of entries in the *ReportEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="7d473-119">*Репортентриес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7d473-119">*ReportEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d473-120">Возвращает массив классов [**Win32 \_ тслиценсерепортентри**](win32-tslicensereportentry.md) .</span><span class="sxs-lookup"><span data-stu-id="7d473-120">Returns an array of [**Win32\_TSLicenseReportEntry**](win32-tslicensereportentry.md) classes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d473-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d473-121">Return value</span></span>

<span data-ttu-id="7d473-122">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="7d473-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7d473-123">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="7d473-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7d473-124">Значение **лсервер \_ I \_ \_ unmore \_ Data** (0x4001) означает, что больше нет записей отчетов.</span><span class="sxs-lookup"><span data-stu-id="7d473-124">A value of **LSERVER\_I\_NO\_MORE\_DATA** (0x4001) indicates that there are no more report entries.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d473-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d473-125">Remarks</span></span>

<span data-ttu-id="7d473-126">Это не статический метод.</span><span class="sxs-lookup"><span data-stu-id="7d473-126">This is not a static method.</span></span> <span data-ttu-id="7d473-127">Этот метод должен вызываться из объекта отчета об использовании лицензий на пользователя.</span><span class="sxs-lookup"><span data-stu-id="7d473-127">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="7d473-128">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="7d473-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="7d473-129">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="7d473-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7d473-130">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="7d473-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7d473-131">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="7d473-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7d473-132">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7d473-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d473-133">Требования</span><span class="sxs-lookup"><span data-stu-id="7d473-133">Requirements</span></span>



| <span data-ttu-id="7d473-134">Требование</span><span class="sxs-lookup"><span data-stu-id="7d473-134">Requirement</span></span> | <span data-ttu-id="7d473-135">Значение</span><span class="sxs-lookup"><span data-stu-id="7d473-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d473-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d473-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7d473-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7d473-137">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="7d473-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d473-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7d473-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d473-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="7d473-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7d473-140">Namespace</span></span><br/>                | <span data-ttu-id="7d473-141">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="7d473-141">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="7d473-142">MOF</span><span class="sxs-lookup"><span data-stu-id="7d473-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d473-143"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d473-143"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d473-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7d473-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d473-145"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d473-145"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d473-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d473-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d473-147">**\_Тслиценсерепорт Win32**</span><span class="sxs-lookup"><span data-stu-id="7d473-147">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="7d473-148">**\_Тслиценсерепортентри Win32**</span><span class="sxs-lookup"><span data-stu-id="7d473-148">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> </dl>

 

