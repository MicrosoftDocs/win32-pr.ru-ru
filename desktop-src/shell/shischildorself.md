---
UID: ''
title: Функция Шисчилдорселф
description: Сравнивает, является ли окно равным, дочерним элементом или потомком второго окна.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: IsChild
ms.topic: reference
req.header: Shlwapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
- SHIsChildOrSelf
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 911bb0b2a544197ca6db761e05adac79e97c3f69
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2020
ms.locfileid: "104997019"
---
# <a name="shischildorself-function"></a><span data-ttu-id="b8bf5-103">Функция Шисчилдорселф</span><span class="sxs-lookup"><span data-stu-id="b8bf5-103">SHIsChildOrSelf function</span></span>

## <a name="description"></a><span data-ttu-id="b8bf5-104">Описание</span><span class="sxs-lookup"><span data-stu-id="b8bf5-104">Description</span></span>

<span data-ttu-id="b8bf5-105">\[Эта функция доступна в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b8bf5-105">\[This function is available through Windows XP and Windows Server 2003.</span></span>
<span data-ttu-id="b8bf5-106">Он может быть изменен или недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b8bf5-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="b8bf5-107">Сравнивает, является ли окно равным, дочерним элементом или потомком второго окна.</span><span class="sxs-lookup"><span data-stu-id="b8bf5-107">Compares whether a window is equal to, a child of, or a descendant of, a second window.</span></span>

```cpp
HRESULT SHIsChildOrSelf(
  _In_ HWND hwndParent,
  _In_ HWND hwnd
);
```

## <a name="parameters"></a><span data-ttu-id="b8bf5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8bf5-108">Parameters</span></span>

### <a name="hwndparent-in"></a><span data-ttu-id="b8bf5-109">Хвндпарент [in]</span><span class="sxs-lookup"><span data-stu-id="b8bf5-109">hwndParent [in]</span></span>

<span data-ttu-id="b8bf5-110">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="b8bf5-110">Type: **HWND**</span></span>

<span data-ttu-id="b8bf5-111">Маркер первого окна.</span><span class="sxs-lookup"><span data-stu-id="b8bf5-111">A handle to the first window.</span></span>

### <a name="hwnd-in"></a><span data-ttu-id="b8bf5-112">HWND [в]</span><span class="sxs-lookup"><span data-stu-id="b8bf5-112">hwnd [in]</span></span>

<span data-ttu-id="b8bf5-113">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="b8bf5-113">Type: **HWND**</span></span>

<span data-ttu-id="b8bf5-114">Описатель для окна, проверяемого на соответствие *хвндпарент*.</span><span class="sxs-lookup"><span data-stu-id="b8bf5-114">A handle to a window to be tested against *hwndParent*.</span></span>

## <a name="returns"></a><span data-ttu-id="b8bf5-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8bf5-115">Returns</span></span>

<span data-ttu-id="b8bf5-116">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b8bf5-116">Type: **HRESULT**</span></span>

<span data-ttu-id="b8bf5-117">Возвращает **S_OK** , если окно, заданное параметром *HWND* , равно, дочерний элемент или потомок окна, заданного параметром *хвндпарент*.</span><span class="sxs-lookup"><span data-stu-id="b8bf5-117">Returns **S_OK** if the window specified by *hwnd* is equal to, a child of, or a descendent of the window specified by *hwndParent*.</span></span>
<span data-ttu-id="b8bf5-118">Возвращает **S_FALSE** , если окно, заданное HWND, не равно, а не является дочерним элементом, а не является потомком окна, заданного параметром *хвндпарент*.</span><span class="sxs-lookup"><span data-stu-id="b8bf5-118">Returns **S_FALSE** if the window specified by hwnd is not equal to, not a child of, and not a descendent of the window specified by *hwndParent*.</span></span>
<span data-ttu-id="b8bf5-119">Возвращаемое значение не определено, если один из окон является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="b8bf5-119">The return value is undefined if either window handle is invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8bf5-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="b8bf5-120">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="b8bf5-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8bf5-121">See also</span></span>

[<span data-ttu-id="b8bf5-122">IsChild</span><span class="sxs-lookup"><span data-stu-id="b8bf5-122">IsChild</span></span>](/windows/desktop/api/winuser/nf-winuser-ischild)
