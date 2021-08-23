---
title: Иажентспичинпутпропертиес
description: Иажентспичинпутпропертиес
ms.assetid: b93e5b46-b8f8-4ca4-8417-7626b97d8928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66e4f3fe070a944ecd9800a6712e8ae4db8d333913e5cfe85c027565cf1cf77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609384"
---
# <a name="iagentspeechinputpropertiesgethotkey"></a>Иажентспичинпутпропертиес:: насочетание клавиш

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 




