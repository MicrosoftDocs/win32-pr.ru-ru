---
title: THEME. Шоверрордиалог
description: Метод Шоверрордиалог отображает стандартное диалоговое окно ошибки.
ms.assetid: cec9ecfd-6665-4b0a-a09c-49120d557a80
keywords:
- Проигрыватель Windows Media THEME. Шоверрордиалог
topic_type:
- apiref
api_name:
- THEME.showErrorDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdc1f9df13ec460ce780507e1bde38a2996f915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688872"
---
# <a name="themeshowerrordialog"></a>THEME. Шоверрордиалог

Метод **шоверрордиалог** отображает стандартное диалоговое окно ошибки.

``` syntax
        theme.showErrorDialog()
```

## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Если **Settings. енаблиррордиалогс** имеет значение false, этот метод можно использовать для программного вывода диалогового окна об ошибке. Если в очереди ошибок нет ошибок, диалоговое окно ошибки не отображается.

Для Windows Media Player 9 Series или более поздней версии этот метод должен вызываться из обработчика событий Error. Проигрыватель Windows Media 9 Series или более поздней версии очищает очередь ошибок для обложек после запуска события ошибки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент THEME**](theme-element.md)
</dt> <dt>

[**Settings. Енаблиррордиалогс**](settings-enableerrordialogs.md)
</dt> </dl>

 

 





