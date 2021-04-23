---
title: Метод Куерицертконтекст класса Win32_TSGatewayServerSettings
description: Указывает, установлен ли указанный сертификат.
ms.assetid: 25d56f72-befd-46b4-84ff-dca748eeaca4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Куерицертконтекст
- Службы удаленных рабочих столов метода Куерицертконтекст, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Куерицертконтекст
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.QueryCertContext
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e158b348debc610682380d793b66949c5a7648
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492708"
---
# <a name="querycertcontext-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="8784e-106">Метод Куерицертконтекст \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="8784e-106">QueryCertContext method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="8784e-107">Указывает, установлен ли указанный сертификат.</span><span class="sxs-lookup"><span data-stu-id="8784e-107">Indicates whether the specified certificate is installed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8784e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8784e-108">Syntax</span></span>


```mof
uint32 QueryCertContext(
  [out] uint8 CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="8784e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8784e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8784e-110">*CertHash* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8784e-110">*CertHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8784e-111">Хэш сертификата, используемого сервером шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="8784e-111">Hash of the certificate that is used by the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8784e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8784e-112">Return value</span></span>

<span data-ttu-id="8784e-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="8784e-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8784e-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8784e-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8784e-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8784e-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8784e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8784e-116">Remarks</span></span>

<span data-ttu-id="8784e-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="8784e-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8784e-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="8784e-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8784e-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="8784e-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8784e-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="8784e-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8784e-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8784e-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8784e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="8784e-122">Requirements</span></span>



| <span data-ttu-id="8784e-123">Требование</span><span class="sxs-lookup"><span data-stu-id="8784e-123">Requirement</span></span> | <span data-ttu-id="8784e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="8784e-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8784e-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8784e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8784e-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8784e-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8784e-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8784e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8784e-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8784e-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="8784e-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8784e-129">Namespace</span></span><br/>                | <span data-ttu-id="8784e-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="8784e-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8784e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="8784e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8784e-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8784e-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="8784e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8784e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8784e-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8784e-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8784e-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8784e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8784e-136">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="8784e-136">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

