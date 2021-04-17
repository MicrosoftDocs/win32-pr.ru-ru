---
title: Метод SetDescription класса Win32_TSGatewayResourceGroup
description: Задает свойство Description для группы ресурсов.
ms.assetid: ab1280c7-ce53-4807-9537-953b597dd636
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода SetDescription
- Службы удаленных рабочих столов метода SetDescription, класс Win32_TSGatewayResourceGroup
- Класс Win32_TSGatewayResourceGroup службы удаленных рабочих столов, метод SetDescription
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetDescription
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d815cc5400a182f2dff3b982643d5e6bfd861002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672871"
---
# <a name="setdescription-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="82809-106">Метод SetDescription \_ класса Win32 тсгатевайресаурцеграуп</span><span class="sxs-lookup"><span data-stu-id="82809-106">SetDescription method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="82809-107">Задает свойство **Description** для группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82809-107">Sets the **Description** property for the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="82809-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82809-108">Syntax</span></span>


```mof
uint32 SetDescription(
  [in] string Description
);
```



## <a name="parameters"></a><span data-ttu-id="82809-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="82809-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82809-110">*Описание* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="82809-110">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82809-111">Описание группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82809-111">Description of the resource group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82809-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82809-112">Return value</span></span>

<span data-ttu-id="82809-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="82809-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="82809-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="82809-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="82809-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="82809-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="82809-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82809-116">Remarks</span></span>

<span data-ttu-id="82809-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="82809-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="82809-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="82809-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="82809-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="82809-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="82809-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="82809-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="82809-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="82809-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="82809-122">Требования</span><span class="sxs-lookup"><span data-stu-id="82809-122">Requirements</span></span>



| <span data-ttu-id="82809-123">Требование</span><span class="sxs-lookup"><span data-stu-id="82809-123">Requirement</span></span> | <span data-ttu-id="82809-124">Значение</span><span class="sxs-lookup"><span data-stu-id="82809-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="82809-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82809-125">Minimum supported client</span></span><br/> | <span data-ttu-id="82809-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="82809-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="82809-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82809-127">Minimum supported server</span></span><br/> | <span data-ttu-id="82809-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82809-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="82809-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="82809-129">Namespace</span></span><br/>                | <span data-ttu-id="82809-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="82809-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="82809-131">MOF</span><span class="sxs-lookup"><span data-stu-id="82809-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82809-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82809-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="82809-133">DLL</span><span class="sxs-lookup"><span data-stu-id="82809-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82809-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82809-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="82809-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82809-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82809-136">**\_Тсгатевайресаурцеграуп Win32**</span><span class="sxs-lookup"><span data-stu-id="82809-136">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

