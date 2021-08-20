---
description: сторонние лица могут создавать приложения, которые запрашивают данные в индексе программным способом и могут расширить Windows поиска для индексирования данных из пользовательских форматов файлов и хранилищ данных.
ms.assetid: 70046df0-ce48-472d-b24b-8231ea3a43c0
title: Windows Поиск по руководству разработчика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84773f23f5e82ce5cbb15c163b0ff2421f9b7c92b18129c9875729be37518b02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117864193"
---
# <a name="windows-search-developers-guide"></a>Windows Поиск по руководству разработчика

сторонние лица могут создавать приложения, которые запрашивают данные в индексе программным способом и могут расширить Windows поиска для индексирования данных из пользовательских форматов файлов и хранилищ данных. чтобы создать приложения поиска Windows, сторонние разработчики должны сначала реализовать хранилище данных оболочки, чтобы обеспечить разумное взаимодействие с пользователем. Дополнительные сведения см. [в разделе Реализация базовых интерфейсов объекта папки](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

кроме того, необходимо скачать [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) для библиотек поиска Windows. [примеры пакета SDK для Windows поиска](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) содержат полезные примеры кода и сборку взаимодействия для разработки с управляемым кодом. дополнительные сведения об использовании примеров кода см. в разделе [Windows поиск примеров кода](-search-3x-wds-sampleentry.md).

Этот раздел организован следующим образом:

- [Управление индексом](-search-3x-wds-mngidx-overview.md)
- [Отправка программных запросов к индексу](-search-3x-wds-qryidx-overview.md)
- [Расширение индекса](-search-3x-wds-extidx-overview.md)
- [Расширение языковых ресурсов](extending-language-resources-in-windows-search.md)

## <a name="additional-resources"></a>Дополнительные ресурсы

- сведения о поддерживаемых сообществом досках сообщений и обсуждениях по технологиям поиска см. на [форуме MSDN: Windows разработке настольных систем](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
- Чтобы скачать примеры кода поиска, выполните следующие действия.
  - [Windows Поиск образцов](-search-samples-ovw.md)
- чтобы скачать Windows SDK, выполните следующие действия.
  - для Windows 10: [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)
  - для Windows 7: [Windows SDK для Windows 7 и платформа .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

## <a name="related-topics"></a>Связанные темы

[Обзор Windows Search](-search-3x-wds-overview.md)

[Windows Поиск ссылки](-search-reference-entry-page.md)

[Windows Поиск примеров кода](-search-samples-ovw.md)

[Федеративный поиск в Windows](-search-federated-search-overview.md)

[Связанные технологии поиска](-search-3x-wds-sampleentry.md)

[Windows Глоссарий поиска](search-glossary.md)
