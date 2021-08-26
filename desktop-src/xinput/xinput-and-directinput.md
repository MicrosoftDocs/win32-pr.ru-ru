---
title: Ксинпут и Директинпут
description: Ксинпут — это API, позволяющий приложениям принимать входные данные от контроллера Xbox для Windows.
ms.assetid: 0f29a47b-24ed-c0fa-e9e9-8a061619845c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01484e7c1419dea097ddf440d82a92edb527327f8696afa5f5864fb1b12453b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926224"
---
# <a name="xinput-and-directinput"></a>Ксинпут и Директинпут

Ксинпут — это API, позволяющий приложениям принимать входные данные от контроллера Xbox для Windows. В этом документе описываются различия между реализациями Ксинпут и [директинпут](/previous-versions/windows/desktop/ee416842(v=vs.85)) в контроллере Xbox, а также способы поддержки устройств ксинпут и устаревших устройств директинпут.

> [!Note]  
> использовать устаревшие [директинпут](/previous-versions/windows/desktop/ee416842(v=vs.85)) не рекомендуется, и директинпут недоступен для приложений магазина Windows.

## <a name="the-new-standard-xinput"></a>Новый стандарт: Ксинпут

Ксинпут теперь доступен для разработки игр. Это новый стандарт ввода для Xbox и Windows. интерфейсы api доступны в пакете SDK для DirectX, и драйвер доступен в Центр обновления Windows.

Использование Ксинпут вместо [директинпут](/previous-versions/windows/desktop/ee416842(v=vs.85))имеет несколько преимуществ.

-   Ксинпут проще в использовании и требует меньше настроек, чем [директинпут](/previous-versions/windows/desktop/ee416842(v=vs.85))
-   как для Xbox, так и для Windowsного программирования будут использоваться одни и те же наборы основных api, что позволяет значительно упростить программирование между различными платформами.
-   Будет установлена большая база установки контроллеров Xbox.
-   Устройства Ксинпут (т. е. контроллеры Xbox) будут иметь функцию вибрации только при использовании интерфейсов API Ксинпут.
-   Будущие контроллеры, выпущенные для консоли Xbox (то есть колеса управления), также будут работать на Windows

### <a name="using-the-xbox-controller-with-directinput"></a>Использование контроллера Xbox с Директинпут

Контроллер Xbox правильно перечислен в [директинпут](/previous-versions/windows/desktop/ee416842(v=vs.85))и может использоваться с директинпутапис. Однако некоторые функции, предоставляемые Ксинпут, будут отсутствовать в реализации Директинпут:

-   Левая и правая кнопки триггера будут действовать как одна кнопка, а не независимо друг от друга.
-   Эффекты вибрации будут недоступны
-   Запросы для головных устройств будут недоступны.

Сочетание левого и правого триггеров в [директинпут](/previous-versions/windows/desktop/ee416842(v=vs.85)) — это проектирование. Игры всегда предполагают, что оси устройств Директинпут будут центрированы при отсутствии взаимодействия с пользователем с устройством. Однако контроллер Xbox был разработан для регистрации минимального значения, а не по центру, если триггеры не удерживаются. Поэтому более старые игры подразумевают взаимодействие с пользователем.

Решением было объединение триггеров, установка одного триггера в положительном направлении, а другое — отрицательное направление, поэтому вмешательство пользователя не [директинпут](/previous-versions/windows/desktop/ee416842(v=vs.85)) , что элемент управления находится в центре.

Чтобы проверить значения триггера по отдельности, необходимо использовать Ксинпут.

## <a name="xinput-and-directinput-side-by-side"></a>Параллельная Ксинпут и Директинпут

Только поддержка Ксинпут, ваша игра не будет работать с устаревшими устройствами [директинпут](/previous-versions/windows/desktop/ee416842(v=vs.85)) . Ксинпут не сможет распознать эти устройства.

Если вы хотите, чтобы ваша игра поддерживала устаревшие устройства [директинпут](/previous-versions/windows/desktop/ee416842(v=vs.85)) , вы можете использовать параллельно Директинпут и ксинпут. При перечислении устройств Директинпут все устройства Директинпут будут перечисляться правильно. Все устройства Ксинпут будут отображаться как устройства Ксинпут и Директинпут, но их не следует обрабатывать с помощью Директинпут. Вам потребуется определить, какие из устройств Директинпут являются устаревшими устройствами, а какие — Ксинпут устройствами, и удалить их из перечисления Директинпут устройств.

Для этого вставьте этот код в обратный вызов перечисления Директинпут:

```cpp
#include <wbemidl.h>
#include <oleauto.h>

#ifndef SAFE_RELEASE
#define SAFE_RELEASE(p) { if (p) { (p)->Release(); (p) = nullptr; } }
#endif

//-----------------------------------------------------------------------------
// Enum each PNP device using WMI and check each device ID to see if it contains 
// "IG_" (ex. "VID_045E&PID_028E&IG_00").  If it does, then it's an XInput device
// Unfortunately this information can not be found by just using DirectInput 
//-----------------------------------------------------------------------------
BOOL IsXInputDevice( const GUID* pGuidProductFromDirectInput )
{
    IWbemLocator*           pIWbemLocator = nullptr;
    IEnumWbemClassObject*   pEnumDevices = nullptr;
    IWbemClassObject*       pDevices[20] = {};
    IWbemServices*          pIWbemServices = nullptr;
    BSTR                    bstrNamespace = nullptr;
    BSTR                    bstrDeviceID = nullptr;
    BSTR                    bstrClassName = nullptr;
    bool                    bIsXinputDevice = false;
    
    // CoInit if needed
    HRESULT hr = CoInitialize(nullptr);
    bool bCleanupCOM = SUCCEEDED(hr);

    // So we can call VariantClear() later, even if we never had a successful IWbemClassObject::Get().
    VARIANT var = {};
    VariantInit(&var);

    // Create WMI
    hr = CoCreateInstance(__uuidof(WbemLocator),
        nullptr,
        CLSCTX_INPROC_SERVER,
        __uuidof(IWbemLocator),
        (LPVOID*)&pIWbemLocator);
    if (FAILED(hr) || pIWbemLocator == nullptr)
        goto LCleanup;

    bstrNamespace = SysAllocString(L"\\\\.\\root\\cimv2");  if (bstrNamespace == nullptr) goto LCleanup;
    bstrClassName = SysAllocString(L"Win32_PNPEntity");     if (bstrClassName == nullptr) goto LCleanup;
    bstrDeviceID = SysAllocString(L"DeviceID");             if (bstrDeviceID == nullptr)  goto LCleanup;
    
    // Connect to WMI 
    hr = pIWbemLocator->ConnectServer(bstrNamespace, nullptr, nullptr, 0L,
        0L, nullptr, nullptr, &pIWbemServices);
    if (FAILED(hr) || pIWbemServices == nullptr)
        goto LCleanup;

    // Switch security level to IMPERSONATE. 
    hr = CoSetProxyBlanket(pIWbemServices,
        RPC_C_AUTHN_WINNT, RPC_C_AUTHZ_NONE, nullptr,
        RPC_C_AUTHN_LEVEL_CALL, RPC_C_IMP_LEVEL_IMPERSONATE,
        nullptr, EOAC_NONE);
    if ( FAILED(hr) )
        goto LCleanup;

    hr = pIWbemServices->CreateInstanceEnum(bstrClassName, 0, nullptr, &pEnumDevices);
    if (FAILED(hr) || pEnumDevices == nullptr)
        goto LCleanup;

    // Loop over all devices
    for (;;)
    {
        ULONG uReturned = 0;
        hr = pEnumDevices->Next(10000, _countof(pDevices), pDevices, &uReturned);
        if (FAILED(hr))
            goto LCleanup;
        if (uReturned == 0)
            break;

        for (size_t iDevice = 0; iDevice < uReturned; ++iDevice)
        {
            // For each device, get its device ID
            hr = pDevices[iDevice]->Get(bstrDeviceID, 0L, &var, nullptr, nullptr);
            if (SUCCEEDED(hr) && var.vt == VT_BSTR && var.bstrVal != nullptr)
            {
                // Check if the device ID contains "IG_".  If it does, then it's an XInput device
                // This information can not be found from DirectInput 
                if (wcsstr(var.bstrVal, L"IG_"))
                {
                    // If it does, then get the VID/PID from var.bstrVal
                    DWORD dwPid = 0, dwVid = 0;
                    WCHAR* strVid = wcsstr(var.bstrVal, L"VID_");
                    if (strVid && swscanf_s(strVid, L"VID_%4X", &dwVid) != 1)
                        dwVid = 0;
                    WCHAR* strPid = wcsstr(var.bstrVal, L"PID_");
                    if (strPid && swscanf_s(strPid, L"PID_%4X", &dwPid) != 1)
                        dwPid = 0;

                    // Compare the VID/PID to the DInput device
                    DWORD dwVidPid = MAKELONG(dwVid, dwPid);
                    if (dwVidPid == pGuidProductFromDirectInput->Data1)
                    {
                        bIsXinputDevice = true;
                        goto LCleanup;
                    }
                }
            }
            VariantClear(&var);
            SAFE_RELEASE(pDevices[iDevice]);
        }
    }

LCleanup:
    VariantClear(&var);
    
    if(bstrNamespace)
        SysFreeString(bstrNamespace);
    if(bstrDeviceID)
        SysFreeString(bstrDeviceID);
    if(bstrClassName)
        SysFreeString(bstrClassName);
        
    for (size_t iDevice = 0; iDevice < _countof(pDevices); ++iDevice)
        SAFE_RELEASE(pDevices[iDevice]);

    SAFE_RELEASE(pEnumDevices);
    SAFE_RELEASE(pIWbemLocator);
    SAFE_RELEASE(pIWbemServices);

    if(bCleanupCOM)
        CoUninitialize();

    return bIsXinputDevice;
}


//-----------------------------------------------------------------------------
// Name: EnumJoysticksCallback()
// Desc: Called once for each enumerated joystick. If we find one, create a
//       device interface on it so we can play with it.
//-----------------------------------------------------------------------------
BOOL CALLBACK EnumJoysticksCallback( const DIDEVICEINSTANCE* pdidInstance,
                                     VOID* pContext )
{
    if( IsXInputDevice( &pdidInstance->guidProduct ) )
        return DIENUM_CONTINUE;

     // Device is verified not XInput, so add it to the list of DInput devices

     return DIENUM_CONTINUE;    
}
```

> Немного улучшенная версия этого кода находится в примере устаревшей Директинпут [джойстика](https://github.com/walbourn/directx-sdk-samples/tree/master/DirectInput/Joystick) .

## <a name="related-topics"></a>Связанные темы

[начало работы с Ксинпут](getting-started-with-xinput.md)

[Справочник по программированию](programming-reference.md)
