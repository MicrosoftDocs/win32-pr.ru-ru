---
description: Объявляет новый индекс в указанной базе данных.
ms.assetid: 21a09201-8f84-4263-b258-77716826a3cd
title: Функция Сдбдеклареиндекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbDeclareIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 68004a29d01288a2e1d177b8a33df32b919e73ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662101"
---
# <a name="sdbdeclareindex-function"></a><span data-ttu-id="96e78-103">Функция Сдбдеклареиндекс</span><span class="sxs-lookup"><span data-stu-id="96e78-103">SdbDeclareIndex function</span></span>

<span data-ttu-id="96e78-104">Объявляет новый индекс в указанной базе данных.</span><span class="sxs-lookup"><span data-stu-id="96e78-104">Declares a new index in the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="96e78-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96e78-105">Syntax</span></span>


```C++
BOOL WINAPI SdbDeclareIndex(
  _In_  PDB     pdb,
  _In_  TAG     tWhich,
  _In_  TAG     tKey,
  _In_  DWORD   dwEntries,
  _In_  BOOL    bUniqueKey,
  _Out_ INDEXID *piiIndex
);
```



## <a name="parameters"></a><span data-ttu-id="96e78-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="96e78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96e78-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="96e78-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e78-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="96e78-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="96e78-109">*твхич* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="96e78-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e78-110">Этот параметр должен быть **\_ \_ списком типов тегов**.</span><span class="sxs-lookup"><span data-stu-id="96e78-110">This parameter must be **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="96e78-111">*tKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="96e78-111">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e78-112">ТЕГ, указывающий тип, который будет использоваться в качестве ключа.</span><span class="sxs-lookup"><span data-stu-id="96e78-112">The TAG that specifies the type to be used as the key.</span></span> <span data-ttu-id="96e78-113">Этот параметр не может **быть \_ \_ списком типов тегов**.</span><span class="sxs-lookup"><span data-stu-id="96e78-113">This parameter cannot be **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="96e78-114">*двентриес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="96e78-114">*dwEntries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e78-115">Число записей для выделения в индексе.</span><span class="sxs-lookup"><span data-stu-id="96e78-115">The number of entries to allocate in the index.</span></span>

</dd> <dt>

<span data-ttu-id="96e78-116">*буникуекэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="96e78-116">*bUniqueKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e78-117">Если этот параметр имеет **значение true**, то индекс является индексом уникального ключа.</span><span class="sxs-lookup"><span data-stu-id="96e78-117">If this parameter is **TRUE**, the index is a unique-key index.</span></span>

</dd> <dt>

<span data-ttu-id="96e78-118">*пиииндекс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="96e78-118">*piiIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96e78-119">Результирующий **индексид** только что объявленного индекса.</span><span class="sxs-lookup"><span data-stu-id="96e78-119">The resulting **INDEXID** of the newly declared index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96e78-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96e78-120">Return value</span></span>

<span data-ttu-id="96e78-121">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="96e78-121">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="96e78-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96e78-122">Remarks</span></span>

<span data-ttu-id="96e78-123">Вызовите эту функцию перед записью тегов в новый индекс.</span><span class="sxs-lookup"><span data-stu-id="96e78-123">Call this function before writing tags to the new index.</span></span>

## <a name="requirements"></a><span data-ttu-id="96e78-124">Требования</span><span class="sxs-lookup"><span data-stu-id="96e78-124">Requirements</span></span>



| <span data-ttu-id="96e78-125">Требование</span><span class="sxs-lookup"><span data-stu-id="96e78-125">Requirement</span></span> | <span data-ttu-id="96e78-126">Значение</span><span class="sxs-lookup"><span data-stu-id="96e78-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96e78-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96e78-127">Minimum supported client</span></span><br/> | <span data-ttu-id="96e78-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96e78-128">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="96e78-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96e78-129">Minimum supported server</span></span><br/> | <span data-ttu-id="96e78-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="96e78-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="96e78-131">DLL</span><span class="sxs-lookup"><span data-stu-id="96e78-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96e78-132"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96e78-132"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96e78-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96e78-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96e78-134">**индексид**</span><span class="sxs-lookup"><span data-stu-id="96e78-134">**INDEXID**</span></span>](indexid.md)
</dt> <dt>

[<span data-ttu-id="96e78-135">**сдбкоммитиндексес**</span><span class="sxs-lookup"><span data-stu-id="96e78-135">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="96e78-136">**сдбстартиндексинг**</span><span class="sxs-lookup"><span data-stu-id="96e78-136">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="96e78-137">**сдбстопиндексинг**</span><span class="sxs-lookup"><span data-stu-id="96e78-137">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




