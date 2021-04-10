---
title: Свойство Description (устаревшие функции среды Windows)
description: Свойство Description
ms.assetid: 81ac4bc7-ef0c-4e7c-b57e-acc4ad315515
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4fb60b20a57f56a914c7e44ced957d91bf7085
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070956"
---
# <a name="description-property-legacy-windows-environment-features"></a>Свойство Description (устаревшие функции среды Windows)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает строку, указывающую описание указанного символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент*. **Символы ("**_чарактерид_*_")._* \[  =  *Строка* описания\]



| Отделение     | Описание                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| *string* | Строковое значение, соответствующее описанию символа (в текущем параметре языка). |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

**Описание** символа может зависеть от параметра **LanguageID** символа. Имя символа на одном языке может отличаться или использовать другие символы, чем в другом. **Описание** символа по умолчанию для конкретного языка определяется при компиляции символа с помощью редактора символов Microsoft Agent.

> [!Note]  
> Параметр свойства **Description** является необязательным и не может быть указан для всех символов.

 

 

 




