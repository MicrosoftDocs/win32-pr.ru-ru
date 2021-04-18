---
title: Иаженткоммандсекс Жетвоицекаптион
description: Иаженткоммандсекс Жетвоицекаптион
ms.assetid: 0e505295-386a-421f-a43c-6da03c8a2b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a757e1c841afd62b9b6ae13f1ef34178f133ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105710267"
---
# <a name="iagentcommandsexgetvoicecaption"></a>Иаженткоммандсекс:: Жетвоицекаптион

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption
);
```

Получает [**воицекаптион**](voicecaption-property.md) для объекта [**команды**](/windows/desktop/lwef/the-command-object) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*пбсзвоицекаптион*
</dt> <dd>

Адрес строки BSTR, которая получает значение текста [**заголовка**](caption-property.md) , отображаемого для [**команды**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Возвращаемый текст определяется для объекта [**команды**](/windows/desktop/lwef/the-command-object) и отображается в окне "команды Voice", если клиентское приложение является входным.

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

## <a name="see-also"></a>См. также:

[**Иаженткоммандсекс:: Сетвоицекаптион**](iagentcommandsex--setvoicecaption.md)


 

 