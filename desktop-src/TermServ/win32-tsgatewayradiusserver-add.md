---
title: Метод Add класса Win32_TSGatewayRADIUSServer
description: Добавляет новый сервер протокол RADIUS (RADIUS).
ms.assetid: 78f74bb6-8f70-4bc1-8e4d-1670a3ae3f31
ms.tgt_platform: multiple
keywords:
- Добавить службы удаленных рабочих столов метода
- Добавление службы удаленных рабочих столов метода, Win32_TSGatewayRADIUSServer интерфейса
- Службы удаленных рабочих столов интерфейса Win32_TSGatewayRADIUSServer, Добавление метода
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Add
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6869c55a6704944c34c68af065875cad92e8385c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672823"
---
# <a name="add-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="939a4-106">Метод Add \_ класса Win32 тсгатевайрадиуссервер</span><span class="sxs-lookup"><span data-stu-id="939a4-106">Add method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="939a4-107">Добавляет новый сервер протокол RADIUS (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="939a4-107">Adds a new Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="939a4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="939a4-108">Syntax</span></span>


```mof
uint32 Add(
  [in] string Name,
  [in] string SharedSecret
);
```



## <a name="parameters"></a><span data-ttu-id="939a4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="939a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="939a4-110">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="939a4-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="939a4-111">Имя сервера RADIUS.</span><span class="sxs-lookup"><span data-stu-id="939a4-111">RADIUS server name.</span></span>

</dd> <dt>

<span data-ttu-id="939a4-112">*SharedSecret* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="939a4-112">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="939a4-113">Общий секрет для сервера RADIUS.</span><span class="sxs-lookup"><span data-stu-id="939a4-113">Shared secret for the RADIUS server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="939a4-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="939a4-114">Return value</span></span>

<span data-ttu-id="939a4-115">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="939a4-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="939a4-116">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="939a4-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="939a4-117">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="939a4-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="939a4-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="939a4-118">Remarks</span></span>

<span data-ttu-id="939a4-119">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="939a4-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="939a4-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="939a4-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="939a4-121">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="939a4-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="939a4-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="939a4-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="939a4-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="939a4-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="939a4-124">Требования</span><span class="sxs-lookup"><span data-stu-id="939a4-124">Requirements</span></span>



| <span data-ttu-id="939a4-125">Требование</span><span class="sxs-lookup"><span data-stu-id="939a4-125">Requirement</span></span> | <span data-ttu-id="939a4-126">Значение</span><span class="sxs-lookup"><span data-stu-id="939a4-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="939a4-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="939a4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="939a4-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="939a4-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="939a4-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="939a4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="939a4-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="939a4-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="939a4-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="939a4-131">Namespace</span></span><br/>                | <span data-ttu-id="939a4-132">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="939a4-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="939a4-133">MOF</span><span class="sxs-lookup"><span data-stu-id="939a4-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="939a4-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="939a4-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="939a4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="939a4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="939a4-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="939a4-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="939a4-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="939a4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="939a4-138">**\_Тсгатевайрадиуссервер Win32**</span><span class="sxs-lookup"><span data-stu-id="939a4-138">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

