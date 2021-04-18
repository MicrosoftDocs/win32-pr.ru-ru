---
title: Свойство достоверности
description: Свойство достоверности
ms.assetid: 28a57970-4649-4a9a-9fb2-bf3f0b2f54ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa004e5690c534b7467c293d26cdf60f327dcfb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412823"
---
# <a name="confidence-property"></a>Свойство достоверности

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает значение, указывающее, отображается ли **достоверность** клиента в Tip прослушивания.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("*** чарактерид ***"). Команды ("*** имя ***")**. * * достоверное* *  \[  =  *число*\]



| Отделение     | Описание                                                                                                                        |
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| *Число* | Числовое выражение, результатом которого является длинное целое число, идентифицирующее значение достоверности для [**команды**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Если возвращенное значение достоверности наилучшего соответствия (UserInput. достоверность) не превышает значение, заданное для свойства **достоверности** , то текст, указанный в [**конфиденцетекст**](confidencetext-property.md) , отображается в подсказке прослушивания.

 

 