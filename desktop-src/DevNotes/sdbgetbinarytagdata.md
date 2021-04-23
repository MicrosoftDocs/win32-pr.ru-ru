---
description: Извлекает двоичные данные для указанного TAGID.
ms.assetid: 18992406-67b4-4c48-9629-04d6bf1c5824
title: Функция Сдбжетбинаритагдата
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetBinaryTagData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 028b073b149482b79b848216e44b8a425d6ffb56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662079"
---
# <a name="sdbgetbinarytagdata-function"></a><span data-ttu-id="f63f7-103">Функция Сдбжетбинаритагдата</span><span class="sxs-lookup"><span data-stu-id="f63f7-103">SdbGetBinaryTagData function</span></span>

<span data-ttu-id="f63f7-104">Извлекает двоичные данные для указанного **TAGID**.</span><span class="sxs-lookup"><span data-stu-id="f63f7-104">Retrieves the binary data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f63f7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f63f7-105">Syntax</span></span>


```C++
PVOID WINAPI SdbGetBinaryTagData(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="f63f7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f63f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f63f7-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="f63f7-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f63f7-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="f63f7-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="f63f7-109">*тивхич* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f63f7-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f63f7-110">**TAGID** , соответствующий получаемым данным.</span><span class="sxs-lookup"><span data-stu-id="f63f7-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f63f7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f63f7-111">Return value</span></span>

<span data-ttu-id="f63f7-112">Функция возвращает указатель на двоичные данные или **значение NULL** , если **TAGID** является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="f63f7-112">The function returns a pointer to the binary data or **NULL** if the **TAGID** is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="f63f7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f63f7-113">Requirements</span></span>



| <span data-ttu-id="f63f7-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f63f7-114">Requirement</span></span> | <span data-ttu-id="f63f7-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f63f7-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f63f7-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f63f7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f63f7-117">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f63f7-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f63f7-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f63f7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f63f7-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f63f7-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f63f7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f63f7-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f63f7-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f63f7-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f63f7-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f63f7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f63f7-123">**сдбжетстрингтагптр**</span><span class="sxs-lookup"><span data-stu-id="f63f7-123">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="f63f7-124">**сдбреаддвордтаг**</span><span class="sxs-lookup"><span data-stu-id="f63f7-124">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="f63f7-125">**сдбреадквордтаг**</span><span class="sxs-lookup"><span data-stu-id="f63f7-125">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="f63f7-126">**сдбреадстрингтаг**</span><span class="sxs-lookup"><span data-stu-id="f63f7-126">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




