---
title: Метод Ремотеконтрол класса Win32_TSRemoteControlSetting
description: Метод Ремотеконтрол задает свойство Левелофконтрол.
ms.assetid: 341f4f8d-17be-4482-834a-b771e041cfec
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремотеконтрол
- Службы удаленных рабочих столов метода Ремотеконтрол, класс Win32_TSRemoteControlSetting
- Класс Win32_TSRemoteControlSetting службы удаленных рабочих столов, метод Ремотеконтрол
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting.RemoteControl
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476269c2f619b7ea46bc6546f106d7ccd2a486e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340630"
---
# <a name="remotecontrol-method-of-the-win32_tsremotecontrolsetting-class"></a><span data-ttu-id="39821-106">Метод Ремотеконтрол \_ класса Win32 тсремотеконтролсеттинг</span><span class="sxs-lookup"><span data-stu-id="39821-106">RemoteControl method of the Win32\_TSRemoteControlSetting class</span></span>

<span data-ttu-id="39821-107">Метод **ремотеконтрол** задает свойство **левелофконтрол** .</span><span class="sxs-lookup"><span data-stu-id="39821-107">The **RemoteControl** method sets the **LevelOfControl** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="39821-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39821-108">Syntax</span></span>


```mof
uint32 RemoteControl(
  [in] uint32 LevelOfControl
);
```



## <a name="parameters"></a><span data-ttu-id="39821-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="39821-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39821-110">*Левелофконтрол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39821-110">*LevelOfControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39821-111">Новое значение свойства **левелофконтрол** , которое указывает, будет ли сеанс просматриваться только удаленным пользователем или просматриваться и контролироваться с помощью клавиатуры и мыши.</span><span class="sxs-lookup"><span data-stu-id="39821-111">New value for the **LevelOfControl** property, which specifies whether the session will only be viewed by the remote user, or viewed and controlled through a keyboard and mouse.</span></span> <span data-ttu-id="39821-112">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="39821-112">For more information, see the Remarks section.</span></span> <span data-ttu-id="39821-113">Поддерживаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="39821-113">The following values are supported.</span></span>

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="39821-114"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Отключить** (0)</span><span class="sxs-lookup"><span data-stu-id="39821-114"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="39821-115">Удаленное управление отключено.</span><span class="sxs-lookup"><span data-stu-id="39821-115">Remote control is disabled.</span></span>

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span data-ttu-id="39821-116"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**Енаблеинпутнотифи** (1)</span><span class="sxs-lookup"><span data-stu-id="39821-116"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span></span>


</dt> <dd>

<span data-ttu-id="39821-117">Пользователь удаленного управления имеет полный контроль над сеансом пользователя с разрешением пользователя.</span><span class="sxs-lookup"><span data-stu-id="39821-117">The user of remote control has full control of the user's session, with the user's permission.</span></span>

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span data-ttu-id="39821-118"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**Енаблеинпутнонотифи** (2)</span><span class="sxs-lookup"><span data-stu-id="39821-118"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="39821-119">Пользователь удаленного управления имеет полный контроль над сеансом пользователя; разрешение пользователя не требуется.</span><span class="sxs-lookup"><span data-stu-id="39821-119">The user of remote control has full control of the user's session; the user's permission is not required.</span></span>

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span data-ttu-id="39821-120"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**Енабленоинпутнотифи** (3)</span><span class="sxs-lookup"><span data-stu-id="39821-120"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span></span>


</dt> <dd>

<span data-ttu-id="39821-121">Пользователь удаленного управления может просматривать сеанс удаленно с разрешением пользователя; удаленный пользователь не может активно управлять сеансом.</span><span class="sxs-lookup"><span data-stu-id="39821-121">The user of remote control can view the session remotely, with the user's permission; the remote user cannot actively control the session.</span></span>

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span data-ttu-id="39821-122"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**Енабленоинпутнонотифи** (4)</span><span class="sxs-lookup"><span data-stu-id="39821-122"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span></span>


</dt> <dd>

<span data-ttu-id="39821-123">Пользователь удаленного управления может просматривать сеанс удаленно, но не управляет им активно. разрешение пользователя не требуется.</span><span class="sxs-lookup"><span data-stu-id="39821-123">The user of remote control can view the session remotely, but not actively control the session; the user's permission is not required.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39821-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39821-124">Return value</span></span>

<span data-ttu-id="39821-125">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="39821-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="39821-126">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="39821-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="39821-127">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="39821-127">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="39821-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39821-128">Remarks</span></span>

<span data-ttu-id="39821-129">Полный контроль над сеансом означает, что удаленный пользователь может активно управлять сеансом пользователя с помощью клавиатуры и мыши.</span><span class="sxs-lookup"><span data-stu-id="39821-129">Full control of a session means that the remote user can actively control the user's session with a keyboard and mouse.</span></span>

<span data-ttu-id="39821-130">Когда пользователь пытается установить подключение удаленного управления, система отображает сообщение удаленному клиенту, запрашивая разрешение на просмотр или участие в активном сеансе.</span><span class="sxs-lookup"><span data-stu-id="39821-130">When a user attempts to establish a remote-control connection, the system displays a message to the remote client, requesting permission to either view or participate actively in the remote session.</span></span>

<span data-ttu-id="39821-131">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="39821-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="39821-132">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="39821-132">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="39821-133">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="39821-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="39821-134">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="39821-134">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="39821-135">Требования</span><span class="sxs-lookup"><span data-stu-id="39821-135">Requirements</span></span>



| <span data-ttu-id="39821-136">Требование</span><span class="sxs-lookup"><span data-stu-id="39821-136">Requirement</span></span> | <span data-ttu-id="39821-137">Значение</span><span class="sxs-lookup"><span data-stu-id="39821-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39821-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39821-138">Minimum supported client</span></span><br/> | <span data-ttu-id="39821-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39821-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39821-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39821-140">Minimum supported server</span></span><br/> | <span data-ttu-id="39821-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39821-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39821-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="39821-142">Namespace</span></span><br/>                | <span data-ttu-id="39821-143">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="39821-143">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="39821-144">MOF</span><span class="sxs-lookup"><span data-stu-id="39821-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39821-145"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39821-145"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="39821-146">DLL</span><span class="sxs-lookup"><span data-stu-id="39821-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39821-147"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39821-147"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39821-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39821-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39821-149">**\_Тсремотеконтролсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="39821-149">**Win32\_TSRemoteControlSetting**</span></span>](win32-tsremotecontrolsetting.md)
</dt> </dl>

 

