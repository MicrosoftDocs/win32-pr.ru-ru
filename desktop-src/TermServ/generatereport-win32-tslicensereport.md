---
title: Метод Женератерепорт класса Win32_TSLicenseReport (GPMgmt. h)
description: Женератерепорт больше не доступен для использования в Windows Server 2012.
ms.assetid: 2d3b16d6-52e8-491f-b6e5-419e9a21013b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Женератерепорт
- Службы удаленных рабочих столов метода Женератерепорт, класс Win32_TSLicenseReport
- Класс Win32_TSLicenseReport службы удаленных рабочих столов, метод Женератерепорт
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5231c87d379decac8d4f6491042bff735c1ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415868"
---
# <a name="generatereport-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="315e5-106">Метод Женератерепорт \_ класса Win32 тслиценсерепорт</span><span class="sxs-lookup"><span data-stu-id="315e5-106">GenerateReport method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="315e5-107">\[**Женератерепорт** больше не доступен для использования в Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="315e5-107">\[**GenerateReport** is no longer available for use as of Windows Server 2012.</span></span> <span data-ttu-id="315e5-108">Вместо этого используйте [**женератерепортекс**](generatereportex-win32-tslicensereport.md).\]</span><span class="sxs-lookup"><span data-stu-id="315e5-108">Instead, use [**GenerateReportEx**](generatereportex-win32-tslicensereport.md).\]</span></span>

<span data-ttu-id="315e5-109">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="315e5-109">This method is not supported.</span></span>

<span data-ttu-id="315e5-110">**Windows server 2008 R2 и Windows server 2008:** Формирует текущий отчет об использовании лицензий на пользователя на сервере лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="315e5-110">**Windows Server 2008 R2 and Windows Server 2008:** Generates a current per user license usage report on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="315e5-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="315e5-111">Syntax</span></span>


```mof
uint32 GenerateReport(
  [in]  uint32 ScopeType,
  [in]  string ScopeValue,
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="315e5-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="315e5-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="315e5-113">*Скопетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="315e5-113">*ScopeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="315e5-114">Область отчета об использовании лицензий.</span><span class="sxs-lookup"><span data-stu-id="315e5-114">Scope of the license usage report.</span></span> <span data-ttu-id="315e5-115">Он может иметь следующие значения.</span><span class="sxs-lookup"><span data-stu-id="315e5-115">It can have the following values.</span></span>

<dt>

<span data-ttu-id="315e5-116">1</span><span class="sxs-lookup"><span data-stu-id="315e5-116">1</span></span>
</dt> <dd>

<span data-ttu-id="315e5-117">Отчет будет создан для всего домена.</span><span class="sxs-lookup"><span data-stu-id="315e5-117">The report will be generated for the entire domain.</span></span>

</dd> <dt>

<span data-ttu-id="315e5-118">2</span><span class="sxs-lookup"><span data-stu-id="315e5-118">2</span></span>
</dt> <dd>

<span data-ttu-id="315e5-119">Отчет будет создан для подразделения, указанного в параметре *скопевалуе* .</span><span class="sxs-lookup"><span data-stu-id="315e5-119">The report will be generated for the organizational unit (OU) that is specified in the *ScopeValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="315e5-120">3</span><span class="sxs-lookup"><span data-stu-id="315e5-120">3</span></span>
</dt> <dd>

<span data-ttu-id="315e5-121">Отчет будет создан для всех доверенных доменов.</span><span class="sxs-lookup"><span data-stu-id="315e5-121">The report will be generated for all trusted domains.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="315e5-122">*Скопевалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="315e5-122">*ScopeValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="315e5-123">Если значение параметра *скопетипе* равно 2, *СКОПЕТИПЕ* указывает подразделение, для которого будет создан отчет.</span><span class="sxs-lookup"><span data-stu-id="315e5-123">If the *ScopeType* parameter is 2, *ScopeType* specifies the OU for which the report will be generated.</span></span> <span data-ttu-id="315e5-124">Необходимо указать *скопевалуе* , используя формат **OU =**_OUName1_*_, OU =_*_OUName2_*_..._*.</span><span class="sxs-lookup"><span data-stu-id="315e5-124">You must specify *ScopeValue* by using the format **OU=**_OUName1_*_,OU=_*_OUName2_*_..._*.</span></span>

</dd> <dt>

<span data-ttu-id="315e5-125">*Имя файла* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="315e5-125">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="315e5-126">Имя файла созданного отчета.</span><span class="sxs-lookup"><span data-stu-id="315e5-126">The file name of the generated report.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="315e5-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="315e5-127">Return value</span></span>

<span data-ttu-id="315e5-128">Возвращает значение **WBEM \_ E \_ не \_ поддерживается**.</span><span class="sxs-lookup"><span data-stu-id="315e5-128">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="315e5-129">**Windows server 2008 R2 и Windows server 2008:** Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="315e5-129">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="315e5-130">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="315e5-130">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="315e5-131">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="315e5-131">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="315e5-132">Remarks</span><span class="sxs-lookup"><span data-stu-id="315e5-132">Remarks</span></span>

<span data-ttu-id="315e5-133">Это статический метод.</span><span class="sxs-lookup"><span data-stu-id="315e5-133">This is a static method.</span></span>

<span data-ttu-id="315e5-134">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="315e5-134">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="315e5-135">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="315e5-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="315e5-136">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="315e5-136">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="315e5-137">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="315e5-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="315e5-138">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="315e5-138">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="315e5-139">Требования</span><span class="sxs-lookup"><span data-stu-id="315e5-139">Requirements</span></span>



| <span data-ttu-id="315e5-140">Требование</span><span class="sxs-lookup"><span data-stu-id="315e5-140">Requirement</span></span> | <span data-ttu-id="315e5-141">Значение</span><span class="sxs-lookup"><span data-stu-id="315e5-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="315e5-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="315e5-142">Minimum supported client</span></span><br/> | <span data-ttu-id="315e5-143">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="315e5-143">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="315e5-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="315e5-144">Minimum supported server</span></span><br/> | <span data-ttu-id="315e5-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="315e5-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="315e5-146">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="315e5-146">End of client support</span></span><br/>    | <span data-ttu-id="315e5-147">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="315e5-147">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="315e5-148">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="315e5-148">End of server support</span></span><br/>    | <span data-ttu-id="315e5-149">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="315e5-149">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="315e5-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="315e5-150">Namespace</span></span><br/>                | <span data-ttu-id="315e5-151">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="315e5-151">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="315e5-152">Header</span><span class="sxs-lookup"><span data-stu-id="315e5-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="315e5-153"><dt>GPMgmt. h</dt></span><span class="sxs-lookup"><span data-stu-id="315e5-153"><dt>Gpmgmt.h</dt></span></span> </dl>       |
| <span data-ttu-id="315e5-154">MOF</span><span class="sxs-lookup"><span data-stu-id="315e5-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="315e5-155"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="315e5-155"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="315e5-156">DLL</span><span class="sxs-lookup"><span data-stu-id="315e5-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="315e5-157"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="315e5-157"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="315e5-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="315e5-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="315e5-159">**\_Тслиценсерепорт Win32**</span><span class="sxs-lookup"><span data-stu-id="315e5-159">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

