---
title: Метод Update класса Win32_TSGatewayResourceGroup
description: Обновляет группу ресурсов.
ms.assetid: b5927046-f461-41cd-861b-0fd77f2008e5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода обновления
- Метод Update службы удаленных рабочих столов, класс Win32_TSGatewayResourceGroup
- Класс Win32_TSGatewayResourceGroup службы удаленных рабочих столов, метод Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a7b1610fc14aa522fa4d8b7caf03fccd7b37375
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415633"
---
# <a name="update-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="60c15-106">Метод Update \_ класса Win32 тсгатевайресаурцеграуп</span><span class="sxs-lookup"><span data-stu-id="60c15-106">Update method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="60c15-107">Обновляет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60c15-107">Updates the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="60c15-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60c15-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string Name,
  [in] string Description,
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="60c15-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="60c15-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60c15-110">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60c15-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60c15-111">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60c15-111">Name of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="60c15-112">*Описание* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60c15-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60c15-113">Описание группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60c15-113">Description of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="60c15-114">*Ресурсы* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60c15-114">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60c15-115">Разделенный точками с запятой список ресурсов в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60c15-115">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="60c15-116">" \* " Означает все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="60c15-116">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60c15-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60c15-117">Return value</span></span>

<span data-ttu-id="60c15-118">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="60c15-118">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="60c15-119">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="60c15-119">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="60c15-120">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="60c15-120">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="60c15-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="60c15-121">Remarks</span></span>

<span data-ttu-id="60c15-122">Если в параметре *Resources* указано несколько ресурсов и один из ресурсов не может быть обработан, никакие ресурсы не будут обработаны.</span><span class="sxs-lookup"><span data-stu-id="60c15-122">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="60c15-123">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="60c15-123">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="60c15-124">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="60c15-124">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="60c15-125">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="60c15-125">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="60c15-126">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="60c15-126">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="60c15-127">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="60c15-127">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="60c15-128">Требования</span><span class="sxs-lookup"><span data-stu-id="60c15-128">Requirements</span></span>



| <span data-ttu-id="60c15-129">Требование</span><span class="sxs-lookup"><span data-stu-id="60c15-129">Requirement</span></span> | <span data-ttu-id="60c15-130">Значение</span><span class="sxs-lookup"><span data-stu-id="60c15-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="60c15-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60c15-131">Minimum supported client</span></span><br/> | <span data-ttu-id="60c15-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="60c15-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="60c15-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60c15-133">Minimum supported server</span></span><br/> | <span data-ttu-id="60c15-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60c15-134">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="60c15-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="60c15-135">Namespace</span></span><br/>                | <span data-ttu-id="60c15-136">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="60c15-136">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="60c15-137">MOF</span><span class="sxs-lookup"><span data-stu-id="60c15-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60c15-138"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60c15-138"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="60c15-139">DLL</span><span class="sxs-lookup"><span data-stu-id="60c15-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60c15-140"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60c15-140"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="60c15-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60c15-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60c15-142">**\_Тсгатевайресаурцеграуп Win32**</span><span class="sxs-lookup"><span data-stu-id="60c15-142">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

