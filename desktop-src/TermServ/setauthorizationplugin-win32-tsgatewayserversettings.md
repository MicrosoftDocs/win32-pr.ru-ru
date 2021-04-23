---
title: Метод Сетаусоризатионплугин класса Win32_TSGatewayServerSettings
description: Задает текущий подключаемый модуль авторизации для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).
ms.assetid: 236c9cca-4efc-433a-8f1f-e3044e0588b3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетаусоризатионплугин
- Службы удаленных рабочих столов метода Сетаусоризатионплугин, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Сетаусоризатионплугин
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthorizationPlugin
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cdb3cb07a7c0a30e84245a2d22e383dea168247
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534559"
---
# <a name="setauthorizationplugin-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="54730-106">Метод Сетаусоризатионплугин \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="54730-106">SetAuthorizationPlugin method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="54730-107">Задает текущий подключаемый модуль авторизации для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="54730-107">Sets the current authorization plug-in for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="54730-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54730-108">Syntax</span></span>


```mof
uint32 SetAuthorizationPlugin(
  [in] string PluginName
);
```



## <a name="parameters"></a><span data-ttu-id="54730-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="54730-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54730-110">*PluginName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54730-110">*PluginName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54730-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="54730-111">Type: **string**</span></span>

<span data-ttu-id="54730-112">Имя нового текущего подключаемого модуля авторизации.</span><span class="sxs-lookup"><span data-stu-id="54730-112">The name of the new current authorization plug-in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54730-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54730-113">Return value</span></span>

<span data-ttu-id="54730-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="54730-114">Type: **uint32**</span></span>

<span data-ttu-id="54730-115">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="54730-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="54730-116">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="54730-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="54730-117">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="54730-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="54730-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54730-118">Remarks</span></span>

<span data-ttu-id="54730-119">Чтобы разрешить работу подключаемого модуля авторизации, необходимо вызвать метод [**рециклерпкаппликатионпулс**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="54730-119">You must call the [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) method to allow the authorization plug-in to work.</span></span>

<span data-ttu-id="54730-120">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="54730-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="54730-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="54730-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="54730-122">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="54730-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="54730-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="54730-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="54730-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="54730-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="54730-125">Требования</span><span class="sxs-lookup"><span data-stu-id="54730-125">Requirements</span></span>



| <span data-ttu-id="54730-126">Требование</span><span class="sxs-lookup"><span data-stu-id="54730-126">Requirement</span></span> | <span data-ttu-id="54730-127">Значение</span><span class="sxs-lookup"><span data-stu-id="54730-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="54730-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54730-128">Minimum supported client</span></span><br/> | <span data-ttu-id="54730-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="54730-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="54730-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54730-130">Minimum supported server</span></span><br/> | <span data-ttu-id="54730-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="54730-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="54730-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="54730-132">Namespace</span></span><br/>                | <span data-ttu-id="54730-133">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="54730-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="54730-134">MOF</span><span class="sxs-lookup"><span data-stu-id="54730-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54730-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54730-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="54730-136">DLL</span><span class="sxs-lookup"><span data-stu-id="54730-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54730-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54730-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="54730-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54730-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54730-139">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="54730-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="54730-140">**рециклерпкаппликатионпулс**</span><span class="sxs-lookup"><span data-stu-id="54730-140">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

