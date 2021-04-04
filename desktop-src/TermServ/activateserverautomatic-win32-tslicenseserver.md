---
title: Метод Активатесервераутоматик класса Win32_TSLicenseServer
description: Автоматически активирует сервер лицензий удаленный рабочий стол через Интернет.
ms.assetid: a33ba72f-3403-4bd2-94a9-0c5ef1cbb03e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Активатесервераутоматик
- Службы удаленных рабочих столов метода Активатесервераутоматик, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Активатесервераутоматик
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68879dbc40cc4161edcfef631bf9bb4b72558df8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988411"
---
# <a name="activateserverautomatic-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="f5630-106">Метод Активатесервераутоматик \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="f5630-106">ActivateServerAutomatic method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="f5630-107">Автоматически активирует сервер лицензий удаленный рабочий стол через Интернет.</span><span class="sxs-lookup"><span data-stu-id="f5630-107">Activates the Remote Desktop license server automatically over the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5630-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5630-108">Syntax</span></span>


```mof
uint32 ActivateServerAutomatic(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="f5630-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5630-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5630-110">*ActivationStatus* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f5630-110">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5630-111">Возвращенное состояние активации может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="f5630-111">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="f5630-112">0</span><span class="sxs-lookup"><span data-stu-id="f5630-112">0</span></span>
</dt> <dd>

<span data-ttu-id="f5630-113">Сервер лицензий удаленный рабочий стол активирован.</span><span class="sxs-lookup"><span data-stu-id="f5630-113">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="f5630-114">1</span><span class="sxs-lookup"><span data-stu-id="f5630-114">1</span></span>
</dt> <dd>

<span data-ttu-id="f5630-115">Сервер лицензирования удаленный рабочий стол не активирован.</span><span class="sxs-lookup"><span data-stu-id="f5630-115">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="f5630-116">2</span><span class="sxs-lookup"><span data-stu-id="f5630-116">2</span></span>
</dt> <dd>

<span data-ttu-id="f5630-117">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f5630-117">An unknown error occurred.</span></span> <span data-ttu-id="f5630-118">Неизвестно, активирован ли сервер лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="f5630-118">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5630-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5630-119">Return value</span></span>

<span data-ttu-id="f5630-120">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="f5630-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f5630-121">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f5630-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f5630-122">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f5630-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f5630-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5630-123">Remarks</span></span>

<span data-ttu-id="f5630-124">Этот метод завершается ошибкой, если не заданы свойства **FirstName**, **LastName**, **Company** и **страна** .</span><span class="sxs-lookup"><span data-stu-id="f5630-124">This method fails unless the **FirstName**, **LastName**, **Company**, and **CountryRegion** properties are set.</span></span>

<span data-ttu-id="f5630-125">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="f5630-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f5630-126">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="f5630-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f5630-127">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="f5630-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f5630-128">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="f5630-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f5630-129">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f5630-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5630-130">Требования</span><span class="sxs-lookup"><span data-stu-id="f5630-130">Requirements</span></span>



| <span data-ttu-id="f5630-131">Требование</span><span class="sxs-lookup"><span data-stu-id="f5630-131">Requirement</span></span> | <span data-ttu-id="f5630-132">Значение</span><span class="sxs-lookup"><span data-stu-id="f5630-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5630-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5630-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f5630-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f5630-134">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f5630-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5630-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f5630-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5630-136">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f5630-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f5630-137">Namespace</span></span><br/>                | <span data-ttu-id="f5630-138">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f5630-138">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f5630-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f5630-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5630-140"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5630-140"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5630-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f5630-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5630-142"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5630-142"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5630-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5630-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5630-144">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="f5630-144">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

