---
description: элемент управления InkPicture можно использовать для визуализации рукописного ввода на Microsoft Windows 2000, Windows Server 2003 и в выпусках, отличных от планшетных пк Windows XP. Однако нельзя использовать элемент управления для ввода рукописного ввода в этих операционных системах.
ms.assetid: e5d00b0f-0a4f-4ea2-ae63-dfb6bc8c2caf
title: Использование функции InkPicture в более ранних версиях Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52423e8eb3e4c7f59da7a7caac299428dd8efcdce2192819444bfe91070f10b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091363"
---
# <a name="using-inkpicture-on-earlier-versions-of-windows"></a>Использование функции InkPicture в более ранних версиях Windows

[элемент управления InkPicture](inkpicture-control.md) можно использовать для визуализации рукописного ввода на Microsoft Windows 2000, Windows Server 2003 и в выпусках, отличных от планшетных пк Windows XP. Однако нельзя использовать элемент управления для ввода рукописного ввода в этих операционных системах.

Свойство [**инкенаблед**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) элемента управления имеет значение **false**, и попытка изменить свойство не оказывает никакого влияния. Можно назначать значения другим свойствам и программно манипулировать рукописным вводом, но нельзя использовать элемент управления для получения рукописных данных.

 

 



