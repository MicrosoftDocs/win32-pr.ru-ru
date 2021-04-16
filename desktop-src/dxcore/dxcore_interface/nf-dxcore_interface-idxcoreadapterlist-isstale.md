---
title: IDXCoreAdapterList::IsStale
description: Определяет, привели ли изменения к этой системе к тому, что этот объект списка адаптеров Дкскоре становится устаревшим.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 68b4e4ba6f3434f76ea5b4a2a98ae4e83486f61e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105719150"
---
# <a name="idxcoreadapterlistisstale-method"></a><span data-ttu-id="81fe5-103">Метод Идкскореадаптерлист:: устареть</span><span class="sxs-lookup"><span data-stu-id="81fe5-103">IDXCoreAdapterList::IsStale method</span></span>

<span data-ttu-id="81fe5-104">Определяет, привели ли изменения к этой системе к тому, что этот объект списка адаптеров Дкскоре становится устаревшим.</span><span class="sxs-lookup"><span data-stu-id="81fe5-104">Determines whether changes to this system have resulted in this DXCore adapter list object becoming out of date.</span></span> <span data-ttu-id="81fe5-105">Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="81fe5-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="81fe5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81fe5-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsStale() = 0;
```

## <a name="returns"></a><span data-ttu-id="81fe5-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81fe5-107">Returns</span></span>

<span data-ttu-id="81fe5-108">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="81fe5-108">Type: **bool**</span></span>

<span data-ttu-id="81fe5-109">Возвращает значение  `true`   , если после создания списка были внесены изменения в системные условия, которые приведут к тому, что список адаптеров станет устаревшим.</span><span class="sxs-lookup"><span data-stu-id="81fe5-109">Returns `true` if, since generating the list, changes to system conditions have occurred that would cause this adapter list to become stale.</span></span> <span data-ttu-id="81fe5-110">В противном случае возвращает  `false` .</span><span class="sxs-lookup"><span data-stu-id="81fe5-110">Otherwise, returns `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="81fe5-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81fe5-111">Remarks</span></span>

<span data-ttu-id="81fe5-112">Можно опросить значение « **устарело** », чтобы определить, не устарели ли в этом списке Системные состояния.</span><span class="sxs-lookup"><span data-stu-id="81fe5-112">You can poll **IsStale** to determine whether changing system conditions have led to this list becoming out of date.</span></span> <span data-ttu-id="81fe5-113">Если функция **устареть** возвращает `true` один раз, она возвращается `true` для оставшегося времени существования объекта списка адаптеров дкскоре.</span><span class="sxs-lookup"><span data-stu-id="81fe5-113">If **IsStale** returns `true` once, then it returns `true` for the remaining lifetime of the DXCore adapter list object.</span></span> <span data-ttu-id="81fe5-114">Устаревший объект списка по-прежнему считается устаревшим, даже если системные условия возвращают состояние, соответствующее списку (те же условия получаются, как и при первом создании списка).</span><span class="sxs-lookup"><span data-stu-id="81fe5-114">A stale list object is still considered stale even if system conditions return to a state that matches the list (the same conditions obtain now as did when the list was first generated).</span></span>

## <a name="see-also"></a><span data-ttu-id="81fe5-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81fe5-115">See also</span></span>

<span data-ttu-id="81fe5-116">[Идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="81fe5-116">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>