---
title: Метод Remove класса Win32_TSGatewayRADIUSServer
description: Удаляет текущий сервер протокол RADIUS (RADIUS).
ms.assetid: 915f6d38-ba6a-4994-8bb9-bfddb9aa6ff8
ms.tgt_platform: multiple
keywords:
- Удалить метод службы удаленных рабочих столов
- Удаление метода службы удаленных рабочих столов, Win32_TSGatewayRADIUSServer Interface
- Службы удаленных рабочих столов интерфейса Win32_TSGatewayRADIUSServer, метод Remove
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Remove
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a91fc4a3ba8bf638dcffd76e3bf3517795674fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341105"
---
# <a name="remove-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="4878f-106">Метод Remove класса Win32 \_ тсгатевайрадиуссервер</span><span class="sxs-lookup"><span data-stu-id="4878f-106">Remove method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="4878f-107">Удаляет текущий сервер протокол RADIUS (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="4878f-107">Removes the current Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="4878f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4878f-108">Syntax</span></span>


```mof
uint32 Remove();
```



## <a name="parameters"></a><span data-ttu-id="4878f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4878f-109">Parameters</span></span>

<span data-ttu-id="4878f-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4878f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4878f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4878f-111">Return value</span></span>

<span data-ttu-id="4878f-112">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="4878f-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4878f-113">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="4878f-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4878f-114">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4878f-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4878f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4878f-115">Remarks</span></span>

<span data-ttu-id="4878f-116">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="4878f-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="4878f-117">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="4878f-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4878f-118">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="4878f-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4878f-119">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="4878f-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4878f-120">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4878f-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4878f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4878f-121">Requirements</span></span>



| <span data-ttu-id="4878f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4878f-122">Requirement</span></span> | <span data-ttu-id="4878f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4878f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4878f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4878f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4878f-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4878f-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4878f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4878f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4878f-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4878f-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4878f-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4878f-128">Namespace</span></span><br/>                | <span data-ttu-id="4878f-129">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="4878f-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="4878f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4878f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4878f-131"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4878f-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="4878f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4878f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4878f-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4878f-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4878f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4878f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4878f-135">**\_Тсгатевайрадиуссервер Win32**</span><span class="sxs-lookup"><span data-stu-id="4878f-135">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

