---
description: Включает создание и изменение индекса для указанной базы данных.
ms.assetid: f780034e-6963-423c-8ffa-9fbe98dca7e1
title: Функция Сдбстартиндексинг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbStartIndexing
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e3324b4cb0d42ca33ee7c3234a1acc099adcb743
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141246"
---
# <a name="sdbstartindexing-function"></a><span data-ttu-id="39a43-103">Функция Сдбстартиндексинг</span><span class="sxs-lookup"><span data-stu-id="39a43-103">SdbStartIndexing function</span></span>

<span data-ttu-id="39a43-104">Включает создание и изменение индекса для указанной базы данных.</span><span class="sxs-lookup"><span data-stu-id="39a43-104">Enables index creation and modification for the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="39a43-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39a43-105">Syntax</span></span>


```C++
BOOL WINAPI SdbStartIndexing(
  _In_ PDB     pdb,
  _In_ INDEXID iiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="39a43-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="39a43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39a43-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="39a43-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39a43-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="39a43-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="39a43-109">*иивхич* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39a43-109">*iiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39a43-110">Идентификатор индекса.</span><span class="sxs-lookup"><span data-stu-id="39a43-110">The index identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39a43-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39a43-111">Return value</span></span>

<span data-ttu-id="39a43-112">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="39a43-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="39a43-113">Требования</span><span class="sxs-lookup"><span data-stu-id="39a43-113">Requirements</span></span>



| <span data-ttu-id="39a43-114">Требование</span><span class="sxs-lookup"><span data-stu-id="39a43-114">Requirement</span></span> | <span data-ttu-id="39a43-115">Значение</span><span class="sxs-lookup"><span data-stu-id="39a43-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39a43-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39a43-116">Minimum supported client</span></span><br/> | <span data-ttu-id="39a43-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39a43-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="39a43-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39a43-118">Minimum supported server</span></span><br/> | <span data-ttu-id="39a43-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="39a43-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="39a43-120">DLL</span><span class="sxs-lookup"><span data-stu-id="39a43-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39a43-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39a43-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39a43-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39a43-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39a43-123">**сдбкоммитиндексес**</span><span class="sxs-lookup"><span data-stu-id="39a43-123">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="39a43-124">**сдбдеклареиндекс**</span><span class="sxs-lookup"><span data-stu-id="39a43-124">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="39a43-125">**сдбстопиндексинг**</span><span class="sxs-lookup"><span data-stu-id="39a43-125">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




