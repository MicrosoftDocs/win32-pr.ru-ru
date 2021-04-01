---
title: Атрибут size_is
description: Атрибут \ size \_ имеет тип, связанный с целой константой, выражением или переменной, указывающей размер выделения массива.
ms.assetid: 5252c1a2-8e07-4e28-8280-6a9563d1b291
keywords:
- size_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7159c68d6bc3c1485c14db20d97c488916cb7b22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890752"
---
# <a name="the-size_is-attribute"></a><span data-ttu-id="ac0be-104">\[Размер \_ является \] атрибутом</span><span class="sxs-lookup"><span data-stu-id="ac0be-104">The \[size\_is\] Attribute</span></span>

<span data-ttu-id="ac0be-105">\[ [Размер \_ является](/windows/desktop/Midl/size-is) \] атрибутом, связанным с целой константой, выражением или переменной, указывающей размер выделения массива.</span><span class="sxs-lookup"><span data-stu-id="ac0be-105">The \[ [size\_is](/windows/desktop/Midl/size-is)\] attribute is associated with an integer constant, expression, or variable that specifies the allocation size of the array.</span></span> <span data-ttu-id="ac0be-106">Рассмотрим массив символов, длина которого определяется входными данными пользователя:</span><span class="sxs-lookup"><span data-stu-id="ac0be-106">Consider a character array whose length is determined by user input:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface arraytest
{
  void fArray2([in] short sSize,
               [in, out, size_is(sSize)] char achArray[*]);
}
```

> [!Note]  
> <span data-ttu-id="ac0be-107">Звездочка ( \* ), которая помечает заполнитель для измерения переменного массива, является необязательной.</span><span class="sxs-lookup"><span data-stu-id="ac0be-107">The asterisk (\*) that marks the placeholder for the variable-array dimension is optional.</span></span>

 

<span data-ttu-id="ac0be-108">Заглушка сервера должна выделить память на сервере, которая соответствует памяти на клиенте для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="ac0be-108">The server stub must allocate memory on the server that corresponds to the memory on the client for that parameter.</span></span> <span data-ttu-id="ac0be-109">Переменная, указывающая размер, всегда должна быть как минимум \[ [в](/windows/desktop/Midl/in) \] параметре in.</span><span class="sxs-lookup"><span data-stu-id="ac0be-109">The variable that specifies the size must always be at least an \[ [in](/windows/desktop/Midl/in)\] parameter.</span></span> <span data-ttu-id="ac0be-110">Атрибут « **\[ в \]** направлении» является обязательным, чтобы значение размера определялось на входе в серверную заглушку.</span><span class="sxs-lookup"><span data-stu-id="ac0be-110">The **\[in\]** directional attribute is required so that the size value is defined on entry to the server stub.</span></span> <span data-ttu-id="ac0be-111">Это значение размера содержит сведения, необходимые заглушке сервера для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="ac0be-111">This size value provides information that the server stub requires to allocate the memory.</span></span>

<span data-ttu-id="ac0be-112">Параметр size также может быть \[ в, [out](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="ac0be-112">The size parameter can also be \[in, [out](/windows/desktop/Midl/out-idl)\].</span></span> <span data-ttu-id="ac0be-113">Это полезно, если, например, массив, отправляемый клиентом, недостаточно велик для данных, которые сервер должен хранить в нем.</span><span class="sxs-lookup"><span data-stu-id="ac0be-113">This is useful if, for instance, the array the client sends is not large enough for the data that the server needs to store in it.</span></span> <span data-ttu-id="ac0be-114">Для отправки требуемого размера обратно в клиентскую программу можно использовать параметр **\[ in, out \]** .</span><span class="sxs-lookup"><span data-stu-id="ac0be-114">You can use an **\[in, out\]** size parameter to send the required size back to the client program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac0be-115">См. также</span><span class="sxs-lookup"><span data-stu-id="ac0be-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac0be-116">Несколько уровней указателей</span><span class="sxs-lookup"><span data-stu-id="ac0be-116">Multiple Levels of Pointers</span></span>](multiple-levels-of-pointers.md)
</dt> </dl>

 

 