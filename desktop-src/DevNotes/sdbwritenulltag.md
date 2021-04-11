---
description: Записывает ПУСТую запись в указанную базу данных.
ms.assetid: 2a29389b-d4f6-4527-a429-c9459b095f2f
title: Функция Сдбвритенуллтаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteNULLTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 662d5c4db31f199df8b3b9f7368aba118ea6e8fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262574"
---
# <a name="sdbwritenulltag-function"></a><span data-ttu-id="e4f83-103">Функция Сдбвритенуллтаг</span><span class="sxs-lookup"><span data-stu-id="e4f83-103">SdbWriteNULLTag function</span></span>

<span data-ttu-id="e4f83-104">Записывает **пустую** запись в указанную базу данных.</span><span class="sxs-lookup"><span data-stu-id="e4f83-104">Writes a **NULL** entry to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4f83-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4f83-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteNULLTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a><span data-ttu-id="e4f83-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4f83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4f83-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="e4f83-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4f83-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="e4f83-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="e4f83-109">*ттаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e4f83-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4f83-110">ТЕГ для записи.</span><span class="sxs-lookup"><span data-stu-id="e4f83-110">The TAG for the entry.</span></span> <span data-ttu-id="e4f83-111">Этот тег должен иметь тип **тега \_ \_ null**.</span><span class="sxs-lookup"><span data-stu-id="e4f83-111">This TAG must be of type **TAG\_TYPE\_NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4f83-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4f83-112">Return value</span></span>

<span data-ttu-id="e4f83-113">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="e4f83-113">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4f83-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e4f83-114">Requirements</span></span>



| <span data-ttu-id="e4f83-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e4f83-115">Requirement</span></span> | <span data-ttu-id="e4f83-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e4f83-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f83-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4f83-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e4f83-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4f83-118">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e4f83-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4f83-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e4f83-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e4f83-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e4f83-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e4f83-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4f83-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4f83-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4f83-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4f83-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4f83-124">**сдбвритебинаритаг**</span><span class="sxs-lookup"><span data-stu-id="e4f83-124">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="e4f83-125">**сдбвритедвордтаг**</span><span class="sxs-lookup"><span data-stu-id="e4f83-125">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="e4f83-126">**сдбвритестрингтаг**</span><span class="sxs-lookup"><span data-stu-id="e4f83-126">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="e4f83-127">**сдбвритевордтаг**</span><span class="sxs-lookup"><span data-stu-id="e4f83-127">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




