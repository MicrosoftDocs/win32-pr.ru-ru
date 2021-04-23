---
title: Метод ИслоадбаланЦингсервер класса Win32_TSGatewayLoadBalancer
description: Определяет, может ли сервер шлюза удаленный рабочий стол (шлюз удаленных рабочих столов) выполнять балансировку нагрузки.
ms.assetid: ae1a91c1-0b8b-4bd0-83f9-41c973247f27
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода ИслоадбаланЦингсервер
- Службы удаленных рабочих столов метода ИслоадбаланЦингсервер, класс Win32_TSGatewayLoadBalancer
- Класс Win32_TSGatewayLoadBalancer службы удаленных рабочих столов, метод ИслоадбаланЦингсервер
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.IsLoadBalancingServer
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eae909df4074c8129a1b49eb0d5c3b336fed5d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681958"
---
# <a name="isloadbalancingserver-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="a5e90-106">Метод ИслоадбаланЦингсервер \_ класса Win32 тсгатевайлоадбаланцер</span><span class="sxs-lookup"><span data-stu-id="a5e90-106">IsLoadBalancingServer method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="a5e90-107">Определяет, может ли сервер шлюза удаленный рабочий стол (шлюз удаленных рабочих столов) выполнять балансировку нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a5e90-107">Determines whether the Remote Desktop Gateway (RD Gateway) server can perform load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5e90-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5e90-108">Syntax</span></span>


```mof
uint32 IsLoadBalancingServer(
  [out] boolean LoadBalancing
);
```



## <a name="parameters"></a><span data-ttu-id="a5e90-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5e90-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5e90-110">*LoadBalancing* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a5e90-110">*LoadBalancing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e90-111">**Значение true** , если сервер может выполнять балансировку нагрузки, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a5e90-111">**TRUE** if the server can perform load balancing, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5e90-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5e90-112">Return value</span></span>

<span data-ttu-id="a5e90-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="a5e90-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a5e90-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="a5e90-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a5e90-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a5e90-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a5e90-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5e90-116">Remarks</span></span>

<span data-ttu-id="a5e90-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="a5e90-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a5e90-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="a5e90-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a5e90-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="a5e90-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a5e90-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="a5e90-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a5e90-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a5e90-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5e90-122">Требования</span><span class="sxs-lookup"><span data-stu-id="a5e90-122">Requirements</span></span>



| <span data-ttu-id="a5e90-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a5e90-123">Requirement</span></span> | <span data-ttu-id="a5e90-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a5e90-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5e90-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5e90-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a5e90-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a5e90-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a5e90-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5e90-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a5e90-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5e90-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a5e90-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a5e90-129">Namespace</span></span><br/>                | <span data-ttu-id="a5e90-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="a5e90-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a5e90-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a5e90-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5e90-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5e90-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5e90-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a5e90-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5e90-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5e90-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a5e90-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5e90-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5e90-136">**\_Тсгатевайлоадбаланцер Win32**</span><span class="sxs-lookup"><span data-stu-id="a5e90-136">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

