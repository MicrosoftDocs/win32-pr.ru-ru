---
description: Закрывает базу данных оболочек совместимости, инициализированную с помощью функции Сдбинитдатабасе.
ms.assetid: 8452ab14-a1e9-41b3-a1ac-7ff3a7d3a7ed
title: Функция Сдбрелеаседатабасе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7df4b62af6b2fe654269a8bea4b2e866d0d765b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538654"
---
# <a name="sdbreleasedatabase-function"></a><span data-ttu-id="9c57b-103">Функция Сдбрелеаседатабасе</span><span class="sxs-lookup"><span data-stu-id="9c57b-103">SdbReleaseDatabase function</span></span>

<span data-ttu-id="9c57b-104">Закрывает базу данных оболочек совместимости, инициализированную с помощью функции [**сдбинитдатабасе**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="9c57b-104">Closes the shim database initialized using the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c57b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c57b-105">Syntax</span></span>


```C++
void WINAPI SdbReleaseDatabase(
  _In_ HSDB hSDB
);
```



## <a name="parameters"></a><span data-ttu-id="9c57b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c57b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c57b-107">*хсдб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c57b-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c57b-108">Маркер базы данных оболочек совместимости, возвращаемый функцией [**сдбинитдатабасе**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="9c57b-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c57b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c57b-109">Return value</span></span>

<span data-ttu-id="9c57b-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9c57b-110">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c57b-111">Требования</span><span class="sxs-lookup"><span data-stu-id="9c57b-111">Requirements</span></span>



| <span data-ttu-id="9c57b-112">Требование</span><span class="sxs-lookup"><span data-stu-id="9c57b-112">Requirement</span></span> | <span data-ttu-id="9c57b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="9c57b-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c57b-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c57b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="9c57b-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c57b-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9c57b-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c57b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="9c57b-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9c57b-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9c57b-118">DLL</span><span class="sxs-lookup"><span data-stu-id="9c57b-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c57b-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c57b-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c57b-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c57b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c57b-121">**сдбинитдатабасе**</span><span class="sxs-lookup"><span data-stu-id="9c57b-121">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




