---
description: Пакет SDK для Windows Search предоставляет сборку взаимодействия для работы с COM-объектами, предоставляемыми средствами поиска Windows и другими программами с интерфейсами и классами с помощью управляемого кода.
ms.assetid: 9ade6f55-de65-4f73-9d22-1be819549704
title: Использование управляемого кода с данными оболочки и Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0a4c0f4182739fe553c21b45bcfc3a3af7a68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144188"
---
# <a name="using-managed-code-with-shell-data-and-windows-search"></a>Использование управляемого кода с данными оболочки и Windows Search

Пакет SDK для Windows Search предоставляет сборку взаимодействия для работы с COM-объектами, предоставляемыми средствами поиска Windows и другими программами с интерфейсами и классами с помощью управляемого кода. Сборка взаимодействия подписана цифровой подписью корпорацией Майкрософт и может быть найдена с помощью [примеров поиска Windows](-search-samples-ovw.md).

Этот раздел организован следующим образом:

-   [Использование Windows API Кодепакк](#using-the-windows-api-codepack)
    -   [Доступ к результатам индекса](#accessing-index-results)
    -   [Пример приложения, использующего API Windows Кодепакк](#sample-application-using-the-windows-api-codepack)
-   [См. также](#related-topics)

## <a name="using-the-windows-api-codepack"></a>Использование Windows API Кодепакк

Если вы работаете в среде Microsoft .NET, используйте [пакет кода Windows API для Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) , чтобы получить результаты поиска, или просто просмотрите пространство имен. [Пакет кода Windows API для Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) предоставляет коллекцию элементов оболочки, которые, по сути, являются оболочками для собственного [интерфейса интерфейса IShellItem](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem). Можно выполнить итерацию по этой коллекции и получить различные значения свойств аналогично перечислению результатов в таблице из запроса связывания и внедрения базы данных (OLE DB).

В следующем фрагменте кода показано, как выполнять итерацию по элементам поиска и получать значения свойств для каждого из них.


```
foreach (ShellObject so in KnownFolders.SavedSearches)
{
    searchFolder = new ShellSearchFolder(finalSearchCondition, (ShellContainer)so);
    List<ShellObject> items = new List<ShellObject>();
    foreach (ShellObject so2 in searchFolder) items.Add(so2);   
}
```



### <a name="accessing-index-results"></a>Доступ к результатам индекса

Получить доступ к результатам индекса можно с помощью OLE DB или модели данных оболочки. Оба подхода имеют преимущества и недостатки. Одно из преимуществ заключается в том, что OLE DB и язык SQL (SQL) знакомы программистам баз данных. Другие преимущества — лучше контролировать производительность при запросе только индексатора и доступ к дополнительным функциям, таким как возможность поиска предыдущих результатов в новом наборе строк быстро.

Преимущество модели данных оболочки заключается в том, что она абстрагирует по разным источникам информации, например OpenSearch, и предоставляет доступ к дополнительным функциям, таким как эскизы и обработчики свойств. Кроме того, объектная модель оболочки не требует особой поддержки для таких результатов, как элементы почты и результаты OneNote, а также для любого элемента, находящегося в индексе пользователя. Обратите внимание, что в Shell [кновнфолдерид](../shell/knownfolderid.md) — это область известных папок для локального индексированного содержимого. Дополнительные сведения о создании источника данных оболочки см. в разделе [реализация базовых интерфейсов объекта папки](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Источники данных OpenSearch не предоставляются через OLE DB для федеративного поиска в Windows 7 и более поздних версиях. По этой причине рекомендуется писать поставщик LINQ для пространства имен оболочки вместо того, чтобы использовать OLE DB для доступа к результатам индексатора. Дополнительные сведения см. в разделе [Пошаговое руководство. Создание поставщика LINQ](/previous-versions/bb546158(v=vs.140)), использующего IQueryable.

### <a name="sample-application-using-the-windows-api-codepack"></a>Пример приложения, использующего API Windows Кодепакк

На следующем снимке экрана представлен макет примера приложения, созданного с помощью [пакета кода Windows API для Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).

![снимок экрана приложения проигрывателя мультимедиа, отображающего сообщения электронной почты](images/folderid-searchhome.png)

## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Федеративный поиск в Windows](-search-federated-search-overview.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[Взаимная совместимость кодов на разных языках](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))
</dt> </dl>

 

 
