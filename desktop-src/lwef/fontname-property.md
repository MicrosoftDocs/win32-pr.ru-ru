---
title: Свойство FontName (объект Commands)
description: FontName, свойство
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b04fa386958a75b55f9cfc50a9149de454d48f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134966"
---
# <a name="fontname-property-commands-object"></a>Свойство FontName (объект Commands)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает шрифт, используемый во всплывающем меню символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Символы Agent. ***("**_чарактерид_*_"). Шрифт Commands. FontName_ *  \[  =  \]



| Отделение   | Описание                                      |
|--------|--------------------------------------------------|
| *Шрифт* | Строковое значение, соответствующее имени шрифта. |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Свойство **FontName** определяет шрифт, используемый для отображения текста во всплывающем меню символа. Значение по умолчанию для параметра Font основано на параметре шрифта меню для параметра **LanguageID** символа или--если этот параметр не задан, используется пользовательский идентификатор языка по умолчанию.

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

 

 




