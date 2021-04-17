---
title: Свойство "шаг"
description: Свойство "шаг"
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 998ee4bcf77878062425086d67066040f5d58421
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411403"
---
# <a name="pitch-property"></a>Свойство "шаг"

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Nописание** 
</dt> <dd>

Возвращает длинное целое число для заданного параметра продачи речевого вывода символа (TTS).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("*** чарактерид * * *"). Тон**

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это свойство применяется только к символам, настроенным для вывода TTS. Если символ не поддерживает вывод TTS, это свойство возвращает ноль (0).

Несмотря на то, что приложение не может записать это значение, можно включить в выходной текст Теги « **смолой** » (высота), которые будут временно увеличивать шаг для конкретного utterance. Однако использование тега **смолой** для изменения высоты не приведет к изменению значения свойства **шаг** . Дополнительные сведения см. в разделе [теги вывода речи](pit-tag.md).

 

 




