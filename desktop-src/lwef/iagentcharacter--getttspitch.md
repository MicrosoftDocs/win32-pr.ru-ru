---
title: Иажентчарактер Жетттспитч
description: Иажентчарактер Жетттспитч
ms.assetid: b21ae1f1-daf6-42e5-9c52-f28722180021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dff1bb7999795cf27e29a7d064dd500b47bb419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691388"
---
# <a name="iagentcharactergetttspitch"></a>Иажентчарактер:: Жетттспитч

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

 

 




