---
description: Чтобы перечислить все устройства на компьютере, вызовите функцию Енумдисплайдевицес. Возвращаемые сведения также указывают, какой монитор является частью рабочего стола.
ms.assetid: 834dee04-66fa-42eb-adff-c08a74c6cea8
title: Перечисление и элемент управления отображением
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8cdfd5e3b1c6ebb5ff0d4ebdfa1ab44b45c2c25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080499"
---
# <a name="enumeration-and-display-control"></a><span data-ttu-id="08058-104">Перечисление и элемент управления отображением</span><span class="sxs-lookup"><span data-stu-id="08058-104">Enumeration and Display Control</span></span>

<span data-ttu-id="08058-105">Чтобы перечислить все устройства на компьютере, вызовите функцию [**енумдисплайдевицес**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) .</span><span class="sxs-lookup"><span data-stu-id="08058-105">To enumerate all the devices on the computer, call the [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) function.</span></span> <span data-ttu-id="08058-106">Возвращаемые сведения также указывают, какой монитор является частью рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="08058-106">The information that is returned also indicates which monitor is part of the desktop.</span></span>

<span data-ttu-id="08058-107">Чтобы перечислить устройства на рабочем столе, пересекающие вырезанную область, вызовите [**енумдисплаймониторс**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors).</span><span class="sxs-lookup"><span data-stu-id="08058-107">To enumerate the devices on the desktop that intersect a clipping region, call [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors).</span></span> <span data-ttu-id="08058-108">При этом возвращается маркер ХМОНИТОР для каждого монитора, который используется с [**жетмониторинфо**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span><span class="sxs-lookup"><span data-stu-id="08058-108">This returns the HMONITOR handle to each monitor, which is used with [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span></span> <span data-ttu-id="08058-109">Чтобы перечислить все устройства на виртуальном экране, используйте **енумдисплаймониторс**.</span><span class="sxs-lookup"><span data-stu-id="08058-109">To enumerate all the devices in the virtual screen, use **EnumDisplayMonitors**.</span></span> <span data-ttu-id="08058-110">как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="08058-110">as shown in the following code:</span></span>


```C++
EnumDisplayMonitors(NULL, NULL, MyInfoEnumProc, 0);  
```



<span data-ttu-id="08058-111">Чтобы получить сведения об устройстве вывода, используйте [**енумдисплайсеттингс**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) или [**енумдисплайсеттингсекс**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa).</span><span class="sxs-lookup"><span data-stu-id="08058-111">To get information about a display device, use [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) or [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa).</span></span>

<span data-ttu-id="08058-112">Функция [**чанжедисплайсеттингсекс**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) используется для управления устройствами вывода на компьютере.</span><span class="sxs-lookup"><span data-stu-id="08058-112">The [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) function is used to control the display devices on the computer.</span></span> <span data-ttu-id="08058-113">Он может изменить конфигурацию устройств, например указать расположение монитора на виртуальном рабочем столе и изменить битовую глубину любого экрана.</span><span class="sxs-lookup"><span data-stu-id="08058-113">It can modify the configuration of the devices, such as specifying the position of a monitor on the virtual desktop and changing the bit depth of any display.</span></span> <span data-ttu-id="08058-114">Как правило, приложение не использует эту функцию.</span><span class="sxs-lookup"><span data-stu-id="08058-114">Typically, an application does not use this function.</span></span> <span data-ttu-id="08058-115">Чтобы добавить монитор отображения в систему с несколькими мониторами программными средствами, задайте для свойства **DEVMODE. дмфиелдс** значение DM \_ и укажите нужное расположение (с помощью **DEVMODE. дмпоситион** ) для добавляемого монитора, который находится рядом по крайней мере с одним пикселем области отображения существующего монитора.</span><span class="sxs-lookup"><span data-stu-id="08058-115">To add a display monitor to a multiple-monitor system programmatically, set **DEVMODE.dmFields** to DM\_POSITION and specify a position (using **DEVMODE.dmPosition** ) for the monitor you are adding that is adjacent to at least one pixel of the display area of an existing monitor.</span></span> <span data-ttu-id="08058-116">Чтобы отключить монитор, задайте для свойства **DEVMODE. дмфиелдс** значение DM \_ и задайте для параметра **DEVMODE. Дмпелсвидс** и **DEVMODE. дмпелшеигхт** значение 0.</span><span class="sxs-lookup"><span data-stu-id="08058-116">To detach the monitor, set **DEVMODE.dmFields** to DM\_POSITION and set **DEVMODE.dmPelsWidth** and **DEVMODE.dmPelsHeight** to zero.</span></span>

<span data-ttu-id="08058-117">В следующем примере кода показано, как отключить все дополнительные устройства отображения с рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="08058-117">The following code demonstrates how to detach all secondary display devices from the desktop:</span></span>


```
void DetachDisplay()
{
    BOOL            FoundSecondaryDisp = FALSE;
    DWORD           DispNum = 0;
    DISPLAY_DEVICE  DisplayDevice;
    LONG            Result;
    TCHAR           szTemp[200];
    int             i = 0;
    DEVMODE   defaultMode;

    // initialize DisplayDevice
    ZeroMemory(&DisplayDevice, sizeof(DisplayDevice));
    DisplayDevice.cb = sizeof(DisplayDevice);

    // get all display devices
    while (EnumDisplayDevices(NULL, DispNum, &DisplayDevice, 0))
        {
        ZeroMemory(&defaultMode, sizeof(DEVMODE));
        defaultMode.dmSize = sizeof(DEVMODE);
        if ( !EnumDisplaySettings((LPSTR)DisplayDevice.DeviceName, ENUM_REGISTRY_SETTINGS, &defaultMode) )
                  OutputDebugString("Store default failed\n");

        if ((DisplayDevice.StateFlags & DISPLAY_DEVICE_ATTACHED_TO_DESKTOP) &&
            !(DisplayDevice.StateFlags & DISPLAY_DEVICE_PRIMARY_DEVICE))
            {
            DEVMODE    DevMode;
            ZeroMemory(&DevMode, sizeof(DevMode));
            DevMode.dmSize = sizeof(DevMode);
            DevMode.dmFields = DM_PELSWIDTH | DM_PELSHEIGHT | DM_BITSPERPEL | DM_POSITION
                        | DM_DISPLAYFREQUENCY | DM_DISPLAYFLAGS ;
            Result = ChangeDisplaySettingsEx((LPSTR)DisplayDevice.DeviceName, 
                                            &DevMode,
                                            NULL,
                                            CDS_UPDATEREGISTRY,
                                            NULL);

            //The code below shows how to re-attach the secondary displays to the desktop

            //ChangeDisplaySettingsEx((LPSTR)DisplayDevice.DeviceName,
            //                       &defaultMode,
            //                       NULL,
            //                       CDS_UPDATEREGISTRY,
            //                       NULL);

            }

        // Reinit DisplayDevice just to be extra clean

        ZeroMemory(&DisplayDevice, sizeof(DisplayDevice));
        DisplayDevice.cb = sizeof(DisplayDevice);
        DispNum++;
        } // end while for all display devices
}
```



<span data-ttu-id="08058-118">Для каждого устройства вывода приложение может сохранить сведения в реестре, описывающем параметры конфигурации для устройства, а также параметры расположения.</span><span class="sxs-lookup"><span data-stu-id="08058-118">For each display device, the application can save information in the registry that describes the configuration parameters for the device, as well as location parameters.</span></span> <span data-ttu-id="08058-119">Приложение также может определить, какие дисплеи являются частью рабочего стола, а какие — нет, с помощью \_ флага Display Device, \_ подключенный \_ к \_ рабочему столу в структуре [**\_ устройства отображения**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) .</span><span class="sxs-lookup"><span data-stu-id="08058-119">The application can also determine which displays are part of the desktop, and which are not, through the DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP flag in the [**DISPLAY\_DEVICE**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) structure.</span></span> <span data-ttu-id="08058-120">После сохранения всех сведений о конфигурации в реестре приложение может снова вызвать [**чанжедисплайсеттингсекс**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) , чтобы динамически изменить параметры без перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="08058-120">Once all the configuration information is stored in the registry, the application can call [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) again to dynamically change the settings, with no restart required.</span></span>

 

 



