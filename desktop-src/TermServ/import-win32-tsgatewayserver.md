---
title: Метод Import класса Win32_TSGatewayServer
description: Импортирует заданную конфигурацию на сервер шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: d849afb9-f6cb-41e6-aab5-e47b30a5581f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода импорта
- Службы удаленных рабочих столов метода импорта, класс Win32_TSGatewayServer
- Win32_TSGatewayServer службы удаленных рабочих столов класса, метод Import
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Import
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b35395342be7c13f2a96f73f914eda103e1ef4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988865"
---
# <a name="import-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="94305-106">Метод Import \_ класса Win32 тсгатевайсервер</span><span class="sxs-lookup"><span data-stu-id="94305-106">Import method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="94305-107">Импортирует заданную конфигурацию на сервер шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="94305-107">Imports a given configuration to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="94305-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94305-108">Syntax</span></span>


```mof
uint32 Import(
  [in]  uint32 ImportType,
  [in]  string XmlString,
  [in]  uint32 MergeOrReplace,
  [out] string LogString
);
```



## <a name="parameters"></a><span data-ttu-id="94305-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="94305-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94305-110">*ImportType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94305-110">*ImportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94305-111">Импортируемое содержимое.</span><span class="sxs-lookup"><span data-stu-id="94305-111">The content to import.</span></span> <span data-ttu-id="94305-112">Задайте тип импорта, задав соответствующие биты в параметре *ImportType* .</span><span class="sxs-lookup"><span data-stu-id="94305-112">Set the import type by setting the corresponding bits in the *ImportType* parameter.</span></span> <span data-ttu-id="94305-113">Можно задать несколько типов импорта.</span><span class="sxs-lookup"><span data-stu-id="94305-113">You can set multiple import types.</span></span> <span data-ttu-id="94305-114">Например, если установлен бит 0, то будут импортированы службы удаленных рабочих столов политики авторизации подключений (RD CAP).</span><span class="sxs-lookup"><span data-stu-id="94305-114">For example, if the 0 bit is set, Remote Desktop Services connection authorization policies (RD CAPs) will be imported.</span></span> <span data-ttu-id="94305-115">Если заданы значения 0 и 2-го бита, то будут импортированы политики авторизации подключений к RD и службы удаленных рабочих столов (RD RAP).</span><span class="sxs-lookup"><span data-stu-id="94305-115">If both the 0 and the 2nd bit is set, both RD CAPs and Remote Desktop Services resource authorization policies (RD RAPs) will be imported.</span></span>

<dt>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>

<span data-ttu-id="94305-116"><span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Импортировать все прописные** (1)</span><span class="sxs-lookup"><span data-stu-id="94305-116"><span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Import all CAPs** (1)</span></span>


</dt> <dd>

<span data-ttu-id="94305-117">Импорт всех политик авторизации подключений к удаленным рабочим столам.</span><span class="sxs-lookup"><span data-stu-id="94305-117">Import all RD CAPs.</span></span>

</dd> <dt>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>

<span data-ttu-id="94305-118"><span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Импорт всех серверов RADIUS** (2)</span><span class="sxs-lookup"><span data-stu-id="94305-118"><span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Import all Radius Servers** (2)</span></span>


</dt> <dd>

<span data-ttu-id="94305-119">Импортируйте список всех серверов сетевых политик (NPS).</span><span class="sxs-lookup"><span data-stu-id="94305-119">Import a list of all Network Policy Server (NPS) servers.</span></span>

</dd> <dt>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>

<span data-ttu-id="94305-120"><span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Импорт всех политик авторизации** подключений (4)</span><span class="sxs-lookup"><span data-stu-id="94305-120"><span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Import all RAPs** (4)</span></span>


</dt> <dd>

<span data-ttu-id="94305-121">Импорт всех политик авторизации подключений к удаленным рабочим столам.</span><span class="sxs-lookup"><span data-stu-id="94305-121">Import all RD RAPs.</span></span>

</dd> <dt>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>

<span data-ttu-id="94305-122"><span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Импорт всех RGs** (8)</span><span class="sxs-lookup"><span data-stu-id="94305-122"><span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Import all RGs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="94305-123">Импортируйте все группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94305-123">Import all resource groups.</span></span>

</dd> <dt>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>

<span data-ttu-id="94305-124"><span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Импорт всех серверов LoadBalancing** (16)</span><span class="sxs-lookup"><span data-stu-id="94305-124"><span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Import all LoadBalancing Servers** (16)</span></span>


</dt> <dd>

<span data-ttu-id="94305-125">Импортируйте список всех серверов балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="94305-125">Import a list of all load-balancing servers.</span></span>

</dd> <dt>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>

<span data-ttu-id="94305-126"><span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Импорт всех параметров сервера** (32)</span><span class="sxs-lookup"><span data-stu-id="94305-126"><span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Import all Server Settings** (32)</span></span>


</dt> <dd>

<span data-ttu-id="94305-127">Импортируйте все параметры сервера, относящиеся к шлюзу удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="94305-127">Import all RD Gateway-related server settings.</span></span>

</dd> <dt>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>

<span data-ttu-id="94305-128"><span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Импорт всех политик работоспособности** (64)</span><span class="sxs-lookup"><span data-stu-id="94305-128"><span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Import all Health Policies** (64)</span></span>


</dt> <dd>

<span data-ttu-id="94305-129">Импортируйте все политики работоспособности.</span><span class="sxs-lookup"><span data-stu-id="94305-129">Import all health policies.</span></span>

<span data-ttu-id="94305-130">\* \* Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 и Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="94305-130">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="94305-131">Это значение не поддерживается до Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="94305-131">This value is not supported before Windows Server 2016.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="94305-132">*Ксмлстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94305-132">*XmlString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94305-133">Конфигурация в виде XML-строки.</span><span class="sxs-lookup"><span data-stu-id="94305-133">The configuration as an XML string.</span></span>

</dd> <dt>

<span data-ttu-id="94305-134">*Мержеорреплаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94305-134">*MergeOrReplace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94305-135">Указывает, следует ли объединять или заменять данные при возникновении конфликта.</span><span class="sxs-lookup"><span data-stu-id="94305-135">Indicates whether to merge or replace data when a conflict occurs.</span></span>

> [!Note]  
> <span data-ttu-id="94305-136">Слияние еще не реализовано.</span><span class="sxs-lookup"><span data-stu-id="94305-136">Merge is not yet implemented.</span></span> <span data-ttu-id="94305-137">Поэтому значение этого параметра игнорируется.</span><span class="sxs-lookup"><span data-stu-id="94305-137">Therefore, this parameter value is ignored.</span></span>

 

</dd> <dt>

<span data-ttu-id="94305-138">*Логстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="94305-138">*LogString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94305-139">Сведения журнала, формируемые во время операции импорта.</span><span class="sxs-lookup"><span data-stu-id="94305-139">The log information that is generated during the import operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94305-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94305-140">Remarks</span></span>

<span data-ttu-id="94305-141">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="94305-141">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="94305-142">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="94305-142">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="94305-143">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="94305-143">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="94305-144">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="94305-144">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="94305-145">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="94305-145">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="94305-146">Требования</span><span class="sxs-lookup"><span data-stu-id="94305-146">Requirements</span></span>



| <span data-ttu-id="94305-147">Требование</span><span class="sxs-lookup"><span data-stu-id="94305-147">Requirement</span></span> | <span data-ttu-id="94305-148">Значение</span><span class="sxs-lookup"><span data-stu-id="94305-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="94305-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94305-149">Minimum supported client</span></span><br/> | <span data-ttu-id="94305-150">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="94305-150">None supported</span></span><br/>                                                                |
| <span data-ttu-id="94305-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94305-151">Minimum supported server</span></span><br/> | <span data-ttu-id="94305-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94305-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="94305-153">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="94305-153">Namespace</span></span><br/>                | <span data-ttu-id="94305-154">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="94305-154">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="94305-155">MOF</span><span class="sxs-lookup"><span data-stu-id="94305-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94305-156"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94305-156"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="94305-157">DLL</span><span class="sxs-lookup"><span data-stu-id="94305-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94305-158"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94305-158"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="94305-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94305-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94305-160">**\_Тсгатевайсервер Win32**</span><span class="sxs-lookup"><span data-stu-id="94305-160">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

