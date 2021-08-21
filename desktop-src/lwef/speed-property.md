---
title: Свойство Speed
description: Свойство Speed
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaca342dde91965ab381f95671a39c4ba9fdcae040835f09867b3fabf5899a6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745956"
---
# <a name="speed-property"></a>Свойство Speed

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает длинное целое число, определяющее текущую скорость речевого вывода символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("**_чарактерид_*_"). Скорость передачи_*

</dd> </dl>

## <a name="remarks"></a>Remarks

Это свойство возвращает значение текущего параметра скорости вывода речи для символа. Для символов, использующих выходные данные TTS, свойство возвращает фактический параметр вывода TTS для символа. Если режим TTS не включен или символ не поддерживает вывод TTS, параметр отражает скорость вывода.

Несмотря на то, что приложение не может записать это значение, можно включить в выходной текст Теги **SPD** (Speed), которые будут временно ускорить вывод для определенного utterance. Однако использование тега **SPD** для изменения речевого вывода символа не влияет на значение свойства **Speed** . Дополнительные сведения см. в разделе [теги вывода речи](microsoft-agent-speech-output-tags.md).

 

 




