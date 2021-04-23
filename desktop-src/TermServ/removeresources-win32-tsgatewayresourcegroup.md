---
title: Метод Ремовересаурцес класса Win32_TSGatewayResourceGroup
description: Удаляет ресурсы из группы ресурсов.
ms.assetid: 5f339990-8273-4658-843e-b6b7a85808e1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремовересаурцес
- Службы удаленных рабочих столов метода Ремовересаурцес, класс Win32_TSGatewayResourceGroup
- Класс Win32_TSGatewayResourceGroup службы удаленных рабочих столов, метод Ремовересаурцес
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.RemoveResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e3d1cc1e39d8c96833fc6a371741493457a28b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416133"
---
# <a name="removeresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="052a8-106">Метод Ремовересаурцес \_ класса Win32 тсгатевайресаурцеграуп</span><span class="sxs-lookup"><span data-stu-id="052a8-106">RemoveResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="052a8-107">Удаляет ресурсы из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="052a8-107">Removes resources from the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="052a8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="052a8-108">Syntax</span></span>


```mof
uint32 RemoveResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="052a8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="052a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="052a8-110">*Ресурсы* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="052a8-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="052a8-111">Разделенный точками с запятой список ресурсов для удаления.</span><span class="sxs-lookup"><span data-stu-id="052a8-111">Semicolon-separated list of resources to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="052a8-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="052a8-112">Return value</span></span>

<span data-ttu-id="052a8-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="052a8-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="052a8-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="052a8-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="052a8-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="052a8-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="052a8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="052a8-116">Remarks</span></span>

<span data-ttu-id="052a8-117">Если в параметре *Resources* указано несколько ресурсов и один из ресурсов не может быть обработан, никакие ресурсы не будут обработаны.</span><span class="sxs-lookup"><span data-stu-id="052a8-117">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="052a8-118">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="052a8-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="052a8-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="052a8-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="052a8-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="052a8-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="052a8-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="052a8-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="052a8-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="052a8-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="052a8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="052a8-123">Requirements</span></span>



| <span data-ttu-id="052a8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="052a8-124">Requirement</span></span> | <span data-ttu-id="052a8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="052a8-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="052a8-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="052a8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="052a8-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="052a8-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="052a8-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="052a8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="052a8-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="052a8-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="052a8-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="052a8-130">Namespace</span></span><br/>                | <span data-ttu-id="052a8-131">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="052a8-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="052a8-132">MOF</span><span class="sxs-lookup"><span data-stu-id="052a8-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="052a8-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="052a8-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="052a8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="052a8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="052a8-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="052a8-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="052a8-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="052a8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="052a8-137">**\_Тсгатевайресаурцеграуп Win32**</span><span class="sxs-lookup"><span data-stu-id="052a8-137">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

