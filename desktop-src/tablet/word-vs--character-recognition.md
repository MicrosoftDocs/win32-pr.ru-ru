---
description: Если для свойства фактоид задано значение None, то распознаватель символов распознает рукописный ввод на основе символьных символов.
ms.assetid: 4dacceab-032e-4b9b-858f-67961fd587b5
title: Сравнение слов и распознавания символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f521b8abf1064ef87c5c79c3293e725c44190ce3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144761"
---
# <a name="word-vs-character-recognition"></a>Сравнение слов и распознавания символов

Если для свойства [фактоид](/previous-versions/ms835848(v=msdn.10)) задано значение **None**, то распознаватель символов распознает рукописный ввод на основе символьных символов.

Свойство [рекотимеаут](/previous-versions/ms835852(v=msdn.10)) ([**Рекотимеаут**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) в службе автоматизации) определяет время задержки между последним [штрихом](/previous-versions/ms552692(v=vs.100)) и окончанием рукописного ввода в миллисекундах. Это значение можно увеличить, чтобы распознать текст до того, как будут записаны целые слова или предложения. Можно также принудительно выполнить распознавание рукописного ввода с помощью метода [Recognize](/previous-versions/ms836275(v=msdn.10)) .

 

 
