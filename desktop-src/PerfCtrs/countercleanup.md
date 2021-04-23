---
description: Удаляет регистрацию поставщиков.
ms.assetid: e52c1ee0-140a-4277-bddd-d93338a512bc
title: Функция Каунтерклеануп
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterCleanup
api_type:
- NA
api_location: ''
ms.openlocfilehash: eb768d3152aad5401c30b18a3f1ff13d1ef2397d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663247"
---
# <a name="countercleanup-function"></a><span data-ttu-id="3492f-103">Функция Каунтерклеануп</span><span class="sxs-lookup"><span data-stu-id="3492f-103">CounterCleanup function</span></span>

<span data-ttu-id="3492f-104">Удаляет регистрацию поставщика.</span><span class="sxs-lookup"><span data-stu-id="3492f-104">Removes the provider's registration.</span></span>

## <a name="syntax"></a><span data-ttu-id="3492f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3492f-105">Syntax</span></span>


```C++
void WINAPI CounterCleanup(void);
```



## <a name="parameters"></a><span data-ttu-id="3492f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3492f-106">Parameters</span></span>

<span data-ttu-id="3492f-107">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="3492f-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3492f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3492f-108">Return value</span></span>

<span data-ttu-id="3492f-109">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3492f-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3492f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3492f-110">Remarks</span></span>

<span data-ttu-id="3492f-111">Поставщик вызывает эту функцию.</span><span class="sxs-lookup"><span data-stu-id="3492f-111">Your provider calls this function.</span></span> <span data-ttu-id="3492f-112">Функция вызывает функцию [**перфстоппровидер**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) для удаления регистрации поставщика.</span><span class="sxs-lookup"><span data-stu-id="3492f-112">The function calls the [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) function to remove the provider's registration.</span></span>

<span data-ttu-id="3492f-113">Средство [**КТРПП**](ctrpp.md) создает эту встроенную функцию при указании аргумента **-o** .</span><span class="sxs-lookup"><span data-stu-id="3492f-113">The [**CTRPP**](ctrpp.md) tool generates this inline function when you specify the **-o** argument.</span></span> <span data-ttu-id="3492f-114">Имя функции включает строку *префикса* , если указан аргумент **-prefix** (например, **_prefix_CounterCleanup**.</span><span class="sxs-lookup"><span data-stu-id="3492f-114">The function's name includes a *prefix* string if you specify the **-prefix** argument (for example, **_prefix_CounterCleanup**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3492f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3492f-115">Requirements</span></span>



| <span data-ttu-id="3492f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3492f-116">Requirement</span></span> | <span data-ttu-id="3492f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3492f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3492f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3492f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3492f-119">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3492f-119">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3492f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3492f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3492f-121">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3492f-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 




