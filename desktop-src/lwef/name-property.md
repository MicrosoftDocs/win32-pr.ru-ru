---
title: Свойство Name (объект characters)
description: Свойство Name
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e7b4a8872952cce0ae68445ec22a5599891674
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488730"
---
# <a name="name-property-characters-object"></a>Свойство Name (объект characters)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает строку, указывающую имя по умолчанию указанного символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("**_чарактерид_*_")._ *  \[  =  *Строка* имени\]



| Отделение     | Описание                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| *string* | Строковое значение, соответствующее имени символа (в текущем параметре языка). |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

**Имя** символа может зависеть от параметра [**LanguageID**](languageid-property.md) символа. Имя символа на одном языке может отличаться или использовать другие символы, чем в другом. **Имя** символа по умолчанию для конкретного языка определяется при компиляции символа с помощью редактора символов Microsoft Agent.

Избегайте переименования символа, особенно при его использовании в сценарии, где другие клиентские приложения могут использовать один и тот же символ. Кроме того, агент использует **имя** символа для автоматического создания команд для скрытия и отображения символа.

 

 




