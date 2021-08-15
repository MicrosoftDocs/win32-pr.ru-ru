---
description: Включает статическую оптимизацию в конвейере видео.
ms.assetid: 62fb3f0f-ab1f-4c61-8e7f-62908b947788
title: Атрибут MF_TOPOLOGY_STATIC_PLAYBACK_OPTIMIZATIONS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f01b22e5b7e972e9d1eb453f317e8db6a902e994e83d075cd791d9261aa6ed09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691246"
---
# <a name="mf_topology_static_playback_optimizations-attribute"></a>\_ \_ \_ Атрибут статической оптимизации воспроизведения \_ топологии MF

Включает статическую оптимизацию в конвейере видео.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфтопологи**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Remarks

Установите этот атрибут перед загрузкой топологии. Если атрибут имеет **значение true**, загрузчик топологии пытается оптимизировать конвейер перед началом воспроизведения.

Если задан этот атрибут, необходимо также задать следующие атрибуты:

-   [\_ \_ Частота воспроизведения в топологии MF \_](mf-topology-playback-framerate.md)
-   [\_ \_ Максимальное число воспроизведений для воспроизведения топологии MF \_ \_](mf-topology-playback-max-dims.md)

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="examples"></a>Примеры


```C++
HRESULT SetPlaybackOptimizations(IMFTopology *pTopology, HWND hwnd)
{
    HRESULT hr = pTopology->SetUINT32(
        MF_TOPOLOGY_STATIC_PLAYBACK_OPTIMIZATIONS, TRUE);

    if (FAILED(hr))
    {
        return hr;
    }

    HMONITOR hCurrentMon = MonitorFromWindow(hwnd, MONITOR_DEFAULTTOPRIMARY);

    if (hCurrentMon)
    {
        MONITORINFO MonitorInfo = {0};
        MonitorInfo.cbSize = sizeof(MONITORINFO);

        BOOL fSucceeded = GetMonitorInfo(hCurrentMon, &MonitorInfo);

        if (fSucceeded )
        {
            const RECT& rcMonitor = MonitorInfo.rcMonitor;

            LONG width = rcMonitor.right - rcMonitor.left;
            LONG height = rcMonitor.bottom - rcMonitor.top;

            hr = MFSetAttributeSize(
                pTopology, 
                MF_TOPOLOGY_PLAYBACK_MAX_DIMS, 
                (UINT32)width, (UINT32)height
                );

            if (FAILED(hr))
            {
                goto done;
            }

            HDC hdc = GetDC(hwnd);

            hr = MFSetAttributeRatio(
                pTopology,
                MF_TOPOLOGY_PLAYBACK_FRAMERATE,
                GetDeviceCaps(hdc, VREFRESH), 1
                );

            ReleaseDC(hwnd, hdc);
        }
    }
done:
    return hr;
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты топологии](topology-attributes.md)
</dt> <dt>

[Управление качеством видео](video-quality-management.md)
</dt> </dl>

 

 




