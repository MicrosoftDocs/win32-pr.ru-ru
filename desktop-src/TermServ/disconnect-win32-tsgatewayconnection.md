---
title: Метод Disconnect класса Win32_TSGatewayConnection
description: Отключает подключение от сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).
ms.assetid: 8c424e58-aa89-4ec6-acea-5b571d3f4c21
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода отключения
- Метод Disconnect службы удаленных рабочих столов, Win32_TSGatewayConnection класс
- Win32_TSGatewayConnection службы удаленных рабочих столов класса, метод Disconnect
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.Disconnect
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53101e5ca3529c5033adc918f1f9ad11a3b45f7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801174"
---
# <a name="disconnect-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="91c1b-106">Метод Disconnect \_ класса Win32 тсгатевайконнектион</span><span class="sxs-lookup"><span data-stu-id="91c1b-106">Disconnect method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="91c1b-107">Отключает подключение от сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="91c1b-107">Disconnects the connection from the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="91c1b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91c1b-108">Syntax</span></span>


```mof
uint32 Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="91c1b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="91c1b-109">Parameters</span></span>

<span data-ttu-id="91c1b-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="91c1b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91c1b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91c1b-111">Return value</span></span>

<span data-ttu-id="91c1b-112">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="91c1b-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="91c1b-113">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="91c1b-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="91c1b-114">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="91c1b-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="91c1b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91c1b-115">Remarks</span></span>

<span data-ttu-id="91c1b-116">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="91c1b-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="91c1b-117">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="91c1b-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="91c1b-118">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="91c1b-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="91c1b-119">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="91c1b-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="91c1b-120">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="91c1b-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="91c1b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="91c1b-121">Requirements</span></span>



| <span data-ttu-id="91c1b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="91c1b-122">Requirement</span></span> | <span data-ttu-id="91c1b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="91c1b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="91c1b-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91c1b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="91c1b-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="91c1b-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="91c1b-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91c1b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="91c1b-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91c1b-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="91c1b-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="91c1b-128">Namespace</span></span><br/>                | <span data-ttu-id="91c1b-129">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="91c1b-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="91c1b-130">MOF</span><span class="sxs-lookup"><span data-stu-id="91c1b-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91c1b-131"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="91c1b-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="91c1b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="91c1b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91c1b-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91c1b-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="91c1b-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91c1b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c1b-135">**\_Тсгатевайконнектион Win32**</span><span class="sxs-lookup"><span data-stu-id="91c1b-135">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

