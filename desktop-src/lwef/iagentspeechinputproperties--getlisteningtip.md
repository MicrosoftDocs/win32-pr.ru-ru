---
title: Иажентспичинпутпропертиес Жетлистенингтип
description: Иажентспичинпутпропертиес Жетлистенингтип
ms.assetid: b0488a54-03f8-43ce-935c-dd49c6ed5dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91218fb7935edb68458d540a8f35fe5402b317ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700469"
---
# <a name="iagentspeechinputpropertiesgetlisteningtip"></a>Иажентспичинпутпропертиес:: Жетлистенингтип

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetListeningTip(
long * pbListeningTip  // address of variable for listening tip flag
);                       
```

Получает значение, указывающее, включен ли tip прослушивания для вывода.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*пблистенингтип*
</dt> <dd>

Адрес переменной, которая получает **значение true** , если TIP прослушивания включен для экрана, или **значение false** , если TIP Listen отключен.

</dd> </dl>

Если функция [**Enable**](iagentspeechinputproperties--getenabled.md) возвращает **значение false**, то запросы к любым другим свойствам речевого ввода возвращают ошибку.

## <a name="see-also"></a>См. также:

[**Иажентспичинпутпропертиес:: enable**](iagentspeechinputproperties--getenabled.md)


 

 




