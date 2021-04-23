---
title: Метод Сетресаурцес класса Win32_TSGatewayResourceGroup
description: Задает свойство Resources для этой группы ресурсов.
ms.assetid: 0043ee04-26d1-4907-87cc-a15f72cb0b93
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетресаурцес
- Службы удаленных рабочих столов метода Сетресаурцес, класс Win32_TSGatewayResourceGroup
- Класс Win32_TSGatewayResourceGroup службы удаленных рабочих столов, метод Сетресаурцес
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23f2ca14597fc7d6ce3660e6e180bf93dfd86cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415149"
---
# <a name="setresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="5515e-106">Метод Сетресаурцес \_ класса Win32 тсгатевайресаурцеграуп</span><span class="sxs-lookup"><span data-stu-id="5515e-106">SetResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="5515e-107">Задает свойство **Resources** для этой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5515e-107">Sets the **Resources** property for this resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="5515e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5515e-108">Syntax</span></span>


```mof
uint32 SetResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="5515e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5515e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5515e-110">*Ресурсы* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5515e-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5515e-111">Разделенный точками с запятой список ресурсов в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5515e-111">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="5515e-112">" \* " Означает все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="5515e-112">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5515e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5515e-113">Return value</span></span>

<span data-ttu-id="5515e-114">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="5515e-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5515e-115">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="5515e-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5515e-116">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5515e-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5515e-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5515e-117">Remarks</span></span>

<span data-ttu-id="5515e-118">Если в параметре *Resources* указано несколько ресурсов и один из ресурсов не может быть обработан, никакие ресурсы не будут обработаны.</span><span class="sxs-lookup"><span data-stu-id="5515e-118">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="5515e-119">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="5515e-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5515e-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="5515e-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5515e-121">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="5515e-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5515e-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="5515e-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5515e-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5515e-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5515e-124">Требования</span><span class="sxs-lookup"><span data-stu-id="5515e-124">Requirements</span></span>



| <span data-ttu-id="5515e-125">Требование</span><span class="sxs-lookup"><span data-stu-id="5515e-125">Requirement</span></span> | <span data-ttu-id="5515e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="5515e-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5515e-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5515e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5515e-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5515e-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5515e-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5515e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5515e-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5515e-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5515e-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5515e-131">Namespace</span></span><br/>                | <span data-ttu-id="5515e-132">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="5515e-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5515e-133">MOF</span><span class="sxs-lookup"><span data-stu-id="5515e-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5515e-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5515e-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5515e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5515e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5515e-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5515e-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5515e-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5515e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5515e-138">**\_Тсгатевайресаурцеграуп Win32**</span><span class="sxs-lookup"><span data-stu-id="5515e-138">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

