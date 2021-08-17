---
title: Иажентчарактер Жетттсспид
description: Иажентчарактер Жетттсспид
ms.assetid: 25526ef7-581f-489c-a299-bd3b5ac9ea61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e7fbe4cbba7eaed22f49865e1a0f0994c512867fb6f233ef2bbfa01dcaafcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609874"
---
# <a name="iagentcharactergetttsspeed"></a>Иажентчарактер:: Жетттсспид

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetTTSSpeed(
   long * pdwSpeed  // address of variable for character TTS output speed
);
```

Возвращает значение параметра "скорость вывода TTS" для символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*пдвспид*
</dt> <dd>

Адрес переменной, которая получает выходную скорость символа в словах в минуту.

</dd> </dl>

Несмотря на то, что приложение не может записать это значение, в выходной текст можно включить Теги Speed, которые будут временно ускорить вывод для определенного utterance.

Это свойство возвращает значение текущего параметра скорости вывода речи для символа. Для символов, использующих вывод TTS, свойство возвращает фактические выходные данные TTS для символа. Если режим TTS не включен или символ не поддерживает вывод TTS, параметр отражает скорость вывода.

 

 




