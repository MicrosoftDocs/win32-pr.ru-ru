---
description: Windows Search предоставляет функции обхода содержимого и поиска, поддерживающие полнотекстовый поиск. Язык запросов, используемый службой поиска Windows, расширяет стандартный синтаксис запросов базы данных SQL-92 и SQL-99, что позволяет повысить его полезность при поиске на основе текста.
ms.assetid: a2eb550a-bb55-4dbd-9ca1-60b776eb9339
title: Запрос к индексу с помощью синтаксиса SQL для поиска Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5696891b14340e8d8fe97f0c0cfbdc75db08e464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497061"
---
# <a name="querying-the-index-with-windows-search-sql-syntax"></a>Запрос к индексу с помощью синтаксиса SQL для поиска Windows

Windows Search предоставляет функции обхода содержимого и поиска, поддерживающие полнотекстовый поиск. Язык запросов, используемый службой поиска Windows, расширяет стандартный синтаксис запросов базы данных SQL-92 и SQL-99, что позволяет повысить его полезность при поиске на основе текста.

Все функции Windows Search язык SQL (SQL) совместимы с Windows Search в Windows Vista и более поздних версий, включая все версии Windows 10.

Этот раздел содержит общие сведения о синтаксисе SQL в Windows Search и содержит следующие разделы:

- [Общие сведения о синтаксисе SQL для службы поиска Windows](-search-sql-ovwofsearchquery.md)
- [Общие сведения о языке запросов](-search-sql-generalqueryinfo.md)
- [ГРУППИРОВАТЬ ПО... Поверх... Баланс](-search-sql-group-on-over.md)
- [Инструкция SELECT](-search-sql-select.md)
- [Предложение FROM](-search-sql-from.md)
- [Предложения WHERE](-search-sql-where.md)
- [Предложение ORDER BY](-search-sql-orderby.md)
- [РАНЖИРОВАНие по предложению](-search-sql-rankby.md)
- [Инструкция SET](-search-sql-set.md)
- [Свойства набора строк](-search-sql-rowset-properties.md)

В этой документации предполагается, что вы знакомы с связыванием объектов и внедрением базы данных (OLE DB) и SQL.

## <a name="code-samples"></a>Примеры кода

В примере кода ВССКЛ показано, как взаимодействовать между Microsoft OLE DB и Windows Search через SQL. В примере кода Всоледб показана библиотека ATL OLE DB доступ к приложениям поиска Windows, а также два дополнительных метода получения результатов из службы поиска Windows. Оба образца доступны в [примерах Windows Search](-search-samples-ovw.md) и [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)

## <a name="related-topics"></a>См. также

[Отправка программных запросов к индексу](-search-3x-wds-qryidx-overview.md)

[Использование методов SQL и АКС для запроса индекса](-search-3x-wds-qryidx-overview.md)

[Запрос индекса с помощью Исеарчкуерихелпер](-search-3x-wds-qryidx-searchqueryhelper.md)

[Запрос индекса с помощью протокола Search-MS](-search-3x-wds-qryidx-searchms.md)

[Запрос к индексу с помощью синтаксиса SQL для поиска Windows](-search-sql-windowssearch-entry.md)

[Использование расширенного синтаксиса запросов программными средствами](-search-3x-advancedquerysyntax.md)
