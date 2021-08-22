---
description: В этом разделе приводятся общие сведения, необходимые для реализации, расширения и тестирования обработчиков протоколов.
ms.assetid: c76d5c82-d62b-4dd4-9743-9572be61e2be
title: разработка обработчиков протоколов для Windows поиска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ef01d36e565471756ee9d6680833401054a6e29b9c570dad7852d316797067
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597834"
---
# <a name="developing-protocol-handlers-for-windows-search"></a>разработка обработчиков протоколов для Windows поиска

В этом разделе приводятся общие сведения, необходимые для реализации, расширения и тестирования обработчиков протоколов.

-   [Основные сведения о обработчиках протоколов](-search-3x-wds-extidx-prot-implementing.md)
-   [Уведомление индекса изменений](-search-3x-wds-notifyingofchanges.md)
-   [Добавление значков и контекстных меню](-search-3x-wds-ph-ui-extensions.md)
-   [Пример кода: расширения оболочки для обработчиков протоколов](-search-3x-wds-ph-ui-samplecode.md)
-   [Установка и регистрация обработчиков протоколов](-search-3x-wds-ph-install-registration.md)
-   [Создание соединителя поиска для обработчика протокола](-search-3x-wds-ph-search-connector.md)
-   [Обработчики протокола отладки](-search-ws-protocolhandlertesting.md)

## <a name="additional-resources"></a>Дополнительные ресурсы

Общие сведения об индексировании см. в следующих разделах:

-   Общие сведения о процессе индексирования см. [в разделе процесс индексирования](-search-indexing-process-overview.md).
-   чтобы расширить Windows поиск для индексирования содержимого и свойств новых форматов файлов и хранилищ данных, см. раздел [расширение индекса](-search-3x-wds-extidx-overview.md).
-   Обзоры диспетчера каталога и диспетчера поиска в каталоге (CSM) см. в разделе [Использование диспетчера каталогов](-search-3x-wds-mngidx-catalog-manager.md) и [диспетчера области сканирования](-search-3x-wds-extidx-csm.md).

Основные сведения о типах файлов и обработчиках см. в следующих разделах:

-   Сведения о расширении оболочки с помощью обработчиков типов файлов см. в разделе [Создание обработчиков расширений оболочки](../shell/handlers.md).
-   Основные сведения о обработчиках фильтров см. в разделе [Разработка обработчиков фильтров](-search-ifilter-conceptual.md).
-   Сведения о создании обработчиков см. [в статьях введение в сопоставления файлов](../shell/fa-intro.md), [Регистрация расширений оболочки](../shell/reg-shell-exts.md), [Создание обработчиков расширений оболочки](../shell/handlers.md), [контекстное меню](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))и [обработчики просмотра](../shell/preview-handlers.md).

Дополнительные сведения о связанных технологиях и реализации хранилища данных см. в следующих разделах:

-   Windows обработчики протоколов поиска используют спецификации проектирования, аналогичные SharePoint Server. они часто взаимозаменяемы. дополнительные сведения см. в разделе [центр разработчиков SharePoint Server](https://developer.microsoft.com/office/docs).
-   в Windows 7 и более поздних версиях SharePoint search Server 2008 и MOSS 2007 SP2 также поддерживают федеративный поиск. дополнительные сведения об федеративного поиска и развертывании search Server 2008 с помощью Office SharePoint Server 2007 см. в статье [федеративный поисковый \[ сервер search server 2008 \] ](/previous-versions/office/bb931109(v=office.14)).
-   Сведения о создании хранилища данных оболочки см. в разделе [реализация базовых интерфейсов объекта папки](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Примеры кода см. на следующих страницах портала:

-   примеры кода поиска см. в разделе [примеры SDK для Windows поиска](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).
-   Примеры кода оболочки см. в разделе [примеры пакетов SDK](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85))для оболочки.

 

 
