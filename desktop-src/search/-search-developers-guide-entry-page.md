---
description: Сторонние лица могут создавать приложения, которые запрашивают в индексе данные программным способом и могут расширять возможности поиска Windows для индексирования данных из пользовательских форматов файлов и хранилищ данных.
ms.assetid: 70046df0-ce48-472d-b24b-8231ea3a43c0
title: Руководством разработчика Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61593f47e081059966936a99a7d2baea114df92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497085"
---
# <a name="windows-search-developers-guide"></a>Руководством разработчика Windows Search

Сторонние лица могут создавать приложения, которые запрашивают в индексе данные программным способом и могут расширять возможности поиска Windows для индексирования данных из пользовательских форматов файлов и хранилищ данных. Для создания приложений Windows Search сторонние разработчики должны сначала реализовать хранилище данных оболочки, чтобы добиться разумного взаимодействия с пользователем. Дополнительные сведения см. [в разделе Реализация базовых интерфейсов объекта папки](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Кроме того, необходимо загрузить [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) для библиотек поиска Windows. [Примеры пакета SDK для Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) содержат полезные примеры кода и сборку взаимодействия для разработки с управляемым кодом. Дополнительные сведения об использовании примеров кода см. в статье [примеры кода для поиска Windows](-search-3x-wds-sampleentry.md).

Этот раздел организован следующим образом:

- [Управление индексом](-search-3x-wds-mngidx-overview.md)
- [Отправка программных запросов к индексу](-search-3x-wds-qryidx-overview.md)
- [Расширение индекса](-search-3x-wds-extidx-overview.md)
- [Расширение языковых ресурсов](extending-language-resources-in-windows-search.md)

## <a name="additional-resources"></a>Дополнительные ресурсы

- Сведения о поддерживаемых сообществом досках сообщений и обсуждениях по технологиям поиска см. на [форуме MSDN: Разработка Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
- Чтобы скачать примеры кода поиска, выполните следующие действия.
  - [Примеры поиска Windows](-search-samples-ovw.md)
- Чтобы скачать Windows SDK, выполните следующие действия.
  - Для Windows 10: [пакет SDK для Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk)
  - Для Windows 7: [Windows SDK для Windows 7 и платформа .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

## <a name="related-topics"></a>См. также

[Обзор Windows Search](-search-3x-wds-overview.md)

[Справочник по поиску Windows](-search-reference-entry-page.md)

[Примеры кода для поиска Windows](-search-samples-ovw.md)

[Федеративный поиск в Windows](-search-federated-search-overview.md)

[Связанные технологии поиска](-search-3x-wds-sampleentry.md)

[Глоссарий поиска Windows](search-glossary.md)
