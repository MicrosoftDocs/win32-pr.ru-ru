---
description: Извлекает тег, связанный с указанным TAGID.
ms.assetid: 194d2035-fc2c-445d-a730-90db2ccea8af
title: Функция Сдбжеттагфромтагид
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetTagFromTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: d81dac026a9b6acc921586aaded54c8c90ad5bdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141467"
---
# <a name="sdbgettagfromtagid-function"></a><span data-ttu-id="2d633-103">Функция Сдбжеттагфромтагид</span><span class="sxs-lookup"><span data-stu-id="2d633-103">SdbGetTagFromTagID function</span></span>

<span data-ttu-id="2d633-104">Извлекает тег, связанный с указанным **TAGID**.</span><span class="sxs-lookup"><span data-stu-id="2d633-104">Retrieves the TAG associated with the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d633-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d633-105">Syntax</span></span>


```C++
TAG WINAPI SdbGetTagFromTagID(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="2d633-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d633-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d633-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="2d633-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d633-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="2d633-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="2d633-109">*тивхич* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2d633-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d633-110">**TAGID** для тега.</span><span class="sxs-lookup"><span data-stu-id="2d633-110">The **TAGID** for the TAG.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d633-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d633-111">Return value</span></span>

<span data-ttu-id="2d633-112">Функция возвращает тег.</span><span class="sxs-lookup"><span data-stu-id="2d633-112">The function returns the TAG.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d633-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2d633-113">Requirements</span></span>



| <span data-ttu-id="2d633-114">Требование</span><span class="sxs-lookup"><span data-stu-id="2d633-114">Requirement</span></span> | <span data-ttu-id="2d633-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2d633-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d633-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d633-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2d633-117">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2d633-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2d633-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d633-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2d633-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2d633-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2d633-120">DLL</span><span class="sxs-lookup"><span data-stu-id="2d633-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d633-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d633-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d633-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d633-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d633-123">**ТЕГАМИ**</span><span class="sxs-lookup"><span data-stu-id="2d633-123">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="2d633-124">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="2d633-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




