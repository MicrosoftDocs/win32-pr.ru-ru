---
title: Метод Сетдефаултплугинсандрециклерпкаппликатионпулс класса Win32_TSGatewayServerSettings
description: Задает текущие подключаемые модули проверки подлинности и авторизации для сервера шлюза удаленный рабочий стол (шлюзов удаленных рабочих столов) и перезапускает пулы приложений RPC в службах IIS.
ms.assetid: 1eac9e42-e533-4020-b2b6-571063f18c3c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетдефаултплугинсандрециклерпкаппликатионпулс
- Службы удаленных рабочих столов метода Сетдефаултплугинсандрециклерпкаппликатионпулс, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Сетдефаултплугинсандрециклерпкаппликатионпулс
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetDefaultPluginsAndRecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9ead29e987b68ec3f041010be5dde64d8a2b54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989244"
---
# <a name="setdefaultpluginsandrecyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="1eeb1-106">Метод Сетдефаултплугинсандрециклерпкаппликатионпулс \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="1eeb1-106">SetDefaultPluginsAndRecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="1eeb1-107">Задает текущие подключаемые модули проверки подлинности и авторизации для сервера шлюза удаленный рабочий стол (шлюзов удаленных рабочих столов) и перезапускает пулы приложений RPC в службах IIS.</span><span class="sxs-lookup"><span data-stu-id="1eeb1-107">Sets the current authentication and authorization plug-ins for the Remote Desktop Gateway (RD Gateway) server and recycles the RPC application pools in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eeb1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1eeb1-108">Syntax</span></span>


```mof
uint32 SetDefaultPluginsAndRecycleRpcApplicationPools();
```



## <a name="parameters"></a><span data-ttu-id="1eeb1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1eeb1-109">Parameters</span></span>

<span data-ttu-id="1eeb1-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1eeb1-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1eeb1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1eeb1-111">Return value</span></span>

<span data-ttu-id="1eeb1-112">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1eeb1-112">Type: **uint32**</span></span>

<span data-ttu-id="1eeb1-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="1eeb1-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1eeb1-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="1eeb1-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1eeb1-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1eeb1-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1eeb1-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1eeb1-116">Remarks</span></span>

<span data-ttu-id="1eeb1-117">Вызов этого метода приводит к отключению всех существующих подключений.</span><span class="sxs-lookup"><span data-stu-id="1eeb1-117">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="1eeb1-118">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="1eeb1-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1eeb1-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="1eeb1-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1eeb1-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="1eeb1-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1eeb1-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="1eeb1-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1eeb1-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1eeb1-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1eeb1-123">Требования</span><span class="sxs-lookup"><span data-stu-id="1eeb1-123">Requirements</span></span>



| <span data-ttu-id="1eeb1-124">Требование</span><span class="sxs-lookup"><span data-stu-id="1eeb1-124">Requirement</span></span> | <span data-ttu-id="1eeb1-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1eeb1-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eeb1-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1eeb1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1eeb1-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1eeb1-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1eeb1-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1eeb1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1eeb1-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1eeb1-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="1eeb1-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1eeb1-130">Namespace</span></span><br/>                | <span data-ttu-id="1eeb1-131">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="1eeb1-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1eeb1-132">MOF</span><span class="sxs-lookup"><span data-stu-id="1eeb1-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1eeb1-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1eeb1-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="1eeb1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1eeb1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1eeb1-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1eeb1-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1eeb1-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1eeb1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eeb1-137">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="1eeb1-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

