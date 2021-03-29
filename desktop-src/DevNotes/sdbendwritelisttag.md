---
description: Завершает операции записи для указанного списка.
ms.assetid: 318aa5dc-b562-47f8-8cd6-daa97f28c0f0
title: Функция Сдбендврителисттаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbEndWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: f5f203e3b643fcae174eae3634b5d337a0d7276a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662063"
---
# <a name="sdbendwritelisttag-function"></a><span data-ttu-id="4409d-103">Функция Сдбендврителисттаг</span><span class="sxs-lookup"><span data-stu-id="4409d-103">SdbEndWriteListTag function</span></span>

<span data-ttu-id="4409d-104">Завершает операции записи для указанного списка.</span><span class="sxs-lookup"><span data-stu-id="4409d-104">Ends the write operations for the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="4409d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4409d-105">Syntax</span></span>


```C++
BOOL WINAPI SdbEndWriteListTag(
  _Inout_ PDB   pdb,
  _In_    TAGID tiList
);
```



## <a name="parameters"></a><span data-ttu-id="4409d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4409d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4409d-107">*pdb* \[ -файл в, out\]</span><span class="sxs-lookup"><span data-stu-id="4409d-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4409d-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="4409d-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="4409d-109">*тилист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4409d-109">*tiList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4409d-110">[**TAGID**](tagid.md) списка</span><span class="sxs-lookup"><span data-stu-id="4409d-110">The [**TAGID**](tagid.md) of the list</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4409d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4409d-111">Return value</span></span>

<span data-ttu-id="4409d-112">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="4409d-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="4409d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4409d-113">Remarks</span></span>

<span data-ttu-id="4409d-114">Вызовите эту функцию после записи всех записей списка. Он помечает конец списка.</span><span class="sxs-lookup"><span data-stu-id="4409d-114">Call this function after writing all list entries; it will mark the end of the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="4409d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4409d-115">Requirements</span></span>



| <span data-ttu-id="4409d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4409d-116">Requirement</span></span> | <span data-ttu-id="4409d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4409d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4409d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4409d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4409d-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4409d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4409d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4409d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4409d-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4409d-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4409d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4409d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4409d-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4409d-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4409d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4409d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4409d-125">**сдббегинврителисттаг**</span><span class="sxs-lookup"><span data-stu-id="4409d-125">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="4409d-126">**сдбклоседатабасе**</span><span class="sxs-lookup"><span data-stu-id="4409d-126">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="4409d-127">**сдбклоседатабасеврите**</span><span class="sxs-lookup"><span data-stu-id="4409d-127">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
</dt> </dl>

 

 




