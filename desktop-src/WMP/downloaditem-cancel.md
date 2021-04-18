---
title: Довнлоадитем. Cancel, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод Cancel отменяет скачивание.
ms.assetid: b3715fde-6a83-45fa-92ea-1cbffbee7274
keywords:
- метод Cancel проигрыватель Windows Media Player
- метод Cancel проигрыватель Windows Media Player, класс Довнлоадитем
- Класс Довнлоадитем Windows Media Player, метод Cancel
topic_type:
- apiref
api_name:
- DownloadItem.cancel
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c14d538e85d0930a43db883e226c007bea70de24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698946"
---
# <a name="downloaditemcancel-method"></a>Довнлоадитем. Cancel, метод

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Метод **Cancel** отменяет скачивание.

## <a name="syntax"></a>Синтаксис


```JScript
DownloadItem.cancel()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Отмененные элементы не удаляются из коллекции загрузки. Отмененные элементы возвращают **довнлоадстате** значение 4 (отменено).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Довнлоадитем**](downloaditem-object.md)
</dt> <dt>

[**Довнлоадитем. Довнлоадстате**](downloaditem-downloadstate.md)
</dt> </dl>

 

 





