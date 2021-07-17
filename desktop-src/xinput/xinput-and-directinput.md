---
title: Ксинпут и Директинпут
description: Ксинпут — это API, позволяющий приложениям принимать входные данные от контроллера Xbox для Windows.
ms.assetid: 0f29a47b-24ed-c0fa-e9e9-8a061619845c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58339616f1e9e3a43529b6853bfc193d359ef11e
ms.sourcegitcommit: b3839bea8d55c981d53cb8802d666bf49093b428
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2021
ms.locfileid: "114373188"
---
# <a name="xinput-and-directinput"></a><span data-ttu-id="374a6-103">Ксинпут и Директинпут</span><span class="sxs-lookup"><span data-stu-id="374a6-103">XInput and DirectInput</span></span>

<span data-ttu-id="374a6-104">Ксинпут — это API, позволяющий приложениям принимать входные данные от контроллера Xbox для Windows.</span><span class="sxs-lookup"><span data-stu-id="374a6-104">XInput is an API that allows applications to receive input from the Xbox Controller for Windows.</span></span> <span data-ttu-id="374a6-105">В этом документе описываются различия между реализациями Ксинпут и [директинпут](/previous-versions/windows/desktop/ee416842(v=vs.85)) в контроллере Xbox, а также способы поддержки устройств ксинпут и устаревших устройств директинпут.</span><span class="sxs-lookup"><span data-stu-id="374a6-105">This document describes the differences between XInput and [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) implementations of the Xbox Controller and how you can support XInput devices and legacy DirectInput devices at the same time.</span></span>

> [!Note]  
> <span data-ttu-id="374a6-106">использовать устаревшие [директинпут](/previous-versions/windows/desktop/ee416842(v=vs.85)) не рекомендуется, и директинпут недоступен для приложений магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="374a6-106">Use of legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) is not recommended, and DirectInput is not available for Windows Store apps.</span></span>

## <a name="the-new-standard-xinput"></a><span data-ttu-id="374a6-107">Новый стандарт: Ксинпут</span><span class="sxs-lookup"><span data-stu-id="374a6-107">The New Standard: XInput</span></span>

<span data-ttu-id="374a6-108">Ксинпут теперь доступен для разработки игр.</span><span class="sxs-lookup"><span data-stu-id="374a6-108">XInput is now available for game development.</span></span> <span data-ttu-id="374a6-109">Это новый стандарт ввода для Xbox и Windows.</span><span class="sxs-lookup"><span data-stu-id="374a6-109">This is the new input standard for both the Xbox and Windows.</span></span> <span data-ttu-id="374a6-110">интерфейсы api доступны в пакете SDK для DirectX, и драйвер доступен в Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="374a6-110">The APIs are available through the DirectX SDK, and the driver is available through Windows Update.</span></span>

<span data-ttu-id="374a6-111">Использование Ксинпут вместо [директинпут](/previous-versions/windows/desktop/ee416842(v=vs.85))имеет несколько преимуществ.</span><span class="sxs-lookup"><span data-stu-id="374a6-111">There are several advantages to using XInput over [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)):</span></span>

-   <span data-ttu-id="374a6-112">Ксинпут проще в использовании и требует меньше настроек, чем [директинпут](/previous-versions/windows/desktop/ee416842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="374a6-112">XInput is easier to use and requires less setup than [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))</span></span>
-   <span data-ttu-id="374a6-113">как для Xbox, так и для Windowsного программирования будут использоваться одни и те же наборы основных api, что позволяет значительно упростить программирование между различными платформами.</span><span class="sxs-lookup"><span data-stu-id="374a6-113">Both Xbox and Windows programming will use the same sets of core APIs, allowing programming to translate cross-platform much easier</span></span>
-   <span data-ttu-id="374a6-114">Будет установлена большая база установки контроллеров Xbox.</span><span class="sxs-lookup"><span data-stu-id="374a6-114">There will be a large installed base of Xbox controllers</span></span>
-   <span data-ttu-id="374a6-115">Устройства Ксинпут (т. е. контроллеры Xbox) будут иметь функцию вибрации только при использовании интерфейсов API Ксинпут.</span><span class="sxs-lookup"><span data-stu-id="374a6-115">XInput devices (that is, the Xbox controllers) will have vibration functionality only when using XInput APIs</span></span>
-   <span data-ttu-id="374a6-116">Будущие контроллеры, выпущенные для консоли Xbox (то есть колеса управления), также будут работать на Windows</span><span class="sxs-lookup"><span data-stu-id="374a6-116">Future controllers released for the Xbox console (that is, steering wheels) will also work on Windows</span></span>

### <a name="using-the-xbox-controller-with-directinput"></a><span data-ttu-id="374a6-117">Использование контроллера Xbox с Директинпут</span><span class="sxs-lookup"><span data-stu-id="374a6-117">Using the Xbox Controller with DirectInput</span></span>

<span data-ttu-id="374a6-118">Контроллер Xbox правильно перечислен в [директинпут](/previous-versions/windows/desktop/ee416842(v=vs.85))и может использоваться с директинпутапис.</span><span class="sxs-lookup"><span data-stu-id="374a6-118">The Xbox Controller is properly enumerated on [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)), and can be used with the DirectInputAPIs.</span></span> <span data-ttu-id="374a6-119">Однако некоторые функции, предоставляемые Ксинпут, будут отсутствовать в реализации Директинпут:</span><span class="sxs-lookup"><span data-stu-id="374a6-119">However, some functionality provided by XInput will be missing from the DirectInput implementation:</span></span>

-   <span data-ttu-id="374a6-120">Левая и правая кнопки триггера будут действовать как одна кнопка, а не независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="374a6-120">The left and right trigger buttons will act as a single button, not independently</span></span>
-   <span data-ttu-id="374a6-121">Эффекты вибрации будут недоступны</span><span class="sxs-lookup"><span data-stu-id="374a6-121">The vibration effects will not be available</span></span>
-   <span data-ttu-id="374a6-122">Запросы для головных устройств будут недоступны.</span><span class="sxs-lookup"><span data-stu-id="374a6-122">Querying for headset devices will not be available</span></span>

<span data-ttu-id="374a6-123">Сочетание левого и правого триггеров в [директинпут](/previous-versions/windows/desktop/ee416842(v=vs.85)) — это проектирование.</span><span class="sxs-lookup"><span data-stu-id="374a6-123">The combination of the left and right triggers in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) is by design.</span></span> <span data-ttu-id="374a6-124">Игры всегда предполагают, что оси устройств Директинпут будут центрированы при отсутствии взаимодействия с пользователем с устройством.</span><span class="sxs-lookup"><span data-stu-id="374a6-124">Games have always assumed that DirectInput device axes are centered when there is no user interaction with the device.</span></span> <span data-ttu-id="374a6-125">Однако контроллер Xbox был разработан для регистрации минимального значения, а не по центру, если триггеры не удерживаются.</span><span class="sxs-lookup"><span data-stu-id="374a6-125">However, the Xbox controller was designed to register minimum value, not center, when the triggers are not being held.</span></span> <span data-ttu-id="374a6-126">Поэтому более старые игры подразумевают взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="374a6-126">Older games would therefore assume user interaction.</span></span>

<span data-ttu-id="374a6-127">Решением было объединение триггеров, установка одного триггера в положительном направлении, а другое — отрицательное направление, поэтому вмешательство пользователя не [директинпут](/previous-versions/windows/desktop/ee416842(v=vs.85)) , что элемент управления находится в центре.</span><span class="sxs-lookup"><span data-stu-id="374a6-127">The solution was to combine the triggers, setting one trigger to a positive direction and the other to a negative direction, so no user interaction is indicative to [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) of the "control" being at center.</span></span>

<span data-ttu-id="374a6-128">Чтобы проверить значения триггера по отдельности, необходимо использовать Ксинпут.</span><span class="sxs-lookup"><span data-stu-id="374a6-128">In order to test the trigger values separately, you must use XInput.</span></span>

## <a name="xinput-and-directinput-side-by-side"></a><span data-ttu-id="374a6-129">Параллельная Ксинпут и Директинпут</span><span class="sxs-lookup"><span data-stu-id="374a6-129">XInput and DirectInput Side by Side</span></span>

<span data-ttu-id="374a6-130">Только поддержка Ксинпут, ваша игра не будет работать с устаревшими устройствами [директинпут](/previous-versions/windows/desktop/ee416842(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="374a6-130">By supporting XInput only, your game will not work with legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) devices.</span></span> <span data-ttu-id="374a6-131">Ксинпут не сможет распознать эти устройства.</span><span class="sxs-lookup"><span data-stu-id="374a6-131">XInput will not recognize these devices.</span></span>

<span data-ttu-id="374a6-132">Если вы хотите, чтобы ваша игра поддерживала устаревшие устройства [директинпут](/previous-versions/windows/desktop/ee416842(v=vs.85)) , вы можете использовать параллельно Директинпут и ксинпут.</span><span class="sxs-lookup"><span data-stu-id="374a6-132">If you want your game to support legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) devices, you may use DirectInput and XInput side by side.</span></span> <span data-ttu-id="374a6-133">При перечислении устройств Директинпут все устройства Директинпут будут перечисляться правильно.</span><span class="sxs-lookup"><span data-stu-id="374a6-133">When enumerating your DirectInput devices, all DirectInput devices will enumerate correctly.</span></span> <span data-ttu-id="374a6-134">Все устройства Ксинпут будут отображаться как устройства Ксинпут и Директинпут, но их не следует обрабатывать с помощью Директинпут.</span><span class="sxs-lookup"><span data-stu-id="374a6-134">All XInput devices will show up as both XInput and DirectInput devices, but they should not be handled through DirectInput.</span></span> <span data-ttu-id="374a6-135">Вам потребуется определить, какие из устройств Директинпут являются устаревшими устройствами, а какие — Ксинпут устройствами, и удалить их из перечисления Директинпут устройств.</span><span class="sxs-lookup"><span data-stu-id="374a6-135">You will need to determine which of your DirectInput devices are legacy devices, and which are XInput devices, and remove them from the enumeration of DirectInput devices.</span></span>

<span data-ttu-id="374a6-136">Для этого вставьте этот код в обратный вызов перечисления Директинпут:</span><span class="sxs-lookup"><span data-stu-id="374a6-136">To do this, insert this code into your DirectInput enumeration callback:</span></span>

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

> <span data-ttu-id="374a6-137">Немного улучшенная версия этого кода находится в примере устаревшей Директинпут [джойстика](https://github.com/walbourn/directx-sdk-samples/tree/master/DirectInput/Joystick) .</span><span class="sxs-lookup"><span data-stu-id="374a6-137">A slightly improved version of this code is in the legacy DirectInput [Joystick](https://github.com/walbourn/directx-sdk-samples/tree/master/DirectInput/Joystick) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="374a6-138">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="374a6-138">Related topics</span></span>

[<span data-ttu-id="374a6-139">начало работы с Ксинпут</span><span class="sxs-lookup"><span data-stu-id="374a6-139">Getting Started With XInput</span></span>](getting-started-with-xinput.md)

[<span data-ttu-id="374a6-140">Справочник по программированию</span><span class="sxs-lookup"><span data-stu-id="374a6-140">Programming Reference</span></span>](programming-reference.md)
