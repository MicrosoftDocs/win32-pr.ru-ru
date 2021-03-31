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
# <a name="building-filter-graphs-in-drm-enabled-applications"></a>Создание графов фильтров в DRM-Enabled приложениях

Если приложение DirectShow поддерживает воспроизведение файлов, защищенных с помощью DRM, то обычно не следует использовать **RenderFile** для создания графа фильтра, так как не существует способа указать, какие права DRM вы запрашиваете перед открытием файла. Средство чтения WM ASF по умолчанию запрашивает только права на воспроизведение. Фильтр не добавляется в граф и поэтому не может быть обнаружен приложениями, пока файл не будет успешно открыт.

Чтобы создать граф воспроизведения с поддержкой DRM с помощью [средства чтения WM ASF](wm-asf-reader-filter.md), необходимо создать экземпляр фильтра с помощью функции **CoCreateInstance**, добавить его в граф фильтра с помощью **играфбуилдер:: аддфилтер**, настроить его, а затем визуализировать выходные контакты. Этот метод показан в примере Плайвндасф. При таком способе построения графа у вас уже есть указатель **ибасефилтер** , который можно использовать для вызова **QueryService** для получения **ивмдрмвритер**. Однако этот интерфейс недоступен, пока объект чтения пакета SDK для формата Windows Media не будет создан модулем чтения WM ASF. Первая возможность, с которой приложение должно устанавливать права DRM, — это ВМТ \_ без \_ \_ обработчика событий ex, как показано в следующем фрагменте кода:


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Функции цифровых Rights Management**](digital-rights-management-features.md)
</dt> <dt>

[**Список атрибутов DRM**](drm-attribute-list.md)
</dt> <dt>

[**Свойства DRM**](drm-properties.md)
</dt> <dt>

[**Включение поддержки DRM**](enabling-drm-support.md)
</dt> <dt>

[**ивмдрмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> <dt>

[**ивмдрмвритер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> </dl>

 

 




