---
description: Очищает кэш совместимости приложений.
ms.assetid: 03f47813-87f6-4b71-b453-77a2facab019
title: Функция Басефлушаппкомпаткаче
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BaseFlushAppcompatCache
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-appcompat-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-appcompat-l1-1-1.dll
ms.openlocfilehash: 6118c78784bb96b9f25e008cd2221112eeb646f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141127"
---
# <a name="baseflushappcompatcache-function"></a><span data-ttu-id="a1458-103">Функция Басефлушаппкомпаткаче</span><span class="sxs-lookup"><span data-stu-id="a1458-103">BaseFlushAppcompatCache function</span></span>

<span data-ttu-id="a1458-104">Очищает кэш совместимости приложений.</span><span class="sxs-lookup"><span data-stu-id="a1458-104">Flushes the application compatibility cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1458-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1458-105">Syntax</span></span>


```C++
BOOL WINAPI BaseFlushAppcompatCache(void);
```



## <a name="parameters"></a><span data-ttu-id="a1458-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1458-106">Parameters</span></span>

<span data-ttu-id="a1458-107">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="a1458-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a1458-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1458-108">Return value</span></span>

<span data-ttu-id="a1458-109">Функция возвращает **значение true** , если она выполняется, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a1458-109">The function returns **TRUE** if it succeeds and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1458-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1458-110">Remarks</span></span>

<span data-ttu-id="a1458-111">Вызывающий объект должен быть администратором.</span><span class="sxs-lookup"><span data-stu-id="a1458-111">The caller must be an administrator.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1458-112">Требования</span><span class="sxs-lookup"><span data-stu-id="a1458-112">Requirements</span></span>



| <span data-ttu-id="a1458-113">Требование</span><span class="sxs-lookup"><span data-stu-id="a1458-113">Requirement</span></span> | <span data-ttu-id="a1458-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a1458-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1458-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1458-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a1458-116">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a1458-116">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a1458-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1458-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a1458-118">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a1458-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a1458-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a1458-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1458-120"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1458-120"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1458-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1458-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1458-122">**шимфлушкаче**</span><span class="sxs-lookup"><span data-stu-id="a1458-122">**ShimFlushCache**</span></span>](shimflushcache.md)
</dt> </dl>

 

 




