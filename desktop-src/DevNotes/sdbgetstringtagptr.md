---
description: Извлекает строковые данные для указанного TAGID.
ms.assetid: c558e0bb-7e35-4298-93fb-400db00a2972
title: Функция Сдбжетстрингтагптр
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetStringTagPtr
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 56c80c4000df95fe13486d95bb872bfc39274389
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990550"
---
# <a name="sdbgetstringtagptr-function"></a><span data-ttu-id="07b2a-103">Функция Сдбжетстрингтагптр</span><span class="sxs-lookup"><span data-stu-id="07b2a-103">SdbGetStringTagPtr function</span></span>

<span data-ttu-id="07b2a-104">Извлекает строковые данные для указанного **TAGID**.</span><span class="sxs-lookup"><span data-stu-id="07b2a-104">Retrieves the string data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="07b2a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07b2a-105">Syntax</span></span>


```C++
LPTSTR WINAPI SdbGetStringTagPtr(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="07b2a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="07b2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07b2a-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="07b2a-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07b2a-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="07b2a-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="07b2a-109">*тивхич* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07b2a-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07b2a-110">**TAGID** , соответствующий строкам данных для извлечения.</span><span class="sxs-lookup"><span data-stu-id="07b2a-110">The **TAGID** that corresponds to the string data to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07b2a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07b2a-111">Return value</span></span>

<span data-ttu-id="07b2a-112">Функция возвращает указатель на строковые данные или **значение NULL** , если **TAGID** является недопустимым или не относится к типу **тегов \_ \_ String** или **\_ type тега \_ стрингреф**.</span><span class="sxs-lookup"><span data-stu-id="07b2a-112">The function returns a pointer to the string data or **NULL** if the **TAGID** is invalid or not of type **TAG\_TYPE\_STRING** or **TAG\_TYPE\_STRINGREF**.</span></span>

## <a name="requirements"></a><span data-ttu-id="07b2a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="07b2a-113">Requirements</span></span>



| <span data-ttu-id="07b2a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="07b2a-114">Requirement</span></span> | <span data-ttu-id="07b2a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="07b2a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07b2a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07b2a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="07b2a-117">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="07b2a-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="07b2a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07b2a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="07b2a-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="07b2a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="07b2a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="07b2a-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07b2a-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07b2a-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07b2a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07b2a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07b2a-123">**сдбжетбинаритагдата**</span><span class="sxs-lookup"><span data-stu-id="07b2a-123">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="07b2a-124">**сдбреаддвордтаг**</span><span class="sxs-lookup"><span data-stu-id="07b2a-124">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="07b2a-125">**сдбреадквордтаг**</span><span class="sxs-lookup"><span data-stu-id="07b2a-125">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="07b2a-126">**сдбреадстрингтаг**</span><span class="sxs-lookup"><span data-stu-id="07b2a-126">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




