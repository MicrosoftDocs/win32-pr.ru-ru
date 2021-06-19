---
title: Свойство Top (объект characters)
description: Сведения о свойстве Top (объект characters). Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a5e26d2ef578a98447d47eb2a3fae3613760a9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396349"
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


 

 




