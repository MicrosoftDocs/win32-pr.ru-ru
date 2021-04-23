---
title: Оператор разрешения области в C++
description: Оператор разрешения области в C++
ms.assetid: 908cf2b0-41d2-442d-aba8-82f3328c72c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb888fa9d56b6a84f8ecbc5efb2c235d1a38be03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888439"
---
# <a name="the-scope-resolution-operator-in-c"></a><span data-ttu-id="6409e-103">Оператор разрешения области в C++</span><span class="sxs-lookup"><span data-stu-id="6409e-103">The Scope Resolution Operator in C++</span></span>

<span data-ttu-id="6409e-104">Два двоеточия (::) используются в C++ в качестве оператора *разрешения области* .</span><span class="sxs-lookup"><span data-stu-id="6409e-104">Two colons (::) are used in C++ as a *scope resolution* operator.</span></span> <span data-ttu-id="6409e-105">Этот оператор обеспечивает большую свободу при именовании переменных, позволяя различать переменные с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="6409e-105">This operator gives you more freedom in naming your variables by letting you distinguish between variables with the same name.</span></span> <span data-ttu-id="6409e-106">Например, класс *MyFile:: Read* относится к методу *Read* класса *MyFile* объектов, а не к *йоурфиле:: Read*, который ссылается на метод *Read* в классе *йоурфиле* .</span><span class="sxs-lookup"><span data-stu-id="6409e-106">For example, *MyFile::Read* refers to the *Read* method of the *MyFile* class of objects, as opposed to *YourFile::Read*, which refers to a *Read* method in the *YourFile* class.</span></span>

 

 




