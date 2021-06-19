---
title: Свойство Visible (объект Command)
description: Сведения о свойстве Visible объекта Command, который возвращает или задает видимость команды во всплывающем меню символа.
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4efec1ad8a97d6412a560a81836273b93ebf2b
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396249"
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



| Часть      | Описание                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Логическое выражение, указывающее, отображается ли заголовок [**команды**](/windows/desktop/lwef/the-command-object)во всплывающем меню символа.<br/> **True** (по умолчанию) заголовок отображается.<br/> **Значение false** Заголовок не отображается.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

Присвойте этому свойству **значение false** , если вы хотите включить речевой ввод для собственных интерфейсов, не выполняя их во всплывающем меню для символа. Если задать для свойства [**Caption**](caption-property.md) объекта [**команды**](/windows/desktop/lwef/the-command-object) пустую строку (""), текст заголовка не будет отображаться во всплывающем меню (например, в виде пустой строки), независимо от значения свойства [**Visible**](visible-property.md) .

Значение свойства [**Visible**](visible-property.md) коллекции родительских [**команд**](/windows/desktop/lwef/the-commands-collection-object) объекта [**команды**](/windows/desktop/lwef/the-command-object) не влияет на значение свойства **Visible** **команды**.

 

