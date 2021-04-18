---
title: Свойство Speed
description: Свойство Speed
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24738ac17d7efac45f2aefe7e4beb5ec018915a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700529"
---
# <a name="speed-property"></a>Свойство Speed

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает длинное целое число, определяющее текущую скорость речевого вывода символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("*** чарактерид * * *"). Установлен**

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это свойство возвращает значение текущего параметра скорости вывода речи для символа. Для символов, использующих выходные данные TTS, свойство возвращает фактический параметр вывода TTS для символа. Если режим TTS не включен или символ не поддерживает вывод TTS, параметр отражает скорость вывода.

Несмотря на то, что приложение не может записать это значение, можно включить в выходной текст Теги **SPD** (Speed), которые будут временно ускорить вывод для определенного utterance. Однако использование тега **SPD** для изменения речевого вывода символа не влияет на значение свойства **Speed** . Дополнительные сведения см. в разделе [теги вывода речи](microsoft-agent-speech-output-tags.md).

 

 




