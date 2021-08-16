---
description: существует несколько способов использования Windows поиска для запроса индекса.
ms.assetid: 2c161b7f-4e28-4e8a-add6-3c1cda00a622
title: Отправка программных запросов к индексу
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76f98d12e4a0615bf19dfb165766a67b8c9e58700ad2d0c897782e2a16ba9dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094945"
---
# <a name="querying-the-index-programmatically"></a>Отправка программных запросов к индексу

существует несколько способов использования Windows поиска для запроса индекса.

В этом разделе представлена концептуальная платформа для выполнения запросов к индексу программным способом.

-   [использование SQL и подходов акс для запроса индекса](using-sql-and-aqs-to-query-the-index.md)
-   [Запрос индекса с помощью Исеарчкуерихелпер](-search-3x-wds-qryidx-searchqueryhelper.md)
-   [Запрос индекса с помощью протокола Search-MS](-search-3x-wds-qryidx-searchms.md)
-   [запрос к индексу с помощью Windows поискового синтаксиса SQL](-search-sql-windowssearch-entry.md)
-   [Использование расширенного синтаксиса запросов программными средствами](-search-3x-advancedquerysyntax.md)

> [!Note]  
> устаревшая совместимость Microsoft Windows Desktop Search (WDS) 2x: на компьютерах под управлением Windows XP и более поздних версий [**исеарчдесктоп**](/previous-versions//aa965729(v=vs.85)) не рекомендуется. вместо этого разработчики должны использовать [**исеарчкуерихелпер**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) для получения строки подключения и анализа запроса пользователя в язык SQL (SQL), а затем выполнить запрос через связывание объектов и внедрение базы данных (OLE DB).

 

## <a name="additional-resources"></a>Дополнительные ресурсы

-   Дополнительные сведения о OLE DB см. в разделе [Общие сведения о программировании OLE DB](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx). сведения о поставщике данных платформа .NET Framework для OLE DB см. в разделе [пространство имен System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1).
-   Дополнительные сведения об использовании свойств в запросах см. в следующих разделах:
    -   [Система свойств](../properties/building-property-handlers.md)
    -   [Свойства системы](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
-   Сведения о создании и изменении папок поиска см. в разделе [**интерфейс исеарчфолдеритемфактори**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory).
-   сведения о поддерживаемых сообществом досках сообщений и обсуждениях по технологиям поиска см. на [форуме MSDN: Windows разработке настольных систем](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
-   Чтобы скачать примеры кода пакета SDK для поиска, выполните следующие действия.
    -   для Windows 7: [Windows примеры поиска на GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)
    -   для Windows Vista: [примеры пакета SDK для Windows поиска](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
-   чтобы скачать Windows SDK, выполните следующие действия.
    -   для Windows 7: [Windows SDK для Windows 7 и платформа .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
    -   для Windows vista: [Windows SDK для Windows vista и платформа .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Windows Поиск по руководству по разработке](-search-developers-guide-entry-page.md)
</dt> <dt>

[Управление индексом](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[расширение индекса поиска Windows](-search-3x-wds-extidx-overview.md)
</dt> <dt>

[Расширение языковых ресурсов](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
