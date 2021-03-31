---
title: Иажентчарактер Жетттсспид
description: Иажентчарактер Жетттсспид
ms.assetid: 25526ef7-581f-489c-a299-bd3b5ac9ea61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 551074e1647cffc88e0b5f9f530cea931cd21ff9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411451"
---
# <a name="iagentcharactergetttsspeed"></a>Иажентчарактер:: Жетттсспид

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

 

 




