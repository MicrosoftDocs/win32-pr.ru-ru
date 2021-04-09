---
description: Получает TAGID и маркер для базы данных оболочек для указанного ТАГРЕФ.
ms.assetid: 869c6af5-4c10-4358-9d6a-1a354be6f4e9
title: Функция Сдбтагрефтотагид
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagRefToTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: faff00adc25a741342e586adea2f645a62eca36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141243"
---
# <a name="sdbtagreftotagid-function"></a><span data-ttu-id="43963-103">Функция Сдбтагрефтотагид</span><span class="sxs-lookup"><span data-stu-id="43963-103">SdbTagRefToTagID function</span></span>

<span data-ttu-id="43963-104">Получает **TAGID** и маркер для базы данных оболочек для указанного [**тагреф**](tagref.md).</span><span class="sxs-lookup"><span data-stu-id="43963-104">Retrieves the **TAGID** and a handle to the shim database for the specified [**TAGREF**](tagref.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="43963-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43963-105">Syntax</span></span>


```C++
BOOL WINAPI SdbTagRefToTagID(
  _In_  HSDB   hSDB,
  _In_  TAGREF trWhich,
  _Out_ PDB    *ppdb,
  _Out_ TAGID  *ptiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="43963-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="43963-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43963-107">*хсдб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43963-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43963-108">Маркер базы данных оболочек совместимости, возвращаемый функцией [**сдбинитдатабасе**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="43963-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="43963-109">*трвхич* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43963-109">*trWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43963-110">[**Тагреф**](tagref.md).</span><span class="sxs-lookup"><span data-stu-id="43963-110">The [**TAGREF**](tagref.md).</span></span>

</dd> <dt>

<span data-ttu-id="43963-111">*ппдб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="43963-111">*ppdb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43963-112">Результирующий обработчик для базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="43963-112">The resulting handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="43963-113">*птивхич* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="43963-113">*ptiWhich* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43963-114">Результирующий **TAGID**.</span><span class="sxs-lookup"><span data-stu-id="43963-114">The resulting **TAGID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43963-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43963-115">Return value</span></span>

<span data-ttu-id="43963-116">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="43963-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="43963-117">Требования</span><span class="sxs-lookup"><span data-stu-id="43963-117">Requirements</span></span>



| <span data-ttu-id="43963-118">Требование</span><span class="sxs-lookup"><span data-stu-id="43963-118">Requirement</span></span> | <span data-ttu-id="43963-119">Значение</span><span class="sxs-lookup"><span data-stu-id="43963-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43963-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43963-120">Minimum supported client</span></span><br/> | <span data-ttu-id="43963-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="43963-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="43963-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43963-122">Minimum supported server</span></span><br/> | <span data-ttu-id="43963-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="43963-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="43963-124">DLL</span><span class="sxs-lookup"><span data-stu-id="43963-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43963-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43963-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43963-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43963-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43963-127">**сдбинитдатабасе**</span><span class="sxs-lookup"><span data-stu-id="43963-127">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> <dt>

[<span data-ttu-id="43963-128">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="43963-128">**TAGID**</span></span>](tagid.md)
</dt> <dt>

[<span data-ttu-id="43963-129">**тагреф**</span><span class="sxs-lookup"><span data-stu-id="43963-129">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




