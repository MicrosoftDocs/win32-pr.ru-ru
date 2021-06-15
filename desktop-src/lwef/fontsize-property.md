---
title: Свойство FontSize (объект Commands)
description: Сведения о свойстве объекта команд FontSize. Microsoft Agent является устаревшим в Windows 7.
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d4e32bf57d129e7bf1d7b45f97846a1fe90756
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068211"
---
# <a name="fontsize-property-commands-object"></a>Свойство FontSize (объект Commands)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает размер шрифта, используемый во всплывающем меню символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Символы Agent. ***("**_чарактерид_*_"). Команды. FontSize,_ *  \[  =  *точки*\]



| Часть     | Описание                                              |
|----------|----------------------------------------------------------|
| *Точки* | Длинное целое значение, указывающее размер шрифта в пунктах. |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

Свойство **FontSize** определяет размер шрифта, используемого для отображения текста во всплывающем меню символа. Значение по умолчанию для параметра Font основано на параметре шрифта меню для параметра **LanguageID** символа или (если он не задан) — параметре языка пользователя по умолчанию.

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

 

 




