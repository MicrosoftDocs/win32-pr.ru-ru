---
title: Свойство Top (объект characters)
description: Свойство Top
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef724c7052ad1d9ba5cb51ea46ccd7647723ed32
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105710421"
---
# <a name="top-property-characters-object"></a>Свойство Top (объект characters)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает верхний край указанного кадра символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("**_чарактерид_*_"). Верхнее_ *  \[  =  *значение*\]



| Отделение    | Описание                                             |
|---------|---------------------------------------------------------|
| *value* | Длинное целое число, указывающее верхнюю границу символа. |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Свойство **Top** всегда выражается в пикселях относительно исходного экрана (в верхнем левом углу). Параметр этого свойства применяется ко всем клиентам символа.

Несмотря на то, что символ отображается в окне области неправильной формы, расположение символа основано на внешних измерениях прямоугольного кадра анимации, используемого при компиляции символа с помощью редактора символов Microsoft Agent.

Чтобы изменить расположение символа, используйте метод [**MoveTo**](moveto-method.md) .

## <a name="see-also"></a>См. также:

[**Свойство Left**](left-property.md), [ **метод moveTo**](moveto-method.md)


 

 




