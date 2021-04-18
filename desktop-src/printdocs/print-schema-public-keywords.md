---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: Общие ключевые слова схемы печати
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3e8fb9a46bbed2b135f4e81456dd65e79be830
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105651248"
---
# <a name="print-schema-public-keywords"></a>Общие ключевые слова схемы печати

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

В следующем разделе указываются открытые ключевые слова, которые определены для схемы печати.

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a>Вывод сведений об использовании общих ключевых слов схемы для возможностей печати

Ключевые слова, указанные в разделе PrintCapabilities Public Keywords, могут отображаться в документе возможностей печати. Дополнительные сведения о взаимодействии этих ключевых слов с технологией PrintCapabilities см. в разделе [Обзор раздела PrintCapabilities](overview-of-the-printcapabilities.md) .

Общедоступные ключевые слова, относящиеся к PrintTicket, не должны отображаться в документе PrintCapabilities.

## <a name="print-schema-public-keywords-usage-for-printticket"></a>Вывод сведений об использовании общедоступных ключевых слов схемы для PrintTicket

Ключевые слова, указанные в разделе PrintTicket Public Keywords, могут присутствовать в PrintTicket. Ключевые слова PrintTicket реализуются как тип элемента свойства. Дополнительные сведения о взаимодействии этих ключевых слов с технологией PrintTicket см. в разделе [сведения о конфигурации, не связанные с PrintCapabilities](configuration-information-not-related-to-printcapabilities.md) .

Ключевые слова, указанные в разделе PrintCapabilities Public Keywords, могут отображаться в PrintTicket в зависимости от реализации PrintTicket в приложении и (или) драйвере. Это позволяет выбирать атрибуты устройств, определенные в документе PrintCapabilities. Дополнительные сведения о взаимодействии между ключевыми словами PrintCapabilities и PrintTicket см. в разделе [назначение PrintTicket](purpose-of-the-printticket.md) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



