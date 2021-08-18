---
title: Дефаулткомманд, свойство
description: Дефаулткомманд, свойство
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7aec703ffbabb98ae16609b0dcb01767fda5c38b42ed40f204e3a3bae5766
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693639"
---
# <a name="defaultcommand-property"></a>Дефаулткомманд, свойство

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает команду по умолчанию для объекта [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

Символы агента. ** * ** *  **("**_Чарактерид_*_"). Строка Commands. дефаулткомманд_* \[  =  \]



| Часть     | Описание                                                                         |
|----------|-------------------------------------------------------------------------------------|
| *строка* | Строковое значение, определяющее имя (идентификатор) [**команды**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

Это свойство позволяет задать [**команду**](/windows/desktop/lwef/the-command-object) в коллекции Commands в [**качестве команды по**](/windows/desktop/lwef/the-commands-collection-object) умолчанию, выводит полужирный шрифт. Это не приводит к изменению обработки команд или двойного щелчка.

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

 

 