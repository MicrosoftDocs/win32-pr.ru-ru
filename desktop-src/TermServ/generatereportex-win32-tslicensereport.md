---
title: Метод Женератерепортекс класса Win32_TSLicenseReport
description: Создает отчет о текущем использовании лицензий для лицензий "на пользователя" и "на устройство".
ms.assetid: c454e0c5-ca1c-41c7-86b2-1e52c414aeb5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Женератерепортекс
- Службы удаленных рабочих столов метода Женератерепортекс, класс Win32_TSLicenseReport
- Класс Win32_TSLicenseReport службы удаленных рабочих столов, метод Женератерепортекс
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReportEx
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893e6e29d1e4716560b0f0f6b41e6109c89e2f5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414932"
---
# <a name="generatereportex-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="8adbc-106">Метод Женератерепортекс \_ класса Win32 тслиценсерепорт</span><span class="sxs-lookup"><span data-stu-id="8adbc-106">GenerateReportEx method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="8adbc-107">Создает отчет о текущем использовании лицензий для лицензий "на пользователя" и "на устройство".</span><span class="sxs-lookup"><span data-stu-id="8adbc-107">Generates a current license usage report for both Per User and Per Device licenses.</span></span>

## <a name="syntax"></a><span data-ttu-id="8adbc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8adbc-108">Syntax</span></span>


```mof
uint32 GenerateReportEx(
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="8adbc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8adbc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8adbc-110">*Имя файла* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8adbc-110">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8adbc-111">Имя файла созданного отчета.</span><span class="sxs-lookup"><span data-stu-id="8adbc-111">The file name of the generated report.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8adbc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8adbc-112">Return value</span></span>

<span data-ttu-id="8adbc-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="8adbc-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8adbc-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8adbc-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8adbc-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8adbc-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8adbc-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="8adbc-116">Remarks</span></span>

<span data-ttu-id="8adbc-117">Это статический метод.</span><span class="sxs-lookup"><span data-stu-id="8adbc-117">This is a static method.</span></span>

<span data-ttu-id="8adbc-118">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="8adbc-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8adbc-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="8adbc-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8adbc-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="8adbc-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8adbc-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="8adbc-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8adbc-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8adbc-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8adbc-123">Требования</span><span class="sxs-lookup"><span data-stu-id="8adbc-123">Requirements</span></span>



| <span data-ttu-id="8adbc-124">Требование</span><span class="sxs-lookup"><span data-stu-id="8adbc-124">Requirement</span></span> | <span data-ttu-id="8adbc-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8adbc-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8adbc-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8adbc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8adbc-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8adbc-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="8adbc-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8adbc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8adbc-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8adbc-129">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="8adbc-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8adbc-130">Namespace</span></span><br/>                | <span data-ttu-id="8adbc-131">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="8adbc-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="8adbc-132">MOF</span><span class="sxs-lookup"><span data-stu-id="8adbc-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8adbc-133"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8adbc-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8adbc-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8adbc-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8adbc-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8adbc-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8adbc-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8adbc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8adbc-137">**\_Тслиценсерепорт Win32**</span><span class="sxs-lookup"><span data-stu-id="8adbc-137">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

