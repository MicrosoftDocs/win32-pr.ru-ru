---
title: Метод Delete класса Win32_TSGatewayResourceAuthorizationPolicy
description: Удаление текущей удаленный рабочий стол политики авторизации ресурсов (RD \ 160; RAP).
ms.assetid: cbabb997-63b8-4a4c-9e16-34f2638fca97
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Delete
- Службы удаленных рабочих столов метода Delete, класс Win32_TSGatewayResourceAuthorizationPolicy
- Класс Win32_TSGatewayResourceAuthorizationPolicy службы удаленных рабочих столов, метод Delete
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Delete
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396a766fb307d1e8a912d614147a2bff2bd924c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414948"
---
# <a name="delete-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="4fbc2-106">Метод DELETE \_ класса Тсгатевайресаурцеаусоризатионполици Win32</span><span class="sxs-lookup"><span data-stu-id="4fbc2-106">Delete method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="4fbc2-107">Удаление текущей удаленный рабочий стол политики авторизации ресурсов (RD RAP).</span><span class="sxs-lookup"><span data-stu-id="4fbc2-107">Deletes the current Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="4fbc2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fbc2-108">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="4fbc2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4fbc2-109">Parameters</span></span>

<span data-ttu-id="4fbc2-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4fbc2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4fbc2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4fbc2-111">Return value</span></span>

<span data-ttu-id="4fbc2-112">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="4fbc2-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4fbc2-113">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="4fbc2-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4fbc2-114">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4fbc2-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4fbc2-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4fbc2-115">Remarks</span></span>

<span data-ttu-id="4fbc2-116">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="4fbc2-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="4fbc2-117">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="4fbc2-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4fbc2-118">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="4fbc2-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4fbc2-119">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="4fbc2-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4fbc2-120">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4fbc2-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4fbc2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4fbc2-121">Requirements</span></span>



| <span data-ttu-id="4fbc2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4fbc2-122">Requirement</span></span> | <span data-ttu-id="4fbc2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4fbc2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fbc2-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fbc2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4fbc2-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4fbc2-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4fbc2-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fbc2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4fbc2-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4fbc2-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4fbc2-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4fbc2-128">Namespace</span></span><br/>                | <span data-ttu-id="4fbc2-129">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="4fbc2-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="4fbc2-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4fbc2-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4fbc2-131"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4fbc2-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="4fbc2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4fbc2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fbc2-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fbc2-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4fbc2-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fbc2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fbc2-135">**\_Тсгатевайресаурцеаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="4fbc2-135">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

