---
title: Обзор эскизов DWM
description: Диспетчер окон рабочего стола (DWM) включает отображение эскизных представлений окон приложений.
ms.assetid: 6d71fcda-0cf0-463c-8c60-0415109d154f
keywords:
- Диспетчер окон рабочего стола (DWM), эскизы
- DWM (диспетчер окон рабочего стола), эскизы
- Диспетчер окон рабочего стола (DWM), эскизные связи
- DWM (диспетчер окон рабочего стола), отношения эскиза
- Эскизы
- отношения эскиза
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3e0f1e6875e447a18ff5e63d703460ff909b25
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "104550596"
---
# <a name="dwm-thumbnail-overview"></a><span data-ttu-id="17564-109">Обзор эскизов DWM</span><span class="sxs-lookup"><span data-stu-id="17564-109">DWM Thumbnail Overview</span></span>

<span data-ttu-id="17564-110">Диспетчер окон рабочего стола (DWM) включает отображение эскизных представлений окон приложений.</span><span class="sxs-lookup"><span data-stu-id="17564-110">Desktop Window Manager (DWM) enables the display of thumbnail representations of application windows.</span></span> <span data-ttu-id="17564-111">Это не статические моментальные снимки окна, но они являются динамическими, постоянными соединениями между окном исходного кода эскиза и расположением в окне назначения, которое получает визуализацию динамического эскиза.</span><span class="sxs-lookup"><span data-stu-id="17564-111">These are not static snapshots of a window, but are instead dynamic, constant connections between a thumbnail source window and a location on a destination window that receives the live thumbnail rendering.</span></span> <span data-ttu-id="17564-112">Это позволяет быстро просматривать работающие приложения путем наведения указателя мыши на приложение на панели задач или с помощью жеста клавиши ALT + TAB для просмотра и быстрого переключения приложения.</span><span class="sxs-lookup"><span data-stu-id="17564-112">This allows a quick view of running applications by hovering over the application on the taskbar or using the ALT-TAB key gesture to see and quickly switch to an application.</span></span>

<span data-ttu-id="17564-113">На следующем рисунке показан экран Windows Vista Live thumbnail, отображаемый при наведении указателя мыши на приложение на панели задач.</span><span class="sxs-lookup"><span data-stu-id="17564-113">The following image illustrates the Windows Vista live thumbnail seen when you hover over the application on the taskbar.</span></span>

![Снимок экрана, на котором показан эскиз D W M, отображаемый при наведении указателя мыши на приложение на панели задач.](images/dwm-livethumbnail.png)

<span data-ttu-id="17564-115">На следующем рисунке показана перелистывание Windows Vista (ALT-TAB), включенная диспетчером DWM.</span><span class="sxs-lookup"><span data-stu-id="17564-115">The following image illustrates the Windows Vista Flip (ALT-TAB) enabled by DWM.</span></span>

![снимок экрана с окном рабочего стола с Alt-Tab](images/dwm-flip.png)

> [!Note]  
> <span data-ttu-id="17564-117">Эскизы DWM не позволяют разработчикам создавать такие приложения, как функция Windows Vista Flip3D (ВИНКЭЙ-TAB).</span><span class="sxs-lookup"><span data-stu-id="17564-117">DWM thumbnails do not enable developers to create applications like the Windows Vista Flip3D (WINKEY-TAB) feature.</span></span> <span data-ttu-id="17564-118">Эскизы подготавливаются к просмотру непосредственно в окне назначения в виде 2-мерная.</span><span class="sxs-lookup"><span data-stu-id="17564-118">Thumbnails are rendered directly to the destination window in 2-D.</span></span>

 

## <a name="dwm-thumbnail-relationships"></a><span data-ttu-id="17564-119">Связи эскизов DWM</span><span class="sxs-lookup"><span data-stu-id="17564-119">DWM Thumbnail Relationships</span></span>

<span data-ttu-id="17564-120">Чтобы отобразить эскизы в приложении, необходимо сначала установить связь между окном исходного кода и конечным окном.</span><span class="sxs-lookup"><span data-stu-id="17564-120">To display thumbnails in your application, you must first establish a relationship between a source window and a destination window.</span></span> <span data-ttu-id="17564-121">Это делается путем вызова функции [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="17564-121">This is done by calling the [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) function.</span></span>

<span data-ttu-id="17564-122">[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) не отображает эскиз в окне назначения, но только создает связь и предоставляет маркер эскиза.</span><span class="sxs-lookup"><span data-stu-id="17564-122">[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) does not render a thumbnail on the destination window but merely creates the relationship and provides the thumbnail handle.</span></span> <span data-ttu-id="17564-123">Эскиз отображается после установки [**\_ \_ свойств эскиза DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) и вызова функции [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) .</span><span class="sxs-lookup"><span data-stu-id="17564-123">The thumbnail is rendered after the [**DWM\_THUMBNAIL\_PROPERTIES**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) have been set and the [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) function has been called.</span></span> <span data-ttu-id="17564-124">Последующие вызовы **DwmUpdateThumbnailProperties** обновляют эскиз с помощью нового набора свойств.</span><span class="sxs-lookup"><span data-stu-id="17564-124">Subsequent calls to **DwmUpdateThumbnailProperties** update the thumbnail with a new set of properties.</span></span> <span data-ttu-id="17564-125">DWM также предоставляет вспомогательную функцию [**двмкуерисумбнаилсаурцесизе**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) для получения размера окна исходного кода из эскиза.</span><span class="sxs-lookup"><span data-stu-id="17564-125">The DWM also provides the helper function [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) to obtain the size of the source window from the thumbnail.</span></span>

<span data-ttu-id="17564-126">Чтобы завершить связь эскиза, вызовите функцию [**двмунрегистерсумбнаил**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="17564-126">To end a thumbnail relationship, call the [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) function.</span></span>

<span data-ttu-id="17564-127">В следующем примере показано, как создать релеатионшип с рабочим столом Windows и отобразить его в приложении.</span><span class="sxs-lookup"><span data-stu-id="17564-127">The following example demonstrates how to create a releationship with the Windows desktop and display it in an application.</span></span>


```
HRESULT hr = S_OK;
HTHUMBNAIL thumbnail = NULL;

// Register the thumbnail
hr = DwmRegisterThumbnail(hwnd, FindWindow(_T("Progman"), NULL), &thumbnail);
if (SUCCEEDED(hr))
{
    // Specify the destination rectangle size
    RECT dest = {0,50,100,150};

    // Set the thumbnail properties for use
    DWM_THUMBNAIL_PROPERTIES dskThumbProps;
    dskThumbProps.dwFlags = DWM_TNP_SOURCECLIENTAREAONLY | DWM_TNP_VISIBLE | DWM_TNP_OPACITY | DWM_TNP_RECTDESTINATION;
    dskThumbProps.fSourceClientAreaOnly = FALSE; 
    dskThumbProps.fVisible = TRUE;
    dskThumbProps.opacity = (255 * 70)/100;
    dskThumbProps.rcDestination = dest;

    // Display the thumbnail
    hr = DwmUpdateThumbnailProperties(thumbnail,&dskThumbProps);
    if (SUCCEEDED(hr))
    {
        // ...
    }
}
return hr;
```



## <a name="related-topics"></a><span data-ttu-id="17564-128">См. также</span><span class="sxs-lookup"><span data-stu-id="17564-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17564-129">Общие сведения о диспетчере окон рабочего стола</span><span class="sxs-lookup"><span data-stu-id="17564-129">Desktop Window Manager Overview</span></span>](dwm-overview.md)
</dt> <dt>

[<span data-ttu-id="17564-130">Включение и контроль композиции DWM</span><span class="sxs-lookup"><span data-stu-id="17564-130">Enable and Control DWM Composition</span></span>](composition-ovw.md)
</dt> <dt>

[<span data-ttu-id="17564-131">Вопросы производительности и рекомендации</span><span class="sxs-lookup"><span data-stu-id="17564-131">Performance Considerations and Best Practices</span></span>](bestpractices-ovw.md)
</dt> </dl>

 

 




