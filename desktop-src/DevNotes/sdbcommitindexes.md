---
description: Фиксирует вновь созданные индексы для указанной базы данных.
ms.assetid: 92f05e5f-599a-4870-8175-61b83c943514
title: Функция Сдбкоммитиндексес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCommitIndexes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0709a913dc78cefdf405a0a3bd29030801941c37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141099"
---
# <a name="sdbcommitindexes-function"></a><span data-ttu-id="4e787-103">Функция Сдбкоммитиндексес</span><span class="sxs-lookup"><span data-stu-id="4e787-103">SdbCommitIndexes function</span></span>

<span data-ttu-id="4e787-104">Фиксирует вновь созданные индексы для указанной базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e787-104">Commits newly created indexes to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e787-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e787-105">Syntax</span></span>


```C++
BOOL WINAPI SdbCommitIndexes(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="4e787-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e787-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e787-107">*pdb* \[ -файл в, out\]</span><span class="sxs-lookup"><span data-stu-id="4e787-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e787-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="4e787-108">A handle to the shim database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e787-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e787-109">Return value</span></span>

<span data-ttu-id="4e787-110">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="4e787-110">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e787-111">Требования</span><span class="sxs-lookup"><span data-stu-id="4e787-111">Requirements</span></span>



| <span data-ttu-id="4e787-112">Требование</span><span class="sxs-lookup"><span data-stu-id="4e787-112">Requirement</span></span> | <span data-ttu-id="4e787-113">Значение</span><span class="sxs-lookup"><span data-stu-id="4e787-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e787-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e787-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4e787-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e787-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4e787-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e787-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4e787-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4e787-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4e787-118">DLL</span><span class="sxs-lookup"><span data-stu-id="4e787-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e787-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e787-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e787-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e787-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e787-121">**сдбдеклареиндекс**</span><span class="sxs-lookup"><span data-stu-id="4e787-121">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="4e787-122">**сдбстартиндексинг**</span><span class="sxs-lookup"><span data-stu-id="4e787-122">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="4e787-123">**сдбстопиндексинг**</span><span class="sxs-lookup"><span data-stu-id="4e787-123">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




