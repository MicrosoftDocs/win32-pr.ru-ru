---
Description: Извлекает двоичные данные для указанного TAGID.
ms.assetid: b349f2af-2505-4efc-bd59-203f7666ce61
title: Функция Сдбреадбинаритаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 024b432c3210b98721a0cf3058bad0f765287fde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654487"
---
# <a name="sdbreadbinarytag-function"></a><span data-ttu-id="56237-103">Функция Сдбреадбинаритаг</span><span class="sxs-lookup"><span data-stu-id="56237-103">SdbReadBinaryTag function</span></span>

<span data-ttu-id="56237-104">Извлекает двоичные данные для указанного **TAGID**.</span><span class="sxs-lookup"><span data-stu-id="56237-104">Retrieves the binary data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="56237-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56237-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadBinaryTag(
  _In_  PDB   pdb,
  _In_  TAGID tiWhich,
  _Out_ PBYTE pBuffer,
  _In_  DWORD dwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="56237-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="56237-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56237-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="56237-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56237-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="56237-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="56237-109">*тивхич* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="56237-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56237-110">**TAGID** , соответствующий получаемым данным.</span><span class="sxs-lookup"><span data-stu-id="56237-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="56237-111">*pBuffer* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="56237-111">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56237-112">Буфер, который получает двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="56237-112">The buffer that receives the binary data.</span></span> <span data-ttu-id="56237-113">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="56237-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="56237-114">*двбуфферсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="56237-114">*dwBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56237-115">Размер буфера *pBuffer* в байтах.</span><span class="sxs-lookup"><span data-stu-id="56237-115">The size of the *pBuffer* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56237-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56237-116">Return value</span></span>

<span data-ttu-id="56237-117">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="56237-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="56237-118">Требования</span><span class="sxs-lookup"><span data-stu-id="56237-118">Requirements</span></span>



| <span data-ttu-id="56237-119">Требование</span><span class="sxs-lookup"><span data-stu-id="56237-119">Requirement</span></span> | <span data-ttu-id="56237-120">Значение</span><span class="sxs-lookup"><span data-stu-id="56237-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56237-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56237-121">Minimum supported client</span></span><br/> | <span data-ttu-id="56237-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="56237-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="56237-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56237-123">Minimum supported server</span></span><br/> | <span data-ttu-id="56237-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="56237-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="56237-125">DLL</span><span class="sxs-lookup"><span data-stu-id="56237-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56237-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56237-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56237-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56237-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56237-128">**сдбжетбинаритагдата**</span><span class="sxs-lookup"><span data-stu-id="56237-128">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="56237-129">**сдбжетстрингтагптр**</span><span class="sxs-lookup"><span data-stu-id="56237-129">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="56237-130">**сдбреаддвордтаг**</span><span class="sxs-lookup"><span data-stu-id="56237-130">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="56237-131">**сдбреадстрингтаг**</span><span class="sxs-lookup"><span data-stu-id="56237-131">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




