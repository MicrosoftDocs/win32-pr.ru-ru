---
title: Свойство Caption (объект Command)
description: Свойство Caption
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0595444bd2e49ca0207c5a6a9fd459e919573958
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105710419"
---
# <a name="caption-property-command-object"></a>Свойство Caption (объект Command)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Определяет текст, отображаемый для [**команды**](/windows/desktop/lwef/the-command-object) во всплывающем меню указанного символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("**_чарактерид_*_"). Команды ("_*_имя_*_")._ *  \[  =  *Строка* заголовка\]



| Отделение     | Описание                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| *string* | Строковое выражение, результатом которого является текст, отображаемый в качестве заголовка для **команды**. |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Чтобы указать клавишу доступа (нелинованной) для **заголовка**, добавьте символ амперсанда (&) перед этим символом.

Если вы не определили **воицекаптион** для команды, будет использоваться параметр **Caption** .

 

 
