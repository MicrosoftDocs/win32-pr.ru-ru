---
title: Метод Рециклерпкаппликатионпулс класса Win32_TSGatewayServerSettings
description: Повторное использование пулов приложений RPC в службах IIS.
ms.assetid: c7b1b797-7792-4d97-97f4-bea3b2f2495b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Рециклерпкаппликатионпулс
- Службы удаленных рабочих столов метода Рециклерпкаппликатионпулс, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Рециклерпкаппликатионпулс
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.RecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1963b8dec826c72a8a5128abdfa01d4a1e841a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490317"
---
# <a name="recyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="7331a-106">Метод Рециклерпкаппликатионпулс \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="7331a-106">RecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="7331a-107">Повторное использование пулов приложений RPC в службах IIS.</span><span class="sxs-lookup"><span data-stu-id="7331a-107">Recycles the RPC application pools in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="7331a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7331a-108">Syntax</span></span>


```mof
uint32 RecycleRpcApplicationPools();
```



## <a name="parameters"></a><span data-ttu-id="7331a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7331a-109">Parameters</span></span>

<span data-ttu-id="7331a-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7331a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7331a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7331a-111">Return value</span></span>

<span data-ttu-id="7331a-112">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7331a-112">Type: **uint32**</span></span>

<span data-ttu-id="7331a-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="7331a-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7331a-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="7331a-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7331a-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7331a-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7331a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7331a-116">Remarks</span></span>

<span data-ttu-id="7331a-117">Вызов этого метода приводит к отключению всех существующих подключений.</span><span class="sxs-lookup"><span data-stu-id="7331a-117">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="7331a-118">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="7331a-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="7331a-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="7331a-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7331a-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="7331a-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7331a-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="7331a-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7331a-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7331a-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7331a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7331a-123">Requirements</span></span>



| <span data-ttu-id="7331a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7331a-124">Requirement</span></span> | <span data-ttu-id="7331a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7331a-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7331a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7331a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7331a-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7331a-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7331a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7331a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7331a-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7331a-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="7331a-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7331a-130">Namespace</span></span><br/>                | <span data-ttu-id="7331a-131">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="7331a-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="7331a-132">MOF</span><span class="sxs-lookup"><span data-stu-id="7331a-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7331a-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7331a-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="7331a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7331a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7331a-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7331a-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="7331a-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7331a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7331a-137">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="7331a-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="7331a-138">**сетаусентикатионплугин**</span><span class="sxs-lookup"><span data-stu-id="7331a-138">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)
</dt> </dl>

 

