---
title: Метод Export класса Win32_TSGatewayServer
description: Возвращает конфигурацию сервера шлюза удаленный рабочий стол (шлюз удаленных рабочих столов) в виде XML-строки.
ms.assetid: abf3a616-2b86-4cfe-934f-f1f17ce3ce31
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода экспорта
- Службы удаленных рабочих столов метода экспорта, класс Win32_TSGatewayServer
- Win32_TSGatewayServer службы удаленных рабочих столов класса, метод Export
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Export
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429e27cb93c319e977d37926ac43488008d62714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989417"
---
# <a name="export-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="52e6f-106">Метод Export \_ класса Win32 тсгатевайсервер</span><span class="sxs-lookup"><span data-stu-id="52e6f-106">Export method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="52e6f-107">Возвращает конфигурацию сервера шлюза удаленный рабочий стол (шлюз удаленных рабочих столов) в виде XML-строки.</span><span class="sxs-lookup"><span data-stu-id="52e6f-107">Returns the Remote Desktop Gateway (RD Gateway) server configuration as an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="52e6f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52e6f-108">Syntax</span></span>


```mof
uint32 Export(
  [in]  uint32 ExportType,
  [out] string XmlString
);
```



## <a name="parameters"></a><span data-ttu-id="52e6f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="52e6f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52e6f-110">*ExportType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="52e6f-110">*ExportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52e6f-111">Содержимое для экспорта.</span><span class="sxs-lookup"><span data-stu-id="52e6f-111">The content to export.</span></span> <span data-ttu-id="52e6f-112">Задайте тип экспорта, задав соответствующие биты в параметре *ExportType* .</span><span class="sxs-lookup"><span data-stu-id="52e6f-112">Set the export type by setting the corresponding bits in the *ExportType* parameter.</span></span> <span data-ttu-id="52e6f-113">Можно задать несколько типов экспорта.</span><span class="sxs-lookup"><span data-stu-id="52e6f-113">You can set multiple export types.</span></span> <span data-ttu-id="52e6f-114">Например, если установлен бит 0, то будут экспортированы службы удаленных рабочих столов политики авторизации подключений (RD CAP).</span><span class="sxs-lookup"><span data-stu-id="52e6f-114">For example, if the 0 bit is set, Remote Desktop Services connection authorization policies (RD CAPs) will be exported.</span></span> <span data-ttu-id="52e6f-115">Если заданы значения 0 и 2-го бита, то будут экспортированы политики авторизации подключений к УДАЛЕНным и службы удаленных рабочих столов ресурсам (RD RAP).</span><span class="sxs-lookup"><span data-stu-id="52e6f-115">If both the 0 and the 2nd bit is set, both RD CAPs and Remote Desktop Services resource authorization policies (RD RAPs) will be exported.</span></span>

<dt>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>

<span data-ttu-id="52e6f-116"><span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Экспортировать все прописные** (1)</span><span class="sxs-lookup"><span data-stu-id="52e6f-116"><span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Export all CAPs** (1)</span></span>


</dt> <dd>

<span data-ttu-id="52e6f-117">Экспорт всех политик авторизации подключений к удаленным рабочим столам.</span><span class="sxs-lookup"><span data-stu-id="52e6f-117">Export all RD CAPs.</span></span>

</dd> <dt>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>

<span data-ttu-id="52e6f-118"><span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Экспорт всех серверов RADIUS** (2)</span><span class="sxs-lookup"><span data-stu-id="52e6f-118"><span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Export all Radius Servers** (2)</span></span>


</dt> <dd>

<span data-ttu-id="52e6f-119">Экспорт списка всех серверов политики сети (NPS).</span><span class="sxs-lookup"><span data-stu-id="52e6f-119">Export a list of all Network Policy Server (NPS) servers.</span></span>

</dd> <dt>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>

<span data-ttu-id="52e6f-120"><span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Экспорт всех политик авторизации** подключений (4)</span><span class="sxs-lookup"><span data-stu-id="52e6f-120"><span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Export all RAPs** (4)</span></span>


</dt> <dd>

<span data-ttu-id="52e6f-121">Экспорт всех политик авторизации подключений к удаленным рабочим столам.</span><span class="sxs-lookup"><span data-stu-id="52e6f-121">Export all RD RAPs.</span></span>

</dd> <dt>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>

<span data-ttu-id="52e6f-122"><span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Экспорт всех RGs** (8)</span><span class="sxs-lookup"><span data-stu-id="52e6f-122"><span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Export all RGs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="52e6f-123">Экспортируйте все группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52e6f-123">Export all resource groups.</span></span>

</dd> <dt>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>

<span data-ttu-id="52e6f-124"><span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Экспортировать все серверы LoadBalancing** (16)</span><span class="sxs-lookup"><span data-stu-id="52e6f-124"><span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Export all LoadBalancing Servers** (16)</span></span>


</dt> <dd>

<span data-ttu-id="52e6f-125">Экспортируйте список всех серверов балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="52e6f-125">Export a list of all load-balancing servers.</span></span>

</dd> <dt>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>

<span data-ttu-id="52e6f-126"><span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Экспорт всех параметров сервера** (32)</span><span class="sxs-lookup"><span data-stu-id="52e6f-126"><span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Export all Server Settings** (32)</span></span>


</dt> <dd>

<span data-ttu-id="52e6f-127">Экспортируйте все параметры сервера, относящиеся к шлюзу удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="52e6f-127">Export all RD Gateway-related server settings.</span></span>

</dd> <dt>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>

<span data-ttu-id="52e6f-128"><span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Экспорт всех политик работоспособности** (64)</span><span class="sxs-lookup"><span data-stu-id="52e6f-128"><span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Export all Health Policies** (64)</span></span>


</dt> <dd>

<span data-ttu-id="52e6f-129">Экспортируйте все политики работоспособности.</span><span class="sxs-lookup"><span data-stu-id="52e6f-129">Export all health policies.</span></span>

<span data-ttu-id="52e6f-130">\* \* Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 и Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="52e6f-130">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="52e6f-131">Это значение не поддерживается до Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="52e6f-131">This value is not supported before Windows Server 2016.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="52e6f-132">*Ксмлстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="52e6f-132">*XmlString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52e6f-133">Строка XML-адреса.</span><span class="sxs-lookup"><span data-stu-id="52e6f-133">The XML string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52e6f-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52e6f-134">Remarks</span></span>

<span data-ttu-id="52e6f-135">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="52e6f-135">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="52e6f-136">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="52e6f-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="52e6f-137">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="52e6f-137">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="52e6f-138">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="52e6f-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="52e6f-139">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="52e6f-139">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="52e6f-140">Требования</span><span class="sxs-lookup"><span data-stu-id="52e6f-140">Requirements</span></span>



| <span data-ttu-id="52e6f-141">Требование</span><span class="sxs-lookup"><span data-stu-id="52e6f-141">Requirement</span></span> | <span data-ttu-id="52e6f-142">Значение</span><span class="sxs-lookup"><span data-stu-id="52e6f-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="52e6f-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52e6f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="52e6f-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="52e6f-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="52e6f-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52e6f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="52e6f-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52e6f-146">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="52e6f-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="52e6f-147">Namespace</span></span><br/>                | <span data-ttu-id="52e6f-148">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="52e6f-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="52e6f-149">MOF</span><span class="sxs-lookup"><span data-stu-id="52e6f-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52e6f-150"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52e6f-150"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="52e6f-151">DLL</span><span class="sxs-lookup"><span data-stu-id="52e6f-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52e6f-152"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52e6f-152"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="52e6f-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52e6f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52e6f-154">**\_Тсгатевайсервер Win32**</span><span class="sxs-lookup"><span data-stu-id="52e6f-154">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

