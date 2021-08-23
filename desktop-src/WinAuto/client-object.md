---
title: Объект Client (Справочник по элементам пользовательского интерфейса MSAA)
description: Клиентская область — это часть окна, в которой приложение отображает выходные данные, такие как текст или графика. Например, приложение для публикации на рабочем столе отображает текущую страницу документа в клиентской области.
ms.assetid: 1b3a800e-e3c1-4737-8ad0-41707eb1e985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33190ebd1013c92a58ecc64b07993a5a5ae1cd842e50c88691295114a128074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645064"
---
# <a name="client-object-msaa-ui-element-reference"></a>Объект Client (Справочник по элементам пользовательского интерфейса MSAA)

Клиентская область — это часть окна, в которой приложение отображает выходные данные, такие как текст или графика. Например, приложение для публикации на рабочем столе отображает текущую страницу документа в клиентской области.

Разработчики серверных приложений несут ответственность за создание специальных объектов, предоставляющих сведения о содержимом клиентской области приложения.

Если клиентское приложение запрашивает сведения о настраиваемом элементе пользовательского интерфейса в приложении и настраиваемом элементе пользовательского интерфейса, который не поддерживает интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , Microsoft Active Accessibility создает объект со специальными возможностями по умолчанию с минимальными сведениями.

## <a name="iaccessible-methods"></a>Методы IAccessible

Клиентская область поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Свойства IAccessible

Клиентская область поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Свойство                                                                             | Примечания                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**получить \_ аккчилдкаунт**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**получить \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**получить \_ акккэйбоардшорткут**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**получить \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Отправляет сообщение [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext) для получения текста окна.                                                                                                                                                                                                                                                                                                                                                                                |
| [**получить \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**получить \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Свойство **Role** является [**\_ \_ клиентской системой роли**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                |
| [**получить \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Свойство **State** представляет собой сочетание одного или нескольких из следующих [значений](object-state-constants.md):[**\_ \_ невидимая**](object-state-constants.md) система состояния система состояния \| [**\_ \_ недоступна**](object-state-constants.md) система состояний, \| [**\_ \_ сфокусированная**](object-state-constants.md) на \| [**\_ \_ системе состояния**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Интерфейс IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

