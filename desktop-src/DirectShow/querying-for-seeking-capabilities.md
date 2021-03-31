---
description: Запрос возможностей поиска
ms.assetid: d1d8c708-75f2-4dc7-a33a-8dd2cea0ee00
title: Запрос возможностей поиска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa763ab11267da0a9a13a920285491d83273a8d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894922"
---
# <a name="querying-for-seeking-capabilities"></a>Запрос возможностей поиска

Microsoft® DirectShow® поддерживает поиск через интерфейс [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . Диспетчер графов фильтров предоставляет этот интерфейс, но функции поиска всегда реализуются фильтрами в графе.

Не удается выполнить поиск некоторых данных. Например, невозможно выполнить поиск потока видео с камеры. Однако если поток доступен для поиска, он может поддерживать различные типы поиска. Сюда входит следующее.

-   Поиск произвольной позицией в потоке.
-   Получение длительности потока.
-   Получение текущей позицией в потоке.
-   Воспроизведение в обратную.

Интерфейс **имедиасикинг** определяет набор флагов, которые [**\_ ищут \_ \_ возможности поиска**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), которые описывают возможные возможности поиска. Чтобы получить возможности потока, вызовите метод [**имедиасикинг:: Capabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) . Метод возвращает побитовое сочетание флагов. Приложение может проверить их с помощью оператора & (побитовое **и**). Например, следующий код проверяет, может ли граф перейти к произвольной должности:


```C++
DWORD dwCap = 0;
HRESULT hr = pSeek->GetCapabilities(&dwCap);
if (AM_SEEKING_CanSeekAbsolute & dwCap)
{
    // Graph can seek to absolute positions.
}
```



 

 



