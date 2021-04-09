---
title: Метод Креатетскграуп класса Win32_TSLicenseServer
description: Креатетскграуп больше не доступен для использования в Windows Server 2012.
ms.assetid: 31751da7-263b-4911-a328-246457a606f0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Креатетскграуп
- Службы удаленных рабочих столов метода Креатетскграуп, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Креатетскграуп
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.CreateTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63f10db61cb02ece09d168cb462e31246e498494
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891577"
---
# <a name="createtscgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="48c86-106">Метод Креатетскграуп \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="48c86-106">CreateTSCGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="48c86-107">\[**Креатетскграуп** больше не доступен для использования в Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="48c86-107">\[**CreateTSCGroup** is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="48c86-108">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="48c86-108">This method is not supported.</span></span>

<span data-ttu-id="48c86-109">**Windows server 2008 R2 и Windows server 2008:** Создает локальную группу "компьютеры сервера терминалов" на сервере лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="48c86-109">**Windows Server 2008 R2 and Windows Server 2008:** Creates the Terminal Server Computers local group on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="48c86-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48c86-110">Syntax</span></span>


```mof
uint32 CreateTSCGroup();
```



## <a name="parameters"></a><span data-ttu-id="48c86-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="48c86-111">Parameters</span></span>

<span data-ttu-id="48c86-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="48c86-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="48c86-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48c86-113">Return value</span></span>

<span data-ttu-id="48c86-114">Возвращает значение **WBEM \_ E \_ не \_ поддерживается**.</span><span class="sxs-lookup"><span data-stu-id="48c86-114">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="48c86-115">**Windows server 2008 R2 и Windows server 2008:** Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="48c86-115">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="48c86-116">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="48c86-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="48c86-117">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="48c86-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="48c86-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="48c86-118">Remarks</span></span>

<span data-ttu-id="48c86-119">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="48c86-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="48c86-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="48c86-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="48c86-121">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="48c86-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="48c86-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="48c86-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="48c86-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="48c86-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="48c86-124">Требования</span><span class="sxs-lookup"><span data-stu-id="48c86-124">Requirements</span></span>



| <span data-ttu-id="48c86-125">Требование</span><span class="sxs-lookup"><span data-stu-id="48c86-125">Requirement</span></span> | <span data-ttu-id="48c86-126">Значение</span><span class="sxs-lookup"><span data-stu-id="48c86-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="48c86-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48c86-127">Minimum supported client</span></span><br/> | <span data-ttu-id="48c86-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="48c86-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="48c86-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48c86-129">Minimum supported server</span></span><br/> | <span data-ttu-id="48c86-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48c86-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="48c86-131">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="48c86-131">End of client support</span></span><br/>    | <span data-ttu-id="48c86-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="48c86-132">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="48c86-133">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="48c86-133">End of server support</span></span><br/>    | <span data-ttu-id="48c86-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="48c86-134">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="48c86-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="48c86-135">Namespace</span></span><br/>                | <span data-ttu-id="48c86-136">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="48c86-136">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="48c86-137">MOF</span><span class="sxs-lookup"><span data-stu-id="48c86-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48c86-138"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48c86-138"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="48c86-139">DLL</span><span class="sxs-lookup"><span data-stu-id="48c86-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48c86-140"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48c86-140"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48c86-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48c86-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48c86-142">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="48c86-142">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="48c86-143">**истскграуппресент**</span><span class="sxs-lookup"><span data-stu-id="48c86-143">**IsTSCGroupPresent**</span></span>](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

