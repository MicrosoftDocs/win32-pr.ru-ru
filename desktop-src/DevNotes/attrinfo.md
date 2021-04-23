---
description: Содержит данные атрибутов для файла.
ms.assetid: f23f801c-826c-4269-bf96-0e01430484f4
title: Структура АТТРИНФО
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 01c061330db3e97989e0700452fd4a205488a9fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895365"
---
# <a name="attrinfo-structure"></a><span data-ttu-id="2524a-103">Структура АТТРИНФО</span><span class="sxs-lookup"><span data-stu-id="2524a-103">ATTRINFO structure</span></span>

<span data-ttu-id="2524a-104">Содержит данные атрибутов для файла.</span><span class="sxs-lookup"><span data-stu-id="2524a-104">Contains the attribute data for a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2524a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2524a-105">Syntax</span></span>


```C++
typedef struct tagATTRINFO {
  TAG   tAttrID;
  DWORD dwFlags;
  union {
    ULONGLONG ullAttr;
    DWORD     dwAttr;
    TCHAR     *lpAttr;
  };
} ATTRINFO, *PATTRINFO;
```



## <a name="members"></a><span data-ttu-id="2524a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="2524a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2524a-107">**таттрид**</span><span class="sxs-lookup"><span data-stu-id="2524a-107">**tAttrID**</span></span>
</dt> <dd>

<span data-ttu-id="2524a-108">Тип атрибута.</span><span class="sxs-lookup"><span data-stu-id="2524a-108">The attribute type.</span></span> <span data-ttu-id="2524a-109">См. раздел [типы тегов](tag-types.md).</span><span class="sxs-lookup"><span data-stu-id="2524a-109">See [TAG Types](tag-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="2524a-110">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="2524a-110">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="2524a-111">Флаги для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="2524a-111">The flags for this attribute.</span></span>



| <span data-ttu-id="2524a-112">Значение</span><span class="sxs-lookup"><span data-stu-id="2524a-112">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="2524a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="2524a-113">Meaning</span></span>                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="ATTRIBUTE_AVAILABLE"></span><span id="attribute_available"></span><dl> <span data-ttu-id="2524a-114"><dt>**Атрибут \_ ДОСТУПное**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="2524a-114"><dt>**ATTRIBUTE\_AVAILABLE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="2524a-115">Атрибут доступен.</span><span class="sxs-lookup"><span data-stu-id="2524a-115">The attribute is available.</span></span><br/>                             |
| <span id="ATTRIBUTE_FAILED"></span><span id="attribute_failed"></span><dl> <span data-ttu-id="2524a-116"><dt>**Атрибут \_ Сбой**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="2524a-116"><dt>**ATTRIBUTE\_FAILED**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="2524a-117">Вызов завершился неудачей, так как атрибут недоступен.</span><span class="sxs-lookup"><span data-stu-id="2524a-117">The call failed because the attribute is not available.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2524a-118">**уллаттр**</span><span class="sxs-lookup"><span data-stu-id="2524a-118">**ullAttr**</span></span>
</dt> <dd>

<span data-ttu-id="2524a-119">Значение **QWORD** (если тип тега — **\_ тип \_ QWORD**).</span><span class="sxs-lookup"><span data-stu-id="2524a-119">A **QWORD** value (if the tag type is **TAG\_TYPE\_QWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="2524a-120">**дваттр**</span><span class="sxs-lookup"><span data-stu-id="2524a-120">**dwAttr**</span></span>
</dt> <dd>

<span data-ttu-id="2524a-121">Значение типа **DWORD** (если тип тега — **\_ тип \_ DWORD**).</span><span class="sxs-lookup"><span data-stu-id="2524a-121">A **DWORD** value (if the tag type is **TAG\_TYPE\_DWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="2524a-122">**лпаттр**</span><span class="sxs-lookup"><span data-stu-id="2524a-122">**lpAttr**</span></span>
</dt> <dd>

<span data-ttu-id="2524a-123">Указатель на строку (если тип тега — **тег \_ типа \_ стрингреф**).</span><span class="sxs-lookup"><span data-stu-id="2524a-123">A pointer to a string (if the tag type is **TAG\_TYPE\_STRINGREF**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2524a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="2524a-124">Requirements</span></span>



| <span data-ttu-id="2524a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="2524a-125">Requirement</span></span> | <span data-ttu-id="2524a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2524a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2524a-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2524a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2524a-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2524a-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2524a-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2524a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2524a-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2524a-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2524a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2524a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2524a-132">**сдбформататтрибуте**</span><span class="sxs-lookup"><span data-stu-id="2524a-132">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
</dt> <dt>

[<span data-ttu-id="2524a-133">**сдбфрифилеаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="2524a-133">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
</dt> <dt>

[<span data-ttu-id="2524a-134">**сдбжетфилеаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="2524a-134">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 




