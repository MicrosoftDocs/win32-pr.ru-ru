---
title: Выгрузка Иажент
description: Выгрузка Иажент
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc30d6c4c06c1d292a26a2f503477dcca651dd18
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337361"
---
# <a name="iagentunload"></a><span data-ttu-id="3efa0-103">Иажент:: unload</span><span class="sxs-lookup"><span data-stu-id="3efa0-103">IAgent::UnLoad</span></span>

<span data-ttu-id="3efa0-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3efa0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT UnLoad(
   long * dwCharID  //character ID
);
```

<span data-ttu-id="3efa0-105">Выгружает символьные данные для указанного символа из коллекции [**символов**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="3efa0-105">Unloads the character data for the specified character from the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

-   <span data-ttu-id="3efa0-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3efa0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3efa0-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*</span><span class="sxs-lookup"><span data-stu-id="3efa0-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="3efa0-108">ИДЕНТИФИКАТОР символа.</span><span class="sxs-lookup"><span data-stu-id="3efa0-108">The character's ID.</span></span>

</dd> </dl>

<span data-ttu-id="3efa0-109">Используйте этот метод, если символ больше не нужен, чтобы освободить память, используемую для хранения сведений об этом символе.</span><span class="sxs-lookup"><span data-stu-id="3efa0-109">Use this method when you no longer need a character, to free up memory used to store information about the character.</span></span> <span data-ttu-id="3efa0-110">При повторном доступе к символу используйте метод [**Load**](load-method.md) .</span><span class="sxs-lookup"><span data-stu-id="3efa0-110">If you access the character again, use the [**Load**](load-method.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="3efa0-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="3efa0-111">See Also</span></span>

[<span data-ttu-id="3efa0-112">**Иажент:: Load**</span><span class="sxs-lookup"><span data-stu-id="3efa0-112">**IAgent::Load**</span></span>](iagent--load.md)


 

 