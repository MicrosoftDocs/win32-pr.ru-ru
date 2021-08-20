---
title: Средство Command-Line MkTypLib
description: MkTypLib — это приложение командной строки, которое обрабатывает IDL-файл для создания библиотеки типов. Его также можно использовать для создания заголовочного файла C или C++.
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b712ed8220dd609dd3ba189bdac6b5ee11d2805f26ff5a1f146c20f17c1f8ab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047942"
---
# <a name="mktyplib-command-line-tool"></a>Средство Command-Line MkTypLib

\[Средство Mktyplib.exe устарело. Вместо этого используйте компилятор MIDL. Если требуется обратная совместимость со старыми программами автоматизации, используйте компилятор MIDL с параметром **/mktyplib203** .\]

MkTypLib — это приложение командной строки, которое обрабатывает IDL-файл для создания библиотеки типов. Его также можно использовать для создания заголовочного файла C или C++.

Создание библиотеки типов из ODL-файла:

-   В командной строке выполните следующую команду:

    * * Мктиплибâ * *_имя_файла_

    где *filename*— имя ODL-файла.

MkTypLib также поддерживает несколько необязательных параметров. Для выполнения полного списка выполните следующую командную строку:

**MkTypLib/?**

Поскольку MkTypLib является устаревшим приложением, он не может анализировать IDL-файлы или файлы с интерфейсами, определенными вне [**библиотечной**](/windows/desktop/Midl/library) инструкции. Дополнительные сведения см. в разделе [различия между MIDL и MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Преобразование в C++](translating-to-c--.md)
</dt> </dl>

 

 