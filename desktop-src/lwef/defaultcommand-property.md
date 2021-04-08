---
title: Дефаулткомманд, свойство
description: Дефаулткомманд, свойство
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d57d937cec575f0fdd99cc1f14511b9c88f9235
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069929"
---
# <a name="defaultcommand-property"></a>Дефаулткомманд, свойство

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает команду по умолчанию для объекта [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

Символы агента. ** * ** *  **("***Чарактерид***"). Строка Commands. дефаулткомманд** \[  =  \]



| Отделение     | Описание                                                                         |
|----------|-------------------------------------------------------------------------------------|
| *string* | Строковое значение, определяющее имя (идентификатор) [**команды**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это свойство позволяет задать [**команду**](/windows/desktop/lwef/the-command-object) в коллекции Commands в [**качестве команды по**](/windows/desktop/lwef/the-commands-collection-object) умолчанию, выводит полужирный шрифт. Это не приводит к изменению обработки команд или двойного щелчка.

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

 

 