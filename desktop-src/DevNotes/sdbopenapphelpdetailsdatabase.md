---
description: Открывает указанную базу данных сведений о AppHelp.
ms.assetid: c3b07c00-a3c6-419c-94c6-34c573a04d6d
title: Функция Сдбопенапфелпдетаилсдатабасе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpDetailsDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2810b0bbe1f10f013f39570aecda448a4ceeea6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140734"
---
# <a name="sdbopenapphelpdetailsdatabase-function"></a><span data-ttu-id="22857-103">Функция Сдбопенапфелпдетаилсдатабасе</span><span class="sxs-lookup"><span data-stu-id="22857-103">SdbOpenApphelpDetailsDatabase function</span></span>

<span data-ttu-id="22857-104">Открывает указанную базу данных сведений о AppHelp.</span><span class="sxs-lookup"><span data-stu-id="22857-104">Opens the specified Apphelp details database.</span></span>

## <a name="syntax"></a><span data-ttu-id="22857-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22857-105">Syntax</span></span>


```C++
PDB WINAPI SdbOpenApphelpDetailsDatabase(
  _In_opt_ LPCWSTR pwsDetailsDatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="22857-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="22857-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22857-107">*пвсдетаилсдатабасепас* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="22857-107">*pwsDetailsDatabasePath* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="22857-108">Путь к базе данных.</span><span class="sxs-lookup"><span data-stu-id="22857-108">The database path.</span></span> <span data-ttu-id="22857-109">Если этот параметр имеет **значение NULL**, то открывается локальная системная база данных.</span><span class="sxs-lookup"><span data-stu-id="22857-109">If this parameter is **NULL**, the local system database is opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22857-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22857-110">Return value</span></span>

<span data-ttu-id="22857-111">Функция возвращает Handle в базу данных AppHelp Details.</span><span class="sxs-lookup"><span data-stu-id="22857-111">The function returns a handle to the Apphelp details database.</span></span>

## <a name="requirements"></a><span data-ttu-id="22857-112">Требования</span><span class="sxs-lookup"><span data-stu-id="22857-112">Requirements</span></span>



| <span data-ttu-id="22857-113">Требование</span><span class="sxs-lookup"><span data-stu-id="22857-113">Requirement</span></span> | <span data-ttu-id="22857-114">Значение</span><span class="sxs-lookup"><span data-stu-id="22857-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22857-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22857-115">Minimum supported client</span></span><br/> | <span data-ttu-id="22857-116">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="22857-116">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="22857-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22857-117">Minimum supported server</span></span><br/> | <span data-ttu-id="22857-118">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="22857-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="22857-119">DLL</span><span class="sxs-lookup"><span data-stu-id="22857-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22857-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22857-120"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




