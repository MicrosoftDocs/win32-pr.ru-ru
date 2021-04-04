---
title: Средство Command-Line MkTypLib
description: MkTypLib — это приложение командной строки, которое обрабатывает IDL-файл для создания библиотеки типов. Его также можно использовать для создания заголовочного файла C или C++.
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc392351327124777c2d52d0bbe0653853dcb52
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794130"
---
# <a name="mktyplib-command-line-tool"></a>Средство Command-Line MkTypLib

\[Средство Mktyplib.exe устарело. Вместо этого используйте компилятор MIDL. Если требуется обратная совместимость со старыми программами автоматизации, используйте компилятор MIDL с параметром **/mktyplib203** .\]

MkTypLib — это приложение командной строки, которое обрабатывает IDL-файл для создания библиотеки типов. Его также можно использовать для создания заголовочного файла C или C++.

Создание библиотеки типов из ODL-файла:

-   В командной строке выполните следующую команду:

    **Мктиплибâ * * * имя_файла*

    где *filename*— имя ODL-файла.

MkTypLib также поддерживает несколько необязательных параметров. Для выполнения полного списка выполните следующую командную строку:

**MkTypLib/?**

Поскольку MkTypLib является устаревшим приложением, он не может анализировать IDL-файлы или файлы с интерфейсами, определенными вне [**библиотечной**](/windows/desktop/Midl/library) инструкции. Дополнительные сведения см. в разделе [различия между MIDL и MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Преобразование в C++](translating-to-c--.md)
</dt> </dl>

 

 