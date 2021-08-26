---
title: Свойство ForeColor
description: Свойство ForeColor
ms.assetid: b5cef81b-55e1-49a5-bdbf-f7101520a13a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cebfc7f0b64a43f7ccb9075426a75df9a777fbb8b1e5e94cb16e747e0681cb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962764"
---
# <a name="forecolor-property"></a>Свойство ForeColor

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает цвет переднего плана, который в данный момент отображается в окне всплывающего окна для указанного символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("**_чарактерид_*_"). Всплывающее сообщение. ForeColor_*

</dd> </dl>

## <a name="remarks"></a>Remarks

Свойство **ForeColor** возвращает значение, определяющее цвет текста в выноске слова. Допустимый диапазон для обычного цвета RGB — от 0 до 16 777 215 (&ХФФФФФФ). Старший байт числа в этом диапазоне равен 0; 3 младших байта, от минимума до наиболее значимого байта, определяют величину красного, зеленого и синего соответственно. Интенсивность красного, зеленого и синего компонентов выражается числом от 0 до 255 (&HFF).

 

 




