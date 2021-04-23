---
title: Метод Енаблецентралкап класса Win32_TSGatewayServerSettings
description: Управляет свойством Централкапенаблед, которое управляет политиками авторизации подключений службы удаленных рабочих столов (RD \ 160; CAP) для сервера шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 43e476df-714d-43bd-b40f-33511b7757a4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Енаблецентралкап
- Службы удаленных рабочих столов метода Енаблецентралкап, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Енаблецентралкап
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableCentralCAP
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 933e91a89f9a5afdcd2ae85fa6cb097ef0c29cd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416168"
---
# <a name="enablecentralcap-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="fc6f7-106">Метод Енаблецентралкап \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="fc6f7-106">EnableCentralCAP method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="fc6f7-107">Управляет свойством **централкапенаблед** , которое управляет политиками авторизации подключений службы удаленных рабочих столов (RD CAP) для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="fc6f7-107">Controls the **CentralCAPEnabled** property, which controls the Remote Desktop Services connection authorization policies (RD CAPs) for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc6f7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc6f7-108">Syntax</span></span>


```mof
uint32 EnableCentralCAP(
  [in] boolean CentralCAPEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="fc6f7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc6f7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc6f7-110">*Централкапенаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc6f7-110">*CentralCAPEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc6f7-111">Если задано **значение true**, будут использоваться RD CAP из центральных серверов Cap.</span><span class="sxs-lookup"><span data-stu-id="fc6f7-111">If set to **True**, RD CAPs from central RD CAP servers will be used.</span></span> <span data-ttu-id="fc6f7-112">Если задано значение **false**, будут использоваться только политики локального сервера.</span><span class="sxs-lookup"><span data-stu-id="fc6f7-112">If set to **False**, only policies from the local server will be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc6f7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc6f7-113">Return value</span></span>

<span data-ttu-id="fc6f7-114">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="fc6f7-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fc6f7-115">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="fc6f7-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fc6f7-116">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fc6f7-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fc6f7-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc6f7-117">Remarks</span></span>

<span data-ttu-id="fc6f7-118">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="fc6f7-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fc6f7-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="fc6f7-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fc6f7-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="fc6f7-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fc6f7-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="fc6f7-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fc6f7-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fc6f7-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc6f7-123">Требования</span><span class="sxs-lookup"><span data-stu-id="fc6f7-123">Requirements</span></span>



| <span data-ttu-id="fc6f7-124">Требование</span><span class="sxs-lookup"><span data-stu-id="fc6f7-124">Requirement</span></span> | <span data-ttu-id="fc6f7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="fc6f7-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc6f7-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc6f7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fc6f7-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fc6f7-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="fc6f7-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc6f7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fc6f7-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc6f7-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fc6f7-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fc6f7-130">Namespace</span></span><br/>                | <span data-ttu-id="fc6f7-131">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="fc6f7-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="fc6f7-132">MOF</span><span class="sxs-lookup"><span data-stu-id="fc6f7-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc6f7-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc6f7-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc6f7-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fc6f7-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc6f7-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc6f7-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="fc6f7-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc6f7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc6f7-137">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="fc6f7-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

