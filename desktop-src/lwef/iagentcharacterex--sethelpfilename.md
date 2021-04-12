---
title: Иажентчарактерекс Сеселпфиленаме
description: Иажентчарактерекс Сеселпфиленаме
ms.assetid: 1f8d2bd7-5821-46c0-b371-7ecbc526df72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1342baecc1e059d4fcb5d1323c0c714bd6bf7087
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132943"
---
# <a name="iagentcharacterexsethelpfilename"></a>Иажентчарактерекс:: Сеселпфиленаме

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetHelpFileName(
   BSTR bszName  // Help filename
);
```

Задает Хелпфиленаме для символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*бсзнаме*
</dt> <dd>

Имя файла справки для символа.

</dd> </dl>

Если для приложения был создан файл справки Windows и задано свойство [**HelpFile**](helpfile-property.md) символа, Microsoft Agent автоматически вызывает справку, когда [**Хелпмодеон**](helpmodeon-property.md) имеет значение **true** , а пользователь щелкает символ или выбирает команду во всплывающем меню. Если в свойстве [**хелпконтекстид**](helpcontextid-property.md) выбранной команды имеется контекстный номер, в справке отображается раздел, соответствующий текущему контексту справки. в противном случае отображается сообщение "нет раздела справки, связанного с этим элементом".

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

> [!Note]  
> Для создания файла справки требуется компилятор справки Microsoft Windows.

 

## <a name="see-also"></a>См. также:

[**Иаженткоммандсекс:: сеселпконтекстид**](iagentcommandsex--sethelpcontextid.md), [**Иажентчарактерекс:: сеселпмодеон**](iagentcharacterex--sethelpmodeon.md), [**иажентчарактерекс:: GetHelpFileName**](iagentcharacterex--gethelpfilename.md)


 

 




