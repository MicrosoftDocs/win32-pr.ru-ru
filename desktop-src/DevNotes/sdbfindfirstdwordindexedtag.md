---
description: Находит первую запись DWORD в указанном индексе, которая соответствует заданным условиям.
ms.assetid: 81302f84-497d-4fef-b348-eee2a53284c7
title: Функция Сдбфиндфирстдвординдекседтаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstDWORDIndexedTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f3c9290f98fb24d856561114bc654da0315c5a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538264"
---
# <a name="sdbfindfirstdwordindexedtag-function"></a><span data-ttu-id="5f9f8-103">Функция Сдбфиндфирстдвординдекседтаг</span><span class="sxs-lookup"><span data-stu-id="5f9f8-103">SdbFindFirstDWORDIndexedTag function</span></span>

<span data-ttu-id="5f9f8-104">Находит первую запись **DWORD** в указанном индексе, которая соответствует заданным условиям.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-104">Finds the first **DWORD** record in the specified index that meets the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f9f8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f9f8-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindFirstDWORDIndexedTag(
  _In_  PDB       pdb,
  _In_  TAG       tWhich,
  _In_  TAG       tKey,
  _In_  DWORD     dwName,
  _Out_ FIND_INFO *pFindInfo
);
```



## <a name="parameters"></a><span data-ttu-id="5f9f8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f9f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f9f8-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="5f9f8-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f9f8-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="5f9f8-109">*твхич* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5f9f8-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f9f8-110">Тип индекса.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-110">The index type.</span></span> <span data-ttu-id="5f9f8-111">Список значений см. в разделе " [**тег**](tag.md) ".</span><span class="sxs-lookup"><span data-stu-id="5f9f8-111">See [**TAG**](tag.md) for a list of values.</span></span>

</dd> <dt>

<span data-ttu-id="5f9f8-112">*tKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5f9f8-112">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f9f8-113">Тип ключа.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-113">The key type.</span></span>

</dd> <dt>

<span data-ttu-id="5f9f8-114">*двнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5f9f8-114">*dwName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f9f8-115">Имя найденных данных.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-115">The name of the data to be found.</span></span> <span data-ttu-id="5f9f8-116">Это значение будет преобразовано в ключ.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-116">This value will be converted into a key.</span></span>

</dd> <dt>

<span data-ttu-id="5f9f8-117">*пфиндинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5f9f8-117">*pFindInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f9f8-118">Структура [**поиска \_ сведений**](find-info.md) , которая получает запись.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-118">A [**FIND\_INFO**](find-info.md) structure that receives the record.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f9f8-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f9f8-119">Return value</span></span>

<span data-ttu-id="5f9f8-120">**TAGID** первого совпадения или **тега \_ null** , если совпадений не найдено.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-120">The **TAGID** of the first match or **TAG\_NULL** if no match is found.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f9f8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="5f9f8-121">Requirements</span></span>



| <span data-ttu-id="5f9f8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="5f9f8-122">Requirement</span></span> | <span data-ttu-id="5f9f8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="5f9f8-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f9f8-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5f9f8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5f9f8-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f9f8-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5f9f8-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5f9f8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5f9f8-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5f9f8-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5f9f8-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5f9f8-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f9f8-129"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f9f8-129"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f9f8-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f9f8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f9f8-131">**сдбфиндфирсттаг**</span><span class="sxs-lookup"><span data-stu-id="5f9f8-131">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> </dl>

 

 




