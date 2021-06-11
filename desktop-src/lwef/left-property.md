---
title: Свойство Left (объект characters)
description: Сведения о свойстве объекта "левые символы". Microsoft Agent является устаревшим в Windows 7.
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e2f860e6827a9c96c42014456e43b791ab70ed4
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988940"
---
# <a name="left-property-characters-object"></a>Свойство Left (объект characters)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает левую границу указанного кадра символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("**_чарактерид_*_"). Левое_ *  \[  =  *значение*\]



| Часть    | Описание                                                           |
|---------|-----------------------------------------------------------------------|
| *value* | Длинное целое число, указывающее левую границу рамки символа. |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

Свойство **Left** всегда выражается в пикселях относительно исходного экрана (в верхнем левом углу). Параметр этого свойства применяется ко всем клиентам символа.

Несмотря на то, что символ отображается в окне области неправильной формы, расположение символа основано на внешних измерениях прямоугольного кадра анимации, используемого при компиляции символа с помощью редактора символов Microsoft Agent.

 

 




