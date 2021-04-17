---
title: Довнлоадитем. Саурцеурл
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Свойство Саурцеурл извлекает URL-адрес источника для скачивания.
ms.assetid: 87af20a5-5721-498d-8417-3e7dbbec38a2
keywords:
- Проигрыватель Windows Media Довнлоадитем. Саурцеурл
topic_type:
- apiref
api_name:
- DownloadItem.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1670fb4fec0ff4adb68269cf6fe6bb39be248e01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694931"
---
# <a name="downloaditemsourceurl"></a>Довнлоадитем. Саурцеурл

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Свойство **саурцеурл** извлекает URL-адрес источника для скачивания.

## <a name="syntax"></a>Синтаксис

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).sourceURL
      
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой**, доступная только для чтения.

## <a name="remarks"></a>Комментарии

Можно скачать только следующие форматы мультимедиа:

-   Advanced Systems Format (ASF)
-   MP3
-   Звуковые файлы в формате WMA
-   Видеофайлы в формате WMV

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Довнлоадитем**](downloaditem-object.md)
</dt> </dl>

 

 





