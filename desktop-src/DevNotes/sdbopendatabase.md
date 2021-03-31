---
description: Открывает указанную базу данных оболочек.
ms.assetid: 148181d7-a20a-467c-984b-e32013960783
title: Функция Сдбопендатабасе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ae0bca035f203593c43bb36e70119fbaf3024059
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807042"
---
# <a name="sdbopendatabase-function"></a><span data-ttu-id="9976a-103">Функция Сдбопендатабасе</span><span class="sxs-lookup"><span data-stu-id="9976a-103">SdbOpenDatabase function</span></span>

<span data-ttu-id="9976a-104">Открывает указанную базу данных оболочек.</span><span class="sxs-lookup"><span data-stu-id="9976a-104">Opens the specified shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="9976a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9976a-105">Syntax</span></span>


```C++
PDB WINAPI SdbOpenDatabase(
  _In_ LPCTSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a><span data-ttu-id="9976a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9976a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9976a-107">*пвсзпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9976a-107">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9976a-108">Путь к базе данных.</span><span class="sxs-lookup"><span data-stu-id="9976a-108">The database path.</span></span> <span data-ttu-id="9976a-109">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9976a-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9976a-110">*eType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9976a-110">*eType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9976a-111">Тип пути.</span><span class="sxs-lookup"><span data-stu-id="9976a-111">The path type.</span></span> <span data-ttu-id="9976a-112">Список значений см. в разделе [**\_ тип пути**](path-type.md) .</span><span class="sxs-lookup"><span data-stu-id="9976a-112">See [**PATH\_TYPE**](path-type.md) for a list of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9976a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9976a-113">Return value</span></span>

<span data-ttu-id="9976a-114">Функция возвращает маркер в базу данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="9976a-114">The function returns a handle to the shim database.</span></span>

## <a name="requirements"></a><span data-ttu-id="9976a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9976a-115">Requirements</span></span>



| <span data-ttu-id="9976a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9976a-116">Requirement</span></span> | <span data-ttu-id="9976a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9976a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9976a-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9976a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9976a-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9976a-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9976a-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9976a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9976a-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9976a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9976a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9976a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9976a-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9976a-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9976a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9976a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9976a-125">**сдбкреатедатабасе**</span><span class="sxs-lookup"><span data-stu-id="9976a-125">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
</dt> </dl>

 

 




