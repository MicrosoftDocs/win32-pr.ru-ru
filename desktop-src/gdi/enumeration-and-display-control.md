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
# <a name="enumeration-and-display-control"></a>Перечисление и элемент управления отображением

Чтобы перечислить все устройства на компьютере, вызовите функцию [**енумдисплайдевицес**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) . Возвращаемые сведения также указывают, какой монитор является частью рабочего стола.

Чтобы перечислить устройства на рабочем столе, пересекающие вырезанную область, вызовите [**енумдисплаймониторс**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors). При этом возвращается маркер ХМОНИТОР для каждого монитора, который используется с [**жетмониторинфо**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa). Чтобы перечислить все устройства на виртуальном экране, используйте **енумдисплаймониторс**. как показано в следующем коде:


```C++
EnumDisplayMonitors(NULL, NULL, MyInfoEnumProc, 0);  
```



Чтобы получить сведения об устройстве вывода, используйте [**енумдисплайсеттингс**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) или [**енумдисплайсеттингсекс**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa).

Функция [**чанжедисплайсеттингсекс**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) используется для управления устройствами вывода на компьютере. Он может изменить конфигурацию устройств, например указать расположение монитора на виртуальном рабочем столе и изменить битовую глубину любого экрана. Как правило, приложение не использует эту функцию. Чтобы добавить монитор отображения в систему с несколькими мониторами программными средствами, задайте для свойства **DEVMODE. дмфиелдс** значение DM \_ и укажите нужное расположение (с помощью **DEVMODE. дмпоситион** ) для добавляемого монитора, который находится рядом по крайней мере с одним пикселем области отображения существующего монитора. Чтобы отключить монитор, задайте для свойства **DEVMODE. дмфиелдс** значение DM \_ и задайте для параметра **DEVMODE. Дмпелсвидс** и **DEVMODE. дмпелшеигхт** значение 0.

В следующем примере кода показано, как отключить все дополнительные устройства отображения с рабочего стола.


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



Для каждого устройства вывода приложение может сохранить сведения в реестре, описывающем параметры конфигурации для устройства, а также параметры расположения. Приложение также может определить, какие дисплеи являются частью рабочего стола, а какие — нет, с помощью \_ флага Display Device, \_ подключенный \_ к \_ рабочему столу в структуре [**\_ устройства отображения**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) . После сохранения всех сведений о конфигурации в реестре приложение может снова вызвать [**чанжедисплайсеттингсекс**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) , чтобы динамически изменить параметры без перезагрузки.

 

 



