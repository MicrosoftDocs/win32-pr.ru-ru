---
title: Свойство Воицекаптион (объект Command)
description: Воицекаптион, свойство
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1077c8d65a52bc8f0cfa329fdceb740e30e6784
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105710426"
---
# <a name="voicecaption-property-command-object"></a>Свойство Воицекаптион (объект Command)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Задает или возвращает текст, отображаемый для [**командного**](/windows/desktop/lwef/the-command-object) объекта в окне "Voice Commands".

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Символы Agent. ***("**_чарактерид_*_"). Команды ("_*_имя_*_")._ *  \[  =  *Строка* воицекаптион\]



| Отделение     | Описание                                               |
|----------|-----------------------------------------------------------|
| *string* | Строковое выражение, результатом которого является отображаемый текст. |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Если вы определяете объект [**Command**](/windows/desktop/lwef/the-command-object) в коллекции [**Commands**](https://www.bing.com/search?q=**Commands**) и устанавливаете его свойство [**Voice**](voice-property.md) , обычно также устанавливается свойство [**воицекаптион**](voicecaption-property.md) . Этот текст будет отображаться в окне "Voice Commands", если ваше клиентское приложение является активным, а сам символ является видимым. Если это свойство не задано, параметр для свойства [**Caption**](caption-property.md) определяет отображаемый текст. Если не задано ни одно свойство **воицекаптион** и **Caption** , команда не отображается в окне "Voice Commands".

### <a name="see-also"></a>См. также:

[**Свойство Caption**](caption-property.md)


 

 
