---
title: Сообщение CB_INITSTORAGE (Winuser. h)
description: Приложение отправляет \_ сообщение ИНИТСТОРАЖЕ CB перед добавлением большого числа элементов в список в поле со списком. Это сообщение выделяет память для хранения элементов списка.
ms.assetid: fb289968-a95b-4ca0-977d-b8651166f357
keywords:
- Элементы управления Windows для CB_INITSTORAGE сообщений
topic_type:
- apiref
api_name:
- CB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78c2ae2592d89ba7a0f6392666dac0404d52e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135862"
---
# <a name="cb_initstorage-message"></a><span data-ttu-id="8c030-105">\_Сообщение ИНИТСТОРАЖЕ CB</span><span class="sxs-lookup"><span data-stu-id="8c030-105">CB\_INITSTORAGE message</span></span>

<span data-ttu-id="8c030-106">Приложение отправляет сообщение **\_ инитстораже CB** перед добавлением большого числа элементов в список в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="8c030-106">An application sends the **CB\_INITSTORAGE** message before adding a large number of items to the list box portion of a combo box.</span></span> <span data-ttu-id="8c030-107">Это сообщение выделяет память для хранения элементов списка.</span><span class="sxs-lookup"><span data-stu-id="8c030-107">This message allocates memory for storing list box items.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c030-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c030-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c030-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c030-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c030-110">Число добавляемых элементов.</span><span class="sxs-lookup"><span data-stu-id="8c030-110">The number of items to add.</span></span>

</dd> <dt>

<span data-ttu-id="8c030-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c030-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c030-112">Объем памяти, выделяемой для строк элемента в байтах.</span><span class="sxs-lookup"><span data-stu-id="8c030-112">The amount of memory to allocate for item strings, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c030-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c030-113">Return value</span></span>

<span data-ttu-id="8c030-114">Если сообщение прошло успешно, возвращаемое значение — это общее число элементов, для которых была предварительно распределена память, то есть общее число элементов, добавленных всеми успешными сообщениями **\_ инитстораже CB** .</span><span class="sxs-lookup"><span data-stu-id="8c030-114">If the message is successful, the return value is the total number of items for which memory has been pre-allocated, that is, the total number of items added by all successful **CB\_INITSTORAGE** messages.</span></span>

<span data-ttu-id="8c030-115">Если сообщение не выполняется, возвращается значение CB \_ еррспаце.</span><span class="sxs-lookup"><span data-stu-id="8c030-115">If the message fails, the return value is CB\_ERRSPACE.</span></span>

<span data-ttu-id="8c030-116">Сообщение выделяет память и возвращает значения успешно и ошибок, описанные выше.</span><span class="sxs-lookup"><span data-stu-id="8c030-116">The message allocates memory and returns the success and error values described above.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c030-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c030-117">Remarks</span></span>

<span data-ttu-id="8c030-118">Сообщение **\_ инитстораже CB** помогает ускорить инициализацию полей со списком, имеющих большое количество элементов (свыше 100).</span><span class="sxs-lookup"><span data-stu-id="8c030-118">The **CB\_INITSTORAGE** message helps speed up the initialization of combo boxes that have a large number of items (over 100).</span></span> <span data-ttu-id="8c030-119">Он резервирует указанный объем памяти, чтобы последующие сообщения [**CB \_ ADDSTRING**](cb-addstring.md), [**CB \_ инсертстринг**](cb-insertstring.md)и [**CB \_ dir**](cb-dir.md) были в кратчайшие сроки.</span><span class="sxs-lookup"><span data-stu-id="8c030-119">It reserves the specified amount of memory so that subsequent [**CB\_ADDSTRING**](cb-addstring.md), [**CB\_INSERTSTRING**](cb-insertstring.md), and [**CB\_DIR**](cb-dir.md) messages take the shortest possible time.</span></span> <span data-ttu-id="8c030-120">Для параметров *wParam* и *lParam* можно использовать оценки.</span><span class="sxs-lookup"><span data-stu-id="8c030-120">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="8c030-121">При превышении лимитной оценки выделяется дополнительный объем памяти, если недооценивать, для элементов, превышающих запрошенный объем, используется нормальное выделение.</span><span class="sxs-lookup"><span data-stu-id="8c030-121">If you overestimate, the extra memory is allocated, if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c030-122">Требования</span><span class="sxs-lookup"><span data-stu-id="8c030-122">Requirements</span></span>



| <span data-ttu-id="8c030-123">Требование</span><span class="sxs-lookup"><span data-stu-id="8c030-123">Requirement</span></span> | <span data-ttu-id="8c030-124">Значение</span><span class="sxs-lookup"><span data-stu-id="8c030-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c030-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c030-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8c030-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c030-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8c030-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c030-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8c030-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8c030-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8c030-129">Header</span><span class="sxs-lookup"><span data-stu-id="8c030-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c030-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c030-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c030-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c030-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="8c030-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="8c030-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8c030-133">**\_ADDSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="8c030-133">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="8c030-134">**\_Каталог CB**</span><span class="sxs-lookup"><span data-stu-id="8c030-134">**CB\_DIR**</span></span>](cb-dir.md)
</dt> <dt>

[<span data-ttu-id="8c030-135">**\_ИНСЕРТСТРИНГ CB**</span><span class="sxs-lookup"><span data-stu-id="8c030-135">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> </dl>

 

 





