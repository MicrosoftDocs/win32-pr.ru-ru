---
title: Довнлоадитем. size
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Свойство Size Извлекает размер загружаемого файла.
ms.assetid: e0fd9cb5-155a-4159-94b8-1bf05b4d1062
keywords:
- проигрыватель Windows Media довнлоадитем. size
topic_type:
- apiref
api_name:
- DownloadItem.size
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 046c48cc324b8d388d9f730dc3ed4d6739632d169d02d11c77201fe1da3e98c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749725"
---
# <a name="downloaditemsize"></a>Довнлоадитем. size

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Свойство **size** Извлекает размер загружаемого файла.

## <a name="syntax"></a>Синтаксис

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).size
      
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Довнлоадитем**](downloaditem-object.md)
</dt> <dt>

[**Довнлоадитем. ход выполнения**](downloaditem-progress.md)
</dt> </dl>

 

 





