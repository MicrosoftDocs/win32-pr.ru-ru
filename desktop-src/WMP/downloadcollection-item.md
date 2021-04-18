---
title: Довнлоадколлектион. Item, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод Item извлекает объект, ожидающий загрузки.
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- метод Item проигрыватель Windows Media Player
- метод Item проигрыватель Windows Media, класс Довнлоадколлектион
- Класс Довнлоадколлектион Windows Media Player, метод Item
topic_type:
- apiref
api_name:
- DownloadCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57db60a776c71d9ff16eceb1584c79a125bbf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698948"
---
# <a name="downloadcollectionitem-method"></a>Довнлоадколлектион. Item, метод

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Метод **Item** извлекает объект, ожидающий загрузки.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = DownloadCollection.item(
  itemId
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

Идентификатор *ItemId* \[ окне\]
</dt> <dd>

**Число** (**длинное**), указывающее индекс извлекаемого **довнлоадитем** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает объект **довнлоадитем** .

## <a name="remarks"></a>Комментарии

Значение *ItemId* отсчитывается от нуля.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Довнлоадколлектион**](downloadcollection-object.md)
</dt> <dt>

[**Объект Довнлоадитем**](downloaditem-object.md)
</dt> </dl>

 

 





