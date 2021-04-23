---
description: Закрывает указанную базу данных оболочек совместимости.
ms.assetid: e4480860-8055-4134-b6ed-926c010d462f
title: Функция Сдбклоседатабасе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 376d97b8386f127a945cb118639be1e38ae68737
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072437"
---
# <a name="sdbclosedatabase-function"></a><span data-ttu-id="d7eb1-103">Функция Сдбклоседатабасе</span><span class="sxs-lookup"><span data-stu-id="d7eb1-103">SdbCloseDatabase function</span></span>

<span data-ttu-id="d7eb1-104">Закрывает указанную базу данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="d7eb1-104">Closes the specified shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7eb1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7eb1-105">Syntax</span></span>


```C++
void WINAPI SdbCloseDatabase(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="d7eb1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7eb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7eb1-107">*pdb* \[ -файл в, out\]</span><span class="sxs-lookup"><span data-stu-id="d7eb1-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7eb1-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="d7eb1-108">A handle to the shim database.</span></span> <span data-ttu-id="d7eb1-109">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d7eb1-109">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7eb1-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7eb1-110">Return value</span></span>

<span data-ttu-id="d7eb1-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d7eb1-111">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7eb1-112">Требования</span><span class="sxs-lookup"><span data-stu-id="d7eb1-112">Requirements</span></span>



| <span data-ttu-id="d7eb1-113">Требование</span><span class="sxs-lookup"><span data-stu-id="d7eb1-113">Requirement</span></span> | <span data-ttu-id="d7eb1-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d7eb1-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7eb1-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7eb1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d7eb1-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7eb1-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d7eb1-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7eb1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d7eb1-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d7eb1-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d7eb1-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d7eb1-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7eb1-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7eb1-120"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7eb1-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7eb1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7eb1-122">**сдбопендатабасе**</span><span class="sxs-lookup"><span data-stu-id="d7eb1-122">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




