---
description: Эти типы данных можно использовать для указания типа значения реестра.
title: Типы данных реестра (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4185e7af-e1f0-40af-91c7-0ff7e27896ae
api_name:
- REG_BINARY
- REG_DWORD
- REG_QWORD
- REG_DWORD_LITTLE_ENDIAN
- REG_QWORD_LITTLE_ENDIAN
- REG_DWORD_BIG_ENDIAN
- REG_EXPAND_SZ
- REG_LINK
- REG_MULTI_SZ
- REG_NONE
- REG_RESOURCE_LIST
- REG_SZ
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4de4595b55716d58df04a598dd6ba298f22829d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104998984"
---
# <a name="registry-data-types"></a><span data-ttu-id="f89a5-103">Типы данных реестра</span><span class="sxs-lookup"><span data-stu-id="f89a5-103">Registry Data Types</span></span>

<span data-ttu-id="f89a5-104">Эти типы данных можно использовать для указания типа значения реестра.</span><span class="sxs-lookup"><span data-stu-id="f89a5-104">These data types can be used to specify the type of a registry value.</span></span>



| <span data-ttu-id="f89a5-105">Константа</span><span class="sxs-lookup"><span data-stu-id="f89a5-105">Constant</span></span>                                                                                                                                                                                      | <span data-ttu-id="f89a5-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f89a5-106">Description</span></span>                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_BINARY"></span><span id="reg_binary"></span><dl> <span data-ttu-id="f89a5-107"><dt>**\_двоичный файл REG**</dt></span><span class="sxs-lookup"><span data-stu-id="f89a5-107"><dt>**REG\_BINARY**</dt></span></span> </dl>                                          | <span data-ttu-id="f89a5-108">Двоичные данные в любой форме.</span><span class="sxs-lookup"><span data-stu-id="f89a5-108">Binary data in any form.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <span id="REG_DWORD"></span><span id="reg_dword"></span><dl> <span data-ttu-id="f89a5-109"><dt>**REG \_ DWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="f89a5-109"><dt>**REG\_DWORD**</dt></span></span> </dl>                                             | <span data-ttu-id="f89a5-110">32-разрядное число.</span><span class="sxs-lookup"><span data-stu-id="f89a5-110">32-bit number.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_QWORD"></span><span id="reg_qword"></span><dl> <span data-ttu-id="f89a5-111"><dt>**REG \_ QWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="f89a5-111"><dt>**REG\_QWORD**</dt></span></span> </dl>                                             | <span data-ttu-id="f89a5-112">64-разрядное число.</span><span class="sxs-lookup"><span data-stu-id="f89a5-112">64-bit number.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_DWORD_LITTLE_ENDIAN"></span><span id="reg_dword_little_endian"></span><dl> <span data-ttu-id="f89a5-113"><dt>**REG \_ DWORD с \_ прямым \_ порядком байтов**</dt></span><span class="sxs-lookup"><span data-stu-id="f89a5-113"><dt>**REG\_DWORD\_LITTLE\_ENDIAN**</dt></span></span> </dl> | <span data-ttu-id="f89a5-114">32-разрядный номер в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="f89a5-114">32-bit number in little-endian format.</span></span> <span data-ttu-id="f89a5-115">Это эквивалентно **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="f89a5-115">This is equivalent to **REG\_DWORD**.</span></span><br/> <span data-ttu-id="f89a5-116">В формате с прямым порядком байтов многобайтовый параметр хранится в памяти с наименьшего байта ("маленький конец") до самого большого байта.</span><span class="sxs-lookup"><span data-stu-id="f89a5-116">In little-endian format, a multibyte value is stored in memory from the lowest byte (the "little end") to the highest byte.</span></span> <span data-ttu-id="f89a5-117">Например, значение 0x12345678 хранится как (0x78 0x56 0x34 0x12) в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="f89a5-117">For example, the value 0x12345678 is stored as (0x78 0x56 0x34 0x12) in little-endian format.</span></span><br/> |
| <span id="REG_QWORD_LITTLE_ENDIAN"></span><span id="reg_qword_little_endian"></span><dl> <span data-ttu-id="f89a5-118"><dt>**REG с обратным \_ \_ \_ порядком байтов**</dt></span><span class="sxs-lookup"><span data-stu-id="f89a5-118"><dt>**REG\_QWORD\_LITTLE\_ENDIAN**</dt></span></span> </dl> | <span data-ttu-id="f89a5-119">64-разрядный номер в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="f89a5-119">A 64-bit number in little-endian format.</span></span> <span data-ttu-id="f89a5-120">Это эквивалентно **reg \_ QWORD**.</span><span class="sxs-lookup"><span data-stu-id="f89a5-120">This is equivalent to **REG\_QWORD**.</span></span> <br/>                                                                                                                                                                                                                                   |
| <span id="REG_DWORD_BIG_ENDIAN"></span><span id="reg_dword_big_endian"></span><dl> <span data-ttu-id="f89a5-121"><dt>**REG \_ байт с \_ обратным \_ порядком байтов**</dt></span><span class="sxs-lookup"><span data-stu-id="f89a5-121"><dt>**REG\_DWORD\_BIG\_ENDIAN**</dt></span></span> </dl>          | <span data-ttu-id="f89a5-122">32-разрядный номер в формате с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="f89a5-122">32-bit number in big-endian format.</span></span><br/> <span data-ttu-id="f89a5-123">В формате с обратным порядком байтов многобайтовый параметр хранится в памяти из самого длинного байта («Big-конец») до наименьшего байта.</span><span class="sxs-lookup"><span data-stu-id="f89a5-123">In big-endian format, a multibyte value is stored in memory from the highest byte (the "big end") to the lowest byte.</span></span> <span data-ttu-id="f89a5-124">Например, значение 0x12345678 сохраняется как (0x12 0x34 0x56 0x78) в формате с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="f89a5-124">For example, the value 0x12345678 is stored as (0x12 0x34 0x56 0x78) in big-endian format.</span></span><br/>                                                   |
| <span id="REG_EXPAND_SZ"></span><span id="reg_expand_sz"></span><dl> <span data-ttu-id="f89a5-125"><dt>**\_распаковать \_ SZ**</dt></span><span class="sxs-lookup"><span data-stu-id="f89a5-125"><dt>**REG\_EXPAND\_SZ**</dt></span></span> </dl>                                | <span data-ttu-id="f89a5-126">Строка, завершающаяся нулем, которая содержит нераскрытные ссылки на переменные среды (например, "% PATH%").</span><span class="sxs-lookup"><span data-stu-id="f89a5-126">Null-terminated string that contains unexpanded references to environment variables (for example, "%PATH%").</span></span> <span data-ttu-id="f89a5-127">Это будет строка в Юникоде или ANSI в зависимости от того, используются ли функции Юникода или ANSI.</span><span class="sxs-lookup"><span data-stu-id="f89a5-127">It will be a Unicode or ANSI string, depending on whether you use the Unicode or ANSI functions.</span></span><br/>                                                                                                     |
| <span id="REG_LINK"></span><span id="reg_link"></span><dl> <span data-ttu-id="f89a5-128"><dt>**Ссылка на REG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f89a5-128"><dt>**REG\_LINK**</dt></span></span> </dl>                                                | <span data-ttu-id="f89a5-129">Символьная ссылка в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="f89a5-129">Unicode symbolic link.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dl> <span data-ttu-id="f89a5-130"><dt>**REG \_ Multi \_ SZ**</dt></span><span class="sxs-lookup"><span data-stu-id="f89a5-130"><dt>**REG\_MULTI\_SZ**</dt></span></span> </dl>                                   | <span data-ttu-id="f89a5-131">Массив строк, заканчивающихся нулем, заканчивающихся двумя символами NULL.</span><span class="sxs-lookup"><span data-stu-id="f89a5-131">Array of null-terminated strings that are terminated by two null characters.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="REG_NONE"></span><span id="reg_none"></span><dl> <span data-ttu-id="f89a5-132"><dt>**REG \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="f89a5-132"><dt>**REG\_NONE**</dt></span></span> </dl>                                                | <span data-ttu-id="f89a5-133">Нет определенного типа значения.</span><span class="sxs-lookup"><span data-stu-id="f89a5-133">No defined value type.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_RESOURCE_LIST"></span><span id="reg_resource_list"></span><dl> <span data-ttu-id="f89a5-134"><dt>**\_список ресурсов \_ реестра**</dt></span><span class="sxs-lookup"><span data-stu-id="f89a5-134"><dt>**REG\_RESOURCE\_LIST**</dt></span></span> </dl>                    | <span data-ttu-id="f89a5-135">Список ресурсов драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="f89a5-135">Device-driver resource list.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="REG_SZ"></span><span id="reg_sz"></span><dl> <span data-ttu-id="f89a5-136"><dt>**REG \_ SZ**</dt></span><span class="sxs-lookup"><span data-stu-id="f89a5-136"><dt>**REG\_SZ**</dt></span></span> </dl>                                                      | <span data-ttu-id="f89a5-137">Строка, завершающаяся символом NULL.</span><span class="sxs-lookup"><span data-stu-id="f89a5-137">Null-terminated string.</span></span> <span data-ttu-id="f89a5-138">Это будет строка в Юникоде или ANSI в зависимости от того, используются ли функции Юникода или ANSI.</span><span class="sxs-lookup"><span data-stu-id="f89a5-138">It will be a Unicode or ANSI string, depending on whether you use the Unicode or ANSI functions.</span></span><br/>                                                                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="f89a5-139">Требования</span><span class="sxs-lookup"><span data-stu-id="f89a5-139">Requirements</span></span>



| <span data-ttu-id="f89a5-140">Требование</span><span class="sxs-lookup"><span data-stu-id="f89a5-140">Requirement</span></span> | <span data-ttu-id="f89a5-141">Значение</span><span class="sxs-lookup"><span data-stu-id="f89a5-141">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f89a5-142">Header</span><span class="sxs-lookup"><span data-stu-id="f89a5-142">Header</span></span><br/> | <dl> <span data-ttu-id="f89a5-143"><dt>Файл Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="f89a5-143"><dt>Winnt.h</dt></span></span> </dl> |



 

 




