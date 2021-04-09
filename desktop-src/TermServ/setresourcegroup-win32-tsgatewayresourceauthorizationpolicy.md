---
title: Метод Сетресаурцеграуп класса Win32_TSGatewayResourceAuthorizationPolicy
description: Задает тип и имя группы ресурсов.
ms.assetid: a3dd0ffa-a39b-46f9-8317-fcc90a8afcd1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетресаурцеграуп
- Службы удаленных рабочих столов метода Сетресаурцеграуп, класс Win32_TSGatewayResourceAuthorizationPolicy
- Класс Win32_TSGatewayResourceAuthorizationPolicy службы удаленных рабочих столов, метод Сетресаурцеграуп
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetResourceGroup
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22c2ceacbbbfc40372d0f0d084cf6525f754934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892261"
---
# <a name="setresourcegroup-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="b6290-106">Метод Сетресаурцеграуп \_ класса Win32 тсгатевайресаурцеаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="b6290-106">SetResourceGroup method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="b6290-107">Задает тип и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b6290-107">Sets the resource group type and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6290-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6290-108">Syntax</span></span>


```mof
uint32 SetResourceGroup(
  [in] string ResourceGroupName,
  [in] string ResourceGroupType
);
```



## <a name="parameters"></a><span data-ttu-id="b6290-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6290-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6290-110">*ResourceGroupName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b6290-110">*ResourceGroupName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6290-111">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b6290-111">Resource group name.</span></span> <span data-ttu-id="b6290-112">Это значение заменяет существующее свойство **ResourceGroupName** .</span><span class="sxs-lookup"><span data-stu-id="b6290-112">This value replaces the existing **ResourceGroupName** property.</span></span>

</dd> <dt>

<span data-ttu-id="b6290-113">*Ресаурцеграуптипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b6290-113">*ResourceGroupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6290-114">Определяет тип группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b6290-114">Identifies the type of the resource group.</span></span> <span data-ttu-id="b6290-115">Это значение заменяет существующее свойство **ресаурцеграуптипе** .</span><span class="sxs-lookup"><span data-stu-id="b6290-115">This value replaces the existing **ResourceGroupType** property.</span></span>

<dt>

<span data-ttu-id="b6290-116">RG</span><span class="sxs-lookup"><span data-stu-id="b6290-116">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="b6290-117">группа ресурсов;</span><span class="sxs-lookup"><span data-stu-id="b6290-117">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="b6290-118">CG</span><span class="sxs-lookup"><span data-stu-id="b6290-118">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="b6290-119">Группа компьютеров, сохраненная в домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="b6290-119">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="b6290-120">КАЖДОГО</span><span class="sxs-lookup"><span data-stu-id="b6290-120">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="b6290-121">Все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="b6290-121">All resources.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6290-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6290-122">Return value</span></span>

<span data-ttu-id="b6290-123">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="b6290-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b6290-124">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="b6290-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b6290-125">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b6290-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b6290-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6290-126">Remarks</span></span>

<span data-ttu-id="b6290-127">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="b6290-127">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b6290-128">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="b6290-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b6290-129">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="b6290-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b6290-130">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="b6290-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b6290-131">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b6290-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6290-132">Требования</span><span class="sxs-lookup"><span data-stu-id="b6290-132">Requirements</span></span>



| <span data-ttu-id="b6290-133">Требование</span><span class="sxs-lookup"><span data-stu-id="b6290-133">Requirement</span></span> | <span data-ttu-id="b6290-134">Значение</span><span class="sxs-lookup"><span data-stu-id="b6290-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6290-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6290-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b6290-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b6290-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b6290-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6290-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b6290-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6290-138">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b6290-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b6290-139">Namespace</span></span><br/>                | <span data-ttu-id="b6290-140">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="b6290-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b6290-141">MOF</span><span class="sxs-lookup"><span data-stu-id="b6290-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6290-142"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6290-142"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6290-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b6290-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6290-144"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6290-144"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b6290-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6290-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6290-146">**\_Тсгатевайресаурцеаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="b6290-146">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

