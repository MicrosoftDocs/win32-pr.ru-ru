---
title: Метод Сеткукиеаусентикатионалловед класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает свойство Кукиеаусентикатионалловед.
ms.assetid: 481b89cb-d73b-4dae-941c-a629c2ae5ac4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сеткукиеаусентикатионалловед
- Службы удаленных рабочих столов метода Сеткукиеаусентикатионалловед, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Сеткукиеаусентикатионалловед
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetCookieAuthenticationAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9293123ab6ce5b1ddcdb172f9258ba73b23fdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135387"
---
# <a name="setcookieauthenticationallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="a58b7-106">Метод Сеткукиеаусентикатионалловед \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="a58b7-106">SetCookieAuthenticationAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="a58b7-107">Задает свойство **кукиеаусентикатионалловед** .</span><span class="sxs-lookup"><span data-stu-id="a58b7-107">Sets the **CookieAuthenticationAllowed** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a58b7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a58b7-108">Syntax</span></span>


```mof
uint32 SetCookieAuthenticationAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="a58b7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a58b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a58b7-110">*Разрешено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a58b7-110">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a58b7-111">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a58b7-111">Type: **boolean**</span></span>

<span data-ttu-id="a58b7-112">Новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="a58b7-112">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a58b7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a58b7-113">Return value</span></span>

<span data-ttu-id="a58b7-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a58b7-114">Type: **uint32**</span></span>

<span data-ttu-id="a58b7-115">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="a58b7-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a58b7-116">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="a58b7-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a58b7-117">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a58b7-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a58b7-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a58b7-118">Remarks</span></span>

<span data-ttu-id="a58b7-119">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="a58b7-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a58b7-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="a58b7-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a58b7-121">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="a58b7-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a58b7-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="a58b7-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a58b7-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a58b7-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a58b7-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a58b7-124">Requirements</span></span>



| <span data-ttu-id="a58b7-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a58b7-125">Requirement</span></span> | <span data-ttu-id="a58b7-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a58b7-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a58b7-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a58b7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a58b7-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a58b7-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a58b7-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a58b7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a58b7-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a58b7-130">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="a58b7-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a58b7-131">Namespace</span></span><br/>                | <span data-ttu-id="a58b7-132">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="a58b7-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a58b7-133">MOF</span><span class="sxs-lookup"><span data-stu-id="a58b7-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a58b7-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a58b7-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a58b7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a58b7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a58b7-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a58b7-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a58b7-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a58b7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a58b7-138">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="a58b7-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

