---
description: Идентификатор индекса, к которому будет осуществляться доступ в базе данных.
ms.assetid: 559e73bf-91c2-4dbf-a667-e5c0431aaffa
title: индексид
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b6ef6b79dd19183f575930e9793a6ab2f1f5cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142157"
---
# <a name="indexid"></a><span data-ttu-id="dff8d-103">индексид</span><span class="sxs-lookup"><span data-stu-id="dff8d-103">INDEXID</span></span>

<span data-ttu-id="dff8d-104">Идентификатор индекса, к которому будет осуществляться доступ в базе данных.</span><span class="sxs-lookup"><span data-stu-id="dff8d-104">The identifier of the index to be accessed in a database.</span></span>


```C++
typedef DWORD INDEXID;
```



## <a name="remarks"></a><span data-ttu-id="dff8d-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dff8d-105">Remarks</span></span>

<span data-ttu-id="dff8d-106">**Индексид** может быть целочисленным значением, представляющим индекс, или следующим значением:</span><span class="sxs-lookup"><span data-stu-id="dff8d-106">An **INDEXID** can be an integer value that represents the index, or the following value:</span></span>

<dl> <dt>

<span data-ttu-id="dff8d-107"><span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>ИНДЕКСИД \_ null ((индексид)-1)</span><span class="sxs-lookup"><span data-stu-id="dff8d-107"><span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>INDEXID\_NULL ((INDEXID)-1)</span></span>
</dt> <dd>

<span data-ttu-id="dff8d-108">Недопустимый **индексид**.</span><span class="sxs-lookup"><span data-stu-id="dff8d-108">An invalid **INDEXID**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dff8d-109">Требования</span><span class="sxs-lookup"><span data-stu-id="dff8d-109">Requirements</span></span>



| <span data-ttu-id="dff8d-110">Требование</span><span class="sxs-lookup"><span data-stu-id="dff8d-110">Requirement</span></span> | <span data-ttu-id="dff8d-111">Значение</span><span class="sxs-lookup"><span data-stu-id="dff8d-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dff8d-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dff8d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="dff8d-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dff8d-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dff8d-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dff8d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="dff8d-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dff8d-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dff8d-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dff8d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff8d-117">**сдбдеклареиндекс**</span><span class="sxs-lookup"><span data-stu-id="dff8d-117">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="dff8d-118">**сдбстартиндексинг**</span><span class="sxs-lookup"><span data-stu-id="dff8d-118">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="dff8d-119">**сдбстопиндексинг**</span><span class="sxs-lookup"><span data-stu-id="dff8d-119">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




