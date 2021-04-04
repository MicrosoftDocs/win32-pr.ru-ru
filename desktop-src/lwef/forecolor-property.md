---
title: Свойство ForeColor
description: Свойство ForeColor
ms.assetid: b5cef81b-55e1-49a5-bdbf-f7101520a13a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef05c9f51e040326c75f142e4649a8dbd0cfdbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887868"
---
# <a name="forecolor-property"></a>Свойство ForeColor

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает цвет переднего плана, который в данный момент отображается в окне всплывающего окна для указанного символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("*** чарактерид * * *"). Всплывающее сообщение. ForeColor**

</dd> </dl>

## <a name="remarks"></a>Комментарии

Свойство **ForeColor** возвращает значение, определяющее цвет текста в выноске слова. Допустимый диапазон для обычного цвета RGB — от 0 до 16 777 215 (&ХФФФФФФ). Старший байт числа в этом диапазоне равен 0; 3 младших байта, от минимума до наиболее значимого байта, определяют величину красного, зеленого и синего соответственно. Интенсивность красного, зеленого и синего компонентов выражается числом от 0 до 255 (&HFF).

 

 




