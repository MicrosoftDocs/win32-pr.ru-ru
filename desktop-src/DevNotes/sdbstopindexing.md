---
description: Отключает создание и изменение индекса для указанной базы данных.
ms.assetid: d079eae2-574e-4ac1-a0f9-11796e56a790
title: Функция Сдбстопиндексинг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbStopIndexing
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3c9c6b34c265d611b57a3e73bb0c8fb1822fe752
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538648"
---
# <a name="sdbstopindexing-function"></a><span data-ttu-id="8e61e-103">Функция Сдбстопиндексинг</span><span class="sxs-lookup"><span data-stu-id="8e61e-103">SdbStopIndexing function</span></span>

<span data-ttu-id="8e61e-104">Отключает создание и изменение индекса для указанной базы данных.</span><span class="sxs-lookup"><span data-stu-id="8e61e-104">Disables index creation and modification for the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e61e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e61e-105">Syntax</span></span>


```C++
BOOL WINAPI SdbStopIndexing(
  _In_ PDB     pdb,
  _In_ INDEXID iiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="8e61e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e61e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e61e-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="8e61e-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e61e-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="8e61e-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="8e61e-109">*иивхич* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e61e-109">*iiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e61e-110">Идентификатор индекса.</span><span class="sxs-lookup"><span data-stu-id="8e61e-110">The index identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e61e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e61e-111">Return value</span></span>

<span data-ttu-id="8e61e-112">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="8e61e-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e61e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8e61e-113">Requirements</span></span>



| <span data-ttu-id="8e61e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8e61e-114">Requirement</span></span> | <span data-ttu-id="8e61e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8e61e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e61e-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e61e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8e61e-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e61e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8e61e-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e61e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8e61e-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8e61e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8e61e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="8e61e-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e61e-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e61e-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e61e-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e61e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e61e-123">**сдбкоммитиндексес**</span><span class="sxs-lookup"><span data-stu-id="8e61e-123">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="8e61e-124">**сдбдеклареиндекс**</span><span class="sxs-lookup"><span data-stu-id="8e61e-124">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="8e61e-125">**сдбстартиндексинг**</span><span class="sxs-lookup"><span data-stu-id="8e61e-125">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> </dl>

 

 




