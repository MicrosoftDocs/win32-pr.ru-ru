---
description: Для NLS Сортировка (также известная как &\# 0034; параметры сортировки&\# 0034;) — Это упорядочение строк.
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: Сортировка (Международная связь)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f49a5abb8371a00ad9ee63f929b4aaf4b18b11be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272809"
---
# <a name="sorting"></a>Сортировка

Для NLS Сортировка (также называемая "параметрами сортировки") представляет собой расположение строк. Существует два типа сортировки:

-   Лингвистическая сортировка. Упорядочивает строки с похожими лингвистическими характеристиками в группы (по сортировке).
-   Порядковые (не лингвистические) сортировки. Упорядочивает строки в упорядоченной последовательности.

При сортировке используются функции сравнения строк NLS, такие как [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) и [**LCMapString завершилось ошибкой**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), или функции API-оболочки, такие как [лстркмп](/windows/win32/api/winbase/nf-winbase-lstrcmpa), которые внутренне вызывают функции сравнения строк NLS.

Дополнительные сведения о реализации сортировки в приложениях см. [в разделе Обработка сортировки в приложениях](handling-sorting-in-your-applications.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сведения о поддержке национальных языков](about-national-language-support.md)
</dt> <dt>

[Обработка сортировки в приложениях](handling-sorting-in-your-applications.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[LCMapString завершилось ошибкой](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> </dl>

 

 
