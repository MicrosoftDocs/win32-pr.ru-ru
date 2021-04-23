---
title: Метод Сетенаблед класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает свойство Enabled, которое включает или отключает текущую политику авторизации подключений службы удаленных рабочих столов (RD \ 160; CAP).
ms.assetid: f8c0b39e-95d4-46cf-83fb-e91b650fbb4d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетенаблед
- Службы удаленных рабочих столов метода Сетенаблед, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Сетенаблед
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6584e8916db2f8070def3904d0ece6ec0ee5ae34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534076"
---
# <a name="setenabled-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="a8afd-106">Метод Сетенаблед \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="a8afd-106">SetEnabled method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="a8afd-107">Задает свойство **Enabled** , которое включает или отключает текущую политику авторизации подключений службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="a8afd-107">Sets the **Enabled** property, which enables or disables the current Remote Desktop Services connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="a8afd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8afd-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="a8afd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8afd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8afd-110">*Включено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a8afd-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8afd-111">**Значение true** , если политика авторизации подключений удаленных рабочих столов должна быть включена, и **false** , если политика авторизации подключений удаленных рабочих столов будет отключена.</span><span class="sxs-lookup"><span data-stu-id="a8afd-111">**True** if the RD CAP is to be enabled, **False** if the RD CAP is to be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8afd-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8afd-112">Return value</span></span>

<span data-ttu-id="a8afd-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="a8afd-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a8afd-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="a8afd-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a8afd-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a8afd-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a8afd-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8afd-116">Remarks</span></span>

<span data-ttu-id="a8afd-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="a8afd-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a8afd-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="a8afd-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a8afd-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="a8afd-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a8afd-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="a8afd-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a8afd-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a8afd-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8afd-122">Требования</span><span class="sxs-lookup"><span data-stu-id="a8afd-122">Requirements</span></span>



| <span data-ttu-id="a8afd-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a8afd-123">Requirement</span></span> | <span data-ttu-id="a8afd-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a8afd-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8afd-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8afd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a8afd-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a8afd-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a8afd-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8afd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a8afd-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8afd-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a8afd-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a8afd-129">Namespace</span></span><br/>                | <span data-ttu-id="a8afd-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="a8afd-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a8afd-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a8afd-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8afd-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8afd-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8afd-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a8afd-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8afd-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8afd-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a8afd-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8afd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8afd-136">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="a8afd-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

