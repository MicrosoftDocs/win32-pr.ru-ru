---
title: Иажентчарактер Жетттспитч
description: Иажентчарактер Жетттспитч
ms.assetid: b21ae1f1-daf6-42e5-9c52-f28722180021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c91d4ebc4f55da6a0e102c30a8c2a16eab12beaf283ff4b5e023d15d3a17b05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693150"
---
# <a name="iagentcharactergetttspitch"></a>Иажентчарактер:: Жетттспитч

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetTTSPitch(
   long * pdwPitch  // address of variable for character TTS pitch
);
```

Извлекает значение параметра "выходные данные" TTS для символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*пдвпитч*
</dt> <dd>

Адрес переменной, которая получает текущий параметр TTS для текущего символа в герцах.

</dd> </dl>

Несмотря на то, что приложение не может записать это значение, в выходной текст можно включить Теги кувшина, которые будут временно увеличивать шаг для конкретного utterance. Этот метод применяется только к символам, настроенным для вывода TTS. Если подсистема синтеза речи (TTS) не включена (или не установлена) или символ не поддерживает вывод TTS, этот метод возвращает ноль (0).

 

 




