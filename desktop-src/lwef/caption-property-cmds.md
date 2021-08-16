---
title: Свойство Caption (объект коллекции Commands)
description: Сведения о свойстве Caption объекта коллекции команд. не рекомендуется использовать Microsoft Agent на Windows 7.
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3467543de127bf0d9e898273f68d4cb921b7ab88ef52e965d73be4c1b465786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976704"
---
# <a name="caption-property-commands-collection-object"></a>Свойство Caption (объект коллекции Commands)

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Определяет текст, отображаемый для объекта [**Command**](/windows/desktop/lwef/the-commands-collection-object) во всплывающем меню символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("**_чарактерид_*_")._ * [Строка Commands. Caption](caption-property.md) \[  =  \]



| Часть     | Описание                                                              |
|----------|--------------------------------------------------------------------------|
| *строка* | Строковое выражение, результатом которого является текст, отображаемый в качестве заголовка. |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

Установка свойства [**Caption**](caption-property.md) для коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) определяет, как она будет отображаться во всплывающем меню символа, если его свойство [**Visible**](visible-property.md) имеет значение true, а приложение не является клиентом ввода-активного. Чтобы указать клавишу доступа (нелинованной) для **заголовка**, добавьте символ амперсанда (&) перед этим символом.

При определении команд для коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , имеющей [**заголовок**](caption-property.md), обычно также определяется **заголовок** для связанной с ней **команды** .

 

 
