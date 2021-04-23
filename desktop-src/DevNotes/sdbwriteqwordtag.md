---
description: Записывает значение QWORD в указанную базу данных.
ms.assetid: 8ce566ea-a941-45fa-b031-26c3144ca02c
title: Функция Сдбвритеквордтаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 58dcaad3487bb1f59a75dd6a671ecb43c9cf1751
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807217"
---
# <a name="sdbwriteqwordtag-function"></a><span data-ttu-id="0c353-103">Функция Сдбвритеквордтаг</span><span class="sxs-lookup"><span data-stu-id="0c353-103">SdbWriteQWORDTag function</span></span>

<span data-ttu-id="0c353-104">Записывает значение **QWORD** в указанную базу данных.</span><span class="sxs-lookup"><span data-stu-id="0c353-104">Writes a **QWORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c353-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c353-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteQWORDTag(
  _In_ PDB       pdb,
  _In_ TAG       tTag,
  _In_ ULONGLONG qwData
);
```



## <a name="parameters"></a><span data-ttu-id="0c353-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c353-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c353-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="0c353-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c353-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="0c353-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="0c353-109">*ттаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0c353-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c353-110">ТЕГ для записи.</span><span class="sxs-lookup"><span data-stu-id="0c353-110">The TAG for the entry.</span></span> <span data-ttu-id="0c353-111">Этот тег должен иметь тип **тега \_ \_ QWORD**.</span><span class="sxs-lookup"><span data-stu-id="0c353-111">This TAG must be of type **TAG\_TYPE\_QWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="0c353-112">*квдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0c353-112">*qwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c353-113">Значение.</span><span class="sxs-lookup"><span data-stu-id="0c353-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c353-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c353-114">Return value</span></span>

<span data-ttu-id="0c353-115">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="0c353-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c353-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0c353-116">Requirements</span></span>



| <span data-ttu-id="0c353-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0c353-117">Requirement</span></span> | <span data-ttu-id="0c353-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0c353-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c353-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c353-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0c353-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c353-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0c353-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c353-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0c353-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0c353-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0c353-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0c353-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c353-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c353-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c353-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c353-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c353-126">**сдбвритебинаритаг**</span><span class="sxs-lookup"><span data-stu-id="0c353-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="0c353-127">**сдбвритедвордтаг**</span><span class="sxs-lookup"><span data-stu-id="0c353-127">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="0c353-128">**сдбвритестрингтаг**</span><span class="sxs-lookup"><span data-stu-id="0c353-128">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="0c353-129">**сдбвритевордтаг**</span><span class="sxs-lookup"><span data-stu-id="0c353-129">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




