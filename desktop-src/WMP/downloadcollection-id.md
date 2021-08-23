---
title: DownloadCollection.id
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Свойство ID извлекает идентификатор коллекции загрузки.
ms.assetid: b5b17f22-913c-4055-8958-e3efac819b2b
keywords:
- DownloadCollection.id проигрыватель Windows Media
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
ms.openlocfilehash: 97e505db2e643286f84b61bfa8604b9edc8ef36fa39cdd040bd9cc49bb98f82d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651273"
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

## <a name="remarks"></a>Remarks

Когда диспетчер загрузки создает новую коллекцию загрузки, он присваивает коллекции ИДЕНТИФИКАЦИОНный номер. номера идентификаторов сохраняются между проигрыватель Windows Media сеансами и сеансами операционной системы.

ИДЕНТИФИКАЦИОНные номера не являются уникальными. Однако в 32-разрядном значении достаточно номеров ИДЕНТИФИКАТОРов, что чрезвычайно маловероятно, что существующий идентификатор будет перезаписан новым.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Довнлоадколлектион**](downloadcollection-object.md)
</dt> </dl>

 

 





