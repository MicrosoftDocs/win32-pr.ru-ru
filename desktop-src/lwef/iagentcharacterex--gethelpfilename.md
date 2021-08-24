---
title: Иажентчарактерекс Жеселпфиленаме
description: Иажентчарактерекс Жеселпфиленаме
ms.assetid: 52d5a874-ad3e-4833-9e3e-ff485414c54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba5acdcfef90d1918f5c4697127b4449e96f2667b20a2de0230fcdf2cd6dd43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105532"
---
# <a name="iagentcharacterexgethelpfilename"></a>Иажентчарактерекс:: Жеселпфиленаме

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetHelpFileName(
   BSTR * pbszName  // address of Help filename
);
```

Возвращает Хелпфиленаме для символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*пбсзнаме*
</dt> <dd>

Адрес переменной, которая получает имя файла справки для символа.

</dd> </dl>

если вы создали файл справки Windows для приложения и настроили свойство [**HelpFile**](helpfile-property.md) символа, Microsoft Agent автоматически вызывает справку, когда [**хелпмодеон**](helpmodeon-property.md) имеет значение **True** , а пользователь щелкает символ или выбирает команду во всплывающем меню. Если в свойстве [**хелпконтекстид**](helpcontextid-property.md) выбранной команды имеется контекстный номер, в справке отображается раздел, соответствующий текущему контексту справки. в противном случае отображается сообщение "нет раздела справки, связанного с этим элементом".

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

> [!Note]  
> для создания файла справки требуется компилятор справки Microsoft Windows.

 

## <a name="see-also"></a>См. также

[**Иаженткоммандсекс:: сеселпконтекстид**](iagentcommandsex--sethelpcontextid.md), [**Иажентчарактерекс:: сеселпмодеон**](iagentcharacterex--sethelpmodeon.md), [**иажентчарактерекс:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 




