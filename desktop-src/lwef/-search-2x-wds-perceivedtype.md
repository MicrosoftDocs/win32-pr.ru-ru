---
title: Распознанные типы (устаревшие функции среды Windows)
description: PerceivedType — это свойство, которое классифицирует элемент в индексе.
ms.assetid: 47a5cf55-79f6-48e7-a585-72fc3d7d53d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afaf7d8b827495a94b441e5504762dd53dbe733c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105691746"
---
# <a name="perceived-types-legacy-windows-environment-features"></a>Распознанные типы (устаревшие функции среды Windows)

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте вместо этого [Поиск Windows](../search/-search-3x-wds-overview.md) .

`PerceivedType` свойство, которое классифицирует элемент в индексе. Эта классификация отличается от классификации "тип", используемой [расширенным синтаксисом запросов](-search-2x-wds-aqsreference.md) , но также позволяет пользователям уточнять результаты поиска. Тип АКС позволяет пользователям ограничить поисковый запрос, тогда как свойство PerceivedType позволяет пользователям фильтровать свои результирующие наборы.

## <a name="types"></a>Типы

Используйте свойство PerceivedType для классификации типа файлов, чтобы пользователи могли фильтровать результаты поиска по типу. Выходные данные должны быть одной из следующих строк:

-   contact
-   IP-адресу (DIP)
-   связь и электронная почта
-   связь и календарь
-   связь/задача
-   Обмен данными и обмен мгновенными сообщениями
-   документ
-   документ/Примечание
-   документ/текст
-   документ/электронная таблица
-   документ/презентация
-   music
-   images
-   изображения и рисунки
-   изображения и видео
-   folder
-   программа

Например, если требуется создать надстройку фильтра для нового типа файла изображений, в интерфейсе [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)необходимо реализовать следующее:

-   Для возврата **блока** фуллпропспек, включающего: D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType
-   **GetValue** возвращает пропвариант, включающий: VT \_ LPWSTR = "Images/Picture"

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[Разработка надстроек IFilter](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Разработка обработчиков протоколов](-search-2x-wds-phaddins.md)
</dt> <dt>

[Синтаксис расширенных запросов](-search-2x-wds-aqsreference.md)
</dt> <dt>

[счематабле](-search-2x-wds-schematable.md)
</dt> </dl>

 

 
