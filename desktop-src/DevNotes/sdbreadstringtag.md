---
Description: Извлекает строку для указанного TAGID.
ms.assetid: d67d386d-a2c5-46e2-8887-9ee20ea427f9
title: Функция Сдбреадстрингтаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3f368d66e0fbc144a46683a04655cd7f650c3bce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989276"
---
# <a name="sdbreadstringtag-function"></a><span data-ttu-id="2ff2c-103">Функция Сдбреадстрингтаг</span><span class="sxs-lookup"><span data-stu-id="2ff2c-103">SdbReadStringTag function</span></span>

<span data-ttu-id="2ff2c-104">Извлекает строку для указанного **TAGID**.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-104">Retrieves the string for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ff2c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ff2c-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadStringTag(
  _In_  PDB    pdb,
  _In_  TAGID  tiWhich,
  _Out_ LPTSTR pwszBuffer,
  _In_  DWORD  cchBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="2ff2c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ff2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ff2c-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="2ff2c-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff2c-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="2ff2c-109">*тивхич* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2ff2c-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff2c-110">**TAGID** , соответствующий получаемым данным.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="2ff2c-111">*пвсзбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2ff2c-111">*pwszBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff2c-112">Буфер, который получает строку.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-112">The buffer that receives the string.</span></span> <span data-ttu-id="2ff2c-113">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2ff2c-114">*кчбуфферсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2ff2c-114">*cchBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff2c-115">Размер буфера *пвсзбуффер* в символах.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-115">The size of the *pwszBuffer* buffer, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ff2c-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ff2c-116">Return value</span></span>

<span data-ttu-id="2ff2c-117">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ff2c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2ff2c-118">Requirements</span></span>



| <span data-ttu-id="2ff2c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2ff2c-119">Requirement</span></span> | <span data-ttu-id="2ff2c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2ff2c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ff2c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2ff2c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2ff2c-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2ff2c-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2ff2c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2ff2c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2ff2c-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2ff2c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2ff2c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2ff2c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ff2c-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ff2c-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ff2c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ff2c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ff2c-128">**сдбжетбинаритагдата**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-128">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="2ff2c-129">**сдбжетстрингтагптр**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-129">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="2ff2c-130">**сдбреадбинаритаг**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-130">**SdbReadBinaryTag**</span></span>](sdbreadbinarytag.md)
</dt> <dt>

[<span data-ttu-id="2ff2c-131">**сдбреаддвордтаг**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-131">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> </dl>

 

 




