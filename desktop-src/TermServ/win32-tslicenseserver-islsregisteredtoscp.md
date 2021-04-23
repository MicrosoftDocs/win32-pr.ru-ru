---
title: Метод Ислсрегистередтоскп класса Win32_TSLicenseServer
description: Возвращает значение, указывающее, зарегистрирован ли сервер лицензий удаленный рабочий стол в качестве точки подключения службы в службах домен Active Directory.
ms.assetid: 013C3711-7C55-4DB4-9229-C3C60E751EF2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ислсрегистередтоскп
- Службы удаленных рабочих столов метода Ислсрегистередтоскп, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Ислсрегистередтоскп
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSRegisteredToSCP
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b203ff580c5ff8871d023c7f349626acdd693f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801289"
---
# <a name="islsregisteredtoscp-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="24747-106">Метод Ислсрегистередтоскп \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="24747-106">IsLSRegisteredToSCP method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="24747-107">Возвращает значение, указывающее, зарегистрирован ли сервер лицензий удаленный рабочий стол в качестве точки подключения службы в службах домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="24747-107">Retrieves whether the Remote Desktop license server is registered as a service connection point in Active Directory Domain Services.</span></span>

## <a name="syntax"></a><span data-ttu-id="24747-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24747-108">Syntax</span></span>


```mof
uint32 IsLSRegisteredToSCP(
  [out] boolean Registered
);
```



## <a name="parameters"></a><span data-ttu-id="24747-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="24747-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24747-110">*Зарегистрировано* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="24747-110">*Registered* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24747-111">Логическое значение, указывающее, зарегистрирован ли сервер лицензий удаленный рабочий стол в качестве точки подключения службы в службах домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="24747-111">Boolean value that indicates whether the Remote Desktop license server is registered as a service connection point in Active Directory Domain Services.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24747-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24747-112">Return value</span></span>

<span data-ttu-id="24747-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="24747-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="24747-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="24747-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="24747-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="24747-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="24747-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24747-116">Remarks</span></span>

<span data-ttu-id="24747-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="24747-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="24747-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="24747-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="24747-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="24747-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="24747-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="24747-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="24747-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="24747-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="24747-122">Требования</span><span class="sxs-lookup"><span data-stu-id="24747-122">Requirements</span></span>



| <span data-ttu-id="24747-123">Требование</span><span class="sxs-lookup"><span data-stu-id="24747-123">Requirement</span></span> | <span data-ttu-id="24747-124">Значение</span><span class="sxs-lookup"><span data-stu-id="24747-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="24747-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24747-125">Minimum supported client</span></span><br/> | <span data-ttu-id="24747-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="24747-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="24747-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24747-127">Minimum supported server</span></span><br/> | <span data-ttu-id="24747-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="24747-128">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="24747-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="24747-129">Namespace</span></span><br/>                | <span data-ttu-id="24747-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="24747-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="24747-131">MOF</span><span class="sxs-lookup"><span data-stu-id="24747-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24747-132"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24747-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="24747-133">DLL</span><span class="sxs-lookup"><span data-stu-id="24747-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24747-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24747-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24747-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24747-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24747-136">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="24747-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

