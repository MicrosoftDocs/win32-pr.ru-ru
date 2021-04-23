---
title: Создание графов фильтров в DRM-Enabled приложениях
description: Создание графов фильтров в DRM-Enabled приложениях
ms.assetid: 447bec2a-0982-4a05-87bb-aed6db684b36
keywords:
- Windows Media Format SDK, создание графов фильтра
- Пакет SDK для Windows Media Format, DirectShow
- Windows Media Format SDK, приложения с поддержкой DRM
- Расширенный формат систем (ASF), создание графов фильтра
- ASF (Расширенный системный формат), создание графов фильтра
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- Расширенный формат систем (ASF), приложения с поддержкой DRM
- ASF (расширенный формат систем), приложения с поддержкой DRM
- DirectShow, создание графов фильтра
- DirectShow, приложения с поддержкой DRM
- Управление цифровыми правами (DRM), DirectShow
- DRM (Управление цифровыми правами), DirectShow
- Управление цифровыми правами (DRM), создание графов фильтров
- DRM (Управление цифровыми правами), создание графов фильтра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944037a00c208e1427d3d19aa6c9dc0a352ec5fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336404"
---
# <a name="building-filter-graphs-in-drm-enabled-applications"></a><span data-ttu-id="58488-118">Создание графов фильтров в DRM-Enabled приложениях</span><span class="sxs-lookup"><span data-stu-id="58488-118">Building Filter Graphs in DRM-Enabled Applications</span></span>

<span data-ttu-id="58488-119">Если приложение DirectShow поддерживает воспроизведение файлов, защищенных с помощью DRM, то обычно не следует использовать **RenderFile** для создания графа фильтра, так как не существует способа указать, какие права DRM вы запрашиваете перед открытием файла.</span><span class="sxs-lookup"><span data-stu-id="58488-119">If your DirectShow application supports playback of DRM-protected files, then you generally should not use **RenderFile** to create the filter graph because there is no way to specify which DRM rights you are requesting before the file is opened.</span></span> <span data-ttu-id="58488-120">Средство чтения WM ASF по умолчанию запрашивает только права на воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="58488-120">The WM ASF Reader by default asks for only playback rights.</span></span> <span data-ttu-id="58488-121">Фильтр не добавляется в граф и поэтому не может быть обнаружен приложениями, пока файл не будет успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="58488-121">The filter is not added to the graph, and is therefore not discoverable by applications, until a file is successfully opened.</span></span>

<span data-ttu-id="58488-122">Чтобы создать граф воспроизведения с поддержкой DRM с помощью [средства чтения WM ASF](wm-asf-reader-filter.md), необходимо создать экземпляр фильтра с помощью функции **CoCreateInstance**, добавить его в граф фильтра с помощью **играфбуилдер:: аддфилтер**, настроить его, а затем визуализировать выходные контакты.</span><span class="sxs-lookup"><span data-stu-id="58488-122">To build a DRM-enabled playback graph using the [WM ASF Reader](wm-asf-reader-filter.md), you must instantiate the filter using **CoCreateInstance**, add it to the filter graph using **IGraphBuilder::AddFilter**, configure it, and then render its output pins.</span></span> <span data-ttu-id="58488-123">Этот метод показан в примере Плайвндасф.</span><span class="sxs-lookup"><span data-stu-id="58488-123">This technique is demonstrated in the PlayWndASF sample.</span></span> <span data-ttu-id="58488-124">При таком способе построения графа у вас уже есть указатель **ибасефилтер** , который можно использовать для вызова **QueryService** для получения **ивмдрмвритер**.</span><span class="sxs-lookup"><span data-stu-id="58488-124">When you build the graph in this way, you already have the **IBaseFilter** pointer that can be used to call **QueryService** to obtain **IWMDRMWriter**.</span></span> <span data-ttu-id="58488-125">Однако этот интерфейс недоступен, пока объект чтения пакета SDK для формата Windows Media не будет создан модулем чтения WM ASF.</span><span class="sxs-lookup"><span data-stu-id="58488-125">However, this interface is not available until the Windows Media Format SDK reader object is created internally by the WM ASF Reader.</span></span> <span data-ttu-id="58488-126">Первая возможность, с которой приложение должно устанавливать права DRM, — это ВМТ \_ без \_ \_ обработчика событий ex, как показано в следующем фрагменте кода:</span><span class="sxs-lookup"><span data-stu-id="58488-126">The first opportunity the application has to set DRM rights is in its WMT\_NO\_RIGHTS\_EX event handler, as shown in this code snippet:</span></span>


```C++
case WMT_NO_RIGHTS_EX:

    IServiceProvider *pServiceProvider;
    IWMDRMReader pWMDRMReader;
    JIF(g_pReader->QueryInterface(IID_IServiceProvider, (void **) &pServiceProvider));
    JIF(pServiceProvider->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader)); 
    SAFE_RELEASE(pServiceProvider);

    // Set the rights we want for this file. These are the actions we 
    // might want to perform on the file. Here we ask for two rights only.
    // In a real application you should enable users to select which 
    // rights they want.
    hr = pWMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
        BYTE*) wszRights, (sizeof(wszRights) / sizeof(wszRights[0])) * 2);
    SAFE_RELEASE(pWMDRMReader);
    if (FAILED(hr))
    {
       Msg(TEXT("SetDRMProperty Failed!  hr=0x%x\n"), hr);
       return hr;
    }
    // Now proceed with license acqusition.
    if( pEventData->pData )
    {
        hr = HandleNoRightsEx(pEventData->hrStatus, 
        (WM_GET_LICENSE_DATA *)pEventData->pData);
    }
    else
    {
         hr = E_FAIL;
    }
    break;

```



## <a name="related-topics"></a><span data-ttu-id="58488-127">См. также</span><span class="sxs-lookup"><span data-stu-id="58488-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58488-128">**Функции цифровых Rights Management**</span><span class="sxs-lookup"><span data-stu-id="58488-128">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="58488-129">**Список атрибутов DRM**</span><span class="sxs-lookup"><span data-stu-id="58488-129">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="58488-130">**Свойства DRM**</span><span class="sxs-lookup"><span data-stu-id="58488-130">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="58488-131">**Включение поддержки DRM**</span><span class="sxs-lookup"><span data-stu-id="58488-131">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="58488-132">**ивмдрмреадер**</span><span class="sxs-lookup"><span data-stu-id="58488-132">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> <dt>

[<span data-ttu-id="58488-133">**ивмдрмвритер**</span><span class="sxs-lookup"><span data-stu-id="58488-133">**IWMDRMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> </dl>

 

 




