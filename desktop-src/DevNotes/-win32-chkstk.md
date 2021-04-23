---
description: Вызывается компилятором, если в функции имеется более одной страницы локальных переменных.
ms.assetid: 154dd992-88b5-44a4-9594-5d13afb71c28
title: _chkstk подпрограммы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a58b31836947dfb1816bea72a54f820354c792
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990314"
---
# <a name="_chkstk-routine"></a><span data-ttu-id="7cd97-103">\_подпрограммы чкстк</span><span class="sxs-lookup"><span data-stu-id="7cd97-103">\_chkstk Routine</span></span>

<span data-ttu-id="7cd97-104">Вызывается компилятором, если в функции имеется более одной страницы локальных переменных.</span><span class="sxs-lookup"><span data-stu-id="7cd97-104">Called by the compiler when you have more than one page of local variables in your function.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cd97-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7cd97-105">Remarks</span></span>

<span data-ttu-id="7cd97-106">\_подпрограммы чкстк — это вспомогательная подпрограммы для компилятора C.</span><span class="sxs-lookup"><span data-stu-id="7cd97-106">\_chkstk Routine is a helper routine for the C compiler.</span></span> <span data-ttu-id="7cd97-107">Для компиляторов x86 \_ подпрограммы чкстк вызываются, когда локальные переменные превышают 4000 байтов; для компиляторов x64 это 8 КБ.</span><span class="sxs-lookup"><span data-stu-id="7cd97-107">For x86 compilers, \_chkstk Routine is called when the local variables exceed 4K bytes; for x64 compilers it is 8K.</span></span>

 

 



