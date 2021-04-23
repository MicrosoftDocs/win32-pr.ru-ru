---
title: Структура Вмдмметадатавиев
description: Структура Вмдмметадатавиев определяет представление метаданных. Содержимое организовано на основе этого определения.
ms.assetid: 787d2295-d433-451d-a1fc-6f73585e10d6
keywords:
- Структура Вмдмметадатавиев Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDMMetadataView
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aa38a8fe7f19137c5caff18417d48ea23168b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694463"
---
# <a name="wmdmmetadataview-structure"></a><span data-ttu-id="30e57-105">Структура Вмдмметадатавиев</span><span class="sxs-lookup"><span data-stu-id="30e57-105">WMDMMetadataView structure</span></span>

<span data-ttu-id="30e57-106">Структура **вмдмметадатавиев** определяет представление метаданных.</span><span class="sxs-lookup"><span data-stu-id="30e57-106">The **WMDMMetadataView** structure defines the metadata view.</span></span> <span data-ttu-id="30e57-107">Содержимое организовано на основе этого определения.</span><span class="sxs-lookup"><span data-stu-id="30e57-107">Content is organized based on this definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="30e57-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30e57-108">Syntax</span></span>


```C++
typedef struct _WMDMMetadataView {
  WCHAR *pwszViewName;
  UINT  nDepth;
  WCHAR **ppwszTags;
} WMDMMetadataView;
```



## <a name="members"></a><span data-ttu-id="30e57-109">Члены</span><span class="sxs-lookup"><span data-stu-id="30e57-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="30e57-110">**пвсзвиевнаме**</span><span class="sxs-lookup"><span data-stu-id="30e57-110">**pwszViewName**</span></span>
</dt> <dd>

<span data-ttu-id="30e57-111">Указатель на строку расширенных символов, заканчивающуюся нулем, которая содержит имя представления.</span><span class="sxs-lookup"><span data-stu-id="30e57-111">Pointer to a wide-character null-terminated string containing the name of the view.</span></span> <span data-ttu-id="30e57-112">Используется в качестве имени корневого узла, в котором представлено это представление.</span><span class="sxs-lookup"><span data-stu-id="30e57-112">This is used as the name of the root node under which this view is presented.</span></span>

</dd> <dt>

<span data-ttu-id="30e57-113">**ндепс**</span><span class="sxs-lookup"><span data-stu-id="30e57-113">**nDepth**</span></span>
</dt> <dd>

<span data-ttu-id="30e57-114">Целое число, содержащее глубину представления, которое указывает, сколько тегов вложенных метаданных используется для представления.</span><span class="sxs-lookup"><span data-stu-id="30e57-114">Integer containing the depth of the view, which indicates how many nested metadata tags are used for the view.</span></span>

</dd> <dt>

<span data-ttu-id="30e57-115">**ппвсзтагс**</span><span class="sxs-lookup"><span data-stu-id="30e57-115">**ppwszTags**</span></span>
</dt> <dd>

<span data-ttu-id="30e57-116">Массив строк тегов метаданных для вложенных тегов.</span><span class="sxs-lookup"><span data-stu-id="30e57-116">Array of metadata tag strings for the nested tags.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="30e57-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="30e57-117">Examples</span></span>

<span data-ttu-id="30e57-118">Следующий код создает представление метаданных:</span><span class="sxs-lookup"><span data-stu-id="30e57-118">The following code creates a metadata view:</span></span>


```C++
WMDMMetadataView view;
view.pwszName = L"My View";
view.nDepth = 3;  // genre, artist, album
LPCWSTR wszTagArray[3]; 
wszTagArray[0] = g_wszWMDMGenre;
wszTagArray[1] = g_wszWMDMAuthor;
wszTagArray[2] = g_wszWMDMAlbumTitle;
view.ppwszTags = wszTagArray;
```



<span data-ttu-id="30e57-119">Приведенный выше код организует содержимое следующим образом:</span><span class="sxs-lookup"><span data-stu-id="30e57-119">The preceding code organizes content as follows:</span></span>

<dl> <span data-ttu-id="30e57-120">Мое представление</span><span class="sxs-lookup"><span data-stu-id="30e57-120">My View</span></span><dl> <span data-ttu-id="30e57-121">Genre1</span><span class="sxs-lookup"><span data-stu-id="30e57-121">Genre1</span></span><dl> <span data-ttu-id="30e57-122">Artist1</span><span class="sxs-lookup"><span data-stu-id="30e57-122">Artist1</span></span><dl> <span data-ttu-id="30e57-123">Album1</span><span class="sxs-lookup"><span data-stu-id="30e57-123">Album1</span></span><dl> <span data-ttu-id="30e57-124">Song1</span><span class="sxs-lookup"><span data-stu-id="30e57-124">Song1</span></span>  
<span data-ttu-id="30e57-125">Song2</span><span class="sxs-lookup"><span data-stu-id="30e57-125">Song2</span></span>  
<span data-ttu-id="30e57-126">...</span><span class="sxs-lookup"><span data-stu-id="30e57-126">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> <span data-ttu-id="30e57-127">Album1</span><span class="sxs-lookup"><span data-stu-id="30e57-127">Album1</span></span><dl> <span data-ttu-id="30e57-128">Song1</span><span class="sxs-lookup"><span data-stu-id="30e57-128">Song1</span></span>  
<span data-ttu-id="30e57-129">Song2</span><span class="sxs-lookup"><span data-stu-id="30e57-129">Song2</span></span>  
<span data-ttu-id="30e57-130">...</span><span class="sxs-lookup"><span data-stu-id="30e57-130">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> </dl> </dd> Genre2<dl> <span data-ttu-id="30e57-131">Artist1</span><span class="sxs-lookup"><span data-stu-id="30e57-131">Artist1</span></span><dl> <span data-ttu-id="30e57-132">Album1</span><span class="sxs-lookup"><span data-stu-id="30e57-132">Album1</span></span><dl> <span data-ttu-id="30e57-133">Song1</span><span class="sxs-lookup"><span data-stu-id="30e57-133">Song1</span></span>  
<span data-ttu-id="30e57-134">Song2</span><span class="sxs-lookup"><span data-stu-id="30e57-134">Song2</span></span>  
<span data-ttu-id="30e57-135">...</span><span class="sxs-lookup"><span data-stu-id="30e57-135">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> <span data-ttu-id="30e57-136">Album1</span><span class="sxs-lookup"><span data-stu-id="30e57-136">Album1</span></span><dl> <span data-ttu-id="30e57-137">Song1</span><span class="sxs-lookup"><span data-stu-id="30e57-137">Song1</span></span>  
<span data-ttu-id="30e57-138">Song2</span><span class="sxs-lookup"><span data-stu-id="30e57-138">Song2</span></span>  
<span data-ttu-id="30e57-139">...</span><span class="sxs-lookup"><span data-stu-id="30e57-139">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> ...  
</dl> </dd> ...  
</dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30e57-140">Требования</span><span class="sxs-lookup"><span data-stu-id="30e57-140">Requirements</span></span>



| <span data-ttu-id="30e57-141">Требование</span><span class="sxs-lookup"><span data-stu-id="30e57-141">Requirement</span></span> | <span data-ttu-id="30e57-142">Значение</span><span class="sxs-lookup"><span data-stu-id="30e57-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="30e57-143">Header</span><span class="sxs-lookup"><span data-stu-id="30e57-143">Header</span></span><br/> | <dl> <span data-ttu-id="30e57-144"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="30e57-144"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30e57-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30e57-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30e57-146">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="30e57-146">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





