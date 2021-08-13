---
title: свойство Description (устаревшие функции Windows среды)
description: Свойство Description
ms.assetid: 81ac4bc7-ef0c-4e7c-b57e-acc4ad315515
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7ff293af98303fa0dab97aca76ed169123ea229c1fc70c156ef2c099472157
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751996"
---
# <a name="description-property-legacy-windows-environment-features"></a>свойство Description (устаревшие функции Windows среды)

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает строку, указывающую описание указанного символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент*. **Символы ("**_чарактерид_*_")._* \[  =  *Строка* описания\]



| Часть     | Описание                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| *строка* | Строковое значение, соответствующее описанию символа (в текущем параметре языка). |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

**Описание** символа может зависеть от параметра **LanguageID** символа. Имя символа на одном языке может отличаться или использовать другие символы, чем в другом. **Описание** символа по умолчанию для конкретного языка определяется при компиляции символа с помощью редактора символов Microsoft Agent.

> [!Note]  
> Параметр свойства **Description** является необязательным и не может быть указан для всех символов.

 

 

 




