---
description: Элемент управления InkPicture можно использовать для визуализации рукописного ввода на Microsoft Windows 2000, Windows Server 2003 и в выпусках Windows XP, отличных от планшетных ПК. Однако нельзя использовать элемент управления для ввода рукописного ввода в этих операционных системах.
ms.assetid: e5d00b0f-0a4f-4ea2-ae63-dfb6bc8c2caf
title: Использование функции InkPicture в более ранних версиях Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbd2bf8545524787c9e37f70c43d954ab440910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710983"
---
# <a name="using-inkpicture-on-earlier-versions-of-windows"></a>Использование функции InkPicture в более ранних версиях Windows

[Элемент управления InkPicture](inkpicture-control.md) можно использовать для визуализации рукописного ввода на Microsoft Windows 2000, windows Server 2003 и в выпусках Windows XP, отличных от планшетных ПК. Однако нельзя использовать элемент управления для ввода рукописного ввода в этих операционных системах.

Свойство [**инкенаблед**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) элемента управления имеет значение **false**, и попытка изменить свойство не оказывает никакого влияния. Можно назначать значения другим свойствам и программно манипулировать рукописным вводом, но нельзя использовать элемент управления для получения рукописных данных.

 

 



