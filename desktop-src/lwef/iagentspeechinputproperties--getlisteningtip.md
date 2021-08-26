---
title: Иажентспичинпутпропертиес Жетлистенингтип
description: Иажентспичинпутпропертиес Жетлистенингтип
ms.assetid: b0488a54-03f8-43ce-935c-dd49c6ed5dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0199e75ad56cee2c299ce53be3aa94376104af5ead40004e8dbbd8fd4dcfec9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014184"
---
# <a name="iagentspeechinputpropertiesgetlisteningtip"></a>Иажентспичинпутпропертиес:: Жетлистенингтип

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 




