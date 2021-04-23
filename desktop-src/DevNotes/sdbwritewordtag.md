---
description: Записывает значение слова в указанную базу данных.
ms.assetid: 8f921e14-4a82-4d8e-83fa-beb78118ecb8
title: Функция Сдбвритевордтаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75a5b3eb430901de36d5aca325f928aae266bc39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538639"
---
# <a name="sdbwritewordtag-function"></a><span data-ttu-id="18949-103">Функция Сдбвритевордтаг</span><span class="sxs-lookup"><span data-stu-id="18949-103">SdbWriteWORDTag function</span></span>

<span data-ttu-id="18949-104">Записывает значение **слова** в указанную базу данных.</span><span class="sxs-lookup"><span data-stu-id="18949-104">Writes a **WORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="18949-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18949-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteWORDTag(
  _In_ PDB  pdb,
  _In_ TAG  tTag,
  _In_ WORD wData
);
```



## <a name="parameters"></a><span data-ttu-id="18949-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="18949-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18949-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="18949-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18949-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="18949-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="18949-109">*ттаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18949-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18949-110">ТЕГ для записи.</span><span class="sxs-lookup"><span data-stu-id="18949-110">The TAG for the entry.</span></span> <span data-ttu-id="18949-111">Этот тег должен иметь тип **тега \_ \_ Word**.</span><span class="sxs-lookup"><span data-stu-id="18949-111">This TAG must be of type **TAG\_TYPE\_WORD**.</span></span>

</dd> <dt>

<span data-ttu-id="18949-112">*вдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18949-112">*wData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18949-113">Значение.</span><span class="sxs-lookup"><span data-stu-id="18949-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18949-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18949-114">Return value</span></span>

<span data-ttu-id="18949-115">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="18949-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="18949-116">Требования</span><span class="sxs-lookup"><span data-stu-id="18949-116">Requirements</span></span>



| <span data-ttu-id="18949-117">Требование</span><span class="sxs-lookup"><span data-stu-id="18949-117">Requirement</span></span> | <span data-ttu-id="18949-118">Значение</span><span class="sxs-lookup"><span data-stu-id="18949-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18949-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18949-119">Minimum supported client</span></span><br/> | <span data-ttu-id="18949-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18949-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="18949-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18949-121">Minimum supported server</span></span><br/> | <span data-ttu-id="18949-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="18949-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="18949-123">DLL</span><span class="sxs-lookup"><span data-stu-id="18949-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18949-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18949-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18949-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18949-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18949-126">**сдбвритебинаритаг**</span><span class="sxs-lookup"><span data-stu-id="18949-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="18949-127">**сдбвритедвордтаг**</span><span class="sxs-lookup"><span data-stu-id="18949-127">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="18949-128">**сдбвритеквордтаг**</span><span class="sxs-lookup"><span data-stu-id="18949-128">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="18949-129">**сдбвритестрингтаг**</span><span class="sxs-lookup"><span data-stu-id="18949-129">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> </dl>

 

 




