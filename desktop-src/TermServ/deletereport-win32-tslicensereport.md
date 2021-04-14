---
title: Метод Делетерепорт класса Win32_TSLicenseReport
description: Удаляет объект отчета на сервере лицензирования удаленный рабочий стол. Это не статический метод.
ms.assetid: cc70526c-7ce5-4d55-b72e-8a5e8799b1d8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Делетерепорт
- Службы удаленных рабочих столов метода Делетерепорт, класс Win32_TSLicenseReport
- Класс Win32_TSLicenseReport службы удаленных рабочих столов, метод Делетерепорт
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.DeleteReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a96c8626e4ecc1f89d0f2fcefa69845fec4df8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533836"
---
# <a name="deletereport-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="923de-107">Метод Делетерепорт \_ класса Win32 тслиценсерепорт</span><span class="sxs-lookup"><span data-stu-id="923de-107">DeleteReport method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="923de-108">Удаляет объект отчета на сервере лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="923de-108">Deletes a report object on the Remote Desktop license server.</span></span> <span data-ttu-id="923de-109">Это не статический метод.</span><span class="sxs-lookup"><span data-stu-id="923de-109">This is not a static method.</span></span>

## <a name="syntax"></a><span data-ttu-id="923de-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="923de-110">Syntax</span></span>


```mof
uint32 DeleteReport();
```



## <a name="parameters"></a><span data-ttu-id="923de-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="923de-111">Parameters</span></span>

<span data-ttu-id="923de-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="923de-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="923de-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="923de-113">Return value</span></span>

<span data-ttu-id="923de-114">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="923de-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="923de-115">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="923de-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="923de-116">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="923de-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="923de-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="923de-117">Remarks</span></span>

<span data-ttu-id="923de-118">Это не статический метод.</span><span class="sxs-lookup"><span data-stu-id="923de-118">This is not a static method.</span></span> <span data-ttu-id="923de-119">Этот метод должен вызываться из объекта отчета об использовании лицензий на пользователя.</span><span class="sxs-lookup"><span data-stu-id="923de-119">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="923de-120">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="923de-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="923de-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="923de-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="923de-122">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="923de-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="923de-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="923de-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="923de-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="923de-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="923de-125">Требования</span><span class="sxs-lookup"><span data-stu-id="923de-125">Requirements</span></span>



| <span data-ttu-id="923de-126">Требование</span><span class="sxs-lookup"><span data-stu-id="923de-126">Requirement</span></span> | <span data-ttu-id="923de-127">Значение</span><span class="sxs-lookup"><span data-stu-id="923de-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="923de-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="923de-128">Minimum supported client</span></span><br/> | <span data-ttu-id="923de-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="923de-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="923de-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="923de-130">Minimum supported server</span></span><br/> | <span data-ttu-id="923de-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="923de-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="923de-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="923de-132">Namespace</span></span><br/>                | <span data-ttu-id="923de-133">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="923de-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="923de-134">MOF</span><span class="sxs-lookup"><span data-stu-id="923de-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="923de-135"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="923de-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="923de-136">DLL</span><span class="sxs-lookup"><span data-stu-id="923de-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="923de-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="923de-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="923de-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="923de-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="923de-139">**\_Тслиценсерепорт Win32**</span><span class="sxs-lookup"><span data-stu-id="923de-139">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

