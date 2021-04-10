---
title: Функция type_from_xmit
description: Заглушки вызывают тип \_ из \_ функции xmit для преобразования данных из переданного типа в тип, представленный для приложения.
ms.assetid: 679a2738-a166-4e73-bca7-950f979ed97a
keywords:
- type_from_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e594e8586522dd3697f5ae62c95851917741f73c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068417"
---
# <a name="the-type_from_xmit-function"></a><span data-ttu-id="7dc4a-104">Тип \_ из \_ функции xmit</span><span class="sxs-lookup"><span data-stu-id="7dc4a-104">The type\_from\_xmit Function</span></span>

<span data-ttu-id="7dc4a-105">Заглушки вызывают **тип \_ из функции \_ xmit** для преобразования данных из переданного типа в тип, представленный для приложения.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-105">The stubs call the **type\_from\_xmit** function to convert data from its transmitted type to the type that is presented to the application.</span></span> <span data-ttu-id="7dc4a-106">Функция определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7dc4a-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_from_xmit ( 
    <xmit_type> __RPC_FAR *, 
    <type> __RPC_FAR *);
```

<span data-ttu-id="7dc4a-107">Первый параметр — это указатель на передаваемые данные.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-107">The first parameter is a pointer to the transmitted data.</span></span> <span data-ttu-id="7dc4a-108">Функция задает второй параметр, указывающий на представленные данные.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-108">The function sets the second parameter to point to the presented data.</span></span>

<span data-ttu-id="7dc4a-109">**Тип \_ из функции \_ xmit** должен управлять памятью для представляемого типа.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-109">The **type\_from\_xmit** function must manage memory for the presented type.</span></span> <span data-ttu-id="7dc4a-110">Функция должна выделить память для всей структуры данных, которая начинается с адреса, указанного вторым параметром, за исключением самого параметра (заглушка выделяет память для корневого узла и передает ее в функцию).</span><span class="sxs-lookup"><span data-stu-id="7dc4a-110">The function must allocate memory for the entire data structure that starts at the address indicated by the second parameter, except for the parameter itself (the stub allocates memory for the root node and passes it to the function).</span></span> <span data-ttu-id="7dc4a-111">Значение второго параметра не может измениться во время вызова.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-111">The value of the second parameter cannot change during the call.</span></span> <span data-ttu-id="7dc4a-112">Функция может изменить содержимое по этому адресу.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-112">The function can change the contents at that address.</span></span>

<span data-ttu-id="7dc4a-113">В этом примере тип двойной ссылки функции \_ \_ \_ из \_ xmit преобразует массив размеров в список с двойным связыванием.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-113">In this example, the function DOUBLE\_LINK\_TYPE\_from\_xmit converts the sized array to a double-linked list.</span></span> <span data-ttu-id="7dc4a-114">Функция удерживает допустимый указатель на начало списка, освобождает память, связанную с остальной частью списка, а затем создает новый список, который начинается с того же указателя.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-114">The function retains the valid pointer to the beginning of the list, frees memory associated with the rest of the list, then creates a new list that starts at the same pointer.</span></span> <span data-ttu-id="7dc4a-115">Функция использует служебную функцию **инсертневноде** для добавления узла списка в конец списка и назначения указателей *пнекст* и *ппревиаус* соответствующим значениям.</span><span class="sxs-lookup"><span data-stu-id="7dc4a-115">The function uses a utility function, **InsertNewNode**, to append a list node to the end of the list and to assign the *pNext* and *pPrevious* pointers to appropriate values.</span></span>


```C++
void __RPC_USER DOUBLE_LINK_TYPE_from_xmit(
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
     DOUBLE_LINK_TYPE __RPC_FAR * pList)
{
    DOUBLE_LINK_TYPE *pCurrent;
    int i;
 
    if (pArray->sSize <= 0) 
    {  
        // error checking
        return;
    }
 
    if (pList == NULL) // if invalid, create the list head
        pList = InsertNewNode(pArray->asNumber[0], NULL);             
    else 
    {    
        DOUBLE_LINK_TYPE_free_inst(pList);  // free all other nodes
        pList->sNumber = pArray->asNumber[0];
        pList->pNext = NULL; 
    }
 
    pCurrent = pList; 
    for (i = 1; i < pArray->sSize; i++)  
        pCurrent = InsertNewNode(pArray->asNumber[i], pCurrent);
    
    return;
}
```



 

 




