---
title: Свойство Height (объект characters)
description: Сведения о свойстве Height объекта Characters. Microsoft Agent является устаревшим в Windows 7.
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93d288276bd9717378c9a1ab0d9b00489959c00
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068519"
---
# <a name="height-property-characters-object"></a>Свойство Height (объект characters)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает высоту рамки указанного символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("**_чарактерид_*_")._ *  \[ =  *Значение* высоты\]



| Часть    | Описание                                                 |
|---------|-------------------------------------------------------------|
| *value* | Длинное целое число, указывающее высоту рамки символа. |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

Свойство **Height** всегда выражается в пикселях относительно экранных координат (в верхнем левом углу). Параметр этого свойства применяется ко всем клиентам символа.

Несмотря на то, что символ отображается в окне области неправильной формы, высота символа основана на внешних измерениях прямоугольного кадра анимации, используемого при компиляции символа с помощью редактора символов Microsoft Agent.

 

 




