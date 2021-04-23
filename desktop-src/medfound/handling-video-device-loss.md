---
description: В этом разделе описывается, как обнаружить потери устройства при использовании устройства видеозаписи.
ms.assetid: 2bffe156-c507-437e-8f32-62aaebedd6f0
title: Обработка потери видеоустройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d083ebeb1203b0bba49a63745f62a4dff6b231
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711354"
---
# <a name="handling-video-device-loss"></a><span data-ttu-id="ef399-103">Обработка потери видеоустройства</span><span class="sxs-lookup"><span data-stu-id="ef399-103">Handling Video Device Loss</span></span>

<span data-ttu-id="ef399-104">В этом разделе описывается, как обнаружить потери устройства при использовании устройства видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="ef399-104">This topic describes how to detect device loss when using a video capture device.</span></span> <span data-ttu-id="ef399-105">Он содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="ef399-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="ef399-106">Регистрация для уведомления устройства</span><span class="sxs-lookup"><span data-stu-id="ef399-106">Register For Device Notification</span></span>](#register-for-device-notification)
-   [<span data-ttu-id="ef399-107">Получение символьной ссылки на устройство</span><span class="sxs-lookup"><span data-stu-id="ef399-107">Get the Symbolic Link of the Device</span></span>](#get-the-symbolic-link-of-the-device)
-   [<span data-ttu-id="ef399-108">Handles WM \_ девицечанже</span><span class="sxs-lookup"><span data-stu-id="ef399-108">Handle WM\_DEVICECHANGE</span></span>](/windows)
-   [<span data-ttu-id="ef399-109">Отменить регистрацию для уведомления</span><span class="sxs-lookup"><span data-stu-id="ef399-109">Unregister For Notification</span></span>](#unregister-for-notification)
-   [<span data-ttu-id="ef399-110">См. также</span><span class="sxs-lookup"><span data-stu-id="ef399-110">Related topics</span></span>](#related-topics)

## <a name="register-for-device-notification"></a><span data-ttu-id="ef399-111">Регистрация для уведомления устройства</span><span class="sxs-lookup"><span data-stu-id="ef399-111">Register For Device Notification</span></span>

<span data-ttu-id="ef399-112">Прежде чем начать сбор с устройства, вызовите функцию [**регистердевиценотификатион**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) для регистрации уведомлений устройства.</span><span class="sxs-lookup"><span data-stu-id="ef399-112">Before you start capturing from the device, call the [**RegisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) function to register for device notifications.</span></span> <span data-ttu-id="ef399-113">Зарегистрируйте класс **устройства \_ Capture кскатегори** , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="ef399-113">Register for the **KSCATEGORY\_CAPTURE** device class, as shown in the following code.</span></span>


```C++
#include <Dbt.h>
#include <ks.h>
#include <ksmedia.h>

HDEVNOTIFY  g_hdevnotify = NULL;

BOOL RegisterForDeviceNotification(HWND hwnd)
{
    DEV_BROADCAST_DEVICEINTERFACE di = { 0 };
    di.dbcc_size = sizeof(di);
    di.dbcc_devicetype  = DBT_DEVTYP_DEVICEINTERFACE;
    di.dbcc_classguid  = KSCATEGORY_CAPTURE; 

    g_hdevnotify = RegisterDeviceNotification(
        hwnd,
        &di,
        DEVICE_NOTIFY_WINDOW_HANDLE
        );

    if (g_hdevnotify == NULL)
    {
        return FALSE;
    }

    return TRUE;
}
```



## <a name="get-the-symbolic-link-of-the-device"></a><span data-ttu-id="ef399-114">Получение символьной ссылки на устройство</span><span class="sxs-lookup"><span data-stu-id="ef399-114">Get the Symbolic Link of the Device</span></span>

<span data-ttu-id="ef399-115">Перечислите видео устройства в системе, как описано в разделе [Перечисление устройств видеозаписи](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="ef399-115">Enumerate the video devices on the system, as described in [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span> <span data-ttu-id="ef399-116">Выберите устройство из списка, а затем выполните запрос к объекту активации для атрибута [MF \_ девсаурце \_ \_ тип источника атрибута \_ \_ видкап \_ символической \_ ссылки](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="ef399-116">Choose a device from the list, and then query the activation object for the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute, as shown in the following code.</span></span>


```C++
WCHAR      *g_pwszSymbolicLink = NULL;
UINT32     g_cchSymbolicLink = 0;

HRESULT GetSymbolicLink(IMFActivate *pActivate)
{
    return pActivate->GetAllocatedString(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
        &g_pwszSymbolicLink,
        &g_cchSymbolicLink
        );
}
```



## <a name="handle-wm_devicechange"></a><span data-ttu-id="ef399-117">Handles WM \_ девицечанже</span><span class="sxs-lookup"><span data-stu-id="ef399-117">Handle WM\_DEVICECHANGE</span></span>

<span data-ttu-id="ef399-118">В цикле обработки сообщений Прослушайте сообщения [**WM \_ девицечанже**](../devio/wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="ef399-118">In your message loop, listen for [**WM\_DEVICECHANGE**](../devio/wm-devicechange.md) messages.</span></span> <span data-ttu-id="ef399-119">Параметр сообщения *lParam* является указателем на HDR- [**структуру \_ вещания \_ для разработки**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) .</span><span class="sxs-lookup"><span data-stu-id="ef399-119">The *lParam* message parameter is a pointer to a [**DEV\_BROADCAST\_HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span>


```C++
    case WM_DEVICECHANGE:
        if (lParam != 0)
        {
            HRESULT hr = S_OK;
            BOOL bDeviceLost = FALSE;

            hr = CheckDeviceLost((PDEV_BROADCAST_HDR)lParam, &bDeviceLost);

            if (FAILED(hr) || bDeviceLost)
            {
                CloseDevice();

                MessageBox(hwnd, L"Lost the capture device.", NULL, MB_OK);
            }
        }
        return TRUE;
```



<span data-ttu-id="ef399-120">Затем сравните сообщение уведомления устройства с символьной ссылкой вашего устройства следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ef399-120">Next, compare the device notification message against the symbolic link of your device, as follows:</span></span>

1.  <span data-ttu-id="ef399-121">Проверьте элемент **дбч \_ типа устройства** в [**\_ \_ HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) -структуре dev.</span><span class="sxs-lookup"><span data-stu-id="ef399-121">Check the **dbch\_devicetype** member of the [**DEV\_BROADCAST\_HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span> <span data-ttu-id="ef399-122">Если значение равно **ДБТ \_ девтип \_ девицеинтерфаце**, приведите указатель структуры к структуре [**\_ \_ девицеинтерфаце**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) , предназначенной для разработки.</span><span class="sxs-lookup"><span data-stu-id="ef399-122">If the value is **DBT\_DEVTYP\_DEVICEINTERFACE**, cast the structure pointer to a [**DEV\_BROADCAST\_DEVICEINTERFACE**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) structure.</span></span>
2.  <span data-ttu-id="ef399-123">Сравните элемент **\_ имени DBCC** этой структуры с символической ссылкой устройства.</span><span class="sxs-lookup"><span data-stu-id="ef399-123">Compare the **dbcc\_name** member of this structure to the symbolic link of the device.</span></span>


```C++
HRESULT CheckDeviceLost(DEV_BROADCAST_HDR *pHdr, BOOL *pbDeviceLost)
{
    DEV_BROADCAST_DEVICEINTERFACE *pDi = NULL;

    if (pbDeviceLost == NULL)
    {
        return E_POINTER;
    }

    *pbDeviceLost = FALSE;
    
    if (g_pSource == NULL)
    {
        return S_OK;
    }
    if (pHdr == NULL)
    {
        return S_OK;
    }
    if (pHdr->dbch_devicetype != DBT_DEVTYP_DEVICEINTERFACE)
    {
        return S_OK;
    }

    // Compare the device name with the symbolic link.

    pDi = (DEV_BROADCAST_DEVICEINTERFACE*)pHdr;

    if (g_pwszSymbolicLink)
    {
        if (_wcsicmp(g_pwszSymbolicLink, pDi->dbcc_name) == 0)
        {
            *pbDeviceLost = TRUE;
        }
    }

    return S_OK;
}
```



## <a name="unregister-for-notification"></a><span data-ttu-id="ef399-124">Отменить регистрацию для уведомления</span><span class="sxs-lookup"><span data-stu-id="ef399-124">Unregister For Notification</span></span>

<span data-ttu-id="ef399-125">Перед выходом из приложения вызовите [**унрегистердевиценотификатион**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) для отмены регистрации уведомлений устройства/</span><span class="sxs-lookup"><span data-stu-id="ef399-125">Before the application exits, call [**UnregisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) to unregister for device notifications/</span></span>


```C++
void OnClose(HWND /*hwnd*/)
{
    if (g_hdevnotify)
    {
        UnregisterDeviceNotification(g_hdevnotify);
    }

    PostQuitMessage(0);
}
```



## <a name="related-topics"></a><span data-ttu-id="ef399-126">См. также</span><span class="sxs-lookup"><span data-stu-id="ef399-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef399-127">Перечисление устройств видеозаписи</span><span class="sxs-lookup"><span data-stu-id="ef399-127">Enumerating Video Capture Devices</span></span>](enumerating-video-capture-devices.md)
</dt> <dt>

[<span data-ttu-id="ef399-128">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="ef399-128">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
