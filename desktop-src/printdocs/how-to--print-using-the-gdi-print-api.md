---
description: в этом разделе рассказывается, как выполнять печать из собственной Windows программы с помощью GDI&\# 160; Печать&\# 160; API.
ms.assetid: C212DD92-2B90-45BC-8746-29C193FBDF69
title: Инструкции. печать с помощью API печати GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19832ef93a80cc537d16136ac751cb20fd8664d7d1d31d295568de68d6dd846
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091934"
---
# <a name="how-to-print-using-the-gdi-print-api"></a>Инструкции. печать с помощью API печати GDI

в этом разделе рассказывается, как выполнять печать из собственной Windows программы с помощью [API печати GDI](gdi-printing.md).

## <a name="overview"></a>Обзор

печать обычно является неотъемлемой частью собственной Windows программы, поэтому она не является функцией, которую можно легко добавить после написания программы. при проектировании программы для Windows 7 следует рассмотреть возможность использования [API печати XPS](xps-printing.md) для предоставления функций печати, так как он обеспечивает наиболее актуальную совместимость в будущем. программы, которые должны работать в Windows Vista и более ранних версиях Windows, скорее всего, будут использовать [API печати GDI](gdi-printing.md) для предоставления функций печати. api печати GDI также поддерживается в Windows 7, но он более ограничен, чем api печати XPS.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование печати](using-printing.md)
</dt> <dt>

[печать из Windows приложения](how-to--print-from-a-windows-application.md)
</dt> </dl>

 

 



