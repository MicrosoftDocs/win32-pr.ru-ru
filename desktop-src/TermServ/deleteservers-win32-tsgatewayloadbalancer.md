---
title: Метод Делетесерверс класса Win32_TSGatewayLoadBalancer
description: Удаляет серверы из свойства Servers.
ms.assetid: 5ef44725-82b6-464a-abab-a68cc8799669
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Делетесерверс
- Службы удаленных рабочих столов метода Делетесерверс, класс Win32_TSGatewayLoadBalancer
- Класс Win32_TSGatewayLoadBalancer службы удаленных рабочих столов, метод Делетесерверс
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.DeleteServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b889f37b783853fbca0b9cb399a83959e2522d0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414941"
---
# <a name="deleteservers-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="5025a-106">Метод Делетесерверс \_ класса Win32 тсгатевайлоадбаланцер</span><span class="sxs-lookup"><span data-stu-id="5025a-106">DeleteServers method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="5025a-107">Удаляет серверы из свойства **Servers** .</span><span class="sxs-lookup"><span data-stu-id="5025a-107">Deletes servers from the **Servers** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5025a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5025a-108">Syntax</span></span>


```mof
uint32 DeleteServers(
  [in] string Servers
);
```



## <a name="parameters"></a><span data-ttu-id="5025a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5025a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5025a-110">*Серверы* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5025a-110">*Servers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5025a-111">Разделенный точками с запятой список серверов балансировки нагрузки шлюза удаленных рабочих столов для удаления из свойства " **серверы** ".</span><span class="sxs-lookup"><span data-stu-id="5025a-111">Semicolon-separated list of RD Gateway load-balancing servers to delete from the **Servers** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5025a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5025a-112">Return value</span></span>

<span data-ttu-id="5025a-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="5025a-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5025a-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="5025a-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5025a-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5025a-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5025a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5025a-116">Remarks</span></span>

<span data-ttu-id="5025a-117">Если в параметре *Servers* указано несколько серверов, и один из серверов не может быть обработан, никакие серверы не будут обработаны.</span><span class="sxs-lookup"><span data-stu-id="5025a-117">If multiple servers are in the *Servers* parameter and one of the servers cannot be processed, none of the servers will be processed.</span></span>

<span data-ttu-id="5025a-118">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="5025a-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5025a-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="5025a-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5025a-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="5025a-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5025a-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="5025a-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5025a-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5025a-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5025a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5025a-123">Requirements</span></span>



| <span data-ttu-id="5025a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5025a-124">Requirement</span></span> | <span data-ttu-id="5025a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5025a-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5025a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5025a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5025a-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5025a-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5025a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5025a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5025a-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5025a-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5025a-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5025a-130">Namespace</span></span><br/>                | <span data-ttu-id="5025a-131">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="5025a-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5025a-132">MOF</span><span class="sxs-lookup"><span data-stu-id="5025a-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5025a-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5025a-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5025a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5025a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5025a-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5025a-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5025a-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5025a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5025a-137">**\_Тсгатевайлоадбаланцер Win32**</span><span class="sxs-lookup"><span data-stu-id="5025a-137">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

