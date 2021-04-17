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
# <a name="handling-video-device-loss"></a>Обработка потери видеоустройства

В этом разделе описывается, как обнаружить потери устройства при использовании устройства видеозаписи. Он содержит следующие подразделы:

-   [Регистрация для уведомления устройства](#register-for-device-notification)
-   [Получение символьной ссылки на устройство](#get-the-symbolic-link-of-the-device)
-   [Handles WM \_ девицечанже](/windows)
-   [Отменить регистрацию для уведомления](#unregister-for-notification)
-   [См. также](#related-topics)

## <a name="register-for-device-notification"></a>Регистрация для уведомления устройства

Прежде чем начать сбор с устройства, вызовите функцию [**регистердевиценотификатион**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) для регистрации уведомлений устройства. Зарегистрируйте класс **устройства \_ Capture кскатегори** , как показано в следующем коде.


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



## <a name="get-the-symbolic-link-of-the-device"></a>Получение символьной ссылки на устройство

Перечислите видео устройства в системе, как описано в разделе [Перечисление устройств видеозаписи](enumerating-video-capture-devices.md). Выберите устройство из списка, а затем выполните запрос к объекту активации для атрибута [MF \_ девсаурце \_ \_ тип источника атрибута \_ \_ видкап \_ символической \_ ссылки](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) , как показано в следующем коде.


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



## <a name="handle-wm_devicechange"></a>Handles WM \_ девицечанже

В цикле обработки сообщений Прослушайте сообщения [**WM \_ девицечанже**](../devio/wm-devicechange.md) . Параметр сообщения *lParam* является указателем на HDR- [**структуру \_ вещания \_ для разработки**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) .


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



Затем сравните сообщение уведомления устройства с символьной ссылкой вашего устройства следующим образом:

1.  Проверьте элемент **дбч \_ типа устройства** в [**\_ \_ HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) -структуре dev. Если значение равно **ДБТ \_ девтип \_ девицеинтерфаце**, приведите указатель структуры к структуре [**\_ \_ девицеинтерфаце**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) , предназначенной для разработки.
2.  Сравните элемент **\_ имени DBCC** этой структуры с символической ссылкой устройства.


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



## <a name="unregister-for-notification"></a>Отменить регистрацию для уведомления

Перед выходом из приложения вызовите [**унрегистердевиценотификатион**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) для отмены регистрации уведомлений устройства/


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Перечисление устройств видеозаписи](enumerating-video-capture-devices.md)
</dt> <dt>

[Видеозапись](video-capture.md)
</dt> </dl>

 

 
