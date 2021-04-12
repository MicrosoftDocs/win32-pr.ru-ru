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
# <a name="peak-meters"></a>Пиковые показатели

Для поддержки приложений Windows, отображающих пиковые показатели, [API ендпоинтволуме](endpointvolume-api.md) включает интерфейс [**иаудиометеринформатион**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) . Этот интерфейс представляет пиковое значение счетчика на [устройстве конечной точки звука](audio-endpoint-devices.md). Для устройства отрисовки значение, полученное из счетчика пиковой нагрузки, представляет максимальное значение выборки, обнаруженное в потоке вывода на устройство в течение предыдущего периода отслеживания. Для устройства записи значение, полученное из счетчика пиковой нагрузки, представляет максимальное значение выборки, обнаруженное во входном потоке с устройства.

Значения счетчика пиковой нагрузки, полученные из методов в интерфейсе [**иаудиометеринформатион**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) , являются числами с плавающей запятой в нормализованном диапазоне от 0,0 до 1,0. Например, если поток PCM содержит 16-разрядные примеры, а пиковое значение в течение определенного периода измерения — 8914, то абсолютное значение, записанное счетчиком "Пиковая загрузка", равно 8914, а нормализованное значение пиковой нагрузки, сообщаемое интерфейсом **иаудиометеринформатион** , — 8914/32768 = 0,272.

Если устройство конечной точки звука реализует счетчик пикового использования оборудования, то интерфейс [**иаудиометеринформатион**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) использует счетчик пиковой нагрузки на оборудование. В противном случае интерфейс реализует счетчик пикового использования программного обеспечения.

Если устройство имеет аппаратный счетчик пиковой нагрузки, счетчик пиковой активности активен как в режиме общего доступа, так и в монопольном режиме. Если устройство не имеет счетчика пикового использования оборудования, счетчик пиковой активности активен в общем режиме, но не в монопольном режиме. В монопольном режиме приложение и звуковые данные обмениваются данными напрямую, минуя счетчик пиковой загрузки программного обеспечения (который всегда сообщает пиковое значение 0,0).

Следующий пример кода C++ — это приложение Windows, которое отображает счетчик пиковой загрузки для устройства отрисовки по умолчанию:


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



В предыдущем примере кода функция [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) вызывает функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для создания экземпляра интерфейса [**иммдевицеенумератор**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) и вызывает метод [**иммдевицеенумератор:: жетдефаултаудиоендпоинт**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) , чтобы получить интерфейс [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) устройства отрисовки по умолчанию. **WinMain** вызывает метод [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) для получения интерфейса [**иаудиометеринформатион**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) устройства и открывает диалоговое окно для вывода на экран счетчика пиковой нагрузки для устройства. Дополнительные сведения о **WinMain** и **CoCreateInstance** см. в документации по Windows SDK. Дополнительные сведения о **иммдевицеенумератор** и **иммдевице** см. в разделе [перечисление звуковых устройств](enumerating-audio-devices.md).

В предыдущем примере кода функция Длгпрок Отображает счетчик пиковой нагрузки в диалоговом окне. Во время обработки сообщения WM \_ инитдиалог функция длгпрок вызывает функцию [**сеттимер**](/windows/win32/api/winuser/nf-winuser-settimer) для настройки таймера, который будет создавать \_ сообщения таймера WM через регулярные интервалы времени. Когда Длгпрок получает \_ сообщение таймера WM, он вызывает [**иаудиометеринформатион:: жетпеаквалуе**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-getpeakvalue) , чтобы получить последний пиковый показания счетчика для потока. Затем Длгпрок вызывает функцию Дравпеакметер для отрисовки обновленного пикового счетчика в диалоговом окне. Дополнительные сведения о **сеттимер** и \_ \_ сообщениях таймера WM инитдиалог и WM см. в документации по Windows SDK.

Приведенный выше пример кода можно легко изменить, чтобы отобразить счетчик пиковой загрузки для устройства отслеживания по умолчанию. В функции [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) измените значение первого параметра в вызове метода [**Иммдевицеенумератор:: жетдефаултаудиоендпоинт**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) с ерендер на екаптуре.

В следующем примере кода показан скрипт ресурсов, определяющий элементы управления, которые отображаются в предыдущем примере кода:


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



В следующем примере кода показан файл заголовка ресурса, который определяет идентификаторы элементов управления, которые отображаются в приведенных выше примерах кода.


```C++
// Resource.h -- Control identifiers

#define IDC_STATIC_MINVOL      1001
#define IDC_STATIC_MAXVOL      1002
#define IDC_PEAK_METER         1003
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Регуляторы громкости](volume-controls.md)
</dt> </dl>

 

 
