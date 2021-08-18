---
title: Довнлоадколлектион. Item, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод Item извлекает объект, ожидающий загрузки.
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- проигрыватель Windows Media метода элемента
- метод item проигрыватель Windows Media, класс довнлоадколлектион
- класс довнлоадколлектион проигрыватель Windows Media, метод item
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
ms.openlocfilehash: 8a82a903236038c2f0372786137eec48ad5c5f502d7fd614eb8944f3f4684aea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997044"
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

## <a name="remarks"></a>Remarks

Значение *ItemId* отсчитывается от нуля.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Довнлоадколлектион**](downloadcollection-object.md)
</dt> <dt>

[**Объект Довнлоадитем**](downloaditem-object.md)
</dt> </dl>

 

 





