---
title: Метод SetName класса Win32_TSGatewayRADIUSServer
description: Задает свойство Name для этого сервера протокол RADIUS (RADIUS).
ms.assetid: 2dabc6fb-7740-4039-9bbd-5b2490fe5988
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода SetName
- Службы удаленных рабочих столов метода SetName, класс Win32_TSGatewayRADIUSServer
- Класс Win32_TSGatewayRADIUSServer службы удаленных рабочих столов, метод SetName
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc4b563c59ce1546b4cf471653407e3390676625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802261"
---
# <a name="setname-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="be034-106">Метод SetName \_ класса Win32 тсгатевайрадиуссервер</span><span class="sxs-lookup"><span data-stu-id="be034-106">SetName method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="be034-107">Задает свойство **Name** для этого сервера протокол RADIUS (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="be034-107">Sets the **Name** property for this Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="be034-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be034-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="be034-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="be034-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be034-110">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be034-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be034-111">Новое имя.</span><span class="sxs-lookup"><span data-stu-id="be034-111">New name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be034-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be034-112">Return value</span></span>

<span data-ttu-id="be034-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="be034-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="be034-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="be034-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="be034-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="be034-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="be034-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be034-116">Remarks</span></span>

<span data-ttu-id="be034-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="be034-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="be034-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="be034-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="be034-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="be034-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="be034-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="be034-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="be034-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="be034-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="be034-122">Требования</span><span class="sxs-lookup"><span data-stu-id="be034-122">Requirements</span></span>



| <span data-ttu-id="be034-123">Требование</span><span class="sxs-lookup"><span data-stu-id="be034-123">Requirement</span></span> | <span data-ttu-id="be034-124">Значение</span><span class="sxs-lookup"><span data-stu-id="be034-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="be034-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be034-125">Minimum supported client</span></span><br/> | <span data-ttu-id="be034-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="be034-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="be034-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be034-127">Minimum supported server</span></span><br/> | <span data-ttu-id="be034-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be034-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="be034-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="be034-129">Namespace</span></span><br/>                | <span data-ttu-id="be034-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="be034-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="be034-131">MOF</span><span class="sxs-lookup"><span data-stu-id="be034-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be034-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be034-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="be034-133">DLL</span><span class="sxs-lookup"><span data-stu-id="be034-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be034-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be034-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="be034-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be034-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be034-136">**\_Тсгатевайрадиуссервер Win32**</span><span class="sxs-lookup"><span data-stu-id="be034-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

