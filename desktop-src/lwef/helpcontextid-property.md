---
title: Свойство Хелпконтекстид (объект коллекции Commands)
description: Хелпконтекстид, свойство
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d530a1563080108ef2a2798589519ecca03416
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488814"
---
# <a name="helpcontextid-property-commands-collection-object"></a>Свойство Хелпконтекстид (объект коллекции Commands)

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает связанный контекстный номер для объекта [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . Используется для предоставления контекстной справки для объекта **Commands** .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Символы Agent. ***("**_чарактерид_*_"). Команды ("_*_имя_*_")._ *  \[  =  *Номер* хелпконтекстид\]



| Отделение     | Описание                                   |
|----------|-----------------------------------------------|
| *Число* | Целое число, указывающее допустимый контекстный номер. |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Если для приложения был создан файл справки Windows и задано свойство [**HelpFile**](helpfile-property.md) символа, агент автоматически вызывает справку, когда [**Хелпмодеон**](helpmodeon-property.md) имеет значение **true** и пользователь выбирает объект [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . Если задать номер контекста в **хелпконтекстид**, агент вызывает справку и ищет раздел, определяемый этим номером контекста.

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

> [!Note]  
> Для создания файла справки требуется компилятор справки Microsoft Windows.

 

## <a name="see-also"></a>См. также:

[**HelpFile, свойство**](helpfile-property.md)


 

 
