---
title: Простые типы данных ADSI (iAds. h)
description: Интерфейсы служб Active Directory (ADSI) определяют и используют следующие простые типы данных.
ms.assetid: 0bd34f13-269f-4f5d-8a18-74577522e402
ms.tgt_platform: multiple
keywords:
- ADS_BOOLEAN
- ADS_CASE_EXACT_STRING
- ADS_CASE_IGNORE_STRING
- ADS_DN_STRING
- ADS_INTEGER
- ADS_LARGE_INTEGER
- ADS_NUMERIC_STRING
- ADS_OBJECT_CLASS
- ADS_PRINTABLE_STRING
- ADS_SEARCH_HANDLE
- ADS_UTC_TIME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5530fda2ca1f4fe967eaf376b668a0bedc29c4b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071262"
---
# <a name="adsi-simple-data-types"></a><span data-ttu-id="ae2e7-114">Простые типы данных ADSI</span><span class="sxs-lookup"><span data-stu-id="ae2e7-114">ADSI Simple Data Types</span></span>

<span data-ttu-id="ae2e7-115">Интерфейсы служб Active Directory (ADSI) определяют и используют следующие простые типы данных.</span><span class="sxs-lookup"><span data-stu-id="ae2e7-115">Active Directory Service Interfaces (ADSI) defines and uses the following simple data types.</span></span>


```C++
typedef DWORD ADS_BOOLEAN, *PADS_BOOLEAN;
typedef LPWSTR ADS_CASE_EXACT_STRING, *PADS_CASE_EXACT_STRING;
typedef LPWSTR ADS_CASE_IGNORE_STRING, *PADS_CASE_IGNORE_STRING;
typedef LPWSTR ADS_DN_STRING, *PADS_DN_STRING;
typedef DWORD ADS_INTEGER, *PADS_INTEGER;
typedef LARGE_INTEGER ADS_LARGE_INTEGER, *PADS_LARGE_INTEGER;
typedef LPWSTR ADS_NUMERIC_STRING, *PADS_NUMERIC_STRING;
typedef LPWSTR ADS_OBJECT_CLASS, *PADS_OBJECT_CLASS;
typedef LPWSTR ADS_PRINTABLE_STRING, *PADS_PRINTABLE_STRING;
typedef HANDLE ADS_SEARCH_HANDLE, *PADS_SEARCH_HANDLE;
typedef SYSTEMTIME ADS_UTC_TIME, *PADS_UTC_TIME;
```



<dl> <dt>

<span data-ttu-id="ae2e7-116">**логические БАННЕРы \_**</span><span class="sxs-lookup"><span data-stu-id="ae2e7-116">**ADS\_BOOLEAN**</span></span>
</dt> <dd>

<span data-ttu-id="ae2e7-117">DWORD</span><span class="sxs-lookup"><span data-stu-id="ae2e7-117">DWORD</span></span>

</dd> <dt>

<span data-ttu-id="ae2e7-118">**\_ \_ Точная \_ строка в рекламном случае**</span><span class="sxs-lookup"><span data-stu-id="ae2e7-118">**ADS\_CASE\_EXACT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="ae2e7-119">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ae2e7-119">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="ae2e7-120">**\_ \_ строка игнорируемого варианта рекламы \_**</span><span class="sxs-lookup"><span data-stu-id="ae2e7-120">**ADS\_CASE\_IGNORE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="ae2e7-121">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ae2e7-121">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="ae2e7-122">**\_строка DN баннера \_**</span><span class="sxs-lookup"><span data-stu-id="ae2e7-122">**ADS\_DN\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="ae2e7-123">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ae2e7-123">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="ae2e7-124">**РЕКЛАМное \_ целое**</span><span class="sxs-lookup"><span data-stu-id="ae2e7-124">**ADS\_INTEGER**</span></span>
</dt> <dd>

<span data-ttu-id="ae2e7-125">DWORD</span><span class="sxs-lookup"><span data-stu-id="ae2e7-125">DWORD</span></span>

</dd> <dt>

<span data-ttu-id="ae2e7-126">**\_большое \_ целое число ADS**</span><span class="sxs-lookup"><span data-stu-id="ae2e7-126">**ADS\_LARGE\_INTEGER**</span></span>
</dt> <dd>

[<span data-ttu-id="ae2e7-127">**БОЛЬШОЕ \_ целое число**</span><span class="sxs-lookup"><span data-stu-id="ae2e7-127">**LARGE\_INTEGER**</span></span>](/windows/win32/api/winnt/ns-winnt-large_integer-r1)

</dd> <dt>

<span data-ttu-id="ae2e7-128">**\_численная \_ строка ADS**</span><span class="sxs-lookup"><span data-stu-id="ae2e7-128">**ADS\_NUMERIC\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="ae2e7-129">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ae2e7-129">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="ae2e7-130">**\_класс объектов \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="ae2e7-130">**ADS\_OBJECT\_CLASS**</span></span>
</dt> <dd>

<span data-ttu-id="ae2e7-131">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ae2e7-131">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="ae2e7-132">**\_Печатная \_ строка ADS**</span><span class="sxs-lookup"><span data-stu-id="ae2e7-132">**ADS\_PRINTABLE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="ae2e7-133">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ae2e7-133">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="ae2e7-134">**\_маркер поиска баннеров \_**</span><span class="sxs-lookup"><span data-stu-id="ae2e7-134">**ADS\_SEARCH\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="ae2e7-135">HANDLE</span><span class="sxs-lookup"><span data-stu-id="ae2e7-135">HANDLE</span></span>

</dd> <dt>

<span data-ttu-id="ae2e7-136">**время ADS в \_ формате UTC \_**</span><span class="sxs-lookup"><span data-stu-id="ae2e7-136">**ADS\_UTC\_TIME**</span></span>
</dt> <dd>

[<span data-ttu-id="ae2e7-137">**SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="ae2e7-137">**SYSTEMTIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae2e7-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae2e7-138">Remarks</span></span>

<span data-ttu-id="ae2e7-139">Когда ADSI считывает атрибут, определенный как **целое число** в схеме LDAP, он всегда будет выполнять целое число как 32-разрядное значение и может усечь данные.</span><span class="sxs-lookup"><span data-stu-id="ae2e7-139">When ADSI reads an attribute that has been defined as an **INTEGER** in the LDAP schema, it will always handle the integer as a 32-bit value and may truncate the data.</span></span> <span data-ttu-id="ae2e7-140">Это касается только LDAP-серверов, которые допускают произвольный размер целочисленных значений.</span><span class="sxs-lookup"><span data-stu-id="ae2e7-140">This is only a concern for LDAP servers that allow arbitrary sized integer values.</span></span> <span data-ttu-id="ae2e7-141">Если атрибут является пользовательским атрибутом, определенным путем расширения схемы, эту проблему можно избежать, определив настраиваемый атрибут в виде строки.</span><span class="sxs-lookup"><span data-stu-id="ae2e7-141">If the attribute is a custom attribute defined by extending the schema, this problem can be avoided by defining the custom attribute as a string.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae2e7-142">Требования</span><span class="sxs-lookup"><span data-stu-id="ae2e7-142">Requirements</span></span>



| <span data-ttu-id="ae2e7-143">Требование</span><span class="sxs-lookup"><span data-stu-id="ae2e7-143">Requirement</span></span> | <span data-ttu-id="ae2e7-144">Значение</span><span class="sxs-lookup"><span data-stu-id="ae2e7-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ae2e7-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae2e7-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ae2e7-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae2e7-146">Windows Vista</span></span><br/>                                                          |
| <span data-ttu-id="ae2e7-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae2e7-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ae2e7-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae2e7-148">Windows Server 2008</span></span><br/>                                                    |
| <span data-ttu-id="ae2e7-149">Header</span><span class="sxs-lookup"><span data-stu-id="ae2e7-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae2e7-150"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae2e7-150"><dt>Iads.h</dt></span></span> </dl> |



 

