---
title: Свойство Top (объект characters)
description: Сведения о свойстве Top (объект characters). Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bdc753bc287e1289b2a75633081c7b325d698a7fbe92ba495cc93662485d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474483"
---
# <a name="top-property-characters-object"></a>Свойство Top (объект characters)

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает верхний край указанного кадра символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("**_чарактерид_*_"). Верхнее_ *  \[  =  *значение*\]



| Часть    | Описание                                             |
|---------|---------------------------------------------------------|
| *value* | Длинное целое число, указывающее верхнюю границу символа. |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

Свойство **Top** всегда выражается в пикселях относительно исходного экрана (в верхнем левом углу). Параметр этого свойства применяется ко всем клиентам символа.

Несмотря на то, что символ отображается в окне области неправильной формы, расположение символа основано на внешних измерениях прямоугольного кадра анимации, используемого при компиляции символа с помощью редактора символов Microsoft Agent.

Чтобы изменить расположение символа, используйте метод [**MoveTo**](moveto-method.md) .

## <a name="see-also"></a>См. также

[**Свойство Left**](left-property.md), [ **метод moveTo**](moveto-method.md)


 

 




