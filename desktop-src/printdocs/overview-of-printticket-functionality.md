---
description: Этот обзор функций PrintTicket описывает формат для задания сведений о конфигурации устройства и использования PrintTicket.
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: Обзор функций PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90aa6f967f5fce25977b52a4d0bec7e9e1ea705
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408547"
---
# <a name="overview-of-printticket-functionality"></a>Обзор функций PrintTicket

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

PrintTicket использует формат на основе XML для представления сведений о конфигурации устройства с помощью конструкций функций, параметров и параметров платформы схемы печати. Сюда входят все стандартные типы элементов, а также возможности расширяемости платформы схемы печати. Предполагается, что PrintTicket является автономным описанием того, как обрабатывается одна страница. Действия, связанные с извлечением и созданием такого элемента PrintTicket из определенного формата документа, здесь не рассматриваются.

PrintTicket можно использовать для получения документа PrintCapabilities, описывающего характеристики устройства для конкретной конфигурации. Кроме того, PrintTicket можно отправить с помощью набора инструкций по подготовке к просмотру, чтобы получить страницу выходных данных, отображаемых и обработанных в соответствии с конфигурацией, указанной в PrintTicket.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



