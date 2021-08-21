---
title: IAgentCharacterEx GetAnimationNames
description: IAgentCharacterEx GetAnimationNames
ms.assetid: d565b258-dc12-422b-a13d-aeec56057f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9cb1bc1b51b0bead2f071e0cd8561ef055ef6b7eb7986b3be969208452331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478035"
---
# <a name="iagentcharacterexgetanimationnames"></a>Иажентчарактерекс:: Жетаниматионнамес

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetAnimationNames(
   IUnknown ** punkEnum // address of IUnknown interface
);
```

Извлекает имена анимаций для символа.

-   Возвращает значение **S \_ , чтобы** указать, что операция выполнена успешно.

<dl> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

Адрес интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) для коллекции анимации символа.

</dd> </dl>

Эта функция позволяет перечислить имена анимаций для символа. Элементы в коллекции не имеют свойств, поэтому доступ к отдельным элементам напрямую невозможен. Чтобы получить доступ к коллекции, запросите Пункенум для интерфейса IEnumVARIANT:


```c++
IEnumVARIANT pEnum;
VARIANT vAnimName;
DWORD dwRetrieved;

hRes = punkEnum->QueryInterface(IID_IEnumVARIANT, (LPVOID *)&pEnum);

if (SUCCEEDED(hRes)) {

    while (TRUE) {

         hRes = pEnum->Next(1, &vAnimName, &dwRetrieved);

         if (hRes != NOERROR)
            break;

         // vAnimName.bstrVal is the animation name

         VariantClear(&vAnimName);
    } 

    pEnum->Release();
}

punkEnum->Release();
```



> [!Note]  
> Для ACF символов коллекция возвращает все анимации, определенные для символа, добавляя к тем, которые были получены с помощью метода [**Get**](https://www.bing.com/search?q=**Get**) .
