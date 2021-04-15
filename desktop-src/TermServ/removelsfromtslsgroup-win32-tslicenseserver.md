---
title: Метод Ремовелсфромтслсграуп класса Win32_TSLicenseServer
description: Удаляет сервер лицензий удаленный рабочий стол из группы серверов лицензирования службы удаленных рабочих столов на контроллере домена в том же домене, что и сервер лицензирования.
ms.assetid: 5ed4595b-0668-4dd8-953e-b6fc61088cfd
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремовелсфромтслсграуп
- Службы удаленных рабочих столов метода Ремовелсфромтслсграуп, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Ремовелсфромтслсграуп
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.RemoveLSfromTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60c7a0e6b836b8fcf268942ba5d8eae1304b818
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534415"
---
# <a name="removelsfromtslsgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="064cf-106">Метод Ремовелсфромтслсграуп \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="064cf-106">RemoveLSfromTSLSGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="064cf-107">Удаляет сервер лицензий удаленный рабочий стол из группы серверов лицензирования службы удаленных рабочих столов на контроллере домена в том же домене, что и сервер лицензирования.</span><span class="sxs-lookup"><span data-stu-id="064cf-107">Removes the Remote Desktop license server from the Remote Desktop Services License Servers group on a domain controller in the same domain as the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="064cf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="064cf-108">Syntax</span></span>


```mof
uint32 RemoveLSfromTSLSGroup();
```



## <a name="parameters"></a><span data-ttu-id="064cf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="064cf-109">Parameters</span></span>

<span data-ttu-id="064cf-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="064cf-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="064cf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="064cf-111">Return value</span></span>

<span data-ttu-id="064cf-112">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="064cf-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="064cf-113">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="064cf-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="064cf-114">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="064cf-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="064cf-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="064cf-115">Remarks</span></span>

<span data-ttu-id="064cf-116">Для вызова этого метода необходимо быть членом группы "Администраторы домена".</span><span class="sxs-lookup"><span data-stu-id="064cf-116">You must be a member of the Domain Admins group to call this method.</span></span>

<span data-ttu-id="064cf-117">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="064cf-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="064cf-118">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="064cf-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="064cf-119">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="064cf-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="064cf-120">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="064cf-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="064cf-121">Требования</span><span class="sxs-lookup"><span data-stu-id="064cf-121">Requirements</span></span>



| <span data-ttu-id="064cf-122">Требование</span><span class="sxs-lookup"><span data-stu-id="064cf-122">Requirement</span></span> | <span data-ttu-id="064cf-123">Значение</span><span class="sxs-lookup"><span data-stu-id="064cf-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="064cf-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="064cf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="064cf-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="064cf-125">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="064cf-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="064cf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="064cf-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="064cf-127">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="064cf-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="064cf-128">Namespace</span></span><br/>                | <span data-ttu-id="064cf-129">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="064cf-129">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="064cf-130">MOF</span><span class="sxs-lookup"><span data-stu-id="064cf-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="064cf-131"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="064cf-131"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="064cf-132">DLL</span><span class="sxs-lookup"><span data-stu-id="064cf-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="064cf-133"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="064cf-133"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="064cf-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="064cf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="064cf-135">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="064cf-135">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

