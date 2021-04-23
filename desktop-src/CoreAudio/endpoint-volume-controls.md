---
description: Элементы управления томами конечных точек
ms.assetid: 667c3659-69ae-469d-9ae0-e32a189cbc71
title: Элементы управления томами конечных точек
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526403be9c600f67791650956bd7e5096f6c9afc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990615"
---
# <a name="endpoint-volume-controls"></a><span data-ttu-id="3c4c8-103">Элементы управления томами конечных точек</span><span class="sxs-lookup"><span data-stu-id="3c4c8-103">Endpoint Volume Controls</span></span>

<span data-ttu-id="3c4c8-104">Интерфейсы [**исимплеаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**ичаннелаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)и [**иаудиостреамволуме**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) позволяют клиентам управлять уровнями громкости [звуковых сеансов](audio-sessions.md), которые являются коллекциями звуковых потоков общего режима.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-104">The [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), and [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interfaces enable clients to control the volume levels of [audio sessions](audio-sessions.md), which are collections of shared-mode audio streams.</span></span> <span data-ttu-id="3c4c8-105">Эти интерфейсы не работают с звуковыми потоками в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-105">These interfaces do not work with exclusive-mode audio streams.</span></span>

<span data-ttu-id="3c4c8-106">Приложения, управляющие потоками с монопольным режимом, могут управлять уровнями громкости этих потоков через интерфейс [**иаудиоендпоинтволуме**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) .</span><span class="sxs-lookup"><span data-stu-id="3c4c8-106">Applications that manage exclusive-mode streams can control the volume levels of those streams through the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface.</span></span> <span data-ttu-id="3c4c8-107">Этот интерфейс управляет уровнем громкости [устройства конечной точки аудио](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="3c4c8-107">This interface controls the volume level of the [audio endpoint device](audio-endpoint-devices.md).</span></span> <span data-ttu-id="3c4c8-108">Он использует аппаратный регулятор громкости для устройства конечной точки, если аудио оборудование реализует такой элемент управления.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-108">It uses the hardware volume control for the endpoint device if the audio hardware implements such a control.</span></span> <span data-ttu-id="3c4c8-109">В противном случае интерфейс **иаудиоендпоинтволуме** реализует регулятор громкости в программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-109">Otherwise, the **IAudioEndpointVolume** interface implements the volume control in software.</span></span>

<span data-ttu-id="3c4c8-110">Если устройство имеет аппаратный регулятор громкости, изменения, вносимые в элемент управления через интерфейс [**иаудиоендпоинтволуме**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) , влияют на уровень громкости как в общем, так и в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-110">If a device has a hardware volume control, changes made to the control through the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface affect the volume level both in shared mode and in exclusive mode.</span></span> <span data-ttu-id="3c4c8-111">Если устройство не имеет аппаратного тома и не имеет элементов управления, изменения, внесенные в программный том и отключения элементов управления через этот интерфейс, влияют на уровень громкости в общем режиме, но не в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-111">If a device lacks hardware volume and mute controls, changes made to the software volume and mute controls through this interface affect the volume level in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="3c4c8-112">В монопольном режиме приложения и аудио оборудование обмениваются данными напрямую, минуя элементы управления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-112">In exclusive mode, the application and the audio hardware exchange audio data directly, bypassing the software controls.</span></span>

<span data-ttu-id="3c4c8-113">Как правило, приложения должны избегать использования интерфейса [**иаудиоендпоинтволуме**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) для управления уровнями громкости потоков в общем режиме.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-113">As a general rule, applications should avoid using the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface to control the volume levels of shared-mode streams.</span></span> <span data-ttu-id="3c4c8-114">Вместо этого для этой цели приложения должны использовать интерфейс [**исимплеаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**ичаннелаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)или [**иаудиостреамволуме**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) .</span><span class="sxs-lookup"><span data-stu-id="3c4c8-114">Instead, applications should use the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), or [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interface for that purpose.</span></span>

<span data-ttu-id="3c4c8-115">Если приложение отображает регулятор громкости, использующий интерфейс [**иаудиоендпоинтволуме**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) для управления уровнем громкости устройства конечной точки аудио, этот элемент управления "Громкость" должен отображать элемент управления громкостью конечной точки, который отображается программой системного управления громкостью, сндвол.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-115">If an application displays a volume control that uses the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface to control the volume level of an audio endpoint device, that volume control should mirror the endpoint volume control displayed by the system volume-control program, Sndvol.</span></span> <span data-ttu-id="3c4c8-116">Как упоминалось ранее, элемент управления "том конечной точки" отображается в левой части окна Сндвол в поле Группа с меткой **устройство**.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-116">As explained previously, the endpoint volume control appears on the left side of the Sndvol window, in the group box labeled **Device**.</span></span> <span data-ttu-id="3c4c8-117">Если пользователь изменяет том конечной точки устройства с помощью элемента управления "Громкость" в Сндвол, соответствующий элемент управления "том конечной точки" в приложении должен перемещаться в одновременном с помощью элемента управления в Сндвол.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-117">If the user changes the endpoint volume of a device through the volume control in Sndvol, the corresponding endpoint volume control in the application should move in unison with the control in Sndvol.</span></span> <span data-ttu-id="3c4c8-118">Аналогичным образом, если пользователь изменяет уровень громкости с помощью элемента управления громкостью конечной точки в окне приложения, соответствующий элемент управления громкостью в Сндвол должен перемещаться в одновременном с помощью элемента управления громкостью приложения.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-118">Similarly, if the user changes the volume level through the endpoint volume control in the application window, the corresponding volume control in Sndvol should move in unison with the application's volume control.</span></span>

<span data-ttu-id="3c4c8-119">Чтобы элемент управления громкостью конечной точки в окне приложения отображал элемент управления громкостью конечной точки в Сндвол, приложение должно реализовать интерфейс [**иаудиоендпоинтволумекаллбакк**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) и зарегистрировать этот интерфейс для получения уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-119">To ensure that the endpoint volume control in an application window mirrors the endpoint volume control in Sndvol, the application should implement an [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface and register that interface to receive notifications.</span></span> <span data-ttu-id="3c4c8-120">Затем каждый раз, когда пользователь изменяет уровень громкости конечной точки в Сндвол, приложение получает вызов уведомления через его метод [**иаудиоендпоинтволумекаллбакк:: OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) .</span><span class="sxs-lookup"><span data-stu-id="3c4c8-120">Thereafter, each time the user changes the endpoint volume level in Sndvol, the application receives a notification call through its [**IAudioEndpointVolumeCallback::OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method.</span></span> <span data-ttu-id="3c4c8-121">Во время этого вызова метод **OnNotify** может обновить элемент управления громкостью конечной точки в окне приложения в соответствии с параметром управления, показанным в сндвол.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-121">During this call, the **OnNotify** method can update the endpoint volume control in the application window to match the control setting shown in Sndvol.</span></span> <span data-ttu-id="3c4c8-122">Аналогичным образом каждый раз, когда пользователь изменяет уровень тома конечной точки с помощью регулятора громкости в окне приложения, Сндвол получает уведомление и немедленно обновляет элемент управления громкостью конечной точки для просмотра нового уровня громкости.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-122">Similarly, each time the user changes the endpoint volume level through volume control in the application window, Sndvol receives a notification and immediately updates its endpoint volume control to display the new volume level.</span></span>

<span data-ttu-id="3c4c8-123">Следующий пример кода представляет собой файл заголовка, в котором показана возможная реализация интерфейса [**иаудиоендпоинтволумекаллбакк**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) :</span><span class="sxs-lookup"><span data-stu-id="3c4c8-123">The following code example is a header file that shows a possible implementation of the [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface:</span></span>


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



<span data-ttu-id="3c4c8-124">Класс Каудиоендпоинтволумекаллбакк в предыдущем примере кода является реализацией интерфейса [**иаудиоендпоинтволумекаллбакк**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) .</span><span class="sxs-lookup"><span data-stu-id="3c4c8-124">The CAudioEndpointVolumeCallback class in the preceding code example is an implementation of the [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface.</span></span> <span data-ttu-id="3c4c8-125">Поскольку **иаудиоендпоинтволумекаллбакк** наследует от [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), определение класса содержит реализации методов **IUnknown** , [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)и [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="3c4c8-125">Because **IAudioEndpointVolumeCallback** inherits from [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), the class definition contains implementations of the **IUnknown** methods [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="3c4c8-126">Метод [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) в определении класса вызывается каждый раз, когда один из следующих методов изменяет уровень громкости конечной точки:</span><span class="sxs-lookup"><span data-stu-id="3c4c8-126">The [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the class definition is called each time one of the following methods changes the endpoint volume level:</span></span>

-   [<span data-ttu-id="3c4c8-127">**Иаудиоендпоинтволуме:: Сетчаннелволумелевел**</span><span class="sxs-lookup"><span data-stu-id="3c4c8-127">**IAudioEndpointVolume::SetChannelVolumeLevel**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [<span data-ttu-id="3c4c8-128">**Иаудиоендпоинтволуме:: Сетчаннелволумелевелскалар**</span><span class="sxs-lookup"><span data-stu-id="3c4c8-128">**IAudioEndpointVolume::SetChannelVolumeLevelScalar**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [<span data-ttu-id="3c4c8-129">**Иаудиоендпоинтволуме:: Сетмастерволумелевел**</span><span class="sxs-lookup"><span data-stu-id="3c4c8-129">**IAudioEndpointVolume::SetMasterVolumeLevel**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)
-   [<span data-ttu-id="3c4c8-130">**Иаудиоендпоинтволуме:: Сетмастерволумелевелскалар**</span><span class="sxs-lookup"><span data-stu-id="3c4c8-130">**IAudioEndpointVolume::SetMasterVolumeLevelScalar**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [<span data-ttu-id="3c4c8-131">**Иаудиоендпоинтволуме:: Сетмуте**</span><span class="sxs-lookup"><span data-stu-id="3c4c8-131">**IAudioEndpointVolume::SetMute**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)
-   [<span data-ttu-id="3c4c8-132">**Иаудиоендпоинтволуме:: Волуместепдовн**</span><span class="sxs-lookup"><span data-stu-id="3c4c8-132">**IAudioEndpointVolume::VolumeStepDown**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [<span data-ttu-id="3c4c8-133">**Иаудиоендпоинтволуме:: Волуместепуп**</span><span class="sxs-lookup"><span data-stu-id="3c4c8-133">**IAudioEndpointVolume::VolumeStepUp**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

<span data-ttu-id="3c4c8-134">Реализация метода [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) в предыдущем примере кода отправляет сообщения в элемент управления "Громкость" в окне приложения, чтобы обновить отображаемый уровень громкости.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-134">The implementation of the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the preceding code example sends messages to the volume control in the application window to update the displayed volume level.</span></span>

<span data-ttu-id="3c4c8-135">Приложение вызывает метод [**иаудиоендпоинтволуме:: регистерконтролчанженотифи**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) , чтобы зарегистрировать его интерфейс [**иаудиоендпоинтволумекаллбакк**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) для получения уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-135">An application calls the [**IAudioEndpointVolume::RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) method to register its [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface to receive notifications.</span></span> <span data-ttu-id="3c4c8-136">Если приложение больше не требует уведомлений, оно вызывает метод [**иаудиоендпоинтволуме:: унрегистерконтролчанженотифи**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) для удаления регистрации.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-136">When the application no longer requires notifications, it calls the [**IAudioEndpointVolume::UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) method to delete the registration.</span></span>

<span data-ttu-id="3c4c8-137">В следующем примере кода представлено приложение Windows, которое вызывает методы [**регистерконтролчанженотифи**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) и [**унрегистерконтролчанженотифи**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) для регистрации и отмены регистрации класса каудиоендпоинтволумекаллбакк в предыдущем примере кода:</span><span class="sxs-lookup"><span data-stu-id="3c4c8-137">The following code example is a Windows application that calls the [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) and [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) methods to register and unregister the CAudioEndpointVolumeCallback class in the preceding code example:</span></span>


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
    if (pEnumerator != NULL)
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



<span data-ttu-id="3c4c8-138">В предыдущем примере кода функция [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) вызывает функцию [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) для создания экземпляра интерфейса [**иммдевицеенумератор**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) и вызывает метод [**иммдевицеенумератор:: жетдефаултаудиоендпоинт**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) , чтобы получить интерфейс [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) устройства отрисовки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-138">In the preceding code example, the [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, and it calls the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to obtain the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the default rendering device.</span></span> <span data-ttu-id="3c4c8-139">**WinMain** вызывает метод [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) для получения интерфейса [**иаудиоендпоинтволуме**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) устройства и вызывает [**регистерконтролчанженотифи**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) , чтобы зарегистрировать приложение для получения уведомлений об изменениях в томах конечных точек.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-139">**WinMain** calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to obtain the device's [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface, and it calls [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) to register the application to receive notifications of endpoint volume changes.</span></span> <span data-ttu-id="3c4c8-140">Затем **WinMain** открывает диалоговое окно для вывода на устройство элемента управления "том".</span><span class="sxs-lookup"><span data-stu-id="3c4c8-140">Next, **WinMain** opens a dialog box to display an endpoint volume control for the device.</span></span> <span data-ttu-id="3c4c8-141">В диалоговом окне также отображается флажок, указывающий, отключено ли устройство.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-141">The dialog box also displays a check box that indicates whether the device is muted.</span></span> <span data-ttu-id="3c4c8-142">Флажок "контроль громкости конечных точек и звук в диалоговом окне" отражает настройки флажка "Управление томами конечных точек" и "выключить", отображаемого Сндвол.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-142">The endpoint volume control and mute check box in the dialog box mirror the settings of the endpoint volume control and mute check box displayed by Sndvol.</span></span> <span data-ttu-id="3c4c8-143">Дополнительные сведения о **WinMain** и **CoCreateInstance** см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-143">For more information about **WinMain** and **CoCreateInstance**, see the Windows SDK documentation.</span></span> <span data-ttu-id="3c4c8-144">Дополнительные сведения о **иммдевицеенумератор** и **иммдевице** см. в разделе [перечисление звуковых устройств](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="3c4c8-144">For more information about **IMMDeviceEnumerator** and **IMMDevice**, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

<span data-ttu-id="3c4c8-145">Процедура диалогового окна, Длгпрок, в предыдущем примере кода, обрабатывает изменения, внесенные пользователем в том, и выключает параметры с помощью элементов управления в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-145">The dialog box procedure, DlgProc, in the preceding code example, handles the changes that the user makes to the volume and mute settings through the controls in the dialog box.</span></span> <span data-ttu-id="3c4c8-146">Когда Длгпрок вызывает [**сетмастерволумелевелскалар**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) или [**сетмуте**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute), сндвол получает уведомление об изменении и обновляет соответствующий элемент управления в своем окне, чтобы отразить новый том или выключить параметр.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-146">When DlgProc calls [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) or [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute), Sndvol receives notification of the change and updates the corresponding control in its window to reflect the new volume or mute setting.</span></span> <span data-ttu-id="3c4c8-147">Если вместо использования диалогового окна пользователь обновляет том и выключает параметры с помощью элементов управления в окне Сндвол, метод [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) в классе каудиоендпоинтволумекаллбакк обновляет элементы управления в диалоговом окне для вывода новых параметров.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-147">If, instead of using the dialog box, the user updates the volume and mute settings through the controls in the Sndvol window, the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the CAudioEndpointVolumeCallback class updates the controls in the dialog box to display the new settings.</span></span>

<span data-ttu-id="3c4c8-148">Если пользователь изменяет том с помощью элементов управления в диалоговом окне, метод [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) в классе каудиоендпоинтволумекаллбакк не отправляет сообщения для обновления элементов управления в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-148">If the user changes the volume through the controls in the dialog box, the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the CAudioEndpointVolumeCallback class does not send messages to update the controls in the dialog box.</span></span> <span data-ttu-id="3c4c8-149">Это может быть избыточным.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-149">To do so would be redundant.</span></span> <span data-ttu-id="3c4c8-150">**OnNotify** обновляет элементы управления в диалоговом окне только в том случае, если изменение тома произошло в сндвол или в другом приложении.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-150">**OnNotify** updates the controls in the dialog box only if the volume change originated in Sndvol or in some other application.</span></span> <span data-ttu-id="3c4c8-151">Второй параметр в вызовах метода [**сетмастерволумелевелскалар**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) и [**Сетмуте**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) в функции длгпрок — это указатель на идентификатор GUID контекста события, который либо метод передает в **OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-151">The second parameter in the [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) and [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) method calls in the DlgProc function is a pointer to an event-context GUID that either method passes to **OnNotify**.</span></span> <span data-ttu-id="3c4c8-152">**OnNotify** проверяет значение GUID контекста события, чтобы определить, является ли диалоговое окно источником изменения тома.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-152">**OnNotify** checks the value of the event-context GUID to determine whether the dialog box is the source of the volume change.</span></span> <span data-ttu-id="3c4c8-153">Дополнительные сведения об идентификаторах GUID контекста событий см. в разделе **иаудиоендпоинтволумекаллбакк:: OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-153">For more information about event-context GUIDs, see **IAudioEndpointVolumeCallback::OnNotify**.</span></span>

<span data-ttu-id="3c4c8-154">Когда пользователь выходит из диалогового окна, вызов [**унрегистерконтролчанженотифи**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) в предыдущем примере кода удаляет регистрацию класса каудиоендпоинтволумекаллбакк перед завершением программы.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-154">When the user exits the dialog box, the [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) call in the preceding code example deletes the registration of the CAudioEndpointVolumeCallback class before the program terminates.</span></span>

<span data-ttu-id="3c4c8-155">Приведенный выше пример кода можно легко изменить, чтобы отобразить громкость и отключить элементы управления для устройства записи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-155">You can easily modify the preceding code example to display volume and mute controls for the default capture device.</span></span> <span data-ttu-id="3c4c8-156">В функции [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) измените значение первого параметра в вызове метода [**Иммдевицеенумератор:: жетдефаултаудиоендпоинт**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) из ерендер в екаптуре.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-156">In the [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function, change the value of the first parameter in the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method from eRender to eCapture.</span></span>

<span data-ttu-id="3c4c8-157">В следующем примере кода показан скрипт ресурсов, который определяет том и выключает элементы управления, отображаемые в предыдущем примере кода:</span><span class="sxs-lookup"><span data-stu-id="3c4c8-157">The following code example is the resource script that defines the volume and mute controls that appear in the preceding code example:</span></span>


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



<span data-ttu-id="3c4c8-158">В следующем примере кода показан файл заголовка ресурса, который определяет идентификаторы элементов управления, которые отображаются в приведенных выше примерах кода.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-158">The following code example is the resource header file that defines the control identifiers that appear in the preceding code examples:</span></span>


```C++
// Resource.h -- Control identifiers (epvolume)

#define IDC_SLIDER_VOLUME      1001
#define IDC_CHECK_MUTE         1002
#define IDC_STATIC_MINVOL      1003
#define IDC_STATIC_MAXVOL      1004
```



<span data-ttu-id="3c4c8-159">Приведенные выше примеры кода образуют простое приложение для управления и наблюдения за томом конечной точки устройства отрисовки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-159">The preceding code examples combine to form a simple application for controlling and monitoring the endpoint volume of the default rendering device.</span></span> <span data-ttu-id="3c4c8-160">Более полезное приложение может дополнительно уведомлять пользователя об изменении состояния устройства.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-160">A more useful application might additionally notify the user when the status of the device changes.</span></span> <span data-ttu-id="3c4c8-161">Например, устройство может быть отключено, отсоединено или удалено.</span><span class="sxs-lookup"><span data-stu-id="3c4c8-161">For example, the device might be disabled, unplugged, or removed.</span></span> <span data-ttu-id="3c4c8-162">Дополнительные сведения о мониторинге этих типов событий см. в разделе [события устройства](device-events.md).</span><span class="sxs-lookup"><span data-stu-id="3c4c8-162">For more information about monitoring these types of events, see [Device Events](device-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c4c8-163">См. также</span><span class="sxs-lookup"><span data-stu-id="3c4c8-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c4c8-164">Регуляторы громкости</span><span class="sxs-lookup"><span data-stu-id="3c4c8-164">Volume Controls</span></span>](volume-controls.md)
</dt> </dl>

 

 
