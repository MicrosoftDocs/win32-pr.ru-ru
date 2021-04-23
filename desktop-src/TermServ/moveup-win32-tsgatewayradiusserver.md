---
title: Метод MoveUp класса Win32_TSGatewayRADIUSServer
description: Перемещает этот протокол RADIUS сервер (RADIUS) на одну точку вверх в порядке приоритета.
ms.assetid: 060bb90d-72c0-4364-a44f-c6368434b174
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода MoveUp
- Службы удаленных рабочих столов метода MoveUp, класс Win32_TSGatewayRADIUSServer
- Класс Win32_TSGatewayRADIUSServer службы удаленных рабочих столов, метод MoveUp
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca93eee44abd147576c6e678dce871ae4d49d921
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535315"
---
# <a name="moveup-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="f5962-106">Метод MoveUp \_ класса Win32 тсгатевайрадиуссервер</span><span class="sxs-lookup"><span data-stu-id="f5962-106">MoveUp method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="f5962-107">Перемещает этот протокол RADIUS сервер (RADIUS) на одну точку вверх в порядке приоритета.</span><span class="sxs-lookup"><span data-stu-id="f5962-107">Moves this Remote Authentication Dial-In User Service (RADIUS) server one position up in the priority order.</span></span> <span data-ttu-id="f5962-108">Этот метод уменьшает свойство **Priority** текущего сервера RADIUS и увеличивает свойство **Priority** сервера RADIUS, предшествующее текущему серверу RADIUS.</span><span class="sxs-lookup"><span data-stu-id="f5962-108">This method decrements the **Priority** property of the current RADIUS server and increments the **Priority** property of the RADIUS server that precedes the current RADIUS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5962-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5962-109">Syntax</span></span>


```mof
uint32 MoveUp();
```



## <a name="parameters"></a><span data-ttu-id="f5962-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5962-110">Parameters</span></span>

<span data-ttu-id="f5962-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f5962-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5962-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5962-112">Return value</span></span>

<span data-ttu-id="f5962-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="f5962-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f5962-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f5962-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f5962-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f5962-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f5962-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5962-116">Remarks</span></span>

<span data-ttu-id="f5962-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="f5962-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f5962-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="f5962-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f5962-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="f5962-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f5962-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="f5962-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f5962-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f5962-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5962-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f5962-122">Requirements</span></span>



| <span data-ttu-id="f5962-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f5962-123">Requirement</span></span> | <span data-ttu-id="f5962-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f5962-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5962-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5962-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f5962-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f5962-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f5962-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5962-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f5962-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5962-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f5962-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f5962-129">Namespace</span></span><br/>                | <span data-ttu-id="f5962-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="f5962-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f5962-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f5962-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5962-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5962-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5962-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f5962-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5962-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5962-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f5962-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5962-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5962-136">**\_Тсгатевайрадиуссервер Win32**</span><span class="sxs-lookup"><span data-stu-id="f5962-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

