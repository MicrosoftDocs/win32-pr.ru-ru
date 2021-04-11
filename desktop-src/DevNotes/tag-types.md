---
description: Описывает тип данных значения, связанного с ТЕГОМ.
ms.assetid: 009ad522-35da-4053-a7f6-61d7d240b98c
title: Типы тегов
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab53b9c3b85263ddcdbe80e3979d576685bd73
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262546"
---
# <a name="tag-types"></a><span data-ttu-id="64575-103">Типы тегов</span><span class="sxs-lookup"><span data-stu-id="64575-103">TAG Types</span></span>

<span data-ttu-id="64575-104">Описывает тип данных значения, связанного с ТЕГОМ.</span><span class="sxs-lookup"><span data-stu-id="64575-104">Describes the data type of the value associated with a TAG.</span></span>



| <span data-ttu-id="64575-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="64575-105">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="64575-106">Описание</span><span class="sxs-lookup"><span data-stu-id="64575-106">Description</span></span>                                           |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| <span id="TAG_TYPE_NULL"></span><span id="tag_type_null"></span><dl> <span data-ttu-id="64575-107"><dt>**Тег \_ Введите \_**</dt> <dt>0x1000</dt> null</span><span class="sxs-lookup"><span data-stu-id="64575-107"><dt>**TAG\_TYPE\_NULL**</dt> <dt>0x1000</dt></span></span> </dl>                | <span data-ttu-id="64575-108">Отсутствует значение, связанное с ТЕГОМ.</span><span class="sxs-lookup"><span data-stu-id="64575-108">There is no value associated with the TAG.</span></span><br/> |
| <span id="TAG_TYPE_BYTE"></span><span id="tag_type_byte"></span><dl> <span data-ttu-id="64575-109"><dt>**Тег \_ Тип \_ Byte**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="64575-109"><dt>**TAG\_TYPE\_BYTE**</dt> <dt>0x2000</dt></span></span> </dl>                | <span data-ttu-id="64575-110">Значение **типа Byte** .</span><span class="sxs-lookup"><span data-stu-id="64575-110">A **BYTE** value.</span></span><br/>                          |
| <span id="TAG_TYPE_WORD"></span><span id="tag_type_word"></span><dl> <span data-ttu-id="64575-111"><dt>**Тег \_ Введите \_ слово**</dt> <dt>0x3000</dt></span><span class="sxs-lookup"><span data-stu-id="64575-111"><dt>**TAG\_TYPE\_WORD**</dt> <dt>0x3000</dt></span></span> </dl>                | <span data-ttu-id="64575-112">Значение **слова** .</span><span class="sxs-lookup"><span data-stu-id="64575-112">A **WORD** value.</span></span><br/>                          |
| <span id="TAG_TYPE_DWORD"></span><span id="tag_type_dword"></span><dl> <span data-ttu-id="64575-113"><dt>**Тег \_ Введите \_ DWORD**</dt> <dt>0x4000</dt></span><span class="sxs-lookup"><span data-stu-id="64575-113"><dt>**TAG\_TYPE\_DWORD**</dt> <dt>0x4000</dt></span></span> </dl>             | <span data-ttu-id="64575-114">Значение **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="64575-114">A **DWORD** value.</span></span><br/>                         |
| <span id="TAG_TYPE_QWORD"></span><span id="tag_type_qword"></span><dl> <span data-ttu-id="64575-115"><dt>**Тег \_ Введите \_ QWORD**</dt> <dt>0x5000</dt></span><span class="sxs-lookup"><span data-stu-id="64575-115"><dt>**TAG\_TYPE\_QWORD**</dt> <dt>0x5000</dt></span></span> </dl>             | <span data-ttu-id="64575-116">Значение **улонглонг** .</span><span class="sxs-lookup"><span data-stu-id="64575-116">A **ULONGLONG** value.</span></span><br/>                     |
| <span id="TAG_TYPE_STRINGREF"></span><span id="tag_type_stringref"></span><dl> <span data-ttu-id="64575-117"><dt>**Тег \_ Введите \_ стрингреф**</dt> <dt>0x6000</dt></span><span class="sxs-lookup"><span data-stu-id="64575-117"><dt>**TAG\_TYPE\_STRINGREF**</dt> <dt>0x6000</dt></span></span> </dl> | <span data-ttu-id="64575-118">Строковое значение с маркерами.</span><span class="sxs-lookup"><span data-stu-id="64575-118">A tokenized string value.</span></span><br/>                  |
| <span id="TAG_TYPE_LIST"></span><span id="tag_type_list"></span><dl> <span data-ttu-id="64575-119"><dt>**Тег \_ Тип \_ List**</dt> <dt>0x7000</dt></span><span class="sxs-lookup"><span data-stu-id="64575-119"><dt>**TAG\_TYPE\_LIST**</dt> <dt>0x7000</dt></span></span> </dl>                | <span data-ttu-id="64575-120">Список значений тегов.</span><span class="sxs-lookup"><span data-stu-id="64575-120">A list of TAG values.</span></span><br/>                      |
| <span id="TAG_TYPE_STRING"></span><span id="tag_type_string"></span><dl> <span data-ttu-id="64575-121"><dt>**Тег \_ \_Строка типа**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="64575-121"><dt>**TAG\_TYPE\_STRING**</dt> <dt>0x8000</dt></span></span> </dl>          | <span data-ttu-id="64575-122">Строковое значение.</span><span class="sxs-lookup"><span data-stu-id="64575-122">A string value.</span></span><br/>                            |
| <span id="TAG_TYPE_BINARY"></span><span id="tag_type_binary"></span><dl> <span data-ttu-id="64575-123"><dt>**Тег \_ Тип \_ binary**</dt> <dt>0x9000</dt></span><span class="sxs-lookup"><span data-stu-id="64575-123"><dt>**TAG\_TYPE\_BINARY**</dt> <dt>0x9000</dt></span></span> </dl>          | <span data-ttu-id="64575-124">Двоичное значение.</span><span class="sxs-lookup"><span data-stu-id="64575-124">A binary value.</span></span><br/>                            |



## <a name="requirements"></a><span data-ttu-id="64575-125">Требования</span><span class="sxs-lookup"><span data-stu-id="64575-125">Requirements</span></span>



| <span data-ttu-id="64575-126">Требование</span><span class="sxs-lookup"><span data-stu-id="64575-126">Requirement</span></span> | <span data-ttu-id="64575-127">Значение</span><span class="sxs-lookup"><span data-stu-id="64575-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="64575-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64575-128">Minimum supported client</span></span><br/> | <span data-ttu-id="64575-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="64575-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="64575-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="64575-130">Minimum supported server</span></span><br/> | <span data-ttu-id="64575-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="64575-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="64575-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64575-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64575-133">**ТЕГАМИ**</span><span class="sxs-lookup"><span data-stu-id="64575-133">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="64575-134">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="64575-134">**TAGID**</span></span>](tagid.md)
</dt> <dt>

[<span data-ttu-id="64575-135">**тагреф**</span><span class="sxs-lookup"><span data-stu-id="64575-135">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




