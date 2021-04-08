---
title: Иажентспичинпутпропертиес
description: Иажентспичинпутпропертиес
ms.assetid: b93e5b46-b8f8-4ca4-8417-7626b97d8928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e672b26f97cfbe92bc71d0ceab165e100c3ecf92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067239"
---
# <a name="iagentspeechinputpropertiesgethotkey"></a>Иажентспичинпутпропертиес:: насочетание клавиш

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetHotKey(
BSTR * pbszHotCharKey  // address of variable for listening key 
);                        
```

Извлекает текущее назначение клавиатуры для ключа прослушивания речевого ввода.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*пбсзотчаркэй*
</dt> <dd>

Адрес BSTR, который получает текущее значение сочетания клавиш, используемое для открытия звукового канала для речевого ввода.

</dd> </dl>

Если функция [**Enable**](iagentspeechinputproperties--getenabled.md) возвращает **значение false**, то при запросе этого параметра возникает ошибка.

## <a name="see-also"></a>См. также:

[**Иажентспичинпутпропертиес:: enable**](iagentspeechinputproperties--getenabled.md)


 

 




