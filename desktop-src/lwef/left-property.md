---
title: Свойство Left (объект characters)
description: Сведения о свойстве объекта "левые символы". не рекомендуется использовать Microsoft Agent на Windows 7.
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e546dc662dc535889eb6c3a476a54b839c5d9577a7e2ff525eeadf79f727fbf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105020"
---
# <a name="left-property-characters-object"></a>Свойство Left (объект characters)

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

 

 




