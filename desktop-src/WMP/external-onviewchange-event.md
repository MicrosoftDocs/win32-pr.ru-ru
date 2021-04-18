---
title: Внешнее событие Онвиевчанже
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается. Событие Онвиевчанже возникает при изменении представления в проигрывателе Windows Media.
ms.assetid: aa1378ad-8b84-4592-85c5-5e284be05ea6
keywords:
- Проигрыватель Windows Media для события external. Онвиевчанже
topic_type:
- apiref
api_name:
- External.OnViewChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7144e03955fb67ed90cad4a4336bf782ca1566
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694492"
---
# <a name="externalonviewchange-event"></a>Внешнее событие Онвиевчанже

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Событие **онвиевчанже** возникает при изменении представления в проигрывателе Windows Media.

``` syntax
window.external.OnViewChange = FunctionName
```

## <a name="possible-values"></a>Возможные значения

Это свойство только для записи, которое указывает имя функции в скрипте, которое вызывает проигрыватель Windows Media при возникновении события.

## <a name="parameters"></a>Параметры

Функция, обрабатывающая это событие, не имеет параметров.

## <a name="remarks"></a>Комментарии

Представление в проигрывателе Windows Media может измениться по любой из следующих причин.

-   Пользователь взаимодействует с пользовательским интерфейсом проигрывателя Windows Media.
-   Пользователь взаимодействует со страницей обнаружения, а скрипт на странице обнаружения вызывает [External. чанжевиев](external-changeview.md).
-   Пользователь взаимодействует со страницей обнаружения, а скрипт на странице обнаружения вызывает [External. чанжевиевонлинелист](external-changeviewonlinelist.md).

При изменении представления в проигрывателе Windows Media проигрыватель вызывает [ивмпконтентпартнер::-Template](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) , чтобы получить отображаемый URL-адрес следующей страницы обнаружения. Однако до того, как проигрыватель отобразит новую страницу обнаружения, он вызывает событие **онвиевчанже** . Если обработчик событий **онвиевчанже** вызывает [External. канцелнавигате](external-cancelnavigate.md), проигрыватель Windows Media не отображает новую страницу обнаружения. Вместо этого будет отображаться текущая страница обнаружения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Внешний объект для Интернет-магазинов типа 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. Чанжевиев**](external-changeview.md)
</dt> <dt>

[**External. Чанжевиевонлинелист**](external-changeviewonlinelist.md)
</dt> </dl>

 

 





