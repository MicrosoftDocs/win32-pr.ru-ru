---
title: Метод Енумаусоризатионплугинс класса Win32_TSGatewayServerSettings
description: Перечисляет все зарегистрированные подключаемые модули авторизации.
ms.assetid: 525b4001-b89c-43cc-986a-00db47dd5518
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Енумаусоризатионплугинс
- Службы удаленных рабочих столов метода Енумаусоризатионплугинс, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Енумаусоризатионплугинс
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnumAuthorizationPlugins
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d955c08f5e4f91547751b0f177681ad2abd57c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892730"
---
# <a name="enumauthorizationplugins-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="e99cf-106">Метод Енумаусоризатионплугинс \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="e99cf-106">EnumAuthorizationPlugins method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="e99cf-107">Перечисляет все зарегистрированные подключаемые модули авторизации.</span><span class="sxs-lookup"><span data-stu-id="e99cf-107">Enumerates all registered authorization plug-ins.</span></span>

## <a name="syntax"></a><span data-ttu-id="e99cf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e99cf-108">Syntax</span></span>


```mof
uint32 EnumAuthorizationPlugins(
  [out] string PluginNames[],
  [out] string CLSIDs[],
  [out] string Descriptions[]
);
```



## <a name="parameters"></a><span data-ttu-id="e99cf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e99cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e99cf-110">*Плугиннамес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e99cf-110">*PluginNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e99cf-111">Тип: **строка \[ \]**</span><span class="sxs-lookup"><span data-stu-id="e99cf-111">Type: **string\[\]**</span></span>

<span data-ttu-id="e99cf-112">Массив **строк** , который получает имена зарегистрированных подключаемых модулей авторизации.</span><span class="sxs-lookup"><span data-stu-id="e99cf-112">A **string** array that receives the names of the registered authorization plug-ins.</span></span>

</dd> <dt>

<span data-ttu-id="e99cf-113">*Идентификаторы CLSID* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e99cf-113">*CLSIDs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e99cf-114">Тип: **строка \[ \]**</span><span class="sxs-lookup"><span data-stu-id="e99cf-114">Type: **string\[\]**</span></span>

<span data-ttu-id="e99cf-115">Массив **строк** , который получает идентификаторы CLSID зарегистрированных подключаемых модулей авторизации.</span><span class="sxs-lookup"><span data-stu-id="e99cf-115">A **string** array that receives the CLSIDs of the registered authorization plug-ins.</span></span>

</dd> <dt>

<span data-ttu-id="e99cf-116">*Описание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e99cf-116">*Descriptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e99cf-117">Тип: **строка \[ \]**</span><span class="sxs-lookup"><span data-stu-id="e99cf-117">Type: **string\[\]**</span></span>

<span data-ttu-id="e99cf-118">Массив **строк** , который получает описания зарегистрированных подключаемых модулей авторизации.</span><span class="sxs-lookup"><span data-stu-id="e99cf-118">A **string** array that receives the descriptions of the registered authorization plug-ins.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e99cf-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e99cf-119">Return value</span></span>

<span data-ttu-id="e99cf-120">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e99cf-120">Type: **uint32**</span></span>

<span data-ttu-id="e99cf-121">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="e99cf-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e99cf-122">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="e99cf-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e99cf-123">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e99cf-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e99cf-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e99cf-124">Remarks</span></span>

<span data-ttu-id="e99cf-125">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="e99cf-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e99cf-126">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="e99cf-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e99cf-127">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="e99cf-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e99cf-128">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="e99cf-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e99cf-129">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e99cf-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e99cf-130">Требования</span><span class="sxs-lookup"><span data-stu-id="e99cf-130">Requirements</span></span>



| <span data-ttu-id="e99cf-131">Требование</span><span class="sxs-lookup"><span data-stu-id="e99cf-131">Requirement</span></span> | <span data-ttu-id="e99cf-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e99cf-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e99cf-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e99cf-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e99cf-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e99cf-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e99cf-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e99cf-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e99cf-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e99cf-136">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="e99cf-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e99cf-137">Namespace</span></span><br/>                | <span data-ttu-id="e99cf-138">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="e99cf-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e99cf-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e99cf-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e99cf-140"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e99cf-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e99cf-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e99cf-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e99cf-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e99cf-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e99cf-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e99cf-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e99cf-144">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="e99cf-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

