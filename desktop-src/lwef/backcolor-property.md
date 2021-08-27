---
title: свойство backcolor (устаревшие функции Windows среды)
description: Свойство BackColor
ms.assetid: a82c23bc-b280-4a52-9272-68879557cac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f799e8b9e00a97770cd004e29df75da8345a6cc01531fce53079ea550402c68d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114814"
---
# <a name="backcolor-property-legacy-windows-environment-features"></a>свойство backcolor (устаревшие функции Windows среды)

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает цвет фона, который в данный момент отображается в окне всплывающей подсказки для указанного символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("**_чарактерид_*_"). Выноски. BackColor_*

</dd> </dl>

## <a name="remarks"></a>Remarks

Допустимый диапазон для обычного цвета RGB — от 0 до 16 777 215 (&ХФФФФФФ). Старший байт числа в этом диапазоне равен 0; 3 младших байта, от минимума до наиболее значимого байта, определяют величину красного, зеленого и синего соответственно. Интенсивность красного, зеленого и синего компонентов выражается числом от 0 до 255 (&HFF).

 

 




