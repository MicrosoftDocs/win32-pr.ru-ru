---
title: Метод Сетаусентикатионплугин класса Win32_TSGatewayServerSettings
description: Задает текущий подключаемый модуль аутентификации для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).
ms.assetid: b79a5e7c-bf55-48f6-a6c0-5338e7eee2a1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетаусентикатионплугин
- Службы удаленных рабочих столов метода Сетаусентикатионплугин, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Сетаусентикатионплугин
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthenticationPlugin
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b5b332dd288a01f96b0eb0b3a99e7e45269cdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803778"
---
# <a name="setauthenticationplugin-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="1c793-106">Метод Сетаусентикатионплугин \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="1c793-106">SetAuthenticationPlugin method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="1c793-107">Задает текущий подключаемый модуль аутентификации для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="1c793-107">Sets the current authentication plug-in for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c793-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c793-108">Syntax</span></span>


```mof
uint32 SetAuthenticationPlugin(
  [in] string PluginName
);
```



## <a name="parameters"></a><span data-ttu-id="1c793-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c793-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c793-110">*PluginName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c793-110">*PluginName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c793-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="1c793-111">Type: **string**</span></span>

<span data-ttu-id="1c793-112">Имя нового подключаемого модуля текущей проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="1c793-112">The name of the new current authentication plug-in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c793-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c793-113">Return value</span></span>

<span data-ttu-id="1c793-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c793-114">Type: **uint32**</span></span>

<span data-ttu-id="1c793-115">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="1c793-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1c793-116">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="1c793-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1c793-117">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1c793-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1c793-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c793-118">Remarks</span></span>

<span data-ttu-id="1c793-119">Чтобы обеспечить работу подключаемого модуля проверки подлинности, необходимо вызвать метод [**рециклерпкаппликатионпулс**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="1c793-119">You must call the [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) method to allow the authentication plug-in to work.</span></span>

<span data-ttu-id="1c793-120">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="1c793-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1c793-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="1c793-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1c793-122">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="1c793-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1c793-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="1c793-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1c793-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1c793-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c793-125">Требования</span><span class="sxs-lookup"><span data-stu-id="1c793-125">Requirements</span></span>



| <span data-ttu-id="1c793-126">Требование</span><span class="sxs-lookup"><span data-stu-id="1c793-126">Requirement</span></span> | <span data-ttu-id="1c793-127">Значение</span><span class="sxs-lookup"><span data-stu-id="1c793-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c793-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c793-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1c793-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1c793-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1c793-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c793-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1c793-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1c793-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="1c793-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1c793-132">Namespace</span></span><br/>                | <span data-ttu-id="1c793-133">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="1c793-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1c793-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1c793-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c793-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c793-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c793-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1c793-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c793-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c793-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1c793-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c793-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c793-139">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="1c793-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="1c793-140">**рециклерпкаппликатионпулс**</span><span class="sxs-lookup"><span data-stu-id="1c793-140">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

