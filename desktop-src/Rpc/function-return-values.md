---
title: Возвращаемые значения функции
description: Значения, возвращаемые функцией, похожи на \ "Параметры \", так как их данные не предоставляются клиентским приложением.
ms.assetid: 98d8d228-7222-49bf-9f29-7749a7a76d5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ada3808d024f201ef01a5f4977149a0ab9c75e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672390"
---
# <a name="function-return-values"></a><span data-ttu-id="bbc42-103">Возвращаемые значения функции</span><span class="sxs-lookup"><span data-stu-id="bbc42-103">Function Return Values</span></span>

<span data-ttu-id="bbc42-104">Значения, возвращаемые функцией, **похожи на параметры, которые используются \[ \]** только в качестве параметров, поскольку их данные не предоставляются клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="bbc42-104">Function return values are similar to **\[out\]**-only parameters because their data is not provided by the client application.</span></span> <span data-ttu-id="bbc42-105">Однако они управляются по-разному.</span><span class="sxs-lookup"><span data-stu-id="bbc42-105">However they are managed differently.</span></span> <span data-ttu-id="bbc42-106">В отличие от **\[ исходящих \]** параметров, они не обязательно должны быть указателями.</span><span class="sxs-lookup"><span data-stu-id="bbc42-106">Unlike **\[out\]**-only parameters, they are not required to be pointers.</span></span> <span data-ttu-id="bbc42-107">Удаленная процедура может возвращать любой допустимый тип данных, за исключением указателей ссылок и неинкапсулированных объединений.</span><span class="sxs-lookup"><span data-stu-id="bbc42-107">The remote procedure can return any valid data type except reference pointers and nonencapsulated unions.</span></span>

<span data-ttu-id="bbc42-108">Однако рекомендуется использовать параметр **\[ out \]** вместо возвращаемого значения для сложных типов данных.</span><span class="sxs-lookup"><span data-stu-id="bbc42-108">However, using an **\[out\]** parameter instead of a return value for complex data types is recommended.</span></span> <span data-ttu-id="bbc42-109">При возврате сложных типов данных компилятор MIDL создаст заглушку режима/OS.</span><span class="sxs-lookup"><span data-stu-id="bbc42-109">While returning complex data types, the MIDL compiler will generate an /Os mode stub.</span></span> <span data-ttu-id="bbc42-110">В результате теряются все последние сведения о проверке ошибок, предоставленные/robust.</span><span class="sxs-lookup"><span data-stu-id="bbc42-110">As a result, all recent error-checking information provided by /robust is lost.</span></span>

<span data-ttu-id="bbc42-111">Возвращаемые функцией значения, которые являются типами указателей, выделяются клиентской заглушкой с помощью вызова [MIDL, \_ \_ выделяемого пользователю](/windows/desktop/Midl/midl-user-allocate-1).</span><span class="sxs-lookup"><span data-stu-id="bbc42-111">Function return values that are pointer types are allocated by the client stub with a call to [midl\_user\_allocate](/windows/desktop/Midl/midl-user-allocate-1).</span></span> <span data-ttu-id="bbc42-112">Соответственно, к возвращаемому типу функции-указателя может применяться только атрибут UNIQUE или Full указатель.</span><span class="sxs-lookup"><span data-stu-id="bbc42-112">Accordingly, only the unique or full pointer attribute can be applied to a pointer function-return type.</span></span>

 

 