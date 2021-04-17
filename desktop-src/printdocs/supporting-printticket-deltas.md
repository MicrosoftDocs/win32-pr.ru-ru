---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Поддержка разностей PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730c8d32d881dd30a6ab57b88d8fc1dfa87eee7a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703525"
---
# <a name="supporting-printticket-deltas"></a>Поддержка разностей PrintTicket

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

В интерфейсе поставщика PrintTicket есть методы, которые можно использовать для внесения добавочных изменений в существующий PrintTicket. Добавочные изменения PrintTicket можно указать в частичном PrintTicket, который называется разностью PrintTicket. Пересмотренный объект PrintTicket создается путем объединения дельты PrintTicket с существующим PrintTicket. Дополнительные сведения о методах, включающих изменения PrintTicket, см. в этом документе.

При обработке разностной учетной операции PrintTicket необходимо выполнить следующие шаги.

1.  Определение экземпляров функций или Параметеринит, общих для существующего объекта PrintTicket (целевой PrintTicket) и дельты PrintTicket.

    -   Для каждого компонента, общего для целевого объекта PrintTicket и разностного изменения PrintTicket, замените функцию в целевом объекте PrintTicket соответствующей функцией в Дельта PrintTicket.

    -   Для каждого Параметеринит, общего для целевого объекта PrintTicket и разностного изменения PrintTicket, замените Параметеринит в целевом объекте PrintTicket соответствующим Параметеринит в Дельта PrintTicket.

2.  Скопируйте все оставшиеся экземпляры компонента и Параметеринит в Дельта PrintTicket в целевой объект PrintTicket.

3.  Если алгоритм разрешения конфликтов позволяет указать приоритеты в самом PrintTicket, вы можете повысить приоритетность компонента и экземпляров Параметеринит, имена которых указаны в Дельта PrintTicket.

4.  Выполните проверку PrintTicket, как описано в [контрольном списке PrintTicket](printticket-validation-checklist.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



