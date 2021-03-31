---
title: _allmul подпрограммы
description: Умножает два целых числа ЛОНГЛОНГ или УЛОНГЛОНГ.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _allmul, ntoskrnl.exe!_allmul
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _allmul
targetos: Windows
ms.openlocfilehash: a82a4d56ecb657e19b9849d10c9b51521af6c262
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2020
ms.locfileid: "104069481"
---
# <a name="_allmul-routine"></a><span data-ttu-id="42ca6-103">\_подпрограммы аллмул</span><span class="sxs-lookup"><span data-stu-id="42ca6-103">\_allmul Routine</span></span>

<span data-ttu-id="42ca6-104">Умножает два целых числа **лонглонг** или **улонглонг** .</span><span class="sxs-lookup"><span data-stu-id="42ca6-104">Multiplies two **LONGLONG** or **ULONGLONG** integers.</span></span>
<span data-ttu-id="42ca6-105">Например, чтобы умножить два значения Int64, компилятор может создать вызов подпрограммы **\_ аллмул** .</span><span class="sxs-lookup"><span data-stu-id="42ca6-105">For example, to multiply two int64 values the compiler might generate a call to the **\_allmul** routine.</span></span>

## <a name="remarks"></a><span data-ttu-id="42ca6-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42ca6-106">Remarks</span></span>

<span data-ttu-id="42ca6-107">Подпрограммы **\_ аллмул** — это вспомогательная подпрограммы для компилятора C.</span><span class="sxs-lookup"><span data-stu-id="42ca6-107">The **\_allmul** routine is a helper routine for the C compiler.</span></span>
<span data-ttu-id="42ca6-108">Будет ли компилятор использовать **\_ аллмул** , полностью зависит от набора оптимизации.</span><span class="sxs-lookup"><span data-stu-id="42ca6-108">Whether the compiler uses **\_allmul** is completely dependent on the optimization set.</span></span>

<span data-ttu-id="42ca6-109">Эта подпрограммы используется только на платформах x86.</span><span class="sxs-lookup"><span data-stu-id="42ca6-109">This routine is used only on x86 platforms.</span></span>
