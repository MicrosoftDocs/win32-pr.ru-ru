---
title: Метод Сетброкерхамоде класса Win32_SessionBrokerServiceProperties
description: Переносит данные из локальной базы данных WID в новую базу данных на основе SQL Server. Он также настраивает сервер брокера для использования центрального SQL Server.
ms.assetid: 8f14590d-3042-403c-a1cb-a3b257866284
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетброкерхамоде
- Службы удаленных рабочих столов метода Сетброкерхамоде, класс Win32_SessionBrokerServiceProperties
- Класс Win32_SessionBrokerServiceProperties службы удаленных рабочих столов, метод Сетброкерхамоде
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4526f8ded96086ccf223b3c8e5aad72d9e0262cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135894"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="f7608-107">Метод Сетброкерхамоде \_ класса Win32 сессионброкерсервицепропертиес</span><span class="sxs-lookup"><span data-stu-id="f7608-107">SetBrokerHAMode method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="f7608-108">Переносит данные из локальной базы данных WID в новую базу данных на основе SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f7608-108">Migrates data from a local WID database to the new SQL server-based database.</span></span> <span data-ttu-id="f7608-109">Он также настраивает сервер брокера для использования центрального SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f7608-109">It also configures the broker server to use the central SQL server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7608-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7608-110">Syntax</span></span>


```mof
uint32 SetBrokerHAMode(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms,
  [in] string brokerDnsRRName,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a><span data-ttu-id="f7608-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7608-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7608-112">*коннстрингтоцентралдбрдкмс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7608-112">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7608-113">Строка подключения к центральной базе данных.</span><span class="sxs-lookup"><span data-stu-id="f7608-113">Connection string to the central database.</span></span>

</dd> <dt>

<span data-ttu-id="f7608-114">*секондариконнстрингтоцентралдбрдкмс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7608-114">*secondaryConnStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7608-115">Вторичная строка подключения к центральной базе данных.</span><span class="sxs-lookup"><span data-stu-id="f7608-115">Secondary connection string to the central database.</span></span>

<span data-ttu-id="f7608-116">**Windows server 2012 R2 и Windows server 2012:** Этот параметр недоступен до Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="f7608-116">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="f7608-117">*брокерднсррнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7608-117">*brokerDnsRRName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7608-118">Имя DNS компонента Service Broker.</span><span class="sxs-lookup"><span data-stu-id="f7608-118">Broker DNS name.</span></span>

</dd> <dt>

<span data-ttu-id="f7608-119">*активеброкернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7608-119">*activeBrokerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7608-120">Имя активного брокера.</span><span class="sxs-lookup"><span data-stu-id="f7608-120">Active broker name.</span></span>

<span data-ttu-id="f7608-121">**Windows server 2012 R2 и Windows server 2012:** Этот параметр недоступен до Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="f7608-121">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7608-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f7608-122">Requirements</span></span>



| <span data-ttu-id="f7608-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f7608-123">Requirement</span></span> | <span data-ttu-id="f7608-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f7608-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7608-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7608-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f7608-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f7608-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f7608-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7608-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f7608-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f7608-128">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="f7608-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f7608-129">Namespace</span></span><br/>                | <span data-ttu-id="f7608-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="f7608-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="f7608-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f7608-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7608-132"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7608-132"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7608-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f7608-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7608-134"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7608-134"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7608-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7608-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7608-136">**\_Сессионброкерсервицепропертиес Win32**</span><span class="sxs-lookup"><span data-stu-id="f7608-136">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





