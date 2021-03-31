---
title: Класс Win32_TSClientSetting
description: Определяет параметры конфигурации для \_ класса терминала Win32, связанного с политикой подключения.
ms.assetid: 438baf22-adc2-410e-bf9b-4b17a05c5ce4
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSClientSetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSClientSetting, описание
topic_type:
- apiref
api_name:
- Win32_TSClientSetting
- Win32_TSClientSetting.Caption
- Win32_TSClientSetting.Description
- Win32_TSClientSetting.InstallDate
- Win32_TSClientSetting.Name
- Win32_TSClientSetting.Status
- Win32_TSClientSetting.TerminalName
- Win32_TSClientSetting.ConnectionPolicy
- Win32_TSClientSetting.ConnectClientDrivesAtLogon
- Win32_TSClientSetting.ConnectPrinterAtLogon
- Win32_TSClientSetting.DefaultToClientPrinter
- Win32_TSClientSetting.PolicySourceDefaultToClientPrinter
- Win32_TSClientSetting.WindowsPrinterMapping
- Win32_TSClientSetting.PolicySourceWindowsPrinterMapping
- Win32_TSClientSetting.LPTPortMapping
- Win32_TSClientSetting.PolicySourceLPTPortMapping
- Win32_TSClientSetting.COMPortMapping
- Win32_TSClientSetting.PolicySourceCOMPortMapping
- Win32_TSClientSetting.DriveMapping
- Win32_TSClientSetting.PolicySourceDriveMapping
- Win32_TSClientSetting.AudioMapping
- Win32_TSClientSetting.PolicySourceAudioMapping
- Win32_TSClientSetting.ClipboardMapping
- Win32_TSClientSetting.PolicySourceClipboardMapping
- Win32_TSClientSetting.ColorDepthPolicy
- Win32_TSClientSetting.PolicySourceColorDepthPolicy
- Win32_TSClientSetting.ColorDepth
- Win32_TSClientSetting.PolicySourceColorDepth
- Win32_TSClientSetting.MaxMonitors
- Win32_TSClientSetting.MaxXResolution
- Win32_TSClientSetting.MaxYResolution
- Win32_TSClientSetting.PolicySourceMaxMonitors
- Win32_TSClientSetting.PolicySourceMaxResolution
- Win32_TSClientSetting.PNPRedirection
- Win32_TSClientSetting.PolicySourcePNPRedirection
- Win32_TSClientSetting.AudioCaptureRedir
- Win32_TSClientSetting.PolicySourceAudioCaptureRedir
- Win32_TSClientSetting.VideoPlaybackRedir
- Win32_TSClientSetting.PolicySourceVideoPlaybackRedir
- Win32_TSClientSetting.AllowDwm
- Win32_TSClientSetting.PolicySourceAllowDwm
- Win32_TSClientSetting.PolicyAdvancedRemoteAppGraphics
- Win32_TSClientSetting.AdvancedRemoteAppGraphics
- Win32_TSClientSetting.RemoteSessionProfile
- Win32_TSClientSetting.PolicySourceRemoteSessionProfile
- Win32_TSClientSetting.AVC444ModePreferred
- Win32_TSClientSetting.PolicySourceAvc444ModePreferred
- Win32_TSClientSetting.EncodeImageQuality
- Win32_TSClientSetting.PolicySourceEncodeImageQuality
- Win32_TSClientSetting.HardwareGraphicsAdapter
- Win32_TSClientSetting.PolicySourceHardwareGraphicsAdapter
- Win32_TSClientSetting.SelectTransport
- Win32_TSClientSetting.PolicySourceSelectTransport
- Win32_TSClientSetting.SelectNetworkDetect
- Win32_TSClientSetting.PolicySourceSelectNetworkDetect
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204f38570e1e023ca070ed1845e4574d9570b8ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137335"
---
# <a name="win32_tsclientsetting-class"></a><span data-ttu-id="ad2a3-105">\_Класс Win32 тсклиентсеттинг</span><span class="sxs-lookup"><span data-stu-id="ad2a3-105">Win32\_TSClientSetting class</span></span>

<span data-ttu-id="ad2a3-106">Класс **WMI \_ Тсклиентсеттинг для Win32** определяет параметры конфигурации для класса [**\_ терминала Win32**](win32-terminal.md) , связанного с политикой подключения.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-106">The **Win32\_TSClientSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to connection policy.</span></span>

<span data-ttu-id="ad2a3-107">Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="ad2a3-108">Справочные сведения о методах см. в таблице методов далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad2a3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad2a3-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSCLIENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSClientSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ConnectionPolicy;
  uint32   ConnectClientDrivesAtLogon;
  uint32   ConnectPrinterAtLogon;
  uint32   DefaultToClientPrinter;
  uint32   PolicySourceDefaultToClientPrinter;
  uint32   WindowsPrinterMapping;
  uint32   PolicySourceWindowsPrinterMapping;
  uint32   LPTPortMapping;
  uint32   PolicySourceLPTPortMapping;
  uint32   COMPortMapping;
  uint32   PolicySourceCOMPortMapping;
  uint32   DriveMapping;
  uint32   PolicySourceDriveMapping;
  uint32   AudioMapping;
  uint32   PolicySourceAudioMapping;
  uint32   ClipboardMapping;
  uint32   PolicySourceClipboardMapping;
  uint32   ColorDepthPolicy;
  uint32   PolicySourceColorDepthPolicy;
  uint32   ColorDepth;
  uint32   PolicySourceColorDepth;
  uint32   MaxMonitors;
  uint32   MaxXResolution;
  uint32   MaxYResolution;
  uint32   PolicySourceMaxMonitors;
  uint32   PolicySourceMaxResolution;
  uint32   PNPRedirection;
  uint32   PolicySourcePNPRedirection;
  uint32   AudioCaptureRedir;
  uint32   PolicySourceAudioCaptureRedir;
  uint32   VideoPlaybackRedir;
  uint32   PolicySourceVideoPlaybackRedir;
  uint32   AllowDwm;
  uint32   PolicySourceAllowDwm;
  uint32   PolicyAdvancedRemoteAppGraphics;
  uint32   AdvancedRemoteAppGraphics;
  uint32   RemoteSessionProfile;
  uint32   PolicySourceRemoteSessionProfile;
  uint32   AVC444ModePreferred;
  uint32   PolicySourceAvc444ModePreferred;
  uint32   EncodeImageQuality;
  uint32   PolicySourceEncodeImageQuality;
  uint32   HardwareGraphicsAdapter;
  uint32   PolicySourceHardwareGraphicsAdapter;
  uint32   SelectTransport;
  uint32   PolicySourceSelectTransport;
  uint32   SelectNetworkDetect;
  uint32   PolicySourceSelectNetworkDetect;
};
```

## <a name="members"></a><span data-ttu-id="ad2a3-110">Члены</span><span class="sxs-lookup"><span data-stu-id="ad2a3-110">Members</span></span>

<span data-ttu-id="ad2a3-111">Класс **Win32 \_ тсклиентсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ad2a3-111">The **Win32\_TSClientSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="ad2a3-112">Методы</span><span class="sxs-lookup"><span data-stu-id="ad2a3-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="ad2a3-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="ad2a3-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ad2a3-114">Методы</span><span class="sxs-lookup"><span data-stu-id="ad2a3-114">Methods</span></span>

<span data-ttu-id="ad2a3-115">Класс **Win32 \_ тсклиентсеттинг** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-115">The **Win32\_TSClientSetting** class has these methods.</span></span>



| <span data-ttu-id="ad2a3-116">Метод</span><span class="sxs-lookup"><span data-stu-id="ad2a3-116">Method</span></span>                                                                   | <span data-ttu-id="ad2a3-117">Описание</span><span class="sxs-lookup"><span data-stu-id="ad2a3-117">Description</span></span>                                                                                                                                                  |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad2a3-118">**ConnectionSettings**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-118">**ConnectionSettings**</span></span>](win32-tsclientsetting-connectionsettings.md)   | <span data-ttu-id="ad2a3-119">Задает свойства **коннектклиентдривесатлогон**, **коннектпринтератлогон** и **дефаулттоклиентпринтер** этого класса.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-119">Sets the **ConnectClientDrivesAtLogon**, **ConnectPrinterAtLogon**, and **DefaultToClientPrinter** properties of this class.</span></span><br/>                      |
| [<span data-ttu-id="ad2a3-120">**сеталловдвм**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-120">**SetAllowDwm**</span></span>](setallowdwm-win32-tsclientsetting.md)                 | <span data-ttu-id="ad2a3-121">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-121">Not supported.</span></span><br/> <span data-ttu-id="ad2a3-122">**Windows 7 и Windows Server 2008 R2:** Задает свойство **алловдвм** .</span><span class="sxs-lookup"><span data-stu-id="ad2a3-122">**Windows 7 and Windows Server 2008 R2:** Sets the **AllowDwm** property.</span></span><br/>                                               |
| [<span data-ttu-id="ad2a3-123">**сетклиентпроперти**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-123">**SetClientProperty**</span></span>](win32-tsclientsetting-setclientproperty.md)     | <span data-ttu-id="ad2a3-124">Задает свойство **лптпортмаппинг**, **компортмаппинг**, **аудиомаппинг**, **клипбоардмаппинг**, **дривемаппинг** или **виндовспринтермаппинг** .</span><span class="sxs-lookup"><span data-stu-id="ad2a3-124">Sets the **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping**, or **WindowsPrinterMapping** property.</span></span><br/> |
| [<span data-ttu-id="ad2a3-125">**сетколордепс**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-125">**SetColorDepth**</span></span>](win32-tsclientsetting-setcolordepth.md)             | <span data-ttu-id="ad2a3-126">Задает свойство **clientareawidth** .</span><span class="sxs-lookup"><span data-stu-id="ad2a3-126">Sets the **ColorDepth** property.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="ad2a3-127">**сетколордепсполици**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-127">**SetColorDepthPolicy**</span></span>](win32-tsclientsetting-setcolordepthpolicy.md) | <span data-ttu-id="ad2a3-128">Задает свойство **колордепсполици** .</span><span class="sxs-lookup"><span data-stu-id="ad2a3-128">Sets the **ColorDepthPolicy** property.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="ad2a3-129">**сетмаксмониторс**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-129">**SetMaxMonitors**</span></span>](setmaxmonitors-win32-tsclientsetting.md)           | <span data-ttu-id="ad2a3-130">Задает свойство **максмониторс** .</span><span class="sxs-lookup"><span data-stu-id="ad2a3-130">Sets the **MaxMonitors** property.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="ad2a3-131">**сетмаксксресолутион**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-131">**SetMaxXResolution**</span></span>](setmaxxresolution-win32-tsclientsetting.md)     | <span data-ttu-id="ad2a3-132">Задает свойство **максксресолутион** .</span><span class="sxs-lookup"><span data-stu-id="ad2a3-132">Sets the **MaxXResolution** property.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="ad2a3-133">**сетмаксиресолутион**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-133">**SetMaxYResolution**</span></span>](setmaxyresolution-win32-tsclientsetting.md)     | <span data-ttu-id="ad2a3-134">Задает свойство **максиресолутион** .</span><span class="sxs-lookup"><span data-stu-id="ad2a3-134">Sets the **MaxYResolution** property.</span></span><br/>                                                                                                             |



 

### <a name="properties"></a><span data-ttu-id="ad2a3-135">Свойства</span><span class="sxs-lookup"><span data-stu-id="ad2a3-135">Properties</span></span>

<span data-ttu-id="ad2a3-136">Класс **Win32 \_ тсклиентсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-136">The **Win32\_TSClientSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad2a3-137">**адванцедремотеаппграфикс**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-137">**AdvancedRemoteAppGraphics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-138">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ad2a3-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-140">Указывает, следует ли включить расширенную графику RemoteFX для RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-140">Specifies whether to enable advanced RemoteFX graphics for RemoteApp.</span></span>

<span data-ttu-id="ad2a3-141">**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство недоступно до Windows Server 2012 R2 и Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-141">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2012 R2 and Windows 8.1.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ad2a3-142"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-142"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-143">Дополнительные графические объекты отключены.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-143">Advanced graphics are disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ad2a3-144"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-144"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-145">Расширенная графика включена.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-145">Advanced graphics are enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-146">**алловдвм**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-146">**AllowDwm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-147">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-149">Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-149">This property is not available.</span></span>

<span data-ttu-id="ad2a3-150">\* \* Windows 7 и Windows Server 2008 R2: \* \*</span><span class="sxs-lookup"><span data-stu-id="ad2a3-150">\*\*Windows 7 and Windows Server 2008 R2:  \*\*</span></span>

<span data-ttu-id="ad2a3-151">Указывает, следует ли включить или отключить композицию удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-151">Specifies whether to enable or disable remote desktop composition.</span></span> <span data-ttu-id="ad2a3-152">Ноль отключит композицию удаленного рабочего стола, а ненулевое значение включит его.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-152">Zero will disable remote desktop composition and a nonzero value will enable it.</span></span>

<span data-ttu-id="ad2a3-153">Чтобы изменить это свойство, используйте метод [**сеталловдвм**](setallowdwm-win32-tsclientsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="ad2a3-153">Use the [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md) method to modify this property.</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-154">**аудиокаптурередир**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-154">**AudioCaptureRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-155">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-157">Указывает, разрешено ли перенаправление захвата звука.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-157">Specifies whether to allow audio capture redirection.</span></span>

<span data-ttu-id="ad2a3-158">**Windows Server 2008 и Windows Vista:** Это свойство недоступно до Windows Server 2008 R2 и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-158">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ad2a3-159">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-159">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ad2a3-160">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-160">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-161">**аудиомаппинг**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-161">**AudioMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-162">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-164">Указывает, включено или отключено сопоставление звука.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-164">Specifies whether audio mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ad2a3-165"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-165"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-166">Сопоставление звука включено.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-166">Audio mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ad2a3-167"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-167"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-168">Сопоставление звука отключено.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-168">Audio mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-169">**AVC444ModePreferred**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-169">**AVC444ModePreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-170">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-171">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ad2a3-171">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-172">Указывает, является ли режим AVC444 предпочтительным.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-172">Specifies whether AVC444 mode is preferred.</span></span>

<span data-ttu-id="ad2a3-173">**Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** Это свойство недоступно до Windows 10 или Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-173">**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 10 or Windows Server 2016.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ad2a3-174">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-174">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ad2a3-175">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-175">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-176">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-179">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-180">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-180">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="ad2a3-181">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ad2a3-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-182">**клипбоардмаппинг**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-182">**ClipboardMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-183">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-185">Указывает, отключено или включено сопоставление буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-185">Specifies whether clipboard mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ad2a3-186"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-186"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-187">Сопоставление буфера обмена включено.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-187">Clipboard mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ad2a3-188"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-188"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-189">Сопоставление буфера обмена отключено.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-189">Clipboard mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-190">**Clientareawidth**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-190">**ColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-191">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-193">Задает глубину цвета.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-193">Specifies the color depth.</span></span> <span data-ttu-id="ad2a3-194">Возможные значения см. в описании метода [**сетколордепс**](win32-tsclientsetting-setcolordepth.md) .</span><span class="sxs-lookup"><span data-stu-id="ad2a3-194">For possible values, see the [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md) method.</span></span>

<dt>

<span id="8_bit"></span><span id="8_BIT"></span>

<span data-ttu-id="ad2a3-195"><span id="8_bit"></span><span id="8_BIT"></span>**8 бит** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-195"><span id="8_bit"></span><span id="8_BIT"></span>**8 bit** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="15_bit"></span><span id="15_BIT"></span>

<span data-ttu-id="ad2a3-196"><span id="15_bit"></span><span id="15_BIT"></span>**15 бит** (2)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-196"><span id="15_bit"></span><span id="15_BIT"></span>**15 bit** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="16_bit"></span><span id="16_BIT"></span>

<span data-ttu-id="ad2a3-197"><span id="16_bit"></span><span id="16_BIT"></span>**16-разрядная** (3)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-197"><span id="16_bit"></span><span id="16_BIT"></span>**16 bit** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="24_bit"></span><span id="24_BIT"></span>

<span data-ttu-id="ad2a3-198"><span id="24_bit"></span><span id="24_BIT"></span>**24 бита** (4)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-198"><span id="24_bit"></span><span id="24_BIT"></span>**24 bit** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="32_bit"></span><span id="32_BIT"></span>

<span data-ttu-id="ad2a3-199"><span id="32_bit"></span><span id="32_BIT"></span>**32 бит** (5)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-199"><span id="32_bit"></span><span id="32_BIT"></span>**32 bit** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-200">**колордепсполици**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-200">**ColorDepthPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-201">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-203">Указывает, следует ли переопределить параметр максимального цвета пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-203">Specifies whether to override the user's maximum color setting.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ad2a3-204"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-204"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-205">Не переопределяйте политику пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-205">Do not override the user's policy.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ad2a3-206"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-206"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-207">Переопределите политику пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-207">Override the user's policy.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-208">**компортмаппинг**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-208">**COMPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-209">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-211">Указывает, включено или отключено сопоставление COM-портов.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-211">Specifies whether COM port mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ad2a3-212"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-212"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-213">Сопоставление COM-портов включено.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-213">COM port mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ad2a3-214"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-214"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-215">Сопоставление COM-портов отключено.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-215">COM port mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-216">**коннектклиентдривесатлогон**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-216">**ConnectClientDrivesAtLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-217">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-219">Указывает, будут ли диски клиента автоматически подключены в процессе входа в систему.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-219">Specifies whether the client's drives will be automatically connected during the logon process.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ad2a3-220"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-220"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-221">Диски не будут автоматически подключены.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-221">Drives will not be automatically connected.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ad2a3-222"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-222"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-223">Диски будут автоматически подключены.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-223">Drives will be automatically connected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-224">**ConnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-224">**ConnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-225">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-226">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ad2a3-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-227">Политика, используемая сервером для получения параметров подключения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-227">The policy the server uses to retrieve the user connection settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="ad2a3-228"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**На пользователя** (0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-228"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-229">Параметры подключения пользователя вступают в действие.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-229">The user's connection settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="ad2a3-230"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Переопределение сервера** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-230"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-231">Параметры подключения пользователя переопределяются сервером.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-231">The user's connection settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-232">**коннектпринтератлогон**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-232">**ConnectPrinterAtLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-233">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-235">Указывает, будут ли все сопоставленные локальные принтеры клиента автоматически подключаться в процессе входа в систему.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-235">Specifies whether all mapped local printers of the client will be automatically connected during the logon process.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ad2a3-236"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-236"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-237">Локальные принтеры не будут автоматически подключены.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-237">Local printers will not be automatically connected.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ad2a3-238"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-238"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-239">Локальные принтеры будут автоматически подключены.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-239">Local printers will be automatically connected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-240">**дефаулттоклиентпринтер**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-240">**DefaultToClientPrinter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-241">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-243">Указывает, будут ли автоматически отправляться задания печати на локальный принтер клиента.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-243">Specifies whether print jobs will be automatically sent to the client's local printer.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ad2a3-244"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-244"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-245">Задания печати не должны автоматически отправляться на локальный принтер клиента.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-245">Print jobs are not to be automatically sent to the client's local printer.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ad2a3-246"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-246"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-247">Задания печати должны автоматически отправляться на локальный принтер клиента.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-247">Print jobs are to be automatically sent to the client's local printer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-248">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-248">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-249">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-250">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-251">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-251">Description of the object.</span></span>

<span data-ttu-id="ad2a3-252">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ad2a3-252">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-253">**дривемаппинг**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-253">**DriveMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-254">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-254">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-255">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-256">Указывает, включено или отключено сопоставление дисков.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-256">Specifies whether drive mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ad2a3-257"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-257"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-258">Сопоставление дисков включено.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-258">Drive mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ad2a3-259"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-259"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-260">Сопоставление дисков отключено.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-260">Drive mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-261">**енкодеимажекуалити**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-261">**EncodeImageQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-262">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-263">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ad2a3-263">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-264">Указывает качество образа для взаимодействия с RDP.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-264">Specifies the image quality for RDP experience.</span></span>

<span data-ttu-id="ad2a3-265">**Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** Это свойство недоступно до Windows 8 или Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-265">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="lossless"></span><span id="LOSSLESS"></span>

<span data-ttu-id="ad2a3-266">**без потерь** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-266">**lossless** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="ad2a3-267">**высокий** (2)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-267">**high** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="ad2a3-268">**средний** (3)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-268">**medium** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-269">**хардвареграфиксадаптер**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-269">**HardwareGraphicsAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-270">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-271">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ad2a3-271">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-272">Указывает, использует ли сервер узла сеансов удаленных рабочих столов аппаратный модуль визуализации графики в качестве адаптера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-272">Specifies whether the RD Session Host server uses the hardware graphics renderer as the default adapter.</span></span>

<span data-ttu-id="ad2a3-273">**Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** Это свойство недоступно до Windows 8 или Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-273">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ad2a3-274">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-274">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ad2a3-275">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-275">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-276">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-276">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-277">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-277">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-279">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="ad2a3-279">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-280">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-280">The date the object was installed.</span></span> <span data-ttu-id="ad2a3-281">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-281">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ad2a3-282">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ad2a3-282">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-283">**лптпортмаппинг**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-283">**LPTPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-284">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-284">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-286">Указывает, отключено или включено сопоставление LPT-портов.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-286">Specifies whether LPT port mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ad2a3-287"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-287"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-288">Сопоставление LPT-портов включено.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-288">LPT port mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ad2a3-289"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-289"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-290">Сопоставление LPT-портов отключено.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-290">LPT port mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-291">**максмониторс**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-291">**MaxMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-292">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-294">Максимальное число мониторов, поддерживаемое сервером.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-294">The maximum number of monitors supported by the server.</span></span> <span data-ttu-id="ad2a3-295">Чтобы изменить это свойство, используйте метод [**сетмаксмониторс**](setmaxmonitors-win32-tsclientsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="ad2a3-295">Use the [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="ad2a3-296">**Windows Server 2008 и Windows Vista:** Это свойство недоступно до Windows Server 2008 R2 и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-296">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-297">**максксресолутион**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-297">**MaxXResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-298">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-298">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-300">Максимальное разрешение по оси X, поддерживаемое сервером.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-300">The maximum X resolution supported by the server.</span></span> <span data-ttu-id="ad2a3-301">Чтобы изменить это свойство, используйте метод [**сетмаксксресолутион**](setmaxxresolution-win32-tsclientsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="ad2a3-301">Use the [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="ad2a3-302">**Windows Server 2008 и Windows Vista:** Это свойство недоступно до Windows Server 2008 R2 и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-302">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-303">**максиресолутион**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-303">**MaxYResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-304">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-304">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-306">Максимальное разрешение по оси Y, поддерживаемое сервером.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-306">The maximum Y resolution supported by the server.</span></span> <span data-ttu-id="ad2a3-307">Чтобы изменить это свойство, используйте метод [**сетмаксиресолутион**](setmaxyresolution-win32-tsclientsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="ad2a3-307">Use the [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="ad2a3-308">**Windows Server 2008 и Windows Vista:** Это свойство недоступно до Windows Server 2008 R2 и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-308">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-309">**Name**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-309">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-310">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-312">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-312">The name of the object.</span></span>

<span data-ttu-id="ad2a3-313">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ad2a3-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-314">**пнпредиректион**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-314">**PNPRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-315">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-317">Указывает, разрешено ли перенаправление самонастраивающийся.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-317">Specifies whether to allow Plug and Play redirection.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ad2a3-318"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-318"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-319">Разрешить перенаправление самонастраивающийся.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-319">Allow Plug and Play redirection.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ad2a3-320"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-320"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-321">Не разрешать перенаправление самонастраивающийся.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-321">Do not allow Plug and Play redirection.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-322">**полициадванцедремотеаппграфикс**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-322">**PolicyAdvancedRemoteAppGraphics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-323">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-323">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-325">Указывает, настроено ли свойство **адванцедремотеаппграфикс** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-325">Indicates whether the **AdvancedRemoteAppGraphics** property is configured by the server or group policy.</span></span>

<span data-ttu-id="ad2a3-326">**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство недоступно до Windows Server 2012 R2 и Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-326">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2012 R2 and Windows 8.1.</span></span>

<dt>

<span data-ttu-id="ad2a3-327">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-327">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-328">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-328">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-329">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-329">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-330">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-330">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-331">**полицисаурцеалловдвм**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-331">**PolicySourceAllowDwm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-332">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-332">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-334">Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-334">This property is not available.</span></span>

<span data-ttu-id="ad2a3-335">\* \* Windows 7 и Windows Server 2008 R2: \* \*</span><span class="sxs-lookup"><span data-stu-id="ad2a3-335">\*\*Windows 7 and Windows Server 2008 R2:  \*\*</span></span>

<span data-ttu-id="ad2a3-336">Указывает, настроено ли свойство **алловдвм** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-336">Indicates whether the **AllowDwm** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="ad2a3-337">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-337">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-338">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-338">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-339">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-339">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-340">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-340">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-341">**полицисаурцеаудиокаптурередир**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-341">**PolicySourceAudioCaptureRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-342">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-344">Указывает, настроено ли свойство **аудиокаптурередир** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-344">Indicates whether the **AudioCaptureRedir** property is configured by the server or group policy.</span></span>

<span data-ttu-id="ad2a3-345">**Windows Server 2008 и Windows Vista:** Это свойство недоступно до Windows Server 2008 R2 и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-345">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="ad2a3-346">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-346">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-347">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-347">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-348">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-348">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-349">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-349">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-350">**полицисаурцеаудиомаппинг**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-350">**PolicySourceAudioMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-351">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-351">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-352">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-353">Указывает, настроено ли свойство **аудиомаппинг** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-353">Indicates whether the **AudioMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="ad2a3-354">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-354">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-355">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-355">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-356">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-356">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-357">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-357">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-358">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-358">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-359">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad2a3-359">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-360">**PolicySourceAvc444ModePreferred**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-360">**PolicySourceAvc444ModePreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-361">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-363">Указывает, как настроено свойство **AVC444ModePreferredis** .</span><span class="sxs-lookup"><span data-stu-id="ad2a3-363">Indicates how the **AVC444ModePreferredis** property is configured.</span></span>

<span data-ttu-id="ad2a3-364">**Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** Это свойство недоступно до Windows 10 или Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-364">**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 10 or Windows Server 2016.</span></span>

<dt>

<span data-ttu-id="ad2a3-365">0</span><span class="sxs-lookup"><span data-stu-id="ad2a3-365">0</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-366">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-366">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-367">1</span><span class="sxs-lookup"><span data-stu-id="ad2a3-367">1</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-368">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-368">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-369">**полицисаурцеклипбоардмаппинг**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-369">**PolicySourceClipboardMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-370">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-372">Указывает, настроено ли свойство **клипбоардмаппинг** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-372">Indicates whether the **ClipboardMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="ad2a3-373">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-373">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-374">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-374">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-375">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-375">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-376">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-376">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-377">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-377">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-378">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad2a3-378">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-379">**полицисаурцеколордепс**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-379">**PolicySourceColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-380">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-381">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-382">Указывает, настроено ли свойство **clientareawidth** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-382">Indicates whether the **ColorDepth** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="ad2a3-383">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-383">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-384">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-384">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-385">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-385">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-386">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-386">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-387">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-387">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-388">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad2a3-388">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-389">**полицисаурцеколордепсполици**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-389">**PolicySourceColorDepthPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-390">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-390">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-391">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-392">Указывает, настроено ли свойство **колордепсполици** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-392">Indicates whether the **ColorDepthPolicy** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="ad2a3-393">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-393">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-394">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-394">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-395">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-395">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-396">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-396">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-397">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-397">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-398">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad2a3-398">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-399">**полицисаурцекомпортмаппинг**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-399">**PolicySourceCOMPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-400">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-400">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-401">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-402">Указывает, настроено ли свойство **компортмаппинг** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-402">Indicates whether the **COMPortMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="ad2a3-403">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-403">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-404">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-404">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-405">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-405">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-406">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-406">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-407">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-407">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-408">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad2a3-408">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-409">**полицисаурцедефаулттоклиентпринтер**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-409">**PolicySourceDefaultToClientPrinter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-410">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-411">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-412">Указывает, настроено ли свойство **дефаулттоклиентпринтер** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-412">Indicates whether the **DefaultToClientPrinter** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="ad2a3-413">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-413">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-414">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-414">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-415">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-415">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-416">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-416">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-417">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-417">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-418">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad2a3-418">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-419">**полицисаурцедривемаппинг**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-419">**PolicySourceDriveMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-420">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-420">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-422">Указывает, настроено ли свойство **дривемаппинг** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-422">Indicates whether the **DriveMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="ad2a3-423">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-423">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-424">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-424">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-425">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-425">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-426">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-426">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-427">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-427">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-428">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad2a3-428">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-429">**полицисаурцеенкодеимажекуалити**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-429">**PolicySourceEncodeImageQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-430">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-430">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-431">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-432">Указывает, как настраивается **енкодеимажекуалити** .</span><span class="sxs-lookup"><span data-stu-id="ad2a3-432">Indicates how the **EncodeImageQualityi** is configured.</span></span>

<span data-ttu-id="ad2a3-433">**Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** Это свойство недоступно до Windows 8 или Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-433">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="ad2a3-434">0</span><span class="sxs-lookup"><span data-stu-id="ad2a3-434">0</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-435">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-435">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-436">1</span><span class="sxs-lookup"><span data-stu-id="ad2a3-436">1</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-437">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-437">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-438">**полицисаурцехардвареграфиксадаптер**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-438">**PolicySourceHardwareGraphicsAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-439">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-439">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-440">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-441">Указывает, как настраивается **хардвареграфиксадаптер** .</span><span class="sxs-lookup"><span data-stu-id="ad2a3-441">Indicates how the **HardwareGraphicsAdapter** is configured.</span></span>

<span data-ttu-id="ad2a3-442">**Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** Это свойство недоступно до Windows 8 или Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-442">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="ad2a3-443">0</span><span class="sxs-lookup"><span data-stu-id="ad2a3-443">0</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-444">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-444">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-445">1</span><span class="sxs-lookup"><span data-stu-id="ad2a3-445">1</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-446">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-446">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-447">**полицисаурцелптпортмаппинг**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-447">**PolicySourceLPTPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-448">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-448">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-449">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-450">Указывает, настроено ли свойство **лптпортмаппинг** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-450">Indicates whether the **LPTPortMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="ad2a3-451">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-451">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-452">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-452">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-453">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-453">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-454">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-454">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-455">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-455">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-456">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad2a3-456">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-457">**полицисаурцемаксмониторс**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-457">**PolicySourceMaxMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-458">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-458">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-459">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-460">Указывает, настроено ли свойство **максмониторс** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-460">Indicates whether the **MaxMonitors** property is configured by the server, group policy, or default.</span></span>

<dt>

<span data-ttu-id="ad2a3-461">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-461">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-462">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-462">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-463">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-463">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-464">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-464">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-465">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-465">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-466">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad2a3-466">Default</span></span>

</dd> </dl>

<span data-ttu-id="ad2a3-467">**Windows Server 2008 и Windows Vista:** Это свойство недоступно до Windows Server 2008 R2 и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-467">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-468">**полицисаурцемаксресолутион**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-468">**PolicySourceMaxResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-469">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-469">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-470">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-471">Указывает, настроены ли свойства **максксресолутион** и **максиресолутион** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-471">Indicates whether the **MaxXResolution** and **MaxYResolution** properties are configured by the server, group policy, or default.</span></span>

<span data-ttu-id="ad2a3-472">**Windows Server 2008 и Windows Vista:** Это свойство недоступно до Windows Server 2008 R2 и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-472">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="ad2a3-473">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-473">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-474">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-474">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-475">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-475">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-476">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-476">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-477">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-477">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-478">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad2a3-478">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-479">**полицисаурцепнпредиректион**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-479">**PolicySourcePNPRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-480">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-480">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-481">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-482">Указывает, настроено ли свойство **пнпредиректион** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-482">Indicates whether the **PNPRedirection** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ad2a3-483">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-483">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-484">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-484">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-485">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-485">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-486">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-486">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-487">**полицисаурцеремотесессионпрофиле**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-487">**PolicySourceRemoteSessionProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-488">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-489">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-490">Указывает, как настраивается **ремотесессионпрофиле** .</span><span class="sxs-lookup"><span data-stu-id="ad2a3-490">Indicates how the **RemoteSessionProfile** is configured.</span></span>

<span data-ttu-id="ad2a3-491">**Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** Это свойство недоступно до Windows 8 или Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-491">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is unavailable prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="ad2a3-492">0</span><span class="sxs-lookup"><span data-stu-id="ad2a3-492">0</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-493">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-493">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-494">1</span><span class="sxs-lookup"><span data-stu-id="ad2a3-494">1</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-495">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-495">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-496">**полицисаурцеселектнетворкдетект**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-496">**PolicySourceSelectNetworkDetect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-497">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-497">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-498">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-498">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-499">Указывает, как настроено свойство **селектнетворкдетект** .</span><span class="sxs-lookup"><span data-stu-id="ad2a3-499">Indicates how the property **SelectNetworkDetect** is configured.</span></span>

<span data-ttu-id="ad2a3-500">**Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** Это свойство недоступно до Windows 8 или Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-500">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="ad2a3-501">0</span><span class="sxs-lookup"><span data-stu-id="ad2a3-501">0</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-502">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-502">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-503">1</span><span class="sxs-lookup"><span data-stu-id="ad2a3-503">1</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-504">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-504">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-505">**полицисаурцеселекттранспорт**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-505">**PolicySourceSelectTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-506">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-507">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-508">Указывает, как настроено свойство **селекттранспорт** .</span><span class="sxs-lookup"><span data-stu-id="ad2a3-508">Indicates how the property **SelectTransport** is configured.</span></span>

<span data-ttu-id="ad2a3-509">**Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** Это свойство недоступно до Windows 8 или Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-509">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="ad2a3-510">0</span><span class="sxs-lookup"><span data-stu-id="ad2a3-510">0</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-511">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-511">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-512">1</span><span class="sxs-lookup"><span data-stu-id="ad2a3-512">1</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-513">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-513">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-514">**полицисаурцевидеоплайбаккредир**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-514">**PolicySourceVideoPlaybackRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-515">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-515">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-516">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-517">Указывает, настроено ли свойство **видеоплайбаккредир** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-517">Indicates whether the **VideoPlaybackRedir** property is configured by the server or group policy.</span></span>

<span data-ttu-id="ad2a3-518">**Windows Server 2008 и Windows Vista:** Это свойство недоступно до Windows Server 2008 R2 и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-518">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="ad2a3-519">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-519">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-520">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-520">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-521">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-521">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-522">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-522">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-523">**полицисаурцевиндовспринтермаппинг**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-523">**PolicySourceWindowsPrinterMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-524">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-524">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-525">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-526">Указывает, настроено ли свойство **виндовспринтермаппинг** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-526">Indicates whether the **WindowsPrinterMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="ad2a3-527">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-527">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-528">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad2a3-528">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-529">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-529">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-530">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad2a3-530">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-531">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-531">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-532">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad2a3-532">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-533">**ремотесессионпрофиле**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-533">**RemoteSessionProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-534">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-534">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-535">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ad2a3-535">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-536">Указывает профиль для взаимодействия с RDP.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-536">Specifies the profile for the RDP experience.</span></span>

<span data-ttu-id="ad2a3-537">**Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** Это свойство недоступно до Windows 8 или Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-537">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="scale"></span><span id="SCALE"></span>

<span data-ttu-id="ad2a3-538">**масштаб** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-538">**scale** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="experience"></span><span id="EXPERIENCE"></span>

<span data-ttu-id="ad2a3-539">**опыт** (2)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-539">**experience** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="bandwidth"></span><span id="BANDWIDTH"></span>

<span data-ttu-id="ad2a3-540">**пропускная способность** (3)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-540">**bandwidth** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-541">**селектнетворкдетект**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-541">**SelectNetworkDetect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-542">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-542">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-543">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ad2a3-543">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-544">Указывает, используется ли обнаружение сети.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-544">Specifies whether network detection is used.</span></span>

<span data-ttu-id="ad2a3-545">**Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** Это свойство недоступно до Windows 8 или Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-545">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="ad2a3-546">0</span><span class="sxs-lookup"><span data-stu-id="ad2a3-546">0</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-547">используется во время подключения и в стабильном состоянии.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-547">used at connect time and in steady state.</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-548">1</span><span class="sxs-lookup"><span data-stu-id="ad2a3-548">1</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-549">отключено во время подключения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-549">disabled at connect time</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-550">2</span><span class="sxs-lookup"><span data-stu-id="ad2a3-550">2</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-551">отключено в стабильном состоянии</span><span class="sxs-lookup"><span data-stu-id="ad2a3-551">disabled in steady state</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-552">3</span><span class="sxs-lookup"><span data-stu-id="ad2a3-552">3</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-553">отключено во время подключения и в стабильном состоянии.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-553">disabled at connect time and in steady state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-554">**селекттранспорт**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-554">**SelectTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-555">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-555">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-556">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ad2a3-556">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-557">Указывает, какие транспортные протоколы можно использовать для доступа к серверу по протоколу RDP.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-557">Specifies which transport protocols can be used for RDP access to server.</span></span>

<span data-ttu-id="ad2a3-558">**Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** Это свойство недоступно до Windows 8 или Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-558">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="ad2a3-559">0</span><span class="sxs-lookup"><span data-stu-id="ad2a3-559">0</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-560">Используйте как UDP, так и TCP.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-560">Use both UDP and TCP.</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-561">1</span><span class="sxs-lookup"><span data-stu-id="ad2a3-561">1</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-562">Используйте только TCP.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-562">Use only TCP.</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-563">2</span><span class="sxs-lookup"><span data-stu-id="ad2a3-563">2</span></span>
</dt> <dd>

<span data-ttu-id="ad2a3-564">Используйте либо UDP, либо TCP.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-564">Use either UDP or TCP.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-565">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-565">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-566">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-566">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-567">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-568">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-568">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-569">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-569">Current status of the object.</span></span> <span data-ttu-id="ad2a3-570">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-570">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ad2a3-571">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="ad2a3-571">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ad2a3-572">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="ad2a3-572">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ad2a3-573">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-573">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ad2a3-574">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-574">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ad2a3-575">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ad2a3-575">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="ad2a3-576">("ОК")</span><span class="sxs-lookup"><span data-stu-id="ad2a3-576">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad2a3-577">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="ad2a3-577">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad2a3-578">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="ad2a3-578">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad2a3-579">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="ad2a3-579">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad2a3-580">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="ad2a3-580">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad2a3-581">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="ad2a3-581">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad2a3-582">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="ad2a3-582">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad2a3-583">("Служба")</span><span class="sxs-lookup"><span data-stu-id="ad2a3-583">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-584">**терминалнаме**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-584">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-585">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-585">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-586">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-586">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-587">Имя терминала.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-587">The name of the terminal.</span></span>

<span data-ttu-id="ad2a3-588">Это свойство наследуется из [**Win32 \_ терминалсеттинг**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="ad2a3-588">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad2a3-589">**видеоплайбаккредир**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-589">**VideoPlaybackRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-590">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-590">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-591">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-592">Указывает, разрешено ли перенаправление воспроизведения видео.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-592">Specifies whether to allow video playback redirection.</span></span>

<span data-ttu-id="ad2a3-593">**Windows Server 2008 и Windows Vista:** Это свойство недоступно до Windows Server 2008 R2 и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-593">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ad2a3-594">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-594">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ad2a3-595">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-595">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad2a3-596">**виндовспринтермаппинг**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-596">**WindowsPrinterMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2a3-597">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-597">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad2a3-598">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad2a3-598">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad2a3-599">Указывает, включено ли сопоставление принтеров для окна клиента.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-599">Specifies whether printer mapping is disabled or enabled for the client's window.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ad2a3-600"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-600"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-601">Сопоставление принтеров включено.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-601">Printer mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ad2a3-602"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ad2a3-602"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ad2a3-603">Сопоставление принтеров отключено.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-603">Printer mapping is disabled.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad2a3-604">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad2a3-604">Remarks</span></span>

<span data-ttu-id="ad2a3-605">Имейте в виду, что станция окна, связанная с сеансом консоли, не может получить доступ к методам и свойствам этого класса.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-605">Be aware that a window station associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="ad2a3-606">Если предпринимается попытка сделать это, указав "Console" в качестве значения свойства **терминалнаме** , методы этого объекта будут возвращать **WBEM \_ E \_ не \_ поддерживаются**.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-606">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="ad2a3-607">Этот код ошибки также возвращается, если станция окна пытается вызвать методы этого объекта для добавления или изменения свойств безопасности учетных записей LocalSystem, LocalService или NetworkService.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-607">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="ad2a3-608">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-608">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="ad2a3-609">Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="ad2a3-609">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="ad2a3-610">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением шесть.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-610">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="ad2a3-611">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-611">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="ad2a3-612">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="ad2a3-612">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ad2a3-613">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="ad2a3-613">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ad2a3-614">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="ad2a3-614">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ad2a3-615">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ad2a3-615">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad2a3-616">Требования</span><span class="sxs-lookup"><span data-stu-id="ad2a3-616">Requirements</span></span>



| <span data-ttu-id="ad2a3-617">Требование</span><span class="sxs-lookup"><span data-stu-id="ad2a3-617">Requirement</span></span> | <span data-ttu-id="ad2a3-618">Значение</span><span class="sxs-lookup"><span data-stu-id="ad2a3-618">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad2a3-619">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad2a3-619">Minimum supported client</span></span><br/> | <span data-ttu-id="ad2a3-620">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad2a3-620">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ad2a3-621">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad2a3-621">Minimum supported server</span></span><br/> | <span data-ttu-id="ad2a3-622">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad2a3-622">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ad2a3-623">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ad2a3-623">Namespace</span></span><br/>                | <span data-ttu-id="ad2a3-624">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="ad2a3-624">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ad2a3-625">MOF</span><span class="sxs-lookup"><span data-stu-id="ad2a3-625">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad2a3-626"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad2a3-626"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad2a3-627">DLL</span><span class="sxs-lookup"><span data-stu-id="ad2a3-627">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad2a3-628"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad2a3-628"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad2a3-629">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad2a3-629">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad2a3-630">**\_Терминал Win32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-630">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="ad2a3-631">**\_Терминалсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-631">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="ad2a3-632">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="ad2a3-632">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

