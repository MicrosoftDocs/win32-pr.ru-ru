---
title: Метод Сетаусентикатионплугинандрециклерпкаппликатионпулс класса Win32_TSGatewayServerSettings
description: Задает текущий подключаемый модуль проверки подлинности для сервера шлюза удаленный рабочий стол шлюза и перезапускает пулы приложений RPC в службах IIS.
ms.assetid: cdceaf50-3d0a-4af0-9ad5-fb43760fcf7b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетаусентикатионплугинандрециклерпкаппликатионпулс
- Службы удаленных рабочих столов метода Сетаусентикатионплугинандрециклерпкаппликатионпулс, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Сетаусентикатионплугинандрециклерпкаппликатионпулс
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthenticationPluginAndRecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b234e04c349d20ea178de12f050190b30193d444
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801690"
---
# <a name="setauthenticationpluginandrecyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="f4cdb-106">Метод Сетаусентикатионплугинандрециклерпкаппликатионпулс \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="f4cdb-106">SetAuthenticationPluginAndRecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="f4cdb-107">Задает текущий подключаемый модуль проверки подлинности для сервера шлюза удаленный рабочий стол шлюза и перезапускает пулы приложений RPC в службах IIS.</span><span class="sxs-lookup"><span data-stu-id="f4cdb-107">Sets the current authentication plug-in for the Remote Desktop Gateway (RD Gateway) server and recycles the RPC application pools in IIS.</span></span>

<span data-ttu-id="f4cdb-108">Этот метод эквивалентен вызову методов [**сетаусентикатионплугин**](setauthenticationplugin-win32-tsgatewayserversettings.md) и [**рециклерпкаппликатионпулс**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) последовательно.</span><span class="sxs-lookup"><span data-stu-id="f4cdb-108">This method is equivalent to calling the [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md) and [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) methods in sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4cdb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4cdb-109">Syntax</span></span>


```mof
uint32 SetAuthenticationPluginAndRecycleRpcApplicationPools(
  [in] string PluginName
);
```



## <a name="parameters"></a><span data-ttu-id="f4cdb-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4cdb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4cdb-111">*PluginName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f4cdb-111">*PluginName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4cdb-112">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4cdb-112">Type: **string**</span></span>

<span data-ttu-id="f4cdb-113">Имя подключаемого модуля проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="f4cdb-113">Name of the authentication plug-in</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4cdb-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4cdb-114">Return value</span></span>

<span data-ttu-id="f4cdb-115">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4cdb-115">Type: **uint32**</span></span>

<span data-ttu-id="f4cdb-116">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="f4cdb-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f4cdb-117">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f4cdb-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f4cdb-118">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f4cdb-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f4cdb-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4cdb-119">Remarks</span></span>

<span data-ttu-id="f4cdb-120">Вызов этого метода приводит к отключению всех существующих подключений.</span><span class="sxs-lookup"><span data-stu-id="f4cdb-120">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="f4cdb-121">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="f4cdb-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f4cdb-122">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="f4cdb-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f4cdb-123">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="f4cdb-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f4cdb-124">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="f4cdb-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f4cdb-125">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f4cdb-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4cdb-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f4cdb-126">Requirements</span></span>



| <span data-ttu-id="f4cdb-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f4cdb-127">Requirement</span></span> | <span data-ttu-id="f4cdb-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f4cdb-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4cdb-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f4cdb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f4cdb-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f4cdb-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f4cdb-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f4cdb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f4cdb-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f4cdb-132">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="f4cdb-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f4cdb-133">Namespace</span></span><br/>                | <span data-ttu-id="f4cdb-134">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="f4cdb-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f4cdb-135">MOF</span><span class="sxs-lookup"><span data-stu-id="f4cdb-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4cdb-136"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4cdb-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4cdb-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f4cdb-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4cdb-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4cdb-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f4cdb-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4cdb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4cdb-140">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="f4cdb-140">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="f4cdb-141">**сетаусентикатионплугин**</span><span class="sxs-lookup"><span data-stu-id="f4cdb-141">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="f4cdb-142">**рециклерпкаппликатионпулс**</span><span class="sxs-lookup"><span data-stu-id="f4cdb-142">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

