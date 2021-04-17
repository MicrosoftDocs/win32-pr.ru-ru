---
title: Элемент Color
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. | Элемент Color
ms.assetid: 36fafe16-b708-4dc1-9325-d4f39265069a
keywords:
- Элемент Color проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Color Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c73aa9fe2c7f731e872c4a2e235bf9c0e29ce05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698994"
---
# <a name="color-element"></a>Элемент Color

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Элемент Color указывает цвет фона для кнопок навигации в Интернет-магазине, текст кнопки и панель задач функции.

``` syntax
<Color
    MediaPlayer = "#FFFFFF"
    MediaPlayerText = "#FFFFFF"
/>
```

## <a name="attributes"></a>Атрибуты

<dl> <dt>

<span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**MediaPlayer** (обязательно)
</dt> <dd>

Шестнадцатеричное значение цвета RGB. Задает цвет фона для кнопок и панели задач.

</dd> <dt>

<span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**Медиаплайертекст** (обязательно)
</dt> <dd>

Шестнадцатеричное значение цвета RGB. Задает цвет для текста кнопки.

</dd> </dl>

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия       | Элемент         |
|-----------------|-----------------|
| Родительские элементы | **ServiceInfo** |
| Дочерние элементы  | Нет            |



 

## <a name="remarks"></a>Remarks

Значение по умолчанию для **MediaPlayer** — \# 7C9AD6. Значение по умолчанию для **медиаплайертекст** — \# FFFFFF.

Не забудьте использовать цвета, которые упрощают чтение текста кнопки пользователем. Например, следует избегать использования белого текста кнопки на светлых цветных кнопках.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 10 или более поздней версии.<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Пример документа ServiceInfo для Интернет-магазина типа 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Пример документа ServiceInfo для Интернет-магазина типа 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Документ ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





