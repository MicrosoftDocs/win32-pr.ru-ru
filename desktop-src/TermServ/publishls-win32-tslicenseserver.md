---
title: Метод Публишлс класса Win32_TSLicenseServer
description: Публикует сервер лицензий удаленный рабочий стол в службах домен Active Directory.
ms.assetid: 726d5dec-e438-455e-adb8-56d646d65d13
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Публишлс
- Службы удаленных рабочих столов метода Публишлс, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Публишлс
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.PublishLS
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad3d20efe8b61cd00e1986bb190500c93fd9473
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137347"
---
# <a name="publishls-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="2e1dd-106">Метод Публишлс \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="2e1dd-106">PublishLS method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="2e1dd-107">Публикует сервер лицензий удаленный рабочий стол в службах домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2e1dd-107">Publishes the Remote Desktop license server in Active Directory Domain Services.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e1dd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e1dd-108">Syntax</span></span>


```mof
uint32 PublishLS();
```



## <a name="parameters"></a><span data-ttu-id="2e1dd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e1dd-109">Parameters</span></span>

<span data-ttu-id="2e1dd-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2e1dd-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e1dd-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e1dd-111">Return value</span></span>

<span data-ttu-id="2e1dd-112">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="2e1dd-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2e1dd-113">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="2e1dd-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2e1dd-114">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2e1dd-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2e1dd-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e1dd-115">Remarks</span></span>

<span data-ttu-id="2e1dd-116">Чтобы вызвать этот метод, необходимо войти в систему в качестве администратора предприятия в лес, членом которого является сервер лицензирования.</span><span class="sxs-lookup"><span data-stu-id="2e1dd-116">To call this method, you must be logged on as an enterprise administrator to the forest in which the license server is a member.</span></span>

<span data-ttu-id="2e1dd-117">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="2e1dd-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2e1dd-118">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="2e1dd-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2e1dd-119">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="2e1dd-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2e1dd-120">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2e1dd-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e1dd-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2e1dd-121">Requirements</span></span>



| <span data-ttu-id="2e1dd-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2e1dd-122">Requirement</span></span> | <span data-ttu-id="2e1dd-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2e1dd-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e1dd-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e1dd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2e1dd-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2e1dd-125">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="2e1dd-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e1dd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2e1dd-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e1dd-127">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="2e1dd-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2e1dd-128">Namespace</span></span><br/>                | <span data-ttu-id="2e1dd-129">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="2e1dd-129">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="2e1dd-130">MOF</span><span class="sxs-lookup"><span data-stu-id="2e1dd-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e1dd-131"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e1dd-131"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e1dd-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2e1dd-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e1dd-133"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e1dd-133"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e1dd-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e1dd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e1dd-135">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="2e1dd-135">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

