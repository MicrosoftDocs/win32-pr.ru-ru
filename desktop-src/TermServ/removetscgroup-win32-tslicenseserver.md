---
title: Метод Ремоветскграуп класса Win32_TSLicenseServer
description: Ремоветскграуп больше не доступен для использования в Windows Server 2012.
ms.assetid: e5e3eca9-4990-4322-b41d-c6b6b3356272
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремоветскграуп
- Службы удаленных рабочих столов метода Ремоветскграуп, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Ремоветскграуп
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.RemoveTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26ca693e7e98ca811ce52292fb26622b7f2174cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535381"
---
# <a name="removetscgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="a0a50-106">Метод Ремоветскграуп \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="a0a50-106">RemoveTSCGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="a0a50-107">\[**Ремоветскграуп** больше не доступен для использования в Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="a0a50-107">\[**RemoveTSCGroup** is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="a0a50-108">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a0a50-108">This method is not supported.</span></span>

<span data-ttu-id="a0a50-109">**Windows server 2008 R2 и Windows server 2008:** Удаляет локальную группу "компьютеры сервера терминалов" с сервера лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="a0a50-109">**Windows Server 2008 R2 and Windows Server 2008:** Removes the Terminal Server Computers local group from the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0a50-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0a50-110">Syntax</span></span>


```mof
uint32 RemoveTSCGroup();
```



## <a name="parameters"></a><span data-ttu-id="a0a50-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0a50-111">Parameters</span></span>

<span data-ttu-id="a0a50-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a0a50-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0a50-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0a50-113">Return value</span></span>

<span data-ttu-id="a0a50-114">Возвращает значение **WBEM \_ E \_ не \_ поддерживается**.</span><span class="sxs-lookup"><span data-stu-id="a0a50-114">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="a0a50-115">**Windows server 2008 R2 и Windows server 2008:** Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="a0a50-115">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a0a50-116">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="a0a50-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a0a50-117">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a0a50-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a0a50-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0a50-118">Remarks</span></span>

<span data-ttu-id="a0a50-119">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="a0a50-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a0a50-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="a0a50-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a0a50-121">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="a0a50-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a0a50-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="a0a50-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a0a50-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a0a50-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0a50-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a0a50-124">Requirements</span></span>



| <span data-ttu-id="a0a50-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a0a50-125">Requirement</span></span> | <span data-ttu-id="a0a50-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a0a50-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a50-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0a50-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a0a50-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a0a50-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="a0a50-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0a50-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a0a50-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0a50-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="a0a50-131">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a0a50-131">End of client support</span></span><br/>    | <span data-ttu-id="a0a50-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a0a50-132">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="a0a50-133">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a0a50-133">End of server support</span></span><br/>    | <span data-ttu-id="a0a50-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a0a50-134">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="a0a50-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a0a50-135">Namespace</span></span><br/>                | <span data-ttu-id="a0a50-136">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="a0a50-136">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="a0a50-137">MOF</span><span class="sxs-lookup"><span data-stu-id="a0a50-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0a50-138"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0a50-138"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0a50-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a0a50-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0a50-140"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0a50-140"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0a50-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0a50-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0a50-142">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="a0a50-142">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="a0a50-143">**истскграуппресент**</span><span class="sxs-lookup"><span data-stu-id="a0a50-143">**IsTSCGroupPresent**</span></span>](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

