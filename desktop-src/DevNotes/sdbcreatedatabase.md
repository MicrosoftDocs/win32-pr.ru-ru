---
description: Создает новую базу данных оболочек совместимости.
ms.assetid: 91fb180d-1a21-4011-821d-ea0fc999dc76
title: Функция Сдбкреатедатабасе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCreateDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 1ab8b8071cc210f6129545985d2d2e089680f0f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990551"
---
# <a name="sdbcreatedatabase-function"></a><span data-ttu-id="38cdb-103">Функция Сдбкреатедатабасе</span><span class="sxs-lookup"><span data-stu-id="38cdb-103">SdbCreateDatabase function</span></span>

<span data-ttu-id="38cdb-104">Создает новую базу данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="38cdb-104">Creates a new shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="38cdb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38cdb-105">Syntax</span></span>


```C++
PDB WINAPI SdbCreateDatabase(
  _In_ LPCWSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a><span data-ttu-id="38cdb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="38cdb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38cdb-107">*пвсзпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38cdb-107">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38cdb-108">Путь, по которому должна быть сохранена база данных.</span><span class="sxs-lookup"><span data-stu-id="38cdb-108">The path where the database should be saved.</span></span> <span data-ttu-id="38cdb-109">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="38cdb-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38cdb-110">*eType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38cdb-110">*eType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38cdb-111">Тип пути.</span><span class="sxs-lookup"><span data-stu-id="38cdb-111">The path type.</span></span> <span data-ttu-id="38cdb-112">Список значений см. в разделе [**\_ тип пути**](path-type.md) .</span><span class="sxs-lookup"><span data-stu-id="38cdb-112">See [**PATH\_TYPE**](path-type.md) for a list of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38cdb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38cdb-113">Return value</span></span>

<span data-ttu-id="38cdb-114">Функция возвращает маркер в базу данных оболочек совместимости или **значение NULL** при сбое.</span><span class="sxs-lookup"><span data-stu-id="38cdb-114">The function returns a handle to the shim database or **NULL** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="38cdb-115">Требования</span><span class="sxs-lookup"><span data-stu-id="38cdb-115">Requirements</span></span>



| <span data-ttu-id="38cdb-116">Требование</span><span class="sxs-lookup"><span data-stu-id="38cdb-116">Requirement</span></span> | <span data-ttu-id="38cdb-117">Значение</span><span class="sxs-lookup"><span data-stu-id="38cdb-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="38cdb-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38cdb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="38cdb-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38cdb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="38cdb-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38cdb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="38cdb-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="38cdb-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="38cdb-122">DLL</span><span class="sxs-lookup"><span data-stu-id="38cdb-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38cdb-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38cdb-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38cdb-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38cdb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38cdb-125">**сдбопендатабасе**</span><span class="sxs-lookup"><span data-stu-id="38cdb-125">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




