---
description: Создает новый тег списка для операций записи.
ms.assetid: 3a52e2f2-9648-45fb-b487-ccfe5ed24f7f
title: Функция Сдббегинврителисттаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbBeginWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a9dcf6bdd3798b18e08b796eb268f93dc4ec6bbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807709"
---
# <a name="sdbbeginwritelisttag-function"></a><span data-ttu-id="a700b-103">Функция Сдббегинврителисттаг</span><span class="sxs-lookup"><span data-stu-id="a700b-103">SdbBeginWriteListTag function</span></span>

<span data-ttu-id="a700b-104">Создает новый тег списка для операций записи.</span><span class="sxs-lookup"><span data-stu-id="a700b-104">Creates a new list TAG for write operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="a700b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a700b-105">Syntax</span></span>


```C++
TAGID WINAPI SdbBeginWriteListTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a><span data-ttu-id="a700b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a700b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a700b-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="a700b-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a700b-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="a700b-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="a700b-109">*ттаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a700b-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a700b-110">ТЕГ для новой записи.</span><span class="sxs-lookup"><span data-stu-id="a700b-110">The TAG for the new entry.</span></span> <span data-ttu-id="a700b-111">Это значение должно иметь тип " **\_ \_ список типов тегов**".</span><span class="sxs-lookup"><span data-stu-id="a700b-111">This value must be of type **TAG\_TYPE\_LIST**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a700b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a700b-112">Return value</span></span>

<span data-ttu-id="a700b-113">Функция возвращает [**TAGID**](tagid.md) нового списка при успешном выполнении или **TAGID \_ null** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="a700b-113">The function returns the [**TAGID**](tagid.md) of the new list on success or **TAGID\_NULL** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a700b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a700b-114">Requirements</span></span>



| <span data-ttu-id="a700b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a700b-115">Requirement</span></span> | <span data-ttu-id="a700b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a700b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a700b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a700b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a700b-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a700b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a700b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a700b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a700b-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a700b-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a700b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a700b-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a700b-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a700b-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a700b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a700b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a700b-124">**сдбклоседатабасе**</span><span class="sxs-lookup"><span data-stu-id="a700b-124">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="a700b-125">**сдбклоседатабасеврите**</span><span class="sxs-lookup"><span data-stu-id="a700b-125">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
</dt> <dt>

[<span data-ttu-id="a700b-126">**сдбендврителисттаг**</span><span class="sxs-lookup"><span data-stu-id="a700b-126">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="a700b-127">**ТЕГАМИ**</span><span class="sxs-lookup"><span data-stu-id="a700b-127">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="a700b-128">Типы тегов</span><span class="sxs-lookup"><span data-stu-id="a700b-128">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="a700b-129">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="a700b-129">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




