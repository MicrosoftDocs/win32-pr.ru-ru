---
title: Метод Делетеаллсерверс класса Win32_TSGatewayLoadBalancer
description: Удаляет все серверы балансировки нагрузки шлюза удаленный рабочий стол (шлюз удаленных рабочих столов), участвующие в ферме балансировки нагрузки.
ms.assetid: 091ed866-8f2b-47b8-990b-e9a6d7e1194c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Делетеаллсерверс
- Службы удаленных рабочих столов метода Делетеаллсерверс, класс Win32_TSGatewayLoadBalancer
- Класс Win32_TSGatewayLoadBalancer службы удаленных рабочих столов, метод Делетеаллсерверс
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.DeleteAllServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8004b4cfe811394acb328938775fcc9947bbbd19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533839"
---
# <a name="deleteallservers-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="689f8-106">Метод Делетеаллсерверс \_ класса Win32 тсгатевайлоадбаланцер</span><span class="sxs-lookup"><span data-stu-id="689f8-106">DeleteAllServers method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="689f8-107">Удаляет все серверы балансировки нагрузки шлюза удаленный рабочий стол (шлюз удаленных рабочих столов), участвующие в ферме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="689f8-107">Deletes all Remote Desktop Gateway (RD Gateway) load-balancing servers that are participating in the load-balancing farm.</span></span>

## <a name="syntax"></a><span data-ttu-id="689f8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="689f8-108">Syntax</span></span>


```mof
uint32 DeleteAllServers();
```



## <a name="parameters"></a><span data-ttu-id="689f8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="689f8-109">Parameters</span></span>

<span data-ttu-id="689f8-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="689f8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="689f8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="689f8-111">Return value</span></span>

<span data-ttu-id="689f8-112">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="689f8-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="689f8-113">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="689f8-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="689f8-114">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="689f8-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="689f8-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="689f8-115">Remarks</span></span>

<span data-ttu-id="689f8-116">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="689f8-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="689f8-117">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="689f8-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="689f8-118">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="689f8-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="689f8-119">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="689f8-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="689f8-120">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="689f8-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="689f8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="689f8-121">Requirements</span></span>



| <span data-ttu-id="689f8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="689f8-122">Requirement</span></span> | <span data-ttu-id="689f8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="689f8-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="689f8-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="689f8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="689f8-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="689f8-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="689f8-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="689f8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="689f8-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="689f8-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="689f8-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="689f8-128">Namespace</span></span><br/>                | <span data-ttu-id="689f8-129">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="689f8-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="689f8-130">MOF</span><span class="sxs-lookup"><span data-stu-id="689f8-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="689f8-131"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="689f8-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="689f8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="689f8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="689f8-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="689f8-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="689f8-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="689f8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="689f8-135">**\_Тсгатевайлоадбаланцер Win32**</span><span class="sxs-lookup"><span data-stu-id="689f8-135">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

