---
title: Свойство FontName (объект Commands)
description: Сведения о свойстве объекта FontName Commands. не рекомендуется использовать Microsoft Agent на Windows 7.
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1f8c9c66e7d205e79a3ac9b076fa4e01852df358657761f8792d42b764b270
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725714"
---
# <a name="fontname-property-commands-object"></a>Свойство FontName (объект Commands)

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает шрифт, используемый во всплывающем меню символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Символы Agent. ***("**_чарактерид_*_"). Шрифт Commands. FontName_ *  \[  =  \]



| Часть   | Описание                                      |
|--------|--------------------------------------------------|
| *Шрифт* | Строковое значение, соответствующее имени шрифта. |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

Свойство **FontName** определяет шрифт, используемый для отображения текста во всплывающем меню символа. Значение по умолчанию для параметра Font основано на параметре шрифта меню для параметра **LanguageID** символа или--если этот параметр не задан, используется пользовательский идентификатор языка по умолчанию.

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

 

 




