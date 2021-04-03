---
description: Записывает строку в указанную базу данных.
ms.assetid: 72c62d91-0c1c-4ff8-8829-1c3ec1fa8648
title: Функция Сдбвритестрингтаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4ac588d99408d0d7f13bc0fd13d8abe8a6580e69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895654"
---
# <a name="sdbwritestringtag-function"></a><span data-ttu-id="913f8-103">Функция Сдбвритестрингтаг</span><span class="sxs-lookup"><span data-stu-id="913f8-103">SdbWriteStringTag function</span></span>

<span data-ttu-id="913f8-104">Записывает строку в указанную базу данных.</span><span class="sxs-lookup"><span data-stu-id="913f8-104">Writes a string to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="913f8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="913f8-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteStringTag(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszData
);
```



## <a name="parameters"></a><span data-ttu-id="913f8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="913f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="913f8-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="913f8-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="913f8-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="913f8-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="913f8-109">*ттаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="913f8-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="913f8-110">ТЕГ для записи.</span><span class="sxs-lookup"><span data-stu-id="913f8-110">The TAG for the entry.</span></span> <span data-ttu-id="913f8-111">Этот тег должен иметь тип **Tag \_ \_ стрингреф**.</span><span class="sxs-lookup"><span data-stu-id="913f8-111">This TAG must be of type **TAG\_TYPE\_STRINGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="913f8-112">*пвсздата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="913f8-112">*pwszData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="913f8-113">Строка, завершающаяся нулем.</span><span class="sxs-lookup"><span data-stu-id="913f8-113">The null-terminated string.</span></span> <span data-ttu-id="913f8-114">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="913f8-114">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="913f8-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="913f8-115">Return value</span></span>

<span data-ttu-id="913f8-116">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="913f8-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="913f8-117">Требования</span><span class="sxs-lookup"><span data-stu-id="913f8-117">Requirements</span></span>



| <span data-ttu-id="913f8-118">Требование</span><span class="sxs-lookup"><span data-stu-id="913f8-118">Requirement</span></span> | <span data-ttu-id="913f8-119">Значение</span><span class="sxs-lookup"><span data-stu-id="913f8-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="913f8-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="913f8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="913f8-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="913f8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="913f8-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="913f8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="913f8-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="913f8-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="913f8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="913f8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="913f8-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="913f8-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="913f8-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="913f8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="913f8-127">**сдбвритебинаритаг**</span><span class="sxs-lookup"><span data-stu-id="913f8-127">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="913f8-128">**сдбвритедвордтаг**</span><span class="sxs-lookup"><span data-stu-id="913f8-128">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="913f8-129">**сдбвритеквордтаг**</span><span class="sxs-lookup"><span data-stu-id="913f8-129">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="913f8-130">**сдбвритевордтаг**</span><span class="sxs-lookup"><span data-stu-id="913f8-130">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




