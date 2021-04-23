---
title: Метод Истскграуппресент класса Win32_TSLicenseServer
description: Истскграуппресент больше не доступен для использования в Windows Server 2012.
ms.assetid: 2bbb00ff-4fb3-4a7a-a0e7-3daabf97d70a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Истскграуппресент
- Службы удаленных рабочих столов метода Истскграуппресент, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Истскграуппресент
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSCGroupPresent
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a16683b10bbfdd08812454d67ebc8ffc169b0ca0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071401"
---
# <a name="istscgrouppresent-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="ae666-106">Метод Истскграуппресент \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="ae666-106">IsTSCGroupPresent method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="ae666-107">\[**Истскграуппресент** больше не доступен для использования в Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="ae666-107">\[**IsTSCGroupPresent** is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="ae666-108">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ae666-108">This method is not supported.</span></span>

<span data-ttu-id="ae666-109">**Windows server 2008 R2 и Windows server 2008:** Возвращает значение, указывающее, существует ли локальная группа компьютеров сервера терминалов на удаленный рабочий стол сервере лицензирования.</span><span class="sxs-lookup"><span data-stu-id="ae666-109">**Windows Server 2008 R2 and Windows Server 2008:** Retrieves whether the Terminal Server Computers local group exists on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae666-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae666-110">Syntax</span></span>


```mof
uint32 IsTSCGroupPresent(
  [out] boolean Present
);
```



## <a name="parameters"></a><span data-ttu-id="ae666-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae666-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae666-112">*Имеется* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ae666-112">*Present* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae666-113">Логическое значение, указывающее, существует ли локальная группа компьютеров сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="ae666-113">Boolean value that indicates whether the Terminal Server Computers local group exists.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae666-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae666-114">Return value</span></span>

<span data-ttu-id="ae666-115">Возвращает значение **WBEM \_ E \_ не \_ поддерживается**.</span><span class="sxs-lookup"><span data-stu-id="ae666-115">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="ae666-116">**Windows server 2008 R2 и Windows server 2008:** Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="ae666-116">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ae666-117">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="ae666-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ae666-118">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ae666-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ae666-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae666-119">Remarks</span></span>

<span data-ttu-id="ae666-120">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="ae666-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ae666-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="ae666-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ae666-122">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="ae666-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ae666-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="ae666-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ae666-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ae666-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae666-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ae666-125">Requirements</span></span>



| <span data-ttu-id="ae666-126">Требование</span><span class="sxs-lookup"><span data-stu-id="ae666-126">Requirement</span></span> | <span data-ttu-id="ae666-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ae666-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae666-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae666-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ae666-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ae666-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="ae666-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae666-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ae666-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae666-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ae666-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="ae666-132">End of client support</span></span><br/>    | <span data-ttu-id="ae666-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ae666-133">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="ae666-134">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="ae666-134">End of server support</span></span><br/>    | <span data-ttu-id="ae666-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ae666-135">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="ae666-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ae666-136">Namespace</span></span><br/>                | <span data-ttu-id="ae666-137">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="ae666-137">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="ae666-138">MOF</span><span class="sxs-lookup"><span data-stu-id="ae666-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae666-139"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae666-139"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae666-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ae666-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae666-141"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae666-141"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae666-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae666-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae666-143">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="ae666-143">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

