---
description: Узнайте, как использовать аргумент стаккедби в пользовательском интерфейсе оболочки Windows. Этот аргумент задает столбец свойств, по которому должны быть упорядочены результаты по стеку.
title: Аргумент СТАККЕДБИ (оболочка Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 781ea9f7-3d82-401b-995f-89bad7d47b3f
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bc786e2ae95309b72f82dd3121692793ac2bd3ab
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403587"
---
# <a name="stackedby-argument-the-windows-shell"></a><span data-ttu-id="a6bfc-104">Аргумент СТАККЕДБИ (оболочка Windows)</span><span class="sxs-lookup"><span data-stu-id="a6bfc-104">STACKEDBY Argument (The Windows Shell)</span></span>

<span data-ttu-id="a6bfc-105">`stackedby`Аргумент указывает столбец свойств, по которому должны быть упорядочены результаты стека.</span><span class="sxs-lookup"><span data-stu-id="a6bfc-105">The `stackedby` argument specifies the property column to stack results by.</span></span> <span data-ttu-id="a6bfc-106">Можно выполнить стек по любому допустимому свойству из системы свойств.</span><span class="sxs-lookup"><span data-stu-id="a6bfc-106">You can stack by any valid property from the property system.</span></span>

## <a name="example"></a><span data-ttu-id="a6bfc-107">Пример</span><span class="sxs-lookup"><span data-stu-id="a6bfc-107">Example</span></span>


```
search:query=vacation&stackedby=System.Author
```



### <a name="argument-information"></a><span data-ttu-id="a6bfc-108">Сведения о аргументе</span><span class="sxs-lookup"><span data-stu-id="a6bfc-108">Argument Information</span></span>



|                              | <span data-ttu-id="a6bfc-109">Значение</span><span class="sxs-lookup"><span data-stu-id="a6bfc-109">Value</span></span>                                   |
|------------------------------|-----------------------------------------|
| <span data-ttu-id="a6bfc-110">**Минимальная операционная система**</span><span class="sxs-lookup"><span data-stu-id="a6bfc-110">**Minimum Operating System**</span></span> | <span data-ttu-id="a6bfc-111">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="a6bfc-111">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



