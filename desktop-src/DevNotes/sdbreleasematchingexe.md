---
description: Высвобождает ресурсы, используемые функцией Сдбжетматчинжексе.
ms.assetid: 4a784f72-2108-4d5e-86e1-1960ac921c8f
title: Функция Сдбрелеасематчинжексе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c98d9a79e8942f4bd3ea4c41119825d862de1418
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072403"
---
# <a name="sdbreleasematchingexe-function"></a><span data-ttu-id="c4e70-103">Функция Сдбрелеасематчинжексе</span><span class="sxs-lookup"><span data-stu-id="c4e70-103">SdbReleaseMatchingExe function</span></span>

<span data-ttu-id="c4e70-104">Высвобождает ресурсы, используемые функцией [**сдбжетматчинжексе**](sdbgetmatchingexe.md) .</span><span class="sxs-lookup"><span data-stu-id="c4e70-104">Releases resources used by the [**SdbGetMatchingExe**](sdbgetmatchingexe.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4e70-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4e70-105">Syntax</span></span>


```C++
void WINAPI SdbReleaseMatchingExe(
  _In_ HSDB   hSDB,
  _In_ TAGREF trExe
);
```



## <a name="parameters"></a><span data-ttu-id="c4e70-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4e70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4e70-107">*хсдб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4e70-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4e70-108">Маркер базы данных оболочек совместимости, возвращаемый функцией [**сдбинитдатабасе**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="c4e70-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="c4e70-109">*трексе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4e70-109">*trExe* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4e70-110">[**Тагреф**](tagref.md) , возвращенный [**сдбжетматчинжексе**](sdbgetmatchingexe.md).</span><span class="sxs-lookup"><span data-stu-id="c4e70-110">The [**TAGREF**](tagref.md) returned by [**SdbGetMatchingExe**](sdbgetmatchingexe.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4e70-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4e70-111">Return value</span></span>

<span data-ttu-id="c4e70-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c4e70-112">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4e70-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c4e70-113">Requirements</span></span>



| <span data-ttu-id="c4e70-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c4e70-114">Requirement</span></span> | <span data-ttu-id="c4e70-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c4e70-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4e70-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4e70-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c4e70-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4e70-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c4e70-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4e70-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c4e70-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c4e70-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c4e70-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c4e70-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4e70-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4e70-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4e70-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4e70-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4e70-123">**сдбжетматчинжексе**</span><span class="sxs-lookup"><span data-stu-id="c4e70-123">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> <dt>

[<span data-ttu-id="c4e70-124">**сдбинитдатабасе**</span><span class="sxs-lookup"><span data-stu-id="c4e70-124">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




