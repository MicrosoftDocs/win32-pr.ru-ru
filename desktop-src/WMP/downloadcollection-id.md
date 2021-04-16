---
title: DownloadCollection.id
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Свойство ID извлекает идентификатор коллекции загрузки.
ms.assetid: b5b17f22-913c-4055-8958-e3efac819b2b
keywords:
- DownloadCollection.id Windows Media Player
topic_type:
- apiref
api_name:
- DownloadCollection.id
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9edcca4f56c485951ca907ae228dfec7a958b308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699212"
---
# <a name="downloadcollectionid"></a>DownloadCollection.id

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Свойство **ID** извлекает идентификатор коллекции загрузки.

## <a name="syntax"></a>Синтаксис

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).id
      
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Комментарии

Когда диспетчер загрузки создает новую коллекцию загрузки, он присваивает коллекции ИДЕНТИФИКАЦИОНный номер. Номера ИДЕНТИФИКАТОРов сохраняются между сеансами проигрывателя Windows Media и сеансами операционной системы.

ИДЕНТИФИКАЦИОНные номера не являются уникальными. Однако в 32-разрядном значении достаточно номеров ИДЕНТИФИКАТОРов, что чрезвычайно маловероятно, что существующий идентификатор будет перезаписан новым.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Довнлоадколлектион**](downloadcollection-object.md)
</dt> </dl>

 

 





