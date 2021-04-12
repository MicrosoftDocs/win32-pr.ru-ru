---
description: Пиковые показатели
ms.assetid: 02f5d1b4-ba4f-424a-897f-b113d1f7cd6b
title: Пиковые показатели
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccd2f1ce0b8fd45fbf1cb3710c878c05544f7d4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141917"
---
# <a name="peak-meters"></a><span data-ttu-id="d0d76-103">Пиковые показатели</span><span class="sxs-lookup"><span data-stu-id="d0d76-103">Peak Meters</span></span>

<span data-ttu-id="d0d76-104">Для поддержки приложений Windows, отображающих пиковые показатели, [API ендпоинтволуме](endpointvolume-api.md) включает интерфейс [**иаудиометеринформатион**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) .</span><span class="sxs-lookup"><span data-stu-id="d0d76-104">To support Windows applications that display peak meters, the [EndpointVolume API](endpointvolume-api.md) includes an [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface.</span></span> <span data-ttu-id="d0d76-105">Этот интерфейс представляет пиковое значение счетчика на [устройстве конечной точки звука](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="d0d76-105">This interface represents a peak meter on an [audio endpoint device](audio-endpoint-devices.md).</span></span> <span data-ttu-id="d0d76-106">Для устройства отрисовки значение, полученное из счетчика пиковой нагрузки, представляет максимальное значение выборки, обнаруженное в потоке вывода на устройство в течение предыдущего периода отслеживания.</span><span class="sxs-lookup"><span data-stu-id="d0d76-106">For a rendering device, the value retrieved from the peak meter represents the maximum sample value encountered in the output stream to the device during the preceding metering period.</span></span> <span data-ttu-id="d0d76-107">Для устройства записи значение, полученное из счетчика пиковой нагрузки, представляет максимальное значение выборки, обнаруженное во входном потоке с устройства.</span><span class="sxs-lookup"><span data-stu-id="d0d76-107">For a capture device, the value retrieved from the peak meter represents the maximum sample value encountered in the input stream from the device.</span></span>

<span data-ttu-id="d0d76-108">Значения счетчика пиковой нагрузки, полученные из методов в интерфейсе [**иаудиометеринформатион**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) , являются числами с плавающей запятой в нормализованном диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="d0d76-108">The peak-meter values obtained from the methods in the [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface are floating-point numbers in the normalized range from 0.0 to 1.0.</span></span> <span data-ttu-id="d0d76-109">Например, если поток PCM содержит 16-разрядные примеры, а пиковое значение в течение определенного периода измерения — 8914, то абсолютное значение, записанное счетчиком "Пиковая загрузка", равно 8914, а нормализованное значение пиковой нагрузки, сообщаемое интерфейсом **иаудиометеринформатион** , — 8914/32768 = 0,272.</span><span class="sxs-lookup"><span data-stu-id="d0d76-109">For example, if a PCM stream contains 16-bit samples, and the peak sample value during a particular metering period is —8914, then the absolute value recorded by the peak meter is 8914, and the normalized peak value reported by the **IAudioMeterInformation** interface is 8914/32768 = 0.272.</span></span>

<span data-ttu-id="d0d76-110">Если устройство конечной точки звука реализует счетчик пикового использования оборудования, то интерфейс [**иаудиометеринформатион**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) использует счетчик пиковой нагрузки на оборудование.</span><span class="sxs-lookup"><span data-stu-id="d0d76-110">If the audio endpoint device implements the peak meter in hardware, the [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface uses the hardware peak meter.</span></span> <span data-ttu-id="d0d76-111">В противном случае интерфейс реализует счетчик пикового использования программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="d0d76-111">Otherwise, the interface implements the peak meter in software.</span></span>

<span data-ttu-id="d0d76-112">Если устройство имеет аппаратный счетчик пиковой нагрузки, счетчик пиковой активности активен как в режиме общего доступа, так и в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="d0d76-112">If a device has a hardware peak meter, the peak meter is active both in shared mode and in exclusive mode.</span></span> <span data-ttu-id="d0d76-113">Если устройство не имеет счетчика пикового использования оборудования, счетчик пиковой активности активен в общем режиме, но не в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="d0d76-113">If a device lacks hardware peak meter, the peak meter is active in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="d0d76-114">В монопольном режиме приложение и звуковые данные обмениваются данными напрямую, минуя счетчик пиковой загрузки программного обеспечения (который всегда сообщает пиковое значение 0,0).</span><span class="sxs-lookup"><span data-stu-id="d0d76-114">In exclusive mode, the application and the audio hardware exchange audio data directly, bypassing the software peak meter (which always reports a peak value of 0.0).</span></span>

<span data-ttu-id="d0d76-115">Следующий пример кода C++ — это приложение Windows, которое отображает счетчик пиковой загрузки для устройства отрисовки по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="d0d76-115">The following C++ code example is a Windows application that displays a peak meter for the default rendering device:</span></span>


```C++
// Peakmeter.cpp -- WinMain and dialog box functions

#include <windows.h>
#include <mmdeviceapi.h>
#include <endpointvolume.h>
#include "resource.h"

static BOOL CALLBACK DlgProc(HWND, UINT, WPARAM, LPARAM);
static void DrawPeakMeter(HWND, float);

// Timer ID and period (in milliseconds)
#define ID_TIMER  1
#define TIMER_PERIOD  125

#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

//-----------------------------------------------------------
// WinMain -- Opens a dialog box that contains a peak meter.
//   The peak meter displays the peak sample value that plays
//   through the default rendering device.
//-----------------------------------------------------------
int APIENTRY WinMain(HINSTANCE hInstance,
                     HINSTANCE hPrevInstance,
                     LPSTR lpCmdLine,
                     int nCmdShow)
{
    HRESULT hr;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioMeterInformation *pMeterInfo = NULL;

    if (hPrevInstance)
    {
        return 0;
    }

    CoInitialize(NULL);

    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get peak meter for default audio-rendering device.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(__uuidof(IAudioMeterInformation),
                           CLSCTX_ALL, NULL, (void**)&pMeterInfo);
    EXIT_ON_ERROR(hr)

    DialogBoxParam(hInstance, L"PEAKMETER", NULL, (DLGPROC)DlgProc, (LPARAM)pMeterInfo);

Exit:
    if (FAILED(hr))
    {
        MessageBox(NULL, TEXT("This program requires Windows Vista."),
                   TEXT("Error termination"), MB_OK);
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pMeterInfo)
    CoUninitialize();
    return 0;
}

//-----------------------------------------------------------
// DlgProc -- Dialog box procedure
//-----------------------------------------------------------

BOOL CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    static IAudioMeterInformation *pMeterInfo = NULL;
    static HWND hPeakMeter = NULL;
    static float peak = 0;
    HRESULT hr;

    switch (message)
    {
    case WM_INITDIALOG:
        pMeterInfo = (IAudioMeterInformation*)lParam;
        SetTimer(hDlg, ID_TIMER, TIMER_PERIOD, NULL);
        hPeakMeter = GetDlgItem(hDlg, IDC_PEAK_METER);
        return TRUE;

    case WM_COMMAND:
        switch ((int)LOWORD(wParam))
        {
        case IDCANCEL:
            KillTimer(hDlg, ID_TIMER);
            EndDialog(hDlg, TRUE);
            return TRUE;
        }
        break;

    case WM_TIMER:
        switch ((int)wParam)
        {
        case ID_TIMER:
            // Update the peak meter in the dialog box.
            hr = pMeterInfo->GetPeakValue(&peak);
            if (FAILED(hr))
            {
                MessageBox(hDlg, TEXT("The program will exit."),
                           TEXT("Fatal error"), MB_OK);
                KillTimer(hDlg, ID_TIMER);
                EndDialog(hDlg, TRUE);
                return TRUE;
            }
            DrawPeakMeter(hPeakMeter, peak);
            return TRUE;
        }
        break;

    case WM_PAINT:
        // Redraw the peak meter in the dialog box.
        ValidateRect(hPeakMeter, NULL);
        DrawPeakMeter(hPeakMeter, peak);
        break;
    }
    return FALSE;
}

//-----------------------------------------------------------
// DrawPeakMeter -- Draws the peak meter in the dialog box.
//-----------------------------------------------------------

void DrawPeakMeter(HWND hPeakMeter, float peak)
{
    HDC hdc;
    RECT rect;

    GetClientRect(hPeakMeter, &rect);
    hdc = GetDC(hPeakMeter);
    FillRect(hdc, &rect, (HBRUSH)(COLOR_3DSHADOW+1));
    rect.left++;
    rect.top++;
    rect.right = rect.left +
                 max(0, (LONG)(peak*(rect.right-rect.left)-1.5));
    rect.bottom--;
    FillRect(hdc, &rect, (HBRUSH)(COLOR_3DHIGHLIGHT+1));
    ReleaseDC(hPeakMeter, hdc);
}
```



<span data-ttu-id="d0d76-116">В предыдущем примере кода функция [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) вызывает функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для создания экземпляра интерфейса [**иммдевицеенумератор**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) и вызывает метод [**иммдевицеенумератор:: жетдефаултаудиоендпоинт**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) , чтобы получить интерфейс [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) устройства отрисовки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d0d76-116">In the preceding code example, the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, and it calls the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to obtain the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the default rendering device.</span></span> <span data-ttu-id="d0d76-117">**WinMain** вызывает метод [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) для получения интерфейса [**иаудиометеринформатион**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) устройства и открывает диалоговое окно для вывода на экран счетчика пиковой нагрузки для устройства.</span><span class="sxs-lookup"><span data-stu-id="d0d76-117">**WinMain** calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to obtain the device's [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface, and it opens a dialog box to display a peak meter for the device.</span></span> <span data-ttu-id="d0d76-118">Дополнительные сведения о **WinMain** и **CoCreateInstance** см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d0d76-118">For more information about **WinMain** and **CoCreateInstance**, see the Windows SDK documentation.</span></span> <span data-ttu-id="d0d76-119">Дополнительные сведения о **иммдевицеенумератор** и **иммдевице** см. в разделе [перечисление звуковых устройств](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="d0d76-119">For more information about **IMMDeviceEnumerator** and **IMMDevice**, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

<span data-ttu-id="d0d76-120">В предыдущем примере кода функция Длгпрок Отображает счетчик пиковой нагрузки в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="d0d76-120">In the preceding code example, the DlgProc function displays the peak meter in the dialog box.</span></span> <span data-ttu-id="d0d76-121">Во время обработки сообщения WM \_ инитдиалог функция длгпрок вызывает функцию [**сеттимер**](/windows/win32/api/winuser/nf-winuser-settimer) для настройки таймера, который будет создавать \_ сообщения таймера WM через регулярные интервалы времени.</span><span class="sxs-lookup"><span data-stu-id="d0d76-121">During processing of the WM\_INITDIALOG message, DlgProc calls the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function to set up a timer that will generate WM\_TIMER messages at regular time intervals.</span></span> <span data-ttu-id="d0d76-122">Когда Длгпрок получает \_ сообщение таймера WM, он вызывает [**иаудиометеринформатион:: жетпеаквалуе**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-getpeakvalue) , чтобы получить последний пиковый показания счетчика для потока.</span><span class="sxs-lookup"><span data-stu-id="d0d76-122">When DlgProc receives a WM\_TIMER message, it calls [**IAudioMeterInformation::GetPeakValue**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-getpeakvalue) to obtain the latest peak-meter reading for the stream.</span></span> <span data-ttu-id="d0d76-123">Затем Длгпрок вызывает функцию Дравпеакметер для отрисовки обновленного пикового счетчика в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="d0d76-123">DlgProc then calls the DrawPeakMeter function to draw the updated peak meter in the dialog box.</span></span> <span data-ttu-id="d0d76-124">Дополнительные сведения о **сеттимер** и \_ \_ сообщениях таймера WM инитдиалог и WM см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d0d76-124">For more information about **SetTimer** and the WM\_INITDIALOG and WM\_TIMER messages, see the Windows SDK documentation.</span></span>

<span data-ttu-id="d0d76-125">Приведенный выше пример кода можно легко изменить, чтобы отобразить счетчик пиковой загрузки для устройства отслеживания по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d0d76-125">You can easily modify the preceding code example to display a peak meter for the default capture device.</span></span> <span data-ttu-id="d0d76-126">В функции [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) измените значение первого параметра в вызове метода [**Иммдевицеенумератор:: жетдефаултаудиоендпоинт**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) с ерендер на екаптуре.</span><span class="sxs-lookup"><span data-stu-id="d0d76-126">In the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function, change the value of the first parameter in the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) from eRender to eCapture.</span></span>

<span data-ttu-id="d0d76-127">В следующем примере кода показан скрипт ресурсов, определяющий элементы управления, которые отображаются в предыдущем примере кода:</span><span class="sxs-lookup"><span data-stu-id="d0d76-127">The following code example is the resource script that defines the controls that appear in the preceding code example:</span></span>


```C++
// Peakmeter.rc -- Resource script

#include "resource.h"
#include "windows.h"

//
// Dialog
//
PEAKMETER DIALOGEX 0, 0, 150, 34
STYLE DS_MODALFRAME | WS_CAPTION | WS_SYSMENU | DS_SETFONT
CAPTION "Peak Meter"
FONT 8, "Arial Rounded MT Bold", 400, 0, 0x0
BEGIN
    CTEXT      "",IDC_PEAK_METER,34,14,82,5
    LTEXT      "Min",IDC_STATIC_MINVOL,10,12,20,12
    RTEXT      "Max",IDC_STATIC_MAXVOL,120,12,20,12
END
```



<span data-ttu-id="d0d76-128">В следующем примере кода показан файл заголовка ресурса, который определяет идентификаторы элементов управления, которые отображаются в приведенных выше примерах кода.</span><span class="sxs-lookup"><span data-stu-id="d0d76-128">The following code example is the resource header file that defines the control identifiers that appear in the preceding code examples:</span></span>


```C++
// Resource.h -- Control identifiers

#define IDC_STATIC_MINVOL      1001
#define IDC_STATIC_MAXVOL      1002
#define IDC_PEAK_METER         1003
```



## <a name="related-topics"></a><span data-ttu-id="d0d76-129">См. также</span><span class="sxs-lookup"><span data-stu-id="d0d76-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0d76-130">Регуляторы громкости</span><span class="sxs-lookup"><span data-stu-id="d0d76-130">Volume Controls</span></span>](volume-controls.md)
</dt> </dl>

 

 
