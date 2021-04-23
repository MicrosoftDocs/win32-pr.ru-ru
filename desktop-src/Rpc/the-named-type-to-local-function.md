---
title: Функция named_type_to_local
description: Заглушки вызывают именованный \_ тип \_ к \_ локальной функции для преобразования данных из передаваемого типа в тип, который они предоставляют приложению.
ms.assetid: c272cc1f-e47b-4d5a-a4e2-cefeaeb8c175
keywords:
- named_type_to_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746cbdd01ea657408b1bf355f41b3b9dfba673a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067973"
---
# <a name="the-named_type_to_local-function"></a><span data-ttu-id="8f4a4-104">Именованный \_ тип \_ для \_ локальной функции</span><span class="sxs-lookup"><span data-stu-id="8f4a4-104">The named\_type\_to\_local Function</span></span>

<span data-ttu-id="8f4a4-105">Заглушки вызывают **именованный \_ тип \_ к \_ локальной** функции для преобразования данных из передаваемого типа в тип, который они предоставляют приложению.</span><span class="sxs-lookup"><span data-stu-id="8f4a4-105">The stubs call the **named\_type\_to\_local** function to convert data from a transmitted type to the type that they present to the application.</span></span> <span data-ttu-id="8f4a4-106">Функция определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8f4a4-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_to_local( 
    <named_type> __RPC_FAR * _RPC_FAR * , 
    <local_type> __RPC_FAR * );
```

<span data-ttu-id="8f4a4-107">Первый параметр указывает на передаваемые данные.</span><span class="sxs-lookup"><span data-stu-id="8f4a4-107">The first parameter points to the transmitted data.</span></span> <span data-ttu-id="8f4a4-108">Функция задает второй параметр, указывающий на представленные данные.</span><span class="sxs-lookup"><span data-stu-id="8f4a4-108">The function sets the second parameter to point to the presented data.</span></span>

<span data-ttu-id="8f4a4-109">**Именованный \_ тип \_ \_ локальной** функции должен управлять памятью для представленного типа.</span><span class="sxs-lookup"><span data-stu-id="8f4a4-109">The **named\_type\_to\_local** function must manage memory for the presented type.</span></span> <span data-ttu-id="8f4a4-110">Функция должна выделить память для всей структуры данных, которая начинается с адреса, указанного вторым параметром, за исключением самого параметра (заглушка выделяет память для корневого узла и передает ее в функцию).</span><span class="sxs-lookup"><span data-stu-id="8f4a4-110">The function must allocate memory for the entire data structure that starts at the address indicated by the second parameter, except for the parameter itself (the stub allocates memory for the root node and passes it to the function).</span></span> <span data-ttu-id="8f4a4-111">Значение второго параметра не может измениться во время вызова.</span><span class="sxs-lookup"><span data-stu-id="8f4a4-111">The value of the second parameter cannot change during the call.</span></span> <span data-ttu-id="8f4a4-112">Функция может изменить содержимое по этому адресу.</span><span class="sxs-lookup"><span data-stu-id="8f4a4-112">The function can change the contents at that address.</span></span>

 

 




