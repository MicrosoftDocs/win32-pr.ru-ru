---
description: Включает статическую оптимизацию в конвейере видео.
ms.assetid: 62fb3f0f-ab1f-4c61-8e7f-62908b947788
title: Атрибут MF_TOPOLOGY_STATIC_PLAYBACK_OPTIMIZATIONS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f9f7d884c49078ca02571f8ba141f9a1e13589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703078"
---
# <a name="mf_topology_static_playback_optimizations-attribute"></a><span data-ttu-id="4a750-103">\_ \_ \_ Атрибут статической оптимизации воспроизведения \_ топологии MF</span><span class="sxs-lookup"><span data-stu-id="4a750-103">MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS attribute</span></span>

<span data-ttu-id="4a750-104">Включает статическую оптимизацию в конвейере видео.</span><span class="sxs-lookup"><span data-stu-id="4a750-104">Enables static optimizations in the video pipeline.</span></span>

## <a name="data-type"></a><span data-ttu-id="4a750-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4a750-105">Data type</span></span>

<span data-ttu-id="4a750-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4a750-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="4a750-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="4a750-107">Get/set</span></span>

<span data-ttu-id="4a750-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="4a750-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="4a750-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="4a750-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="4a750-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="4a750-110">Applies to</span></span>

[<span data-ttu-id="4a750-111">**имфтопологи**</span><span class="sxs-lookup"><span data-stu-id="4a750-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="4a750-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a750-112">Remarks</span></span>

<span data-ttu-id="4a750-113">Установите этот атрибут перед загрузкой топологии.</span><span class="sxs-lookup"><span data-stu-id="4a750-113">Set this attribute before loading a topology.</span></span> <span data-ttu-id="4a750-114">Если атрибут имеет **значение true**, загрузчик топологии пытается оптимизировать конвейер перед началом воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="4a750-114">If the attribute is **TRUE**, the topology loader attempts to optimize the pipeline before playback starts.</span></span>

<span data-ttu-id="4a750-115">Если задан этот атрибут, необходимо также задать следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="4a750-115">If you set this attribute, you should also set the following attributes:</span></span>

-   [<span data-ttu-id="4a750-116">\_ \_ Частота воспроизведения в топологии MF \_</span><span class="sxs-lookup"><span data-stu-id="4a750-116">MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE</span></span>](mf-topology-playback-framerate.md)
-   [<span data-ttu-id="4a750-117">\_ \_ Максимальное число воспроизведений для воспроизведения топологии MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="4a750-117">MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS</span></span>](mf-topology-playback-max-dims.md)

<span data-ttu-id="4a750-118">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="4a750-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="4a750-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="4a750-119">Examples</span></span>


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



## <a name="requirements"></a><span data-ttu-id="4a750-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4a750-120">Requirements</span></span>



| <span data-ttu-id="4a750-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4a750-121">Requirement</span></span> | <span data-ttu-id="4a750-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4a750-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a750-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a750-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4a750-124">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4a750-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4a750-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a750-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4a750-126">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4a750-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4a750-127">Header</span><span class="sxs-lookup"><span data-stu-id="4a750-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a750-128"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a750-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a750-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a750-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a750-130">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4a750-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4a750-131">Атрибуты топологии</span><span class="sxs-lookup"><span data-stu-id="4a750-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="4a750-132">Управление качеством видео</span><span class="sxs-lookup"><span data-stu-id="4a750-132">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




