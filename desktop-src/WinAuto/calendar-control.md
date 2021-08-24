---
title: Элемент управления Calendar (Справочник по элементам пользовательского интерфейса MSAA)
description: Элементы управления "Календарь" предоставляют пользователю простой и интуитивно понятный способ выбора даты из привычного интерфейса.
ms.assetid: cfb1e420-bb8f-4100-9c83-304d11573c0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f41daf9e86f178f4b22a7908e4d9d10d1dab1a2f867ca2d09c62d111cbc806
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899562"
---
# <a name="calendar-control-msaa-ui-element-reference"></a>Элемент управления Calendar (Справочник по элементам пользовательского интерфейса MSAA)

> [!Note]  
> В этом разделе описываются **управляющие объекты календаря** в целях справочника по элементам ПОЛЬЗОВАТЕЛЬСКОГО интерфейса MSAA. Создание **управляющих объектов календаря** в различных ПЛАТФОРМАХ пользовательского интерфейса не описывается здесь. См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.

 

Элементы управления "Календарь" предоставляют пользователю простой и интуитивно понятный способ выбора даты из привычного интерфейса.

Имя класса окна для элемента управления "календарь месяца" — это \_ класс монскал, который определен как "SysMonthCal32" в коммктрл. h. Сведения в этом разделе относятся к элементу управления "Календарь на месяц" в версии 5 файла Коммктрл. h.

## <a name="iaccessible-methods"></a>Методы IAccessible

Элементы управления Calendar поддерживают следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Свойства IAccessible

Элементы управления Calendar поддерживают следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Свойство                                                                 | Примечания                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**получить \_ аккчилдкаунт**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Свойство **ChildCount** равно нулю.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**получить \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**получить \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | Свойство **Name** получается из статического текстового элемента управления, который помечает элемент управления Calendar. При создании элементов управления разработчики сервера должны убедиться, что статический текстовый элемент управления непосредственно предшествует элементу управления, который он помечает в последовательности табуляции.                                                                                                                                                                                                                 |
| [**получить \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | **Родительское** свойство является окном ( [**\_ \_ окно системы ролей**](object-roles.md) ), которое окружает элемент управления и имеет **то же имя** свойства и класса окна, что и элемент управления.                                                                                                                                                                                                                                                             |
| [**получить \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | Свойство **Role** является [**\_ \_ клиентской системой роли**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                               |
| [**получить \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | Свойство **State** представляет собой сочетание одной или нескольких следующих значений: системная [](object-state-constants.md)[**\_ \_ невидимая**](object-state-constants.md) система состояний \| [**\_ \_ недоступна**](object-state-constants.md) система состояний, \| [**\_ \_ сфокусированная**](object-state-constants.md) на \| [**\_ системе \_ состояния**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Интерфейс IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





