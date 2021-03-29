---
title: Реализация COM-объекта контекстного меню
description: Расширение контекстного меню — это COM-объект, реализованный как внутрипроцессный сервер.
ms.assetid: 362dd8e5-1518-4bf4-ac53-115263cd6c62
ms.tgt_platform: multiple
keywords:
- контекстное меню COM-объекта в Active Directory
- контекстное меню COM-объекта в Active Directory, реализация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34d6b487d130327b379ed845f2d0157f2b28056
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "105654288"
---
# <a name="implementing-the-context-menu-com-object"></a>Реализация COM-объекта контекстного меню

Расширение контекстного меню — это COM-объект, реализованный как внутрипроцессный сервер. Расширение контекстного меню должно реализовывать интерфейсы [**ишеллекстинит**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) и [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . При отображении контекстного меню для объекта класса, для которого зарегистрировано расширение контекстного меню, создается экземпляр расширения контекстного меню.

## <a name="implementing-ishellextinit"></a>Реализация Ишеллекстинит

После создания экземпляра COM-объекта расширения контекстного меню вызывается метод [**ишеллекстинит:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) . **Ишеллекстинит:: Initialize** предоставляет расширение контекстного меню с объектом [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) , который содержит данные, относящиеся к объекту каталога, к которому применяется контекстное меню.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) содержит данные в формате [**кфстр \_ дсобжектнамес**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) . Формат данных **кфстр \_ дсобжектнамес** — это **Хглобал** , содержащий структуру [**дсобжектнамес**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) . Структура **дсобжектнамес** содержит данные о объекте каталога, к которому применяется расширение страницы свойств.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) также содержит данные в формате [**\_ \_ \_ \_ параметров отображаемой спецификации кфстр DS**](cfstr-ds-display-spec-options.md) . Формат **данных \_ \_ \_ \_ параметров отображаемой спецификации кфстр DS** — это **хглобал** , содержащий структуру [**дсдисплайспекоптионс**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) . **Дсдисплайспекоптионс** содержит данные конфигурации для использования расширением.

Если в [**ишеллекстинит:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)возвращается любое значение, отличное от **S \_ OK** , то расширение контекстного меню не будет использоваться.

Параметры *пидлфолдер* и *хкэйпрогид* метода [**ишеллекстинит:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) не используются.

## <a name="implementing-icontextmenu"></a>Реализация IContextMenu

После возврата [**ишеллекстинит:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) вызывается метод [**IContextMenu:: куериконтекстмену**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) для получения пункта меню или элементов, которые будет добавлять расширение контекстного меню. Реализация **куериконтекстмену** довольно проста. Расширение контекстного меню добавляет элементы меню с помощью [**инсертменуитем**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) или аналогичной функции. Идентификаторы команд меню должны быть больше или равны *идкмдфирст* и должны быть меньше *идкмдласт*. **Куериконтекстмену** должен возвращать наибольший числовой идентификатор, добавленный в меню, и один из них. Лучший способ назначения идентификаторов команд меню — начать с нуля и последовательно работать. Если расширение контекстного меню не нуждается ни в одном из пунктов меню, оно должно просто не добавлять элементы в меню и возвращать ноль из **куериконтекстмену**.

[**IContextMenu:: жеткоммандстринг**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) вызывается для получения текстовых данных для пункта меню, например текста справки, отображаемого для данного пункта меню. Возможно, что узел контекстного меню будет использовать строки в Юникоде, а расширение использует строки ANSI. По этой причине **глобальные \_ хелптекста**, **GC \_ Хелптекств**, **GC \_ verb** и **GC \_ вербв** должны обрабатываться по отдельности. Реализация этого метода является необязательной.

[**IContextMenu:: инвокекомманд**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) вызывается, когда выбран один из пунктов меню, устанавливаемых расширением контекстного меню. Контекстное меню выполняет или инициирует нужные действия в ответ на этот метод.

 

 