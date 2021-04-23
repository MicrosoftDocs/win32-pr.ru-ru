---
Description: Извлекает значение QWORD для указанного TAGID.
ms.assetid: 5fa94a95-c7f3-477b-ab7c-931e8d62d501
title: Функция Сдбреадквордтаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 15227f3d7c3177a226f1b3cc77fc78efd34379d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416073"
---
# <a name="sdbreadqwordtag-function"></a><span data-ttu-id="9b02b-103">Функция Сдбреадквордтаг</span><span class="sxs-lookup"><span data-stu-id="9b02b-103">SdbReadQWORDTag function</span></span>

<span data-ttu-id="9b02b-104">Извлекает значение **QWORD** для указанного **TAGID**.</span><span class="sxs-lookup"><span data-stu-id="9b02b-104">Retrieves the **QWORD** value for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b02b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b02b-105">Syntax</span></span>


```C++
ULONGLONG WINAPI SdbReadQWORDTag(
  _In_ PDB       pdb,
  _In_ TAGID     tiWhich,
  _In_ ULONGLONG qwDefault
);
```



## <a name="parameters"></a><span data-ttu-id="9b02b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b02b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b02b-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="9b02b-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b02b-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="9b02b-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="9b02b-109">*тивхич* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b02b-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b02b-110">**TAGID** , соответствующий получаемым данным.</span><span class="sxs-lookup"><span data-stu-id="9b02b-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="9b02b-111">*квдефаулт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b02b-111">*qwDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b02b-112">Значение по умолчанию, возвращаемое при сбое.</span><span class="sxs-lookup"><span data-stu-id="9b02b-112">The default value to be returned on failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b02b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b02b-113">Return value</span></span>

<span data-ttu-id="9b02b-114">Функция возвращает значение в случае успеха или *квдефаулт* при сбое.</span><span class="sxs-lookup"><span data-stu-id="9b02b-114">The function returns the value on success or *qwDefault* on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b02b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9b02b-115">Requirements</span></span>



| <span data-ttu-id="9b02b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9b02b-116">Requirement</span></span> | <span data-ttu-id="9b02b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9b02b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b02b-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b02b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9b02b-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9b02b-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9b02b-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b02b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9b02b-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9b02b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9b02b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9b02b-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b02b-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b02b-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b02b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b02b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b02b-125">**сдбжетбинаритагдата**</span><span class="sxs-lookup"><span data-stu-id="9b02b-125">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="9b02b-126">**сдбжетстрингтагптр**</span><span class="sxs-lookup"><span data-stu-id="9b02b-126">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="9b02b-127">**сдбреаддвордтаг**</span><span class="sxs-lookup"><span data-stu-id="9b02b-127">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="9b02b-128">**сдбреадстрингтаг**</span><span class="sxs-lookup"><span data-stu-id="9b02b-128">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




