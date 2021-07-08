---
description: Элементы управления томами конечных точек
ms.assetid: 667c3659-69ae-469d-9ae0-e32a189cbc71
title: Элементы управления томами конечных точек
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57be477a86a1de4584a7590d20d4e0199e782f10
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481889"
---
# <a name="endpoint-volume-controls"></a>Элементы управления томами конечных точек

Интерфейсы [**исимплеаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**ичаннелаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)и [**иаудиостреамволуме**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) позволяют клиентам управлять уровнями громкости [звуковых сеансов](audio-sessions.md), которые являются коллекциями звуковых потоков общего режима. Эти интерфейсы не работают с звуковыми потоками в монопольном режиме.

Приложения, управляющие потоками с монопольным режимом, могут управлять уровнями громкости этих потоков через интерфейс [**иаудиоендпоинтволуме**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) . Этот интерфейс управляет уровнем громкости [устройства конечной точки аудио](audio-endpoint-devices.md). Он использует аппаратный регулятор громкости для устройства конечной точки, если аудио оборудование реализует такой элемент управления. В противном случае интерфейс **иаудиоендпоинтволуме** реализует регулятор громкости в программном обеспечении.

Если устройство имеет аппаратный регулятор громкости, изменения, вносимые в элемент управления через интерфейс [**иаудиоендпоинтволуме**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) , влияют на уровень громкости как в общем, так и в монопольном режиме. Если устройство не имеет аппаратного тома и не имеет элементов управления, изменения, внесенные в программный том и отключения элементов управления через этот интерфейс, влияют на уровень громкости в общем режиме, но не в монопольном режиме. В монопольном режиме приложения и аудио оборудование обмениваются данными напрямую, минуя элементы управления программного обеспечения.

Как правило, приложения должны избегать использования интерфейса [**иаудиоендпоинтволуме**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) для управления уровнями громкости потоков в общем режиме. Вместо этого для этой цели приложения должны использовать интерфейс [**исимплеаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**ичаннелаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)или [**иаудиостреамволуме**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) .

Если приложение отображает регулятор громкости, использующий интерфейс [**иаудиоендпоинтволуме**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) для управления уровнем громкости устройства конечной точки аудио, этот элемент управления "Громкость" должен отображать элемент управления громкостью конечной точки, который отображается программой системного управления громкостью, сндвол. Как упоминалось ранее, элемент управления "том конечной точки" отображается в левой части окна Сндвол в поле Группа с меткой **устройство**. Если пользователь изменяет том конечной точки устройства с помощью элемента управления "Громкость" в Сндвол, соответствующий элемент управления "том конечной точки" в приложении должен перемещаться в одновременном с помощью элемента управления в Сндвол. Аналогичным образом, если пользователь изменяет уровень громкости с помощью элемента управления громкостью конечной точки в окне приложения, соответствующий элемент управления громкостью в Сндвол должен перемещаться в одновременном с помощью элемента управления громкостью приложения.

Чтобы элемент управления громкостью конечной точки в окне приложения отображал элемент управления громкостью конечной точки в Сндвол, приложение должно реализовать интерфейс [**иаудиоендпоинтволумекаллбакк**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) и зарегистрировать этот интерфейс для получения уведомлений. Затем каждый раз, когда пользователь изменяет уровень громкости конечной точки в Сндвол, приложение получает вызов уведомления через его метод [**иаудиоендпоинтволумекаллбакк:: OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) . Во время этого вызова метод **OnNotify** может обновить элемент управления громкостью конечной точки в окне приложения в соответствии с параметром управления, показанным в сндвол. Аналогичным образом каждый раз, когда пользователь изменяет уровень тома конечной точки с помощью регулятора громкости в окне приложения, Сндвол получает уведомление и немедленно обновляет элемент управления громкостью конечной точки для просмотра нового уровня громкости.

Следующий пример кода представляет собой файл заголовка, в котором показана возможная реализация интерфейса [**иаудиоендпоинтволумекаллбакк**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) :


```C++
// Epvolume.h -- Implementation of IAudioEndpointVolumeCallback interface

#include <windows.h>
#include <commctrl.h>
#include <mmdeviceapi.h>
#include <endpointvolume.h>
#include "resource.h"

// Dialog handle from dialog box procedure
extern HWND g_hDlg;

// Client's proprietary event-context GUID
extern GUID g_guidMyContext;

// Maximum volume level on trackbar
#define MAX_VOL  100

#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

//-----------------------------------------------------------
// Client implementation of IAudioEndpointVolumeCallback
// interface. When a method in the IAudioEndpointVolume
// interface changes the volume level or muting state of the
// endpoint device, the change initiates a call to the
// client's IAudioEndpointVolumeCallback::OnNotify method.
//-----------------------------------------------------------
class CAudioEndpointVolumeCallback : public IAudioEndpointVolumeCallback
{
    LONG _cRef;

public:
    CAudioEndpointVolumeCallback() :
        _cRef(1)
    {
    }

    ~CAudioEndpointVolumeCallback()
    {
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid, VOID **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IAudioEndpointVolumeCallback) == riid)
        {
            AddRef();
            *ppvInterface = (IAudioEndpointVolumeCallback*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Callback method for endpoint-volume-change notifications.

    HRESULT STDMETHODCALLTYPE OnNotify(PAUDIO_VOLUME_NOTIFICATION_DATA pNotify)
    {
        if (pNotify == NULL)
        {
            return E_INVALIDARG;
        }
        if (g_hDlg != NULL && pNotify->guidEventContext != g_guidMyContext)
        {
            PostMessage(GetDlgItem(g_hDlg, IDC_CHECK_MUTE), BM_SETCHECK,
                        (pNotify->bMuted) ? BST_CHECKED : BST_UNCHECKED, 0);

            PostMessage(GetDlgItem(g_hDlg, IDC_SLIDER_VOLUME),
                        TBM_SETPOS, TRUE,
                        LPARAM((UINT32)(MAX_VOL*pNotify->fMasterVolume + 0.5)));
        }
        return S_OK;
    }
};
```



Класс Каудиоендпоинтволумекаллбакк в предыдущем примере кода является реализацией интерфейса [**иаудиоендпоинтволумекаллбакк**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) . Поскольку **иаудиоендпоинтволумекаллбакк** наследует от [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), определение класса содержит реализации методов **IUnknown** , [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)и [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Метод [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) в определении класса вызывается каждый раз, когда один из следующих методов изменяет уровень громкости конечной точки:

-   [**Иаудиоендпоинтволуме:: Сетчаннелволумелевел**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [**Иаудиоендпоинтволуме:: Сетчаннелволумелевелскалар**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [**Иаудиоендпоинтволуме:: Сетмастерволумелевел**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)
-   [**Иаудиоендпоинтволуме:: Сетмастерволумелевелскалар**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [**Иаудиоендпоинтволуме:: Сетмуте**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)
-   [**Иаудиоендпоинтволуме:: Волуместепдовн**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [**Иаудиоендпоинтволуме:: Волуместепуп**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

Реализация метода [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) в предыдущем примере кода отправляет сообщения в элемент управления "Громкость" в окне приложения, чтобы обновить отображаемый уровень громкости.

Приложение вызывает метод [**иаудиоендпоинтволуме:: регистерконтролчанженотифи**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) , чтобы зарегистрировать его интерфейс [**иаудиоендпоинтволумекаллбакк**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) для получения уведомлений. Если приложение больше не требует уведомлений, оно вызывает метод [**иаудиоендпоинтволуме:: унрегистерконтролчанженотифи**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) для удаления регистрации.

следующий пример кода является Windows приложением, которое вызывает методы [**регистерконтролчанженотифи**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) и [**унрегистерконтролчанженотифи**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) для регистрации и отмены регистрации класса каудиоендпоинтволумекаллбакк в предыдущем примере кода:


```C++
// Epvolume.cpp -- WinMain and dialog box functions

#include "stdafx.h"
#include "Epvolume.h"

HWND g_hDlg = NULL;
GUID g_guidMyContext = GUID_NULL;

static IAudioEndpointVolume *g_pEndptVol = NULL;
static BOOL CALLBACK DlgProc(HWND, UINT, WPARAM, LPARAM);

#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define ERROR_CANCEL(hr)  \
              if (FAILED(hr)) {  \
                  MessageBox(hDlg, TEXT("The program will exit."),  \
                             TEXT("Fatal error"), MB_OK);  \
                  EndDialog(hDlg, TRUE); return TRUE; }

//-----------------------------------------------------------
// WinMain -- Registers an IAudioEndpointVolumeCallback
//   interface to monitor endpoint volume level, and opens
//   a dialog box that displays a volume control that will
//   mirror the endpoint volume control in SndVol.
//-----------------------------------------------------------
int APIENTRY WinMain(HINSTANCE hInstance,
                     HINSTANCE hPrevInstance,
                     LPSTR lpCmdLine,
                     int nCmdShow)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    CAudioEndpointVolumeCallback EPVolEvents;

    if (hPrevInstance)
    {
        return 0;
    }

    CoInitialize(NULL);

    hr = CoCreateGuid(&g_guidMyContext);
    EXIT_ON_ERROR(hr)

    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get default audio-rendering device.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(__uuidof(IAudioEndpointVolume),
                           CLSCTX_ALL, NULL, (void**)&g_pEndptVol);
    EXIT_ON_ERROR(hr)

    hr = g_pEndptVol->RegisterControlChangeNotify(
                     (IAudioEndpointVolumeCallback*)&EPVolEvents);
    EXIT_ON_ERROR(hr)

    InitCommonControls();
    DialogBox(hInstance, L"VOLUMECONTROL", NULL, (DLGPROC)DlgProc);

Exit:
    if (FAILED(hr))
    {
        MessageBox(NULL, TEXT("This program requires Windows Vista."),
                   TEXT("Error termination"), MB_OK);
    }
    if (g_pEndptVol != NULL)
    {
        g_pEndptVol->UnregisterControlChangeNotify(
                    (IAudioEndpointVolumeCallback*)&EPVolEvents);
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(g_pEndptVol)
    CoUninitialize();
    return 0;
}

//-----------------------------------------------------------
// DlgProc -- Dialog box procedure
//-----------------------------------------------------------

BOOL CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    HRESULT hr;
    BOOL bMute;
    float fVolume;
    int nVolume;
    int nChecked;

    switch (message)
    {
    case WM_INITDIALOG:
        g_hDlg = hDlg;
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETRANGEMIN, FALSE, 0);
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETRANGEMAX, FALSE, MAX_VOL);
        hr = g_pEndptVol->GetMute(&bMute);
        ERROR_CANCEL(hr)
        SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_SETCHECK,
                           bMute ? BST_CHECKED : BST_UNCHECKED, 0);
        hr = g_pEndptVol->GetMasterVolumeLevelScalar(&fVolume);
        ERROR_CANCEL(hr)
        nVolume = (int)(MAX_VOL*fVolume + 0.5);
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETPOS, TRUE, nVolume);
        return TRUE;

    case WM_HSCROLL:
        switch (LOWORD(wParam))
        {
        case SB_THUMBPOSITION:
        case SB_THUMBTRACK:
        case SB_LINERIGHT:
        case SB_LINELEFT:
        case SB_PAGERIGHT:
        case SB_PAGELEFT:
        case SB_RIGHT:
        case SB_LEFT:
            // The user moved the volume slider in the dialog box.
            SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_SETCHECK, BST_UNCHECKED, 0);
            hr = g_pEndptVol->SetMute(FALSE, &g_guidMyContext);
            ERROR_CANCEL(hr)
            nVolume = SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_GETPOS, 0, 0);
            fVolume = (float)nVolume/MAX_VOL;
            hr = g_pEndptVol->SetMasterVolumeLevelScalar(fVolume, &g_guidMyContext);
            ERROR_CANCEL(hr)
            return TRUE;
        }
        break;

    case WM_COMMAND:
        switch ((int)LOWORD(wParam))
        {
        case IDC_CHECK_MUTE:
            // The user selected the Mute check box in the dialog box.
            nChecked = SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_GETCHECK, 0, 0);
            bMute = (BST_CHECKED == nChecked);
            hr = g_pEndptVol->SetMute(bMute, &g_guidMyContext);
            ERROR_CANCEL(hr)
            return TRUE;
        case IDCANCEL:
            EndDialog(hDlg, TRUE);
            return TRUE;
        }
        break;
    }
    return FALSE;
}
```



В предыдущем примере кода функция [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) вызывает функцию [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) для создания экземпляра интерфейса [**иммдевицеенумератор**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) и вызывает метод [**иммдевицеенумератор:: жетдефаултаудиоендпоинт**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) , чтобы получить интерфейс [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) устройства отрисовки по умолчанию. **WinMain** вызывает метод [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) для получения интерфейса [**иаудиоендпоинтволуме**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) устройства и вызывает [**регистерконтролчанженотифи**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) , чтобы зарегистрировать приложение для получения уведомлений об изменениях в томах конечных точек. Затем **WinMain** открывает диалоговое окно для вывода на устройство элемента управления "том". В диалоговом окне также отображается флажок, указывающий, отключено ли устройство. Флажок "контроль громкости конечных точек и звук в диалоговом окне" отражает настройки флажка "Управление томами конечных точек" и "выключить", отображаемого Сндвол. дополнительные сведения о **WinMain** и **cocreateinstance** см. в документации по Windows SDK. Дополнительные сведения о **иммдевицеенумератор** и **иммдевице** см. в разделе [перечисление звуковых устройств](enumerating-audio-devices.md).

Процедура диалогового окна, Длгпрок, в предыдущем примере кода, обрабатывает изменения, внесенные пользователем в том, и выключает параметры с помощью элементов управления в диалоговом окне. Когда Длгпрок вызывает [**сетмастерволумелевелскалар**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) или [**сетмуте**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute), сндвол получает уведомление об изменении и обновляет соответствующий элемент управления в своем окне, чтобы отразить новый том или выключить параметр. Если вместо использования диалогового окна пользователь обновляет том и выключает параметры с помощью элементов управления в окне Сндвол, метод [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) в классе каудиоендпоинтволумекаллбакк обновляет элементы управления в диалоговом окне для вывода новых параметров.

Если пользователь изменяет том с помощью элементов управления в диалоговом окне, метод [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) в классе каудиоендпоинтволумекаллбакк не отправляет сообщения для обновления элементов управления в диалоговом окне. Это может быть избыточным. **OnNotify** обновляет элементы управления в диалоговом окне только в том случае, если изменение тома произошло в сндвол или в другом приложении. Второй параметр в вызовах метода [**сетмастерволумелевелскалар**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) и [**Сетмуте**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) в функции длгпрок — это указатель на идентификатор GUID контекста события, который либо метод передает в **OnNotify**. **OnNotify** проверяет значение GUID контекста события, чтобы определить, является ли диалоговое окно источником изменения тома. Дополнительные сведения об идентификаторах GUID контекста событий см. в разделе **иаудиоендпоинтволумекаллбакк:: OnNotify**.

Когда пользователь выходит из диалогового окна, вызов [**унрегистерконтролчанженотифи**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) в предыдущем примере кода удаляет регистрацию класса каудиоендпоинтволумекаллбакк перед завершением программы.

Приведенный выше пример кода можно легко изменить, чтобы отобразить громкость и отключить элементы управления для устройства записи по умолчанию. В функции [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) измените значение первого параметра в вызове метода [**Иммдевицеенумератор:: жетдефаултаудиоендпоинт**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) из ерендер в екаптуре.

В следующем примере кода показан скрипт ресурсов, который определяет том и выключает элементы управления, отображаемые в предыдущем примере кода:


```C++
// Epvolume.rc -- Resource script

#include "resource.h"
#include "windows.h"
#include "commctrl.h"

//
// Dialog box
//
VOLUMECONTROL DIALOGEX 0, 0, 160, 60
STYLE DS_MODALFRAME | WS_CAPTION | WS_SYSMENU | DS_SETFONT
CAPTION "Audio Endpoint Volume"
FONT 8, "Arial Rounded MT Bold", 400, 0, 0x0
BEGIN
    LTEXT      "Min",IDC_STATIC_MINVOL,10,10,20,12
    RTEXT      "Max",IDC_STATIC_MAXVOL,130,10,20,12
    CONTROL    "",IDC_SLIDER_VOLUME,"msctls_trackbar32",
               TBS_BOTH | TBS_NOTICKS | WS_TABSTOP,10,20,140,12
    CONTROL    "Mute",IDC_CHECK_MUTE,"Button",
               BS_AUTOCHECKBOX | WS_TABSTOP,20,40,70,12
END
```



В следующем примере кода показан файл заголовка ресурса, который определяет идентификаторы элементов управления, которые отображаются в приведенных выше примерах кода.


```C++
// Resource.h -- Control identifiers (epvolume)

#define IDC_SLIDER_VOLUME      1001
#define IDC_CHECK_MUTE         1002
#define IDC_STATIC_MINVOL      1003
#define IDC_STATIC_MAXVOL      1004
```



Приведенные выше примеры кода образуют простое приложение для управления и наблюдения за томом конечной точки устройства отрисовки по умолчанию. Более полезное приложение может дополнительно уведомлять пользователя об изменении состояния устройства. Например, устройство может быть отключено, отсоединено или удалено. Дополнительные сведения о мониторинге этих типов событий см. в разделе [события устройства](device-events.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Регуляторы громкости](volume-controls.md)
</dt> </dl>

 

 
