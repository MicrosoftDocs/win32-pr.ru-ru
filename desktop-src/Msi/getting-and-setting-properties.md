---
description: Чтобы использовать свойства в установке служб, можно получать и устанавливать значения свойств из программ, использующих MsiGetProperty и MsiSetProperty, и включать их как часть условных операторов в базу данных установки.
ms.assetid: 65fe46d7-16b6-46ef-a440-73f954b03105
title: Получение и задание свойств (установщик Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0154b84af656d295b9fa84ebcca881eab1c288f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910947"
---
# <a name="getting-and-setting-properties-windows-installer"></a>Получение и задание свойств (установщик Windows)

Чтобы использовать [Свойства](properties.md) в установке служб, можно получать и устанавливать значения свойств из программ, использующих [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) и [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) , и включать их как часть условных операторов в базу данных установки.

-   Чтобы получить текущее свойство, вызовите функцию [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) .
-   Чтобы получить текущее состояние установки, вызовите функцию [**мсижетмоде**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) .
-   Чтобы получить язык для текущей установки, вызовите функцию [**мсижетлангуаже**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) .
-   Чтобы задать свойство, вызовите функцию [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) .
-   Чтобы задать состояние установки, вызовите функцию [**мсисетмоде**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) .
-   Чтобы очистить свойство (присвоив ему значение null), задайте в качестве значения свойства пустую строку: "".

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование свойств](using-properties.md)
</dt> <dt>

[Установка значений открытых свойств в командной строке](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[Очистка свойства установщика](clearing-an-installer-property.md)
</dt> </dl>

 

 



