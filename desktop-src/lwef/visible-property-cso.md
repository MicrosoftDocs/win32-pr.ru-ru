---
title: Свойство Visible (объект Commands)
description: Свойство Visible
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaba059a375c23569195ddaea82e6d03cb943ec
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414613"
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



| Отделение      | Описание                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Логическое выражение, указывающее, отображается ли объект [**Commands**](/windows/desktop/lwef/the-commands-collection-object) во всплывающем меню символа. <br/> **Значение true** Отобразится заголовок.<br/> **Значение false** Заголовок не отображается.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Чтобы заголовок отображался во всплывающем меню символа, если приложение не является клиентом input-Active, для этого свойства необходимо задать значение **true** и свойство [**Caption**](caption-property.md) , заданное для коллекции команд. Кроме того, для этого свойства необходимо задать значение **true** , чтобы команды в коллекции отображались во всплывающем меню, если приложение является входным.

 

