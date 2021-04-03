---
title: Полные указатели
description: В отличие от уникальных указателей, полные указатели поддерживают псевдонимы.
ms.assetid: 38023942-a4c2-4de7-b7d5-10d508cf083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18687b496ddd28dca9e70afca8deafb18774500a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987614"
---
# <a name="full-pointers"></a><span data-ttu-id="f203e-103">Полные указатели</span><span class="sxs-lookup"><span data-stu-id="f203e-103">Full Pointers</span></span>

<span data-ttu-id="f203e-104">В отличие от [уникальных](unique-pointers.md) указателей, полные указатели поддерживают псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="f203e-104">Unlike [unique](unique-pointers.md) pointers, full pointers support aliasing.</span></span> <span data-ttu-id="f203e-105">Это означает, что несколько указателей могут ссылаться на одни и те же данные, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="f203e-105">This means that multiple pointers can refer to the same data, as shown in the following figure:</span></span>

![два указателя, ссылающихся на одни и те же данные](images/prog-a02.png)

<span data-ttu-id="f203e-107">Полный указатель имеет следующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="f203e-107">A full pointer has the following characteristics:</span></span>

-   <span data-ttu-id="f203e-108">Оно может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="f203e-108">It can have the value null.</span></span>
-   <span data-ttu-id="f203e-109">При вызове может измениться со значения NULL на значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="f203e-109">It can change from null to non-null during the call.</span></span> <span data-ttu-id="f203e-110">Когда значение изменяется со значением, отличным от NULL, заглушка клиента выделяет новую память, выделенную при возврате.</span><span class="sxs-lookup"><span data-stu-id="f203e-110">When the value changes to non-null, the client stub allocates new memory allocated on return.</span></span> <span data-ttu-id="f203e-111">Клиентская программа должна освободить эту память до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="f203e-111">The client program should free this memory before it terminates.</span></span>
-   <span data-ttu-id="f203e-112">Во время вызова он может измениться с значения, отличного от NULL, на null.</span><span class="sxs-lookup"><span data-stu-id="f203e-112">It can change from non-null to null during the call.</span></span> <span data-ttu-id="f203e-113">Когда значение изменяется на null, приложение отвечает за освобождение памяти.</span><span class="sxs-lookup"><span data-stu-id="f203e-113">When the value changes to null, the application is responsible for freeing the memory.</span></span>
-   <span data-ttu-id="f203e-114">Значение может изменяться от одного значения, отличного от NULL, к другому.</span><span class="sxs-lookup"><span data-stu-id="f203e-114">The value can change from one non-null value to another.</span></span>
-   <span data-ttu-id="f203e-115">Доступ к хранилищу, на который указывает полный указатель, может получить другой указатель или имя в операции.</span><span class="sxs-lookup"><span data-stu-id="f203e-115">The storage that a full pointer points to may be accessed by another pointer or name in the operation.</span></span>
-   <span data-ttu-id="f203e-116">Возвращаемые данные записываются в существующее хранилище, если указатель не имеет значения NULL.</span><span class="sxs-lookup"><span data-stu-id="f203e-116">Return data is written into existing storage if the pointer does not have the value null.</span></span>

<span data-ttu-id="f203e-117">Используйте атрибут \[ [**ptr**](/windows/desktop/Midl/ptr) \] для указания полного указателя, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="f203e-117">Use the \[ [**ptr**](/windows/desktop/Midl/ptr) \] attribute to specify a full pointer, as shown in the following example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface FullPtrInterface
{
  void RemoteFn([in,ptr,string]) char *ptrName1,
                [in,ptr,string]  char *ptrName2);
}
```

<span data-ttu-id="f203e-118">В этом примере параметры *ptrName1* и *ptrName2* определены как полные указатели на строку.</span><span class="sxs-lookup"><span data-stu-id="f203e-118">In this example the parameters *ptrName1* and *ptrName2* are defined as full pointers to a string.</span></span> <span data-ttu-id="f203e-119">Оба указателя могут указывать на один и тот же адрес памяти, содержащий одну строку.</span><span class="sxs-lookup"><span data-stu-id="f203e-119">It is possible for both pointers to point to the same memory address containing a single string.</span></span>

<span data-ttu-id="f203e-120">\[**ptr** \] -записи является обязательным при предоставлении поддержки псевдонимов.</span><span class="sxs-lookup"><span data-stu-id="f203e-120">\[**ptr**\] is required when providing aliasing support.</span></span> <span data-ttu-id="f203e-121">Однако, поскольку для этого требуется наибольшая обработка всех указателей, доступных в RPC, не рекомендуется для большинства приложений.</span><span class="sxs-lookup"><span data-stu-id="f203e-121">However, since it requires the most processing of all the pointers available in RPC, it is not recommended for most applications.</span></span>

 

 