---
title: Примеры кода клиента DRM для Microsoft Windows Media
description: Примеры кода клиента DRM для Microsoft Windows Media
ms.assetid: 75db2663-9eb8-406d-b1a9-8f6092c95f9d
keywords:
- Windows Media Format SDK, примеры кода
- Windows Media Format SDK, пример кода
- Windows Media Format SDK, примеры кода DRM
- Управление цифровыми правами (DRM), примеры кода
- DRM (Управление цифровыми правами), примеры кода
- Управление цифровыми правами (DRM), пример кода
- DRM (Управление цифровыми правами), пример кода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 054d1ed804873c8aca104203ee1f235ecb3856f5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414420"
---
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a>Примеры кода клиента DRM для Microsoft Windows Media

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

    

## <a name="related-topics"></a>См. также

<dl> <dt>

[**начало работы**](drm-getting-started.md)
</dt> </dl>

 

 




