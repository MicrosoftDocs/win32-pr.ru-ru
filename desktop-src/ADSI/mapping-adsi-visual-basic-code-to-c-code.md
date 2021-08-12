---
title: сопоставление кода Visual Basic ADSI с кодом C++
description: Интерфейсы ADSI состоят из более чем 50 интерфейсов.
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a924f403dcbdbe89b1b0bbf846c95223b401a04d1925ce9362a5300faf828fe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179211"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a>сопоставление кода Visual Basic ADSI с кодом C++

Интерфейсы ADSI состоят из более чем 50 интерфейсов. Большинство операций с каталогами можно выполнить, используя только пять интерфейсов. К ним относятся:

-   [**иадсопендсобжект**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)
-   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

В следующей таблице перечислены сопоставления из кода ADSI VB/VBS с кодом C++. Имейте в виду, что это не полный список.



| Код VBS                           | Код VC                                                               |
|------------------------------------|-----------------------------------------------------------------------|
| Set obj = GetObject ()              | HR = Адсжетобжект ()                                                   |
| расширением. Установите obj. Получить obj. Источника         | IADs или Идиректорйобжект                                              |
| расширением. Создайте obj. Удалить obj. мовехере | иадсконтаинер                                                         |
| Для каждого... в...                      | Адсбуилденумератор () Адсенумератенекст ()                               |
| Подключение, команда, набор записей     | IDirectorySearch                                                      |
| Дескриптор безопасности, ACL, ACE      | Иадссекуритидескриптор, Иадсакцессконтроллист, Иадсакцессконтролентри |



 

 

 




