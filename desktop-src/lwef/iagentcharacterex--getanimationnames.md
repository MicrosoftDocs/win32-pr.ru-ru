---
title: IAgentCharacterEx GetAnimationNames
description: IAgentCharacterEx GetAnimationNames
ms.assetid: d565b258-dc12-422b-a13d-aeec56057f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31dcb7ea34a9f0d833f8c1665a092fe4f3a30e7
ms.sourcegitcommit: baa7cd1709e48672f5f07ff83a9c9d5699c0efcd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/14/2021
ms.locfileid: "105693802"
---
# <a name="iagentcharacterexgetanimationnames"></a><span data-ttu-id="c0973-103">Иажентчарактерекс:: Жетаниматионнамес</span><span class="sxs-lookup"><span data-stu-id="c0973-103">IAgentCharacterEx::GetAnimationNames</span></span>

<span data-ttu-id="c0973-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c0973-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAnimationNames(
   IUnknown ** punkEnum // address of IUnknown interface
);
```

<span data-ttu-id="c0973-105">Извлекает имена анимаций для символа.</span><span class="sxs-lookup"><span data-stu-id="c0973-105">Retrieves the animation names for a character.</span></span>

-   <span data-ttu-id="c0973-106">Возвращает значение **S \_ , чтобы** указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c0973-106">Returns **S\_OK** to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c0973-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span><span class="sxs-lookup"><span data-stu-id="c0973-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span></span>
</dt> <dd>

<span data-ttu-id="c0973-108">Адрес интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) для коллекции анимации символа.</span><span class="sxs-lookup"><span data-stu-id="c0973-108">The address of the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface for the character's animation collection.</span></span>

</dd> </dl>

<span data-ttu-id="c0973-109">Эта функция позволяет перечислить имена анимаций для символа.</span><span class="sxs-lookup"><span data-stu-id="c0973-109">This function enables you to enumerate the names of the animations for a character.</span></span> <span data-ttu-id="c0973-110">Элементы в коллекции не имеют свойств, поэтому доступ к отдельным элементам напрямую невозможен.</span><span class="sxs-lookup"><span data-stu-id="c0973-110">Items in the collection have no properties, so individual items cannot be accessed directly.</span></span> <span data-ttu-id="c0973-111">Чтобы получить доступ к коллекции, запросите Пункенум для интерфейса IEnumVARIANT:</span><span class="sxs-lookup"><span data-stu-id="c0973-111">To access the collection, query punkEnum for the IEnumVARIANT interface:</span></span>


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
> <span data-ttu-id="c0973-112">Для ACF символов коллекция возвращает все анимации, определенные для символа, добавляя к тем, которые были получены с помощью метода [**Get**](https://www.bing.com/search?q=**Get**) .</span><span class="sxs-lookup"><span data-stu-id="c0973-112">For ACF characters, the collection returns all the animations that have been defined for the character, adding to the ones that have been retrieved with the [**Get**](https://www.bing.com/search?q=**Get**) method.</span></span>
