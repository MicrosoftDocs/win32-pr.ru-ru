---
title: Ошибка роли ARIA
description: Ошибка роли ARIA
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- ариаролиррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df04ad94d68ae1e8e2e8d3352aa349834a2389fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "105681708"
---
# <a name="aria-role-error"></a>Ошибка роли ARIA

## <a name="text"></a>Текст

Элемент имеет недопустимую роль ожидать-ARIA.

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Эта ошибка применяется ко всем элементам, имеющим атрибут [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) . Он указывает, что атрибут **Role** не является допустимым значением роли "веб-приложения со специальными возможностями" (ожидать-ARIA), доступным в соответствии со спецификацией ожидать-ARIA. Задание допустимой роли позволяет убедиться, что элемент правильно интерпретируется программами чтения с экрана и другими средствами вспомогательных технологий.

Чтобы устранить эту ошибку, присвойте атрибуту [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) допустимое значение роли ожидать-ARIA. Обратите внимание, что абстрактные роли ожидать-ARIA недопустимы.

## <a name="example"></a>Пример


```HTML
<!—The invalid role will not expose this element as a button. -->
<div role="backbutton" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >

<!—Setting the correct role will expose this as a button that can be clicked. -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Ошибка роли контейнера ARIA](aria-container-role.md)
</dt> </dl>

 

 




