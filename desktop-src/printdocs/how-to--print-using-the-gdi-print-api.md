---
description: В этом разделе рассказывается, как выполнять печать из собственной программы Windows с помощью GDI&\# 160; Печать&\# 160; API.
ms.assetid: C212DD92-2B90-45BC-8746-29C193FBDF69
title: Инструкции. печать с помощью API печати GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d6351e228297b5378b54879548b823f81894b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913152"
---
# <a name="how-to-print-using-the-gdi-print-api"></a>Инструкции. печать с помощью API печати GDI

В этом разделе рассказывается, как выполнять печать из собственной программы Windows с помощью [API печати GDI](gdi-printing.md).

## <a name="overview"></a>Обзор

Печать обычно является неотъемлемой частью собственной программы Windows, поэтому она не является функцией, которую можно легко добавить после написания программы. При проектировании программы для Windows 7 следует рассмотреть возможность использования [API печати XPS](xps-printing.md) для предоставления функций печати, так как он обеспечивает наиболее актуальную совместимость в будущем. Программы, которые должны работать в Windows Vista и более ранних версиях Windows, скорее всего, будут использовать [API печати GDI](gdi-printing.md) для предоставления функций печати. API печати GDI также поддерживается в Windows 7, но он более ограничен, чем API печати XPS.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование печати](using-printing.md)
</dt> <dt>

[Печать из приложения Windows](how-to--print-from-a-windows-application.md)
</dt> </dl>

 

 



