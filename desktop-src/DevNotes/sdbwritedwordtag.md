---
description: Записывает значение DWORD в указанную базу данных.
ms.assetid: 2ecbfcac-5bb1-4129-9501-79210672aa1b
title: Функция Сдбвритедвордтаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5b549a91037aa308b5b88d0e3e2a51e153002bd5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262575"
---
# <a name="sdbwritedwordtag-function"></a><span data-ttu-id="2958c-103">Функция Сдбвритедвордтаг</span><span class="sxs-lookup"><span data-stu-id="2958c-103">SdbWriteDWORDTag function</span></span>

<span data-ttu-id="2958c-104">Записывает значение **DWORD** в указанную базу данных.</span><span class="sxs-lookup"><span data-stu-id="2958c-104">Writes a **DWORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="2958c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2958c-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteDWORDTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ DWORD dwData
);
```



## <a name="parameters"></a><span data-ttu-id="2958c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2958c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2958c-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="2958c-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2958c-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="2958c-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="2958c-109">*ттаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2958c-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2958c-110">ТЕГ для записи.</span><span class="sxs-lookup"><span data-stu-id="2958c-110">The TAG for the entry.</span></span> <span data-ttu-id="2958c-111">Этот тег должен иметь тип **тега \_ \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2958c-111">This TAG must be of type **TAG\_TYPE\_DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="2958c-112">*двдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2958c-112">*dwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2958c-113">Значение.</span><span class="sxs-lookup"><span data-stu-id="2958c-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2958c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2958c-114">Return value</span></span>

<span data-ttu-id="2958c-115">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="2958c-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="2958c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="2958c-116">Requirements</span></span>



| <span data-ttu-id="2958c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="2958c-117">Requirement</span></span> | <span data-ttu-id="2958c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2958c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2958c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2958c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2958c-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2958c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2958c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2958c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2958c-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2958c-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2958c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="2958c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2958c-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2958c-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2958c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2958c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2958c-126">**сдбвритебинаритаг**</span><span class="sxs-lookup"><span data-stu-id="2958c-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="2958c-127">**сдбвритеквордтаг**</span><span class="sxs-lookup"><span data-stu-id="2958c-127">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="2958c-128">**сдбвритестрингтаг**</span><span class="sxs-lookup"><span data-stu-id="2958c-128">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="2958c-129">**сдбвритевордтаг**</span><span class="sxs-lookup"><span data-stu-id="2958c-129">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




