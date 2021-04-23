---
title: Метод Ислсинтслсграуп класса Win32_TSLicenseServer
description: Возвращает значение, указывающее, входит ли сервер лицензий удаленный рабочий стол в группу серверов лицензирования удаленный рабочий стол на контроллере домена в данном домене.
ms.assetid: a6ad7f09-8972-47d4-8b3b-cd129b400ea8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ислсинтслсграуп
- Службы удаленных рабочих столов метода Ислсинтслсграуп, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Ислсинтслсграуп
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSinTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de3577e4632167612b4d71841501a2a2845203a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672721"
---
# <a name="islsintslsgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="1044d-106">Метод Ислсинтслсграуп \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="1044d-106">IsLSinTSLSGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="1044d-107">Возвращает значение, указывающее, входит ли сервер лицензий удаленный рабочий стол в группу серверов лицензирования удаленный рабочий стол на контроллере домена в данном домене.</span><span class="sxs-lookup"><span data-stu-id="1044d-107">Retrieves whether the Remote Desktop license server is a member of the Remote Desktop license server group on a domain controller in a given domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="1044d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1044d-108">Syntax</span></span>


```mof
uint32 IsLSinTSLSGroup(
  [in]  string  Domain,
  [out] boolean IsMember
);
```



## <a name="parameters"></a><span data-ttu-id="1044d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1044d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1044d-110">*Домен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1044d-110">*Domain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1044d-111">Имя домена.</span><span class="sxs-lookup"><span data-stu-id="1044d-111">The domain name.</span></span>

</dd> <dt>

<span data-ttu-id="1044d-112">*Элемент* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1044d-112">*IsMember* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1044d-113">Логическое значение, указывающее, является ли сервер лицензирования членом группы серверов лицензирования удаленный рабочий стол в домене.</span><span class="sxs-lookup"><span data-stu-id="1044d-113">Boolean value that indicates whether the license server is a member of the Remote Desktop license server group in the domain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1044d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1044d-114">Return value</span></span>

<span data-ttu-id="1044d-115">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="1044d-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1044d-116">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="1044d-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1044d-117">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1044d-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1044d-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1044d-118">Remarks</span></span>

<span data-ttu-id="1044d-119">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="1044d-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1044d-120">Если доменное имя не указано, запрашивается контроллер домена в том же домене, что и сервер лицензирования.</span><span class="sxs-lookup"><span data-stu-id="1044d-120">If no domain name is provided, a domain controller in the same domain as the license server is queried.</span></span>

<span data-ttu-id="1044d-121">Если сервер настроен для использования области обнаружения домена или леса, сервер лицензирования должен быть членом группы серверов лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="1044d-121">The license server should be a member of the Remote Desktop license server group if the server is configured to use the domain or forest discovery scope.</span></span> <span data-ttu-id="1044d-122">Если сервер лицензирования не входит в эту группу, отслеживание лицензий для каждого пользователя и создание отчетов не будут работать.</span><span class="sxs-lookup"><span data-stu-id="1044d-122">If the license server is not a member of this group, per-user license tracking and reporting will not work.</span></span>

<span data-ttu-id="1044d-123">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="1044d-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1044d-124">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="1044d-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1044d-125">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="1044d-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1044d-126">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1044d-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1044d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="1044d-127">Requirements</span></span>



| <span data-ttu-id="1044d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="1044d-128">Requirement</span></span> | <span data-ttu-id="1044d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="1044d-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1044d-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1044d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1044d-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1044d-131">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="1044d-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1044d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1044d-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1044d-133">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="1044d-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1044d-134">Namespace</span></span><br/>                | <span data-ttu-id="1044d-135">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="1044d-135">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="1044d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="1044d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1044d-137"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1044d-137"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1044d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1044d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1044d-139"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1044d-139"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1044d-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1044d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1044d-141">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="1044d-141">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="1044d-142">**аддлстотслсграуп**</span><span class="sxs-lookup"><span data-stu-id="1044d-142">**AddLStoTSLSGroup**</span></span>](addlstotslsgroup-win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="1044d-143">**ремовелсфромтслсграуп**</span><span class="sxs-lookup"><span data-stu-id="1044d-143">**RemoveLSfromTSLSGroup**</span></span>](removelsfromtslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

