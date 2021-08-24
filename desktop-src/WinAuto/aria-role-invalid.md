---
title: Ошибка роли ARIA
description: Ошибка роли ARIA
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- ариаролиррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c0fcef639a54bcd805bcb3f239e8d42cfeda8c5111d128c5f54157db75d7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134017"
---
# <a name="aria-role-error"></a>Ошибка роли ARIA

## <a name="text"></a>Текст

Элемент имеет недопустимую роль ожидать-ARIA.

## <a name="type"></a>Тип

Error

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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Ошибка роли контейнера ARIA](aria-container-role.md)
</dt> </dl>

 

 




