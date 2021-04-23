---
UID: ''
title: Функция InterlockedPushListSList
description: Вставляет однонаправленный список в начале другого однонаправленного списка.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: InterlockedPushListSListEx
ms.topic: reference
req.header:
- WinBase.h on Windows Vista, Windows 7, Windows Server 2008 and Windows Server 2008 R2
- InterlockedAPI.h on Windows 8 and Windows Server 2012
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-interlocked-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-interlocked-l1-1-0.dll
api_name:
- InterlockedPushListSList
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: ccecdae3af5119a86594c31856dac11ecb4507bc
ms.sourcegitcommit: be77ed1f97d3be57a2f42070589de21b66034adf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2020
ms.locfileid: "104412716"
---
# <a name="interlockedpushlistslist-function"></a><span data-ttu-id="cad3f-103">Функция InterlockedPushListSList</span><span class="sxs-lookup"><span data-stu-id="cad3f-103">InterlockedPushListSList function</span></span>

## <a name="description"></a><span data-ttu-id="cad3f-104">Описание</span><span class="sxs-lookup"><span data-stu-id="cad3f-104">Description</span></span>

<span data-ttu-id="cad3f-105">Вставляет однонаправленный список в начале другого однонаправленного списка.</span><span class="sxs-lookup"><span data-stu-id="cad3f-105">Inserts a singly-linked list at the front of another singly linked list.</span></span>
<span data-ttu-id="cad3f-106">Доступ к спискам синхронизируется в многопроцессорной системе.</span><span class="sxs-lookup"><span data-stu-id="cad3f-106">Access to the lists is synchronized on a multiprocessor system.</span></span>

```cpp
PSLIST_ENTRY  FASTCALL InterlockedPushListSList(
  _Inout_ PSLIST_HEADER ListHead,
  _Inout_ PSLIST_ENTRY  List,
  _Inout_ PSLIST_ENTRY  ListEnd,
  _In_    ULONG         Count
);
```

## <a name="parameters"></a><span data-ttu-id="cad3f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cad3f-107">Parameters</span></span>

### <a name="listhead-in-out"></a><span data-ttu-id="cad3f-108">Лиссеад [вход, выход]</span><span class="sxs-lookup"><span data-stu-id="cad3f-108">ListHead [in, out]</span></span>

<span data-ttu-id="cad3f-109">Указатель на структуру **SLIST_HEADER** , представляющую собой заголовок однонаправленного списка.</span><span class="sxs-lookup"><span data-stu-id="cad3f-109">Pointer to an **SLIST_HEADER** structure that represents the head of a singly linked list.</span></span>
<span data-ttu-id="cad3f-110">Список, указанный в *списке* и *прослушиваемых* параметрах, вставляется в начало этого списка.</span><span class="sxs-lookup"><span data-stu-id="cad3f-110">The list specified by the *List* and *ListEnd* parameters is inserted at the front of this list.</span></span>

### <a name="list-in-out"></a><span data-ttu-id="cad3f-111">List [входные и выходные]</span><span class="sxs-lookup"><span data-stu-id="cad3f-111">List [in, out]</span></span>

<span data-ttu-id="cad3f-112">Указатель на структуру [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) , представляющую первый элемент в списке для вставки.</span><span class="sxs-lookup"><span data-stu-id="cad3f-112">Pointer to an [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) structure that represents the first item in the list to be inserted.</span></span>

### <a name="listend-in-out"></a><span data-ttu-id="cad3f-113">ListEned [вход, выход]</span><span class="sxs-lookup"><span data-stu-id="cad3f-113">ListEnd [in, out]</span></span>

<span data-ttu-id="cad3f-114">Указатель на структуру [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) , представляющую последний элемент в вставляемом списке.</span><span class="sxs-lookup"><span data-stu-id="cad3f-114">Pointer to an [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) structure that represents the last item in the list to be inserted.</span></span>

### <a name="count-in"></a><span data-ttu-id="cad3f-115">Число [в]</span><span class="sxs-lookup"><span data-stu-id="cad3f-115">Count [in]</span></span>

<span data-ttu-id="cad3f-116">Число вставляемых элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="cad3f-116">The number of items in the list to be inserted.</span></span>

## <a name="returns"></a><span data-ttu-id="cad3f-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cad3f-117">Returns</span></span>

<span data-ttu-id="cad3f-118">Возвращаемое значение — это предыдущий первый элемент в списке, заданном параметром *лиссеад* .</span><span class="sxs-lookup"><span data-stu-id="cad3f-118">The return value is the previous first item in the list specified by the *ListHead* parameter.</span></span>
<span data-ttu-id="cad3f-119">Если список был ранее пустым, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="cad3f-119">If the list was previously empty, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cad3f-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cad3f-120">Remarks</span></span>

<span data-ttu-id="cad3f-121">Все элементы списка должны быть согласованы по границе **MEMORY_ALLOCATION_ALIGNMENT** ; в противном случае эта функция будет вести себя непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="cad3f-121">All list items must be aligned on a **MEMORY_ALLOCATION_ALIGNMENT** boundary; otherwise, this function will behave unpredictably.</span></span>
<span data-ttu-id="cad3f-122">См. **_aligned_malloc**.</span><span class="sxs-lookup"><span data-stu-id="cad3f-122">See **_aligned_malloc**.</span></span>

<span data-ttu-id="cad3f-123">**Windows 8 и Windows Server 2012:**  Эта функция была заменена [интерлоккедпушлистслистекс](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex).</span><span class="sxs-lookup"><span data-stu-id="cad3f-123">**Windows 8 and Windows Server 2012:**  This function has been superceded by [InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex).</span></span>
<span data-ttu-id="cad3f-124">При компиляции с **NTDDI_VERSION** , для которого задано значение **NTDDI_WIN8** или больше, вызовы **Интерлоккедпушлистслист** будут переходят в **интерлоккедпушлистслистекс** .</span><span class="sxs-lookup"><span data-stu-id="cad3f-124">When compiling with **NTDDI_VERSION** set to **NTDDI_WIN8** or greater, calls to **InterlockedPushListSList** will go to **InterlockedPushListSListEx** instead.</span></span>

## <a name="see-also"></a><span data-ttu-id="cad3f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cad3f-125">See also</span></span>

[<span data-ttu-id="cad3f-126">Взаимозаблокированные однонаправленные списки</span><span class="sxs-lookup"><span data-stu-id="cad3f-126">Interlocked Singly Linked Lists</span></span>](/windows/desktop/Sync/interlocked-singly-linked-lists)

[<span data-ttu-id="cad3f-127">интерлоккедпопентрислист</span><span class="sxs-lookup"><span data-stu-id="cad3f-127">InterlockedPopEntrySList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)

[<span data-ttu-id="cad3f-128">интерлоккедпушентрислист</span><span class="sxs-lookup"><span data-stu-id="cad3f-128">InterlockedPushEntrySList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)

[<span data-ttu-id="cad3f-129">интерлоккедпушлистслистекс</span><span class="sxs-lookup"><span data-stu-id="cad3f-129">InterlockedPushListSListEx</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)

[<span data-ttu-id="cad3f-130">интерлоккедфлушслист</span><span class="sxs-lookup"><span data-stu-id="cad3f-130">InterlockedFlushSList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist)

[<span data-ttu-id="cad3f-131">SLIST_ENTRY</span><span class="sxs-lookup"><span data-stu-id="cad3f-131">SLIST_ENTRY</span></span>](/windows/win32/api/winnt/ns-winnt-slist_entry)

[<span data-ttu-id="cad3f-132">Использование однонаправленных списков</span><span class="sxs-lookup"><span data-stu-id="cad3f-132">Using Singly Linked Lists</span></span>](/windows/desktop/Sync/using-singly-linked-lists)
