---
title: Свойство BackColor (устаревшие функции среды Windows)
description: Свойство BackColor
ms.assetid: a82c23bc-b280-4a52-9272-68879557cac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332fcc6a9081b52300dbee4c69c77602e84a62e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800892"
---
# <a name="backcolor-property-legacy-windows-environment-features"></a>Свойство BackColor (устаревшие функции среды Windows)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает цвет фона, который в данный момент отображается в окне всплывающей подсказки для указанного символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("**_чарактерид_*_"). Выноски. BackColor_*

</dd> </dl>

## <a name="remarks"></a>Комментарии

Допустимый диапазон для обычного цвета RGB — от 0 до 16 777 215 (&ХФФФФФФ). Старший байт числа в этом диапазоне равен 0; 3 младших байта, от минимума до наиболее значимого байта, определяют величину красного, зеленого и синего соответственно. Интенсивность красного, зеленого и синего компонентов выражается числом от 0 до 255 (&HFF).

 

 




