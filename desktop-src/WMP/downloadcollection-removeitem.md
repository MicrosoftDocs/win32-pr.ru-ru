---
title: Довнлоадколлектион. removeItem, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод removeItem удаляет скачанный элемент из коллекции загрузки.
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- removeItem метод Windows Media Player
- removeItem метод Windows Media Player, класс Довнлоадколлектион
- Класс Довнлоадколлектион Windows Media Player, метод removeItem
topic_type:
- apiref
api_name:
- DownloadCollection.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1798665b79327b7956c1b78509b55cc6e6dd70c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699210"
---
# <a name="downloadcollectionremoveitem-method"></a>Довнлоадколлектион. removeItem, метод

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Метод **RemoveItem** удаляет скачанный элемент из коллекции загрузки.

## <a name="syntax"></a>Синтаксис


```JScript
DownloadCollection.removeItem(
  itemID
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

Идентификатор *ItemId* \[ окне\]
</dt> <dd>

**Число** (**длинное**), определяющее индекс удаляемого **довнлоадитем** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Если выполняется загрузка, представленная идентификатором *ItemId* , этот метод отменяет скачивание.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Довнлоадколлектион. Item**](downloadcollection-item.md)
</dt> <dt>

[**Объект Довнлоадколлектион**](downloadcollection-object.md)
</dt> </dl>

 

 





