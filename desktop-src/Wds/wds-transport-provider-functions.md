---
title: Функции поставщика транспорта WDS
description: Пользовательские поставщики содержимого могут предоставлять следующие функции обратного вызова серверу многоадресной рассылки.
ms.assetid: 30ec1969-4e90-458e-8a9f-39a7bbf4cd79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1044c923226dcc618e816219dcec9d7edf78855e03acf13b76ba4d7ed9ad15a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053262"
---
# <a name="wds-transport-provider-functions"></a>Функции поставщика транспорта WDS

Пользовательские поставщики содержимого могут предоставлять следующие функции обратного вызова серверу многоадресной рассылки.



| Функция                                                                               | Описание                                                                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [*вдстранспортпровидерклосеконтент*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderclosecontent)             | Закрывает поток содержимого, указанный в маркере.                                                                          |
| [*вдстранспортпровидерклосеинстанце*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercloseinstance)           | Закрывает экземпляр поставщика содержимого, указанный в маркере.                                                         |
| [*вдстранспортпровидеркомпареконтент*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercomparecontent)         | Сравнивает указанное имя и экземпляр содержимого с открытым потоком содержимого, чтобы определить, совпадают ли они.             |
| [*вдстранспортпровидеркреатеинстанце*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercreateinstance)         | Открывает новый экземпляр поставщика содержимого.                                                                             |
| [*вдстранспортпровидердумпстате*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderdumpstate)                   | Указывает поставщику транспорта распечатать сводку состояния и другие важные сведения в журнале трассировки. |
| [*вдстранспортпровидержетконтентметадата*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentmetadata) | Извлекает метаданные для открытого потока содержимого.                                                                          |
| [*вдстранспортпровидержетконтентсизе*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentsize)         | Возвращает размер открытого потока содержимого.                                                                           |
| [*вдстранспортпровидеринитиализе*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)                 | Инициализирует поставщик содержимого.                                                                                         |
| [*вдстранспортпровидеропенконтент*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent)               | Открывает новое статическое представление потока содержимого.                                                                            |
| [*вдстранспортпровидерреадконтент*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderreadcontent)               | Считывает содержимое из открытого потока содержимого.                                                                              |
| [*вдстранспортпровидеррефрешсеттингс*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderrefreshsettings)       | Предписывает поставщику транспорта пересчитать все необходимые параметры.                                                       |
| [*вдстранспортпровидершутдовн*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidershutdown)                     | Шутсдовн поставщика содержимого.                                                                                         |
| [*вдстранспортпровидерусеракцессчекк*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideruseraccesscheck)       | Указывает доступ к потоку содержимого на основе маркера пользователя.                                                           |



 

 

 




