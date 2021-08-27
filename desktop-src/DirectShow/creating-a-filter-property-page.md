---
description: Создание страницы свойств фильтра
ms.assetid: 028e2c4e-0241-4057-8514-d3e9b456ab6e
title: Создание страницы свойств фильтра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a46d891c42a6cdb2f1c636278a8270fb13a69580697a31fe78f2f3687246f20b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108264"
---
# <a name="creating-a-filter-property-page"></a>Создание страницы свойств фильтра

в этом разделе описывается создание страницы свойств для настраиваемого фильтра DirectShow с помощью класса [**кбасепропертипаже**](cbasepropertypage.md) . В примере кода в этом разделе показаны все шаги, необходимые для создания страницы свойств. В примере показана страница свойств для гипотетического фильтра видеоэффектов, поддерживающего свойство насыщенности. На странице свойств имеется ползунок, который пользователь может перемещать для настройки уровня насыщенности фильтра.

В этом разделе рассматриваются следующие вопросы.

-   [Шаг 1. Определение механизма установки свойства](step-1--define-a-mechanism-for-setting-the-property.md)
-   [Шаг 2. Реализация ИспеЦифипропертипажес](step-2--implement-ispecifypropertypages.md)
-   [Шаг 3. Поддержка QueryInterface](step-3--support-queryinterface.md)
-   [Шаг 4. Создание страницы свойств](step-4--create-the-property-page.md)
-   [Шаг 5. Сохранение указателя на фильтр](step-5--store-a-pointer-to-the-filter.md)
-   [Шаг 6. Инициализация диалогового окна](step-6--initialize-the-dialog.md)
-   [Шаг 7. Обработку сообщений окна](step-7--handle-window-messages.md)
-   [Шаг 8. Применить изменения свойств](step-8--apply-property-changes.md)
-   [Шаг 9. Отключение страницы свойств](step-9--disconnect-the-property-page.md)
-   [Шаг 10. Поддержка регистрации COM](step-10--support-com-registration.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[написание фильтров DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



