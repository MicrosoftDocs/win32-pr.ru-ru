---
title: Свойство Visible (объект Commands)
description: Сведения о свойстве Visible объекта Commands, который определяет, отображается ли заголовок коллекции команд во всплывающем меню символа.
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ea780ed5f19dbe732b18de741f9d7ee376df67
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396259"
---
# <a name="visible-property-commands-object"></a>Свойство Visible (объект Commands)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает значение, определяющее, отображается ли заголовок коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) во всплывающем меню символа.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax** 
</dt> <dd>

*Агент ***. Символы (**"* чарактерид *" * *). Команда. видимое* *  \[  =  *логическое значение*\]



| Часть      | Описание                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Логическое выражение, указывающее, отображается ли объект [**Commands**](/windows/desktop/lwef/the-commands-collection-object) во всплывающем меню символа. <br/> **Значение true** Отобразится заголовок.<br/> **Значение false** Заголовок не отображается.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

Чтобы заголовок отображался во всплывающем меню символа, если приложение не является клиентом input-Active, для этого свойства необходимо задать значение **true** и свойство [**Caption**](caption-property.md) , заданное для коллекции команд. Кроме того, для этого свойства необходимо задать значение **true** , чтобы команды в коллекции отображались во всплывающем меню, если приложение является входным.

 

