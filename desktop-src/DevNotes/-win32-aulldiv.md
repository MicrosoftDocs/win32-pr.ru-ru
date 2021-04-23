---
title: _aulldiv подпрограммы
description: Делит два целых числа УЛОНГЛОНГ.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _aulldiv, ntoskrnl.exe!_aulldiv
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _aulldiv
targetos: Windows
ms.openlocfilehash: 2fce346ee9608f20667c76841a63a8a3fb9cfe21
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2020
ms.locfileid: "104487264"
---
# <a name="_aulldiv-routine"></a><span data-ttu-id="b8b1d-103">\_подпрограммы ауллдив</span><span class="sxs-lookup"><span data-stu-id="b8b1d-103">\_aulldiv Routine</span></span>

<span data-ttu-id="b8b1d-104">Делит два целых числа **улонглонг** .</span><span class="sxs-lookup"><span data-stu-id="b8b1d-104">Divides two **ULONGLONG** integers.</span></span>
<span data-ttu-id="b8b1d-105">Например, чтобы разделить два значения UInt64, компилятор может создать вызов подпрограммы **\_ ауллдив** .</span><span class="sxs-lookup"><span data-stu-id="b8b1d-105">For example, to divide two uint64 values the compiler might generate a call to the **\_aulldiv** routine.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8b1d-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8b1d-106">Remarks</span></span>

<span data-ttu-id="b8b1d-107">Подпрограммы **\_ ауллдив** — это вспомогательная подпрограммы для компилятора C.</span><span class="sxs-lookup"><span data-stu-id="b8b1d-107">The **\_aulldiv** routine is a helper routine for the C compiler.</span></span>
<span data-ttu-id="b8b1d-108">Будет ли компилятор использовать **\_ ауллдив** , полностью зависит от набора оптимизации.</span><span class="sxs-lookup"><span data-stu-id="b8b1d-108">Whether the compiler uses **\_aulldiv** is completely dependent on the optimization set.</span></span>

<span data-ttu-id="b8b1d-109">Эта функция используется только на платформах x86.</span><span class="sxs-lookup"><span data-stu-id="b8b1d-109">This function is used only on x86 platforms.</span></span>
