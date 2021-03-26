---
description: Палитры полутонов предназначены для использования всякий раз, когда режим растяжения в контексте устройства установлен в ПОЛУТОНА.
ms.assetid: ee171379-2ab3-4c38-8e86-ff80fa63a357
title: Палитра полутонов и настройка цвета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e6708aff92387b792424f07e9b82a1f6125ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544479"
---
# <a name="halftone-palette-and-color-adjustment"></a>Палитра полутонов и настройка цвета

Палитры полутонов предназначены для использования всякий раз, когда режим растяжения в контексте устройства установлен в ПОЛУТОНА. Приложение создает палитру полутонов с помощью функции [**креатехалфтонепалетте**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) . Приложение должно выбрать и реализовать эту палитру в контексте устройства перед вызовом функции [**стретчблт**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) или [**стретчдибитс**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) .

Система автоматически корректирует входной цвет исходных битовых рисунков каждый раз, когда приложения вызывают функции [**стретчблт**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) и [**стретчдибитс**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) , а режим растяжения контекста устройства установлен в полутона. Эти корректировки цвета влияют на определенные атрибуты изображения, такие как контрастность и яркость. Приложение может задать значения коррекции цвета с помощью функции [**сетколораджустмент**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) . Приложение может извлекать значения коррекции цвета для указанного контекста устройства с помощью функции [**жетколораджустмент**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) .

 

 



