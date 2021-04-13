---
title: Иаженткоммандс вставить
description: Иаженткоммандс вставить
ms.assetid: f450aae4-db6f-4326-ae14-ddb68ab0953a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f15df0c24e16a7554881cf3d0e6c41c4ee42b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412865"
---
# <a name="iagentcommandsinsert"></a>Иаженткоммандс:: INSERT

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT Insert(
   BSTR bszCaption,  // Caption setting for Command
   BSTR bszVoice,    // Voice setting for Command
   long bEnabled,    // Enabled setting for Command
   long bVisible,    // Visible setting for Command
   long dwRefID,     // reference Command for insertion
   long dBefore,     // insertion position flag
   long * pdwID      // address for variable for Command ID
);
```

Вставляет объект [**Command**](/windows/desktop/lwef/the-command-object) в коллекцию [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*бсзкаптион*
</dt> <dd>

Объект BSTR, указывающий значение текста [**заголовка**](caption-property.md) , отображаемого для [**команды**](/windows/desktop/lwef/the-command-object).

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*бсзвоице*
</dt> <dd>

Объект BSTR, указывающий значение параметра текста [**голоса**](voice-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*бенаблед*
</dt> <dd>

Логическое выражение, задающее параметр [**Enabled**](enabled-property.md) для [**команды**](/windows/desktop/lwef/the-command-object). Если параметр имеет **значение true**, **команда** включена и может быть выбрана. Если задано **значение false**, **команда** отключена.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*бвисибле*
</dt> <dd>

Логическое выражение, указывающее [**видимый**](visible-property.md) параметр для [**команды**](/windows/desktop/lwef/the-command-object). Если параметр имеет **значение true**, **команда** будет видна во всплывающем меню символа (если также задано свойство [**Caption**](caption-property.md) ).

</dd> <dt>

<span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*дврефид*
</dt> <dd>

Идентификатор [**команды**](/windows/desktop/lwef/the-command-object) , используемой в качестве ссылки относительной вставки новой **команды**.

</dd> <dt>

<span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*дбефоре*
</dt> <dd>

Логическое выражение, указывающее место размещения [**команды**](/windows/desktop/lwef/the-command-object). Если этот параметр имеет **значение true**, то новая **команда** вставляется перед указанной **командой**. Если **значение равно false**, то новая **команда** помещается после указанной **команды**.

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*пдвид* 
</dt> <dd>

Адрес переменной, которая получает идентификатор для вставленной [**команды**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иаженткоммандс:: Add**](iagentcommands--add.md), [**иаженткоммандс:: Remove**](iagentcommands--remove.md), [**иаженткоммандс:: RemoveAll**](iagentcommands--removeall.md)


 

 