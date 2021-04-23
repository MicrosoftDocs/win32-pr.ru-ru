---
Description: Возвращает значение DWORD для указанного TAGID.
ms.assetid: 6610e101-9068-4812-b0ca-528658b62535
title: Функция Сдбреаддвордтаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0f1f7acc113bc40388d62927b6d98f8ff7bdebf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137398"
---
# <a name="sdbreaddwordtag-function"></a><span data-ttu-id="892c0-103">Функция Сдбреаддвордтаг</span><span class="sxs-lookup"><span data-stu-id="892c0-103">SdbReadDWORDTag function</span></span>

<span data-ttu-id="892c0-104">Возвращает значение **DWORD** для указанного **TAGID**.</span><span class="sxs-lookup"><span data-stu-id="892c0-104">Retrieves the **DWORD** value for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="892c0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="892c0-105">Syntax</span></span>


```C++
DWORD WINAPI SdbReadDWORDTag(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich,
  _In_ DWORD dwDefault
);
```



## <a name="parameters"></a><span data-ttu-id="892c0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="892c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="892c0-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="892c0-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="892c0-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="892c0-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="892c0-109">*тивхич* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="892c0-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="892c0-110">**TAGID** , соответствующий получаемым данным.</span><span class="sxs-lookup"><span data-stu-id="892c0-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="892c0-111">*двдефаулт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="892c0-111">*dwDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="892c0-112">Значение по умолчанию, возвращаемое при сбое.</span><span class="sxs-lookup"><span data-stu-id="892c0-112">The default value to be returned on failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="892c0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="892c0-113">Return value</span></span>

<span data-ttu-id="892c0-114">Функция возвращает значение в случае успеха или *двдефаулт* при сбое.</span><span class="sxs-lookup"><span data-stu-id="892c0-114">The function returns the value on success or *dwDefault* on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="892c0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="892c0-115">Requirements</span></span>



| <span data-ttu-id="892c0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="892c0-116">Requirement</span></span> | <span data-ttu-id="892c0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="892c0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="892c0-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="892c0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="892c0-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="892c0-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="892c0-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="892c0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="892c0-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="892c0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="892c0-122">DLL</span><span class="sxs-lookup"><span data-stu-id="892c0-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="892c0-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="892c0-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="892c0-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="892c0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="892c0-125">**сдбжетбинаритагдата**</span><span class="sxs-lookup"><span data-stu-id="892c0-125">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="892c0-126">**сдбжетстрингтагптр**</span><span class="sxs-lookup"><span data-stu-id="892c0-126">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="892c0-127">**сдбреадквордтаг**</span><span class="sxs-lookup"><span data-stu-id="892c0-127">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="892c0-128">**сдбреадстрингтаг**</span><span class="sxs-lookup"><span data-stu-id="892c0-128">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




