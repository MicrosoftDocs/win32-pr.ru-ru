---
title: Свойство "шаг"
description: Свойство "шаг"
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e346ea0fbb7ebb819d8f00b2fc6aab1ab95e72f391bddc696da18a49f0b2a09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475414"
---
# <a name="pitch-property"></a>Свойство "шаг"

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Nописание** 
</dt> <dd>

Возвращает длинное целое число для заданного параметра продачи речевого вывода символа (TTS).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("**_чарактерид_*_"). Шаг_*

</dd> </dl>

## <a name="remarks"></a>Remarks

Это свойство применяется только к символам, настроенным для вывода TTS. Если символ не поддерживает вывод TTS, это свойство возвращает ноль (0).

Несмотря на то, что приложение не может записать это значение, можно включить в выходной текст Теги « **смолой** » (высота), которые будут временно увеличивать шаг для конкретного utterance. Однако использование тега **смолой** для изменения высоты не приведет к изменению значения свойства **шаг** . Дополнительные сведения см. в разделе [теги вывода речи](pit-tag.md).

 

 




