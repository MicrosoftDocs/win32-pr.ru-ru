---
title: Довнлоадколлектион. removeItem, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод removeItem удаляет скачанный элемент из коллекции загрузки.
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- проигрыватель Windows Media метода removeItem
- проигрыватель Windows Media метода removeItem, класс довнлоадколлектион
- класс довнлоадколлектион проигрыватель Windows Media, метод removeItem
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
ms.openlocfilehash: d1d7eaa7b26a4d64070cae426d1bbc23418593fa8ec5472e870ed7529ce8a122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997074"
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

## <a name="remarks"></a>Remarks

Если выполняется загрузка, представленная идентификатором *ItemId* , этот метод отменяет скачивание.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Довнлоадколлектион. Item**](downloadcollection-item.md)
</dt> <dt>

[**Объект Довнлоадколлектион**](downloadcollection-object.md)
</dt> </dl>

 

 





