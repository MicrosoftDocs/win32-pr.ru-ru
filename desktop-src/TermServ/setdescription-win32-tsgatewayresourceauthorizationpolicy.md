---
title: Метод SetDescription класса Win32_TSGatewayResourceAuthorizationPolicy
description: Задает свойство Description для политики авторизации ресурсов удаленный рабочий стол (RD \ 160; RAP).
ms.assetid: 5a0f4c4b-50a4-4bd2-960f-8af7f4686d07
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода SetDescription
- Службы удаленных рабочих столов метода SetDescription, класс Win32_TSGatewayResourceAuthorizationPolicy
- Класс Win32_TSGatewayResourceAuthorizationPolicy службы удаленных рабочих столов, метод SetDescription
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetDescription
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5dfdbcf67096dacc694061b5ff7e704c788bd2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415437"
---
# <a name="setdescription-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="8e0cf-106">Метод SetDescription \_ класса Win32 тсгатевайресаурцеаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="8e0cf-106">SetDescription method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="8e0cf-107">Задает свойство **Description** для политики авторизации ресурсов (RD RAP) удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="8e0cf-107">Sets the **Description** property for the Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="8e0cf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e0cf-108">Syntax</span></span>


```mof
uint32 SetDescription(
  [in] string Description
);
```



## <a name="parameters"></a><span data-ttu-id="8e0cf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e0cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e0cf-110">*Описание* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e0cf-110">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e0cf-111">Описание политики авторизации ресурсов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="8e0cf-111">Description of the RD RAP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e0cf-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e0cf-112">Return value</span></span>

<span data-ttu-id="8e0cf-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="8e0cf-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8e0cf-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8e0cf-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8e0cf-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8e0cf-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8e0cf-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e0cf-116">Remarks</span></span>

<span data-ttu-id="8e0cf-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="8e0cf-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8e0cf-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="8e0cf-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8e0cf-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="8e0cf-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8e0cf-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="8e0cf-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8e0cf-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8e0cf-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e0cf-122">Требования</span><span class="sxs-lookup"><span data-stu-id="8e0cf-122">Requirements</span></span>



| <span data-ttu-id="8e0cf-123">Требование</span><span class="sxs-lookup"><span data-stu-id="8e0cf-123">Requirement</span></span> | <span data-ttu-id="8e0cf-124">Значение</span><span class="sxs-lookup"><span data-stu-id="8e0cf-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e0cf-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e0cf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8e0cf-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8e0cf-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8e0cf-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e0cf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8e0cf-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e0cf-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="8e0cf-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8e0cf-129">Namespace</span></span><br/>                | <span data-ttu-id="8e0cf-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="8e0cf-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8e0cf-131">MOF</span><span class="sxs-lookup"><span data-stu-id="8e0cf-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e0cf-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e0cf-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e0cf-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8e0cf-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e0cf-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e0cf-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8e0cf-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e0cf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e0cf-136">**\_Тсгатевайресаурцеаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="8e0cf-136">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

