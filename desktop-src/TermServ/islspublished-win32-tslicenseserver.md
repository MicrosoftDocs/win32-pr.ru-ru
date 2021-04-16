---
title: Метод Ислспублишед класса Win32_TSLicenseServer
description: Возвращает значение, указывающее, опубликован ли сервер лицензий удаленный рабочий стол в службах домен Active Directory Services (AD \ 160; DS).
ms.assetid: 0e97c9df-5cb0-4e28-8436-08093a8667d9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ислспублишед
- Службы удаленных рабочих столов метода Ислспублишед, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Ислспублишед
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPublished
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69add751497ed52a107ea7183bb4b7cce4ea88c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672719"
---
# <a name="islspublished-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="9918e-106">Метод Ислспублишед \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="9918e-106">IsLSPublished method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="9918e-107">Возвращает значение, указывающее, опубликован ли сервер лицензирования удаленный рабочий стол в службах домен Active Directory Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="9918e-107">Retrieves whether the Remote Desktop license server is published in Active Directory Domain Services (AD DS).</span></span>

## <a name="syntax"></a><span data-ttu-id="9918e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9918e-108">Syntax</span></span>


```mof
uint32 IsLSPublished(
  [out] boolean Published
);
```



## <a name="parameters"></a><span data-ttu-id="9918e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9918e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9918e-110">*Дата публикации* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9918e-110">*Published* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9918e-111">Логическое значение, указывающее, опубликован ли сервер лицензирования в AD DS.</span><span class="sxs-lookup"><span data-stu-id="9918e-111">Boolean value that indicates whether the license server is published in AD DS.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9918e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9918e-112">Return value</span></span>

<span data-ttu-id="9918e-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="9918e-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9918e-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="9918e-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9918e-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9918e-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9918e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9918e-116">Remarks</span></span>

<span data-ttu-id="9918e-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="9918e-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9918e-118">Если сервер лицензирования опубликован в AD DS, он будет автоматически обнаруживаться удаленный рабочий стол серверами узлов сеансов удаленных рабочих столов в том же лесу.</span><span class="sxs-lookup"><span data-stu-id="9918e-118">If the license server is published in AD DS, it will be automatically discoverable by Remote Desktop Session Host (RD Session Host) servers in the same forest.</span></span>

<span data-ttu-id="9918e-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="9918e-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9918e-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="9918e-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9918e-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="9918e-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9918e-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9918e-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9918e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9918e-123">Requirements</span></span>



| <span data-ttu-id="9918e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9918e-124">Requirement</span></span> | <span data-ttu-id="9918e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9918e-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9918e-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9918e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9918e-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9918e-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="9918e-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9918e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9918e-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9918e-129">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="9918e-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9918e-130">Namespace</span></span><br/>                | <span data-ttu-id="9918e-131">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="9918e-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="9918e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="9918e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9918e-133"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9918e-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9918e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9918e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9918e-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9918e-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9918e-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9918e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9918e-137">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="9918e-137">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

