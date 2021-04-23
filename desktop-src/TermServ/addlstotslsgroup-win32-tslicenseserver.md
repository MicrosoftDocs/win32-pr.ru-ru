---
title: Метод Аддлстотслсграуп класса Win32_TSLicenseServer
description: Добавляет удаленный рабочий стол сервер лицензирования в группу серверов лицензирования подключение к удаленному рабочему столу Broker (RDCB) на контроллере домена в том же домене, что и сервер лицензирования удаленный рабочий стол.
ms.assetid: 65c6b7cf-324a-44f1-8dfc-40e35ed45d4f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Аддлстотслсграуп
- Службы удаленных рабочих столов метода Аддлстотслсграуп, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Аддлстотслсграуп
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.AddLStoTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53934f6682d1a23f99916588aa4eac3b18526c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415213"
---
# <a name="addlstotslsgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="7fcc5-106">Метод Аддлстотслсграуп \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="7fcc5-106">AddLStoTSLSGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="7fcc5-107">Добавляет удаленный рабочий стол сервер лицензирования в группу серверов лицензирования подключение к удаленному рабочему столу Broker (RDCB) на контроллере домена в том же домене, что и сервер лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-107">Adds the Remote Desktop license server to the Remote Desktop Connection Broker (RD Connection Broker) License Servers group on a domain controller in the same domain as the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fcc5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7fcc5-108">Syntax</span></span>


```mof
uint32 AddLStoTSLSGroup();
```



## <a name="parameters"></a><span data-ttu-id="7fcc5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7fcc5-109">Parameters</span></span>

<span data-ttu-id="7fcc5-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7fcc5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7fcc5-111">Return value</span></span>

<span data-ttu-id="7fcc5-112">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7fcc5-113">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7fcc5-114">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7fcc5-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7fcc5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7fcc5-115">Remarks</span></span>

<span data-ttu-id="7fcc5-116">Для вызова этого метода необходимо быть членом группы "Администраторы домена".</span><span class="sxs-lookup"><span data-stu-id="7fcc5-116">You must be a member of the Domain Admins group to call this method.</span></span>

<span data-ttu-id="7fcc5-117">Если сервер настроен для использования области обнаружения домена или леса, сервер лицензирования должен быть членом группы "серверы лицензий удаленный рабочий стол".</span><span class="sxs-lookup"><span data-stu-id="7fcc5-117">The license server should be a member of the Remote Desktop license servers group if the server is configured to use the domain or forest discovery scope.</span></span>

<span data-ttu-id="7fcc5-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="7fcc5-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7fcc5-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="7fcc5-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7fcc5-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7fcc5-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7fcc5-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fcc5-122">Требования</span><span class="sxs-lookup"><span data-stu-id="7fcc5-122">Requirements</span></span>



| <span data-ttu-id="7fcc5-123">Требование</span><span class="sxs-lookup"><span data-stu-id="7fcc5-123">Requirement</span></span> | <span data-ttu-id="7fcc5-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7fcc5-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fcc5-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7fcc5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7fcc5-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7fcc5-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="7fcc5-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7fcc5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7fcc5-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fcc5-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="7fcc5-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7fcc5-129">Namespace</span></span><br/>                | <span data-ttu-id="7fcc5-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="7fcc5-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="7fcc5-131">MOF</span><span class="sxs-lookup"><span data-stu-id="7fcc5-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fcc5-132"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7fcc5-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fcc5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7fcc5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fcc5-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fcc5-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fcc5-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7fcc5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fcc5-136">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="7fcc5-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="7fcc5-137">**ислсинтслсграуп**</span><span class="sxs-lookup"><span data-stu-id="7fcc5-137">**IsLSinTSLSGroup**</span></span>](islsintslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

