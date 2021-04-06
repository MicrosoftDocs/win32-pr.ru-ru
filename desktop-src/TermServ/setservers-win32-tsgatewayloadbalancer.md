---
title: Метод Сетсерверс класса Win32_TSGatewayLoadBalancer
description: Задает свойство Servers со списком серверов балансировки нагрузки шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: c82de8e2-301b-465d-b375-038b8a480cde
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсерверс
- Службы удаленных рабочих столов метода Сетсерверс, класс Win32_TSGatewayLoadBalancer
- Класс Win32_TSGatewayLoadBalancer службы удаленных рабочих столов, метод Сетсерверс
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.SetServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b28d1123ce82844fb501f3562014b93337502b51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802927"
---
# <a name="setservers-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="44fab-106">Метод Сетсерверс \_ класса Win32 тсгатевайлоадбаланцер</span><span class="sxs-lookup"><span data-stu-id="44fab-106">SetServers method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="44fab-107">Задает свойство **Servers** со списком серверов балансировки нагрузки шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="44fab-107">Sets the **Servers** property with the list of Remote Desktop Gateway (RD Gateway) load-balancing servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="44fab-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44fab-108">Syntax</span></span>


```mof
uint32 SetServers(
  [in] string Servers
);
```



## <a name="parameters"></a><span data-ttu-id="44fab-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="44fab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44fab-110">*Серверы* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44fab-110">*Servers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44fab-111">Разделенный точками с запятой список серверов балансировки нагрузки шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="44fab-111">Semicolon-separated list of RD Gateway load-balancing servers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44fab-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44fab-112">Return value</span></span>

<span data-ttu-id="44fab-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="44fab-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="44fab-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="44fab-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="44fab-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="44fab-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="44fab-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44fab-116">Remarks</span></span>

<span data-ttu-id="44fab-117">Если в параметре *Servers* указано несколько серверов, и один из серверов не может быть обработан, никакие серверы не будут обработаны.</span><span class="sxs-lookup"><span data-stu-id="44fab-117">If multiple servers are in the *Servers* parameter and one of the servers cannot be processed, none of the servers will be processed.</span></span>

<span data-ttu-id="44fab-118">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="44fab-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="44fab-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="44fab-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="44fab-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="44fab-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="44fab-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="44fab-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="44fab-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="44fab-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="44fab-123">Требования</span><span class="sxs-lookup"><span data-stu-id="44fab-123">Requirements</span></span>



| <span data-ttu-id="44fab-124">Требование</span><span class="sxs-lookup"><span data-stu-id="44fab-124">Requirement</span></span> | <span data-ttu-id="44fab-125">Значение</span><span class="sxs-lookup"><span data-stu-id="44fab-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="44fab-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44fab-126">Minimum supported client</span></span><br/> | <span data-ttu-id="44fab-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="44fab-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="44fab-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44fab-128">Minimum supported server</span></span><br/> | <span data-ttu-id="44fab-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44fab-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="44fab-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="44fab-130">Namespace</span></span><br/>                | <span data-ttu-id="44fab-131">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="44fab-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="44fab-132">MOF</span><span class="sxs-lookup"><span data-stu-id="44fab-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44fab-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44fab-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="44fab-134">DLL</span><span class="sxs-lookup"><span data-stu-id="44fab-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44fab-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44fab-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="44fab-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44fab-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44fab-137">**\_Тсгатевайлоадбаланцер Win32**</span><span class="sxs-lookup"><span data-stu-id="44fab-137">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

