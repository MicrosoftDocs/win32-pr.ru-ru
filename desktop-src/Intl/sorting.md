---
description: Для NLS Сортировка (также известная как &\# 0034; параметры сортировки&\# 0034;) — Это упорядочение строк.
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: Сортировка (Международная связь)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3dbedf872c953a45ca7064eccd4ba16019a857c35186261695e094be03cd054
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130214"
---
# <a name="sorting"></a>Сортировка

Для NLS Сортировка (также называемая "параметрами сортировки") представляет собой расположение строк. Существует два типа сортировки:

-   Лингвистическая сортировка. Упорядочивает строки с похожими лингвистическими характеристиками в группы (по сортировке).
-   Порядковые (не лингвистические) сортировки. Упорядочивает строки в упорядоченной последовательности.

При сортировке используются функции сравнения строк NLS, такие как [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) и [**LCMapString завершилось ошибкой**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), или функции API-оболочки, такие как [лстркмп](/windows/win32/api/winbase/nf-winbase-lstrcmpa), которые внутренне вызывают функции сравнения строк NLS.

Дополнительные сведения о реализации сортировки в приложениях см. [в разделе Обработка сортировки в приложениях](handling-sorting-in-your-applications.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сведения о поддержке национальных языков](about-national-language-support.md)
</dt> <dt>

[Обработка сортировки в приложениях](handling-sorting-in-your-applications.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[LCMapString завершилось ошибкой](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> </dl>

 

 
