---
title: Метод CheckStatus класса Win32_TSGatewayConnection
description: Проверяет состояние подключения сервера шлюза удаленный рабочий стол (удаленных рабочих столов) к другому компьютеру и определяет, настроен ли целевой компьютер для балансировки нагрузки.
ms.assetid: e8ee3d40-76eb-401f-b255-bccd7ba8c058
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода CheckStatus
- Службы удаленных рабочих столов метода CheckStatus, класс Win32_TSGatewayConnection
- Класс Win32_TSGatewayConnection службы удаленных рабочих столов, метод CheckStatus
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.CheckStatus
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babb083af5c0581abe27d442a466c3d6114b957a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681812"
---
# <a name="checkstatus-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="5930a-106">Метод CheckStatus \_ класса Win32 тсгатевайконнектион</span><span class="sxs-lookup"><span data-stu-id="5930a-106">CheckStatus method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="5930a-107">Проверяет состояние подключения сервера шлюза удаленный рабочий стол (удаленных рабочих столов) к другому компьютеру и определяет, настроен ли целевой компьютер для балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5930a-107">Checks the status of a Remote Desktop Gateway (RD Gateway) server connection to another computer, and determines whether the target computer is configured for load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="5930a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5930a-108">Syntax</span></span>


```mof
uint32 CheckStatus(
  [in] string ServerName,
  [in] string EndPointName
);
```



## <a name="parameters"></a><span data-ttu-id="5930a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5930a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5930a-110">*Имя сервера* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5930a-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5930a-111">Имя исходного сервера шлюза удаленных рабочих столов, с которого проверяется подключение.</span><span class="sxs-lookup"><span data-stu-id="5930a-111">The name of the source RD Gateway server from which the connection is checked.</span></span>

</dd> <dt>

<span data-ttu-id="5930a-112">*EndPointName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5930a-112">*EndPointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5930a-113">Имя целевого сервера (конечной точки), к которому проверяется доступ с исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="5930a-113">The name of the target server (the endpoint) to which access is checked from the source server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5930a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5930a-114">Return value</span></span>

<span data-ttu-id="5930a-115">Этот метод возвращает следующие возможные возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="5930a-115">This method returns the following possible return values.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="5930a-116">0</span><span class="sxs-lookup"><span data-stu-id="5930a-116">0</span></span>

<span data-ttu-id="5930a-117">Состояние подключения — ОК.</span><span class="sxs-lookup"><span data-stu-id="5930a-117">The connection status is OK.</span></span> <span data-ttu-id="5930a-118">Конечная точка доступна и настроена для балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5930a-118">The endpoint is reachable and is configured for load balancing.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5930a-119">1</span><span class="sxs-lookup"><span data-stu-id="5930a-119">1</span></span>

<span data-ttu-id="5930a-120">Состояние подключения неизвестно.</span><span class="sxs-lookup"><span data-stu-id="5930a-120">The connection status is unknown.</span></span> <span data-ttu-id="5930a-121">Скорее всего, возникло исключение.</span><span class="sxs-lookup"><span data-stu-id="5930a-121">Most likely, an exception occurred.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5930a-122">0x80075c34</span><span class="sxs-lookup"><span data-stu-id="5930a-122">0x80075c34</span></span>

<span data-ttu-id="5930a-123">Конечная точка либо недоступна, либо не настроена для балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5930a-123">The endpoint is either not reachable, or it is not configured for load balancing.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5930a-124">0x80075c32</span><span class="sxs-lookup"><span data-stu-id="5930a-124">0x80075c32</span></span>

<span data-ttu-id="5930a-125">Произошла ошибка состояния.</span><span class="sxs-lookup"><span data-stu-id="5930a-125">A status error occurred.</span></span> <span data-ttu-id="5930a-126">Конечная точка доступна, но служба балансировки нагрузки RPC/HTTP (РПЧТТПЛБС) не запущена на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="5930a-126">The endpoint is reachable, but the RPC/HTTP Load Balancing Service (RPCHTTPLBS) service is not started on the target computer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5930a-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5930a-127">Remarks</span></span>

<span data-ttu-id="5930a-128">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="5930a-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5930a-129">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="5930a-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5930a-130">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="5930a-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5930a-131">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5930a-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5930a-132">Требования</span><span class="sxs-lookup"><span data-stu-id="5930a-132">Requirements</span></span>



| <span data-ttu-id="5930a-133">Требование</span><span class="sxs-lookup"><span data-stu-id="5930a-133">Requirement</span></span> | <span data-ttu-id="5930a-134">Значение</span><span class="sxs-lookup"><span data-stu-id="5930a-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5930a-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5930a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5930a-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5930a-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5930a-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5930a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5930a-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5930a-138">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5930a-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5930a-139">Namespace</span></span><br/>                | <span data-ttu-id="5930a-140">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="5930a-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5930a-141">MOF</span><span class="sxs-lookup"><span data-stu-id="5930a-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5930a-142"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5930a-142"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5930a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5930a-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5930a-144"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5930a-144"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5930a-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5930a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5930a-146">**\_Тсгатевайконнектион Win32**</span><span class="sxs-lookup"><span data-stu-id="5930a-146">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

