---
title: Свойство Visible (объект characters)
description: Свойство Visible
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a994fd59e5eaaebcaabbd9257b860fa4e27a09b4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105691718"
---
# <a name="visible-property-characters-object"></a>Свойство Visible (объект characters)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает логическое значение, указывающее, является ли символ видимым.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax** 
</dt> <dd>

*Агент ***. Символы (**"* чарактерид *" * *). Видимый**



| Значение | Описание                            |
|-------|----------------------------------------|
| True  | Отображается символ.            |
| Неверно | Символ скрыт (невидимый). |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это свойство указывает, отображается ли кадр символа. Это не обязательно означает, что на экране есть изображение. Например, это свойство возвращает **значение true** , даже если символ находится вне видимой области отображения или если текущая символьная рамка не содержит изображений. Параметр этого свойства применяется ко всем клиентам символа.

Это свойство доступно только для чтения. Чтобы сделать символ видимым или скрытым, используйте методы [**Показать**](show-method.md) или [**Скрыть**](https://www.bing.com/search?q=**Hide**) .

 

 




