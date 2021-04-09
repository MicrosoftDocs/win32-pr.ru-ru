---
title: Метод Сетцертификатеакл класса Win32_TSGatewayServerSettings
description: Задает сертификат, необходимый для доступа к серверу шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 274c24bf-4e44-42ea-a109-99d0249c2f78
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетцертификатеакл
- Службы удаленных рабочих столов метода Сетцертификатеакл, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Сетцертификатеакл
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetCertificateACL
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7a43e737b39b9bea18ee3925b5c3f55440d2a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071987"
---
# <a name="setcertificateacl-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="f8c12-106">Метод Сетцертификатеакл \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="f8c12-106">SetCertificateACL method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="f8c12-107">Задает сертификат, необходимый для доступа к серверу шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="f8c12-107">Sets the certificate that is required to access the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8c12-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8c12-108">Syntax</span></span>


```mof
uint32 SetCertificateACL(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="f8c12-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8c12-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8c12-110">*CertHash* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8c12-110">*CertHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c12-111">Хэш сертификата, используемого сервером шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="f8c12-111">Hash of the certificate that is used by the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8c12-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8c12-112">Return value</span></span>

<span data-ttu-id="f8c12-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="f8c12-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f8c12-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f8c12-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f8c12-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f8c12-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f8c12-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8c12-116">Remarks</span></span>

<span data-ttu-id="f8c12-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="f8c12-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f8c12-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="f8c12-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f8c12-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="f8c12-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f8c12-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="f8c12-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f8c12-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f8c12-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8c12-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f8c12-122">Requirements</span></span>



| <span data-ttu-id="f8c12-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f8c12-123">Requirement</span></span> | <span data-ttu-id="f8c12-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f8c12-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8c12-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8c12-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f8c12-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f8c12-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f8c12-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8c12-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f8c12-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8c12-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f8c12-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f8c12-129">Namespace</span></span><br/>                | <span data-ttu-id="f8c12-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="f8c12-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f8c12-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f8c12-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8c12-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8c12-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8c12-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f8c12-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8c12-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8c12-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f8c12-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8c12-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8c12-136">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="f8c12-136">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

