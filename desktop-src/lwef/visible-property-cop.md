---
title: Свойство Visible (объект Command)
description: Свойство Visible
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feaa6603812bf0938e6639021eb0f8660382af37
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105710411"
---
# <a name="visible-property-command-object"></a>Свойство Visible (объект Command)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает значение, указывающее, отображается ли [**команда**](/windows/desktop/lwef/the-command-object) во всплывающем меню символа.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax** 
</dt> <dd>

*Агент ***. Символы (**"* чарактерид *"**). Команды (**"* имя *" * *). Видимое* *  \[  =  *логическое значение*\]



| Отделение      | Описание                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Логическое выражение, указывающее, отображается ли заголовок [**команды**](/windows/desktop/lwef/the-command-object)во всплывающем меню символа.<br/> **True** (по умолчанию) заголовок отображается.<br/> **Значение false** Заголовок не отображается.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Присвойте этому свойству **значение false** , если вы хотите включить речевой ввод для собственных интерфейсов, не выполняя их во всплывающем меню для символа. Если задать для свойства [**Caption**](caption-property.md) объекта [**команды**](/windows/desktop/lwef/the-command-object) пустую строку (""), текст заголовка не будет отображаться во всплывающем меню (например, в виде пустой строки), независимо от значения свойства [**Visible**](visible-property.md) .

Значение свойства [**Visible**](visible-property.md) коллекции родительских [**команд**](/windows/desktop/lwef/the-commands-collection-object) объекта [**команды**](/windows/desktop/lwef/the-command-object) не влияет на значение свойства **Visible** **команды**.

 

