---
title: Свойство Воицекаптион (объект Commands)
description: Сведения о свойстве Воицекаптион объекта Commands, который возвращает или задает текст, отображаемый для объекта Commands в окне "Voice Commands".
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4a2113e0a952f253df901d192b42466fa30350
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396129"
---
# <a name="voicecaption-property-commands-object"></a>Свойство Воицекаптион (объект Commands)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает текст, отображаемый для объекта [**Commands**](/windows/desktop/lwef/the-commands-collection-object) в окне "Voice Commands".

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Символы Agent. ***("**_чарактерид_*_"). Строка Commands. воицекаптион_ *  \[  =  \]



| Часть     | Описание                                               |
|----------|-----------------------------------------------------------|
| *строка* | Строковое выражение, результатом которого является отображаемый текст. |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

Если задать свойство [**Voice**](voice-property.md) коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , то обычно также устанавливается свойство **воицекаптион** . Параметр текст **воицекаптион** отображается в окне "Voice Commands", если клиентское приложение является входным, а сам символ является видимым. Если это свойство не задано, то отображаемый текст определяется параметром свойства [**Caption**](caption-property.md) коллекции **Commands** . Если ни одно свойство **воицекаптион** или **Caption** не задано, команды в коллекции отображаются в окне "командные строки" в разделе "(неопределенная команда)", когда клиентское приложение становится входным.

Параметр **воицекаптион** также определяет текст, отображаемый в Tip прослушивания для указания команд, прослушиваемых этим символом.

## <a name="see-also"></a>См. также

[Свойство Caption](caption-property.md)


 

 
