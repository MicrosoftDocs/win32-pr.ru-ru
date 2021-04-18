---
description: Внедренный объект — это объект класса, который существует в объявлении класса или экземпляра другого класса.
ms.assetid: 11a4556b-f682-4850-aedc-793602c5745b
ms.tgt_platform: multiple
title: Внедрение объектов в класс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b94296a6869dddca7fd3df08739615a4a0c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712547"
---
# <a name="embedding-objects-in-a-class"></a>Внедрение объектов в класс

Внедренный объект — это объект класса, который существует в объявлении класса или экземпляра другого класса. Например, класс [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) содержит внедренные [**объекты \_ доверенного лица Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) . Каждый из объектов **\_ доверенного лица Win32** содержит [**объект \_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) . Инструментарий WMI не ограничивает глубину, до которой класс может иметь внедренные объекты. Однако использование другой структуры, например создание класса взаимосвязей, может сделать более управляемой схему.

Дополнительные сведения о внедренных объектах см. в следующих разделах:

-   [Создание внедренных объектов](creating-embedded-objects.md)
-   [Запрос внедренных объектов](querying-embedded-objects.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Разработка классов MOF-файл (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
