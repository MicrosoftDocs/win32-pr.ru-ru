---
title: примеры кода клиента DRM Microsoft Windows Media
description: примеры кода клиента DRM Microsoft Windows Media
ms.assetid: 75db2663-9eb8-406d-b1a9-8f6092c95f9d
keywords:
- Windows Пакет SDK для формата мультимедиа, примеры кода
- Windows Пакет SDK для формата мультимедиа, пример кода
- Windows Пакет SDK для формата мультимедиа, примеры кода DRM
- Управление цифровыми правами (DRM), примеры кода
- DRM (Управление цифровыми правами), примеры кода
- Управление цифровыми правами (DRM), пример кода
- DRM (Управление цифровыми правами), пример кода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e14ef7e1d003dec8270bb4cfb63d5b4ead7f11751eb94dd09cd771ebd34b3ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704217"
---
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a>примеры кода клиента DRM Microsoft Windows Media

Примеры кода включены в эту документацию, чтобы продемонстрировать использование компонентов. Примеры записываются как можно более четкие и лаконичные. При чтении примеров следует учитывать следующие соглашения.

-   Предполагается, что все примеры включают в себя Windows. h и вмдрмсдк. h. В примере будет содержаться Примечание, если для компиляции требуются другие заголовки.
-   В случае возникновения ошибки проверка ошибок была ограничена до выхода из функции. В приложении следует проверить определенные коды ошибок и предоставить некоторый тип отчетов об ошибках.
-   Интерфейсы и память освобождаются в примерах кода с помощью макросов с именем безопасного \_ выпуска и безопасного \_ массива \_ Delete. Эти макросы определяются в следующем коде:
    ```C++
    #ifndef SAFE_RELEASE
    #define SAFE_RELEASE(x) \
       if(x != NULL)        \
       {                    \
          x->Release();     \
          x = NULL;         \
       }
    #endif

    #ifndef SAFE_ARRAY_DELETE
    #define SAFE_ARRAY_DELETE(x) \
       if(x != NULL)             \
       {                         \
          delete[] x;            \
          x = NULL;              \
       }
    #endif
    ```

    

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**начало работы**](drm-getting-started.md)
</dt> </dl>

 

 




