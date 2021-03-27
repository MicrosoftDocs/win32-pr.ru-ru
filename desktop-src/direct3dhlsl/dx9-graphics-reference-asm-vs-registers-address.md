---
title: Регистр адресов
description: Регистр a0 — это регистр адресов.
ms.assetid: ad86013c-3358-4770-a01c-544c868691f4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e58f42848034d12063611e14b82cb2f2d132cb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888819"
---
# <a name="address-register"></a><span data-ttu-id="6ab84-103">Регистр адресов</span><span class="sxs-lookup"><span data-stu-id="6ab84-103">Address Register</span></span>

<span data-ttu-id="6ab84-104">Регистр a0 — это регистр адресов.</span><span class="sxs-lookup"><span data-stu-id="6ab84-104">The a0 register is an address register.</span></span> <span data-ttu-id="6ab84-105">Один регистр доступен в версии VS 1 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6ab84-105">A single register is available in version vs\_1\_1.</span></span> <span data-ttu-id="6ab84-106">Регистр адресов, обозначенный как a0. x в VS \_ 1 \_ 1, может использоваться как смещение целого числа со знаком для относительной адресации в файле регистра констант.</span><span class="sxs-lookup"><span data-stu-id="6ab84-106">The address register, designated as a0.x in vs\_1\_1, can be used as a signed integer offset for relative addressing into the constant register file.</span></span> <span data-ttu-id="6ab84-107">Для версий VS \_ 2 \_ и выше все четыре компонента (. x,. y,. z,. w) доступны для относительной адресации.</span><span class="sxs-lookup"><span data-stu-id="6ab84-107">For versions vs\_2\_0 and above, all four components (.x, .y, .z, .w) are available for relative addressing.</span></span>


```
c[a0.x + n]
```



<span data-ttu-id="6ab84-108">Невозможно прочитать регистр адресов с помощью шейдера вершин, он может использоваться только для относительной адресации регистра констант.</span><span class="sxs-lookup"><span data-stu-id="6ab84-108">The address register cannot be read by a vertex shader, it can only be used for relative addressing of a constant register.</span></span> <span data-ttu-id="6ab84-109">При чтении значений за пределами допустимого диапазона будут возвращены значения (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="6ab84-109">Reading values outside of the legal range will return (0.0, 0.0, 0.0, 0.0).</span></span> <span data-ttu-id="6ab84-110">Регистр адресов может быть назначен только для инструкций [MOV-VS](mov---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="6ab84-110">The address register can only be a destination for the [mov - vs](mov---vs.md) instruction.</span></span> <span data-ttu-id="6ab84-111">Если число с плавающей запятой перемещается в целочисленный регистр, происходит преобразование «цикл-к-ближайшей».</span><span class="sxs-lookup"><span data-stu-id="6ab84-111">If a floating-point number is moved into an integer register, a round-to-nearest conversion happens.</span></span>

<span data-ttu-id="6ab84-112">Все шейдеры должны инициализировать регистр адресов, прежде чем использовать его.</span><span class="sxs-lookup"><span data-stu-id="6ab84-112">All shaders must initialize the address register before using it.</span></span> <span data-ttu-id="6ab84-113">В сравнении с версиями \_ \_ и 2 0 и выше инструкция [МОВА-VS](mova---vs.md) может переместить значение с плавающей запятой в регистр адресов.</span><span class="sxs-lookup"><span data-stu-id="6ab84-113">For version vs\_2\_0 and above, the [mova - vs](mova---vs.md) instruction can move a floating-point value to an address register.</span></span>



| <span data-ttu-id="6ab84-114">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="6ab84-114">Vertex shader versions</span></span> | <span data-ttu-id="6ab84-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="6ab84-115">1\_1</span></span> | <span data-ttu-id="6ab84-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6ab84-116">2\_0</span></span> | <span data-ttu-id="6ab84-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6ab84-117">2\_sw</span></span> | <span data-ttu-id="6ab84-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6ab84-118">2\_x</span></span> | <span data-ttu-id="6ab84-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6ab84-119">3\_0</span></span> | <span data-ttu-id="6ab84-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6ab84-120">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="6ab84-121">Регистр адресов</span><span class="sxs-lookup"><span data-stu-id="6ab84-121">Address Register</span></span>       | <span data-ttu-id="6ab84-122">x</span><span class="sxs-lookup"><span data-stu-id="6ab84-122">x</span></span>    | <span data-ttu-id="6ab84-123">x</span><span class="sxs-lookup"><span data-stu-id="6ab84-123">x</span></span>    | <span data-ttu-id="6ab84-124">x</span><span class="sxs-lookup"><span data-stu-id="6ab84-124">x</span></span>     | <span data-ttu-id="6ab84-125">x</span><span class="sxs-lookup"><span data-stu-id="6ab84-125">x</span></span>    | <span data-ttu-id="6ab84-126">x</span><span class="sxs-lookup"><span data-stu-id="6ab84-126">x</span></span>    | <span data-ttu-id="6ab84-127">x</span><span class="sxs-lookup"><span data-stu-id="6ab84-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="6ab84-128">См. также</span><span class="sxs-lookup"><span data-stu-id="6ab84-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ab84-129">Регистры шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="6ab84-129">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




