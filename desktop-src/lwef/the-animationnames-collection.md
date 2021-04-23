---
title: Коллекция Аниматионнамес
description: Коллекция Аниматионнамес
ms.assetid: 3b06e497-1d03-43be-8d33-e69ef2972237
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9e0c2c1d42f51f9d50bafaee61b6ab51d5b85f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888404"
---
# <a name="the-animationnames-collection"></a><span data-ttu-id="24a28-103">Коллекция Аниматионнамес</span><span class="sxs-lookup"><span data-stu-id="24a28-103">The AnimationNames Collection</span></span>

<span data-ttu-id="24a28-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="24a28-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="24a28-105">Коллекция [**аниматионнамес**](https://www.bing.com/search?q=**AnimationNames**) — это специальная коллекция, содержащая список имен анимаций, скомпилированных для символа.</span><span class="sxs-lookup"><span data-stu-id="24a28-105">The [**AnimationNames**](https://www.bing.com/search?q=**AnimationNames**) collection is a special collection that contains the list of animation names compiled for a character.</span></span> <span data-ttu-id="24a28-106">С помощью коллекции можно перечислить имена анимаций для символа.</span><span class="sxs-lookup"><span data-stu-id="24a28-106">You can use the collection to enumerate the names of the animations for a character.</span></span> <span data-ttu-id="24a28-107">Например, в Visual Basic или VBScript (2,0 или более поздней версии) доступ к этим именам можно получить с помощью команды **For Each... Следующие** операторы:</span><span class="sxs-lookup"><span data-stu-id="24a28-107">For example, in Visual Basic or VBScript (2.0 or later) you can access these names using the **For Each...Next** statements:</span></span>


```
   For Each Animation in Genie.AnimationNames
      Genie.Play Animation
   Next
```



<span data-ttu-id="24a28-108">Элементы в коллекции не имеют свойств, поэтому доступ к отдельным элементам напрямую невозможен.</span><span class="sxs-lookup"><span data-stu-id="24a28-108">Items in the collection have no properties, so individual items cannot be accessed directly.</span></span>

<span data-ttu-id="24a28-109">Предмет. ACF символов коллекция возвращает все анимации, определенные для символа, а не только те, которые были получены с помощью метода [**Get**](get-method.md) .</span><span class="sxs-lookup"><span data-stu-id="24a28-109">For .ACF characters, the collection returns all the animations that have been defined for the character, not just the ones that have been retrieved with the [**Get**](get-method.md) method.</span></span>

 

 




