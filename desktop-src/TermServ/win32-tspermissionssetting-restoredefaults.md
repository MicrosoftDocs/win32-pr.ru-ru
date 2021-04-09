---
title: Метод Ресторедефаултс класса Win32_TSPermissionsSetting (Netfw. h)
description: Восстанавливает значения набора разрешений по умолчанию для терминала.
ms.assetid: bdd01290-7c7c-4355-85dc-ade51b2abd94
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ресторедефаултс
- Службы удаленных рабочих столов метода Ресторедефаултс, класс Win32_TSPermissionsSetting
- Класс Win32_TSPermissionsSetting службы удаленных рабочих столов, метод Ресторедефаултс
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.RestoreDefaults
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073a8f8267ab9e7f7cbd50f15f4f3f20594d2e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891741"
---
# <a name="restoredefaults-method-of-the-win32_tspermissionssetting-class"></a><span data-ttu-id="a3d74-106">Метод Ресторедефаултс \_ класса Win32 тспермиссионссеттинг</span><span class="sxs-lookup"><span data-stu-id="a3d74-106">RestoreDefaults method of the Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="a3d74-107">Метод **ресторедефаултс** восстанавливает значения набора разрешений по умолчанию для терминала.</span><span class="sxs-lookup"><span data-stu-id="a3d74-107">The **RestoreDefaults** method restores the default permission set values for the terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3d74-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3d74-108">Syntax</span></span>


```mof
uint32 RestoreDefaults();
```



## <a name="parameters"></a><span data-ttu-id="a3d74-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3d74-109">Parameters</span></span>

<span data-ttu-id="a3d74-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a3d74-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3d74-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3d74-111">Return value</span></span>

<span data-ttu-id="a3d74-112">Возвращает успешное выполнение, в противном случае — сбой.</span><span class="sxs-lookup"><span data-stu-id="a3d74-112">Returns Success on success, otherwise Failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3d74-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3d74-113">Remarks</span></span>

<span data-ttu-id="a3d74-114">Разрешения по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="a3d74-114">Default permissions are the following:</span></span>

-   <span data-ttu-id="a3d74-115">Учетные записи администратора, системы и удаленный рабочий стол помощника имеют все [разрешения службы удаленных рабочих столов](terminal-services-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="a3d74-115">The Administrators, System, and Remote Desktop Help Assistant accounts have all [Remote Desktop Services Permissions](terminal-services-permissions.md).</span></span>
-   <span data-ttu-id="a3d74-116">Учетная запись пользователя удаленный рабочий стол имеет разрешение Вход, подключение, запрос сведений и отправка сообщения.</span><span class="sxs-lookup"><span data-stu-id="a3d74-116">The Remote Desktop Users account has Logon, Connect, Query Information, and Send Message permission.</span></span>
-   <span data-ttu-id="a3d74-117">Учетные записи локальной службы и сетевой службы содержат сведения о запросах и разрешение отправлять сообщение.</span><span class="sxs-lookup"><span data-stu-id="a3d74-117">The Local Service and Network Service accounts have Query Information, and Send Message permission.</span></span>

<span data-ttu-id="a3d74-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="a3d74-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a3d74-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="a3d74-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a3d74-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="a3d74-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a3d74-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a3d74-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3d74-122">Требования</span><span class="sxs-lookup"><span data-stu-id="a3d74-122">Requirements</span></span>



| <span data-ttu-id="a3d74-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a3d74-123">Requirement</span></span> | <span data-ttu-id="a3d74-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a3d74-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3d74-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3d74-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a3d74-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3d74-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a3d74-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3d74-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a3d74-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3d74-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a3d74-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a3d74-129">Namespace</span></span><br/>                | <span data-ttu-id="a3d74-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="a3d74-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a3d74-131">Header</span><span class="sxs-lookup"><span data-stu-id="a3d74-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3d74-132"><dt>Netfw. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3d74-132"><dt>Netfw.h</dt></span></span> </dl>      |
| <span data-ttu-id="a3d74-133">MOF</span><span class="sxs-lookup"><span data-stu-id="a3d74-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3d74-134"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3d74-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3d74-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a3d74-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3d74-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3d74-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3d74-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3d74-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3d74-138">**\_Тспермиссионссеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="a3d74-138">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> </dl>

 

