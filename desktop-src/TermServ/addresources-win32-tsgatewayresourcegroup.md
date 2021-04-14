---
title: Метод Аддресаурцес класса Win32_TSGatewayResourceGroup
description: Добавляет ресурсы в группу ресурсов.
ms.assetid: 3210b468-6b82-4edb-ac8b-95f66a7b9328
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Аддресаурцес
- Службы удаленных рабочих столов метода Аддресаурцес, класс Win32_TSGatewayResourceGroup
- Класс Win32_TSGatewayResourceGroup службы удаленных рабочих столов, метод Аддресаурцес
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.AddResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37498accf76b28f16e0de45565916c18ab8d9dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533848"
---
# <a name="addresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="ba60a-106">Метод Аддресаурцес \_ класса Win32 тсгатевайресаурцеграуп</span><span class="sxs-lookup"><span data-stu-id="ba60a-106">AddResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="ba60a-107">Добавляет ресурсы в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba60a-107">Adds resources to the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba60a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba60a-108">Syntax</span></span>


```mof
uint32 AddResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="ba60a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba60a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba60a-110">*Ресурсы* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ba60a-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba60a-111">Разделенный точками с запятой список ресурсов, которые будут добавлены в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba60a-111">Semicolon-separated list of resources to be added to the resource group.</span></span> <span data-ttu-id="ba60a-112">" \* " Означает все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="ba60a-112">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba60a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba60a-113">Return value</span></span>

<span data-ttu-id="ba60a-114">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="ba60a-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ba60a-115">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="ba60a-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ba60a-116">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ba60a-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ba60a-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba60a-117">Remarks</span></span>

<span data-ttu-id="ba60a-118">Если в параметре *Resources* указано несколько ресурсов и один из ресурсов не может быть обработан, никакие ресурсы не будут обработаны.</span><span class="sxs-lookup"><span data-stu-id="ba60a-118">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="ba60a-119">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="ba60a-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ba60a-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="ba60a-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ba60a-121">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="ba60a-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ba60a-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="ba60a-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ba60a-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ba60a-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba60a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="ba60a-124">Requirements</span></span>



| <span data-ttu-id="ba60a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="ba60a-125">Requirement</span></span> | <span data-ttu-id="ba60a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ba60a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba60a-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba60a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ba60a-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ba60a-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ba60a-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba60a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ba60a-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba60a-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ba60a-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ba60a-131">Namespace</span></span><br/>                | <span data-ttu-id="ba60a-132">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="ba60a-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="ba60a-133">MOF</span><span class="sxs-lookup"><span data-stu-id="ba60a-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba60a-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba60a-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba60a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ba60a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba60a-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba60a-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ba60a-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba60a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba60a-138">**\_Тсгатевайресаурцеграуп Win32**</span><span class="sxs-lookup"><span data-stu-id="ba60a-138">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

