---
title: Метод Create класса Win32_TSGatewayResourceGroup
description: Создает группу ресурсов.
ms.assetid: 715e6086-1c7d-4b20-983a-3ab98e875ca5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Create
- Создание службы удаленных рабочих столов метода, Win32_TSGatewayResourceGroup класса
- Класс Win32_TSGatewayResourceGroup службы удаленных рабочих столов, метод Create
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9c5179967c143faa36763b7a2aabb8849d2f13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071288"
---
# <a name="create-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="86f52-106">Метод Create \_ класса Win32 тсгатевайресаурцеграуп</span><span class="sxs-lookup"><span data-stu-id="86f52-106">Create method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="86f52-107">Создает группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86f52-107">Creates a resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="86f52-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86f52-108">Syntax</span></span>


```mof
uint32 Create(
  [in] string Name,
  [in] string Description,
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="86f52-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="86f52-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86f52-110">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86f52-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86f52-111">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86f52-111">Name of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="86f52-112">*Описание* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86f52-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86f52-113">Описание группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86f52-113">Description of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="86f52-114">*Ресурсы* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86f52-114">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86f52-115">Разделенный точками с запятой список ресурсов в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86f52-115">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="86f52-116">" \* " Означает все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="86f52-116">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86f52-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86f52-117">Return value</span></span>

<span data-ttu-id="86f52-118">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="86f52-118">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="86f52-119">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="86f52-119">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="86f52-120">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="86f52-120">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="86f52-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86f52-121">Remarks</span></span>

<span data-ttu-id="86f52-122">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="86f52-122">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="86f52-123">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="86f52-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="86f52-124">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="86f52-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="86f52-125">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="86f52-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="86f52-126">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="86f52-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="86f52-127">Требования</span><span class="sxs-lookup"><span data-stu-id="86f52-127">Requirements</span></span>



| <span data-ttu-id="86f52-128">Требование</span><span class="sxs-lookup"><span data-stu-id="86f52-128">Requirement</span></span> | <span data-ttu-id="86f52-129">Значение</span><span class="sxs-lookup"><span data-stu-id="86f52-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="86f52-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86f52-130">Minimum supported client</span></span><br/> | <span data-ttu-id="86f52-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="86f52-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="86f52-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86f52-132">Minimum supported server</span></span><br/> | <span data-ttu-id="86f52-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86f52-133">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="86f52-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="86f52-134">Namespace</span></span><br/>                | <span data-ttu-id="86f52-135">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="86f52-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="86f52-136">MOF</span><span class="sxs-lookup"><span data-stu-id="86f52-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86f52-137"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86f52-137"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="86f52-138">DLL</span><span class="sxs-lookup"><span data-stu-id="86f52-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86f52-139"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86f52-139"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="86f52-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86f52-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86f52-141">**\_Тсгатевайресаурцеграуп Win32**</span><span class="sxs-lookup"><span data-stu-id="86f52-141">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

