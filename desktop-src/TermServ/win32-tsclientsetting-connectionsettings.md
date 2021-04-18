---
title: Метод ConnectionSettings класса Win32_TSClientSetting
description: Метод ConnectionSettings задает параметры сеанса, которые применяются к процессу подключения и входа.
ms.assetid: 603807fe-f341-4358-a3b0-0300785cbdb1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода ConnectionSettings
- Службы удаленных рабочих столов метода ConnectionSettings, класс Win32_TSClientSetting
- Класс Win32_TSClientSetting службы удаленных рабочих столов, метод ConnectionSettings
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.ConnectionSettings
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec255f00656684751b750e92d7a3df8290e3573e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534061"
---
# <a name="connectionsettings-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="9d72c-106">Метод ConnectionSettings \_ класса Win32 тсклиентсеттинг</span><span class="sxs-lookup"><span data-stu-id="9d72c-106">ConnectionSettings method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="9d72c-107">Метод **ConnectionSettings** задает параметры сеанса, которые применяются к процессу подключения и входа.</span><span class="sxs-lookup"><span data-stu-id="9d72c-107">The **ConnectionSettings** method sets the session settings that apply to the connection and logon process.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d72c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d72c-108">Syntax</span></span>


```mof
uint32 ConnectionSettings(
  [in] uint32 ConnectClientDrivesAtLogon,
  [in] uint32 ConnectPrinterAtLogon,
  [in] uint32 DefaultToClientPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="9d72c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d72c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d72c-110">*Коннектклиентдривесатлогон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d72c-110">*ConnectClientDrivesAtLogon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d72c-111">Флаг включения или отключения свойства **коннектклиентдривесатлогон** , которое указывает, будут ли диски клиента автоматически подключены во время процедуры входа в систему.</span><span class="sxs-lookup"><span data-stu-id="9d72c-111">Flag enabling or disabling the **ConnectClientDrivesAtLogon** property which specifies whether the client's drives are automatically connected during the logon procedure.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="9d72c-112"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="9d72c-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="9d72c-113">Диски клиента не подключаются автоматически.</span><span class="sxs-lookup"><span data-stu-id="9d72c-113">The client's drives are not automatically connected.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="9d72c-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="9d72c-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="9d72c-115">Диски клиента автоматически соединяются.</span><span class="sxs-lookup"><span data-stu-id="9d72c-115">The client's drives are automatically connected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9d72c-116">*Коннектпринтератлогон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d72c-116">*ConnectPrinterAtLogon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d72c-117">Флаг включения или отключения свойства **коннектпринтератлогон** , которое указывает, будут ли все сопоставленные локальные клиентские принтеры автоматически подключены во время процедуры входа в систему.</span><span class="sxs-lookup"><span data-stu-id="9d72c-117">Flag enabling or disabling the **ConnectPrinterAtLogon** property, which specifies whether all mapped local client printers are automatically connected during the logon procedure.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="9d72c-118"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="9d72c-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="9d72c-119">Все сопоставленные локальные принтеры не подключены автоматически.</span><span class="sxs-lookup"><span data-stu-id="9d72c-119">All mapped local printers are not automatically connected.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="9d72c-120"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="9d72c-120"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="9d72c-121">Все сопоставленные локальные принтеры автоматически соединяются.</span><span class="sxs-lookup"><span data-stu-id="9d72c-121">All mapped local printers are automatically connected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9d72c-122">*Дефаулттоклиентпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d72c-122">*DefaultToClientPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d72c-123">Флаг включения или отключения свойства **дефаулттоклиентпринтер** , которое указывает, будут ли задания печати автоматически отправляться на локальный принтер клиента.</span><span class="sxs-lookup"><span data-stu-id="9d72c-123">Flag enabling or disabling the **DefaultToClientPrinter** property which specifies whether print jobs are automatically sent to the client's local printer.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="9d72c-124"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="9d72c-124"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="9d72c-125">Задания печати не отправляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="9d72c-125">Print jobs are not automatically sent.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="9d72c-126"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="9d72c-126"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="9d72c-127">Задания печати автоматически отправляются.</span><span class="sxs-lookup"><span data-stu-id="9d72c-127">Print jobs are automatically sent.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d72c-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d72c-128">Return value</span></span>

<span data-ttu-id="9d72c-129">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="9d72c-129">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="9d72c-130">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="9d72c-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="9d72c-131">Метод возвращает ошибку, если параметры соединения пользователя переопределяются сервером.</span><span class="sxs-lookup"><span data-stu-id="9d72c-131">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d72c-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d72c-132">Remarks</span></span>

<span data-ttu-id="9d72c-133">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="9d72c-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9d72c-134">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="9d72c-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9d72c-135">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="9d72c-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9d72c-136">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9d72c-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d72c-137">Требования</span><span class="sxs-lookup"><span data-stu-id="9d72c-137">Requirements</span></span>



| <span data-ttu-id="9d72c-138">Требование</span><span class="sxs-lookup"><span data-stu-id="9d72c-138">Requirement</span></span> | <span data-ttu-id="9d72c-139">Значение</span><span class="sxs-lookup"><span data-stu-id="9d72c-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d72c-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d72c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9d72c-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d72c-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9d72c-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d72c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9d72c-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d72c-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9d72c-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9d72c-144">Namespace</span></span><br/>                | <span data-ttu-id="9d72c-145">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="9d72c-145">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9d72c-146">MOF</span><span class="sxs-lookup"><span data-stu-id="9d72c-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d72c-147"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d72c-147"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d72c-148">DLL</span><span class="sxs-lookup"><span data-stu-id="9d72c-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d72c-149"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d72c-149"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d72c-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d72c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d72c-151">**\_Тсклиентсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="9d72c-151">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

