---
description: Определяет один объект фильтра просмотра.
ms.assetid: 865b55f3-9294-43c5-b4dc-eb5128ce3a38
title: Структура ФИЛТЕРОБЖЕКТ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILTEROBJECT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7649ab294f2ecad90946926dcc68d6937b357666
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673202"
---
# <a name="filterobject-structure"></a><span data-ttu-id="c2a5e-103">Структура ФИЛТЕРОБЖЕКТ</span><span class="sxs-lookup"><span data-stu-id="c2a5e-103">FILTEROBJECT structure</span></span>

<span data-ttu-id="c2a5e-104">Структура **филтеробжект** определяет один объект фильтра просмотра.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-104">The **FILTEROBJECT** structure defines a single object of a display filter.</span></span> <span data-ttu-id="c2a5e-105">Функция [**филтераддобжект**](filteraddobject.md) использует **филтеробжект** для создания фильтра просмотра.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-105">The [**FilterAddObject**](filteraddobject.md) function uses **FILTEROBJECT** to build a display filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2a5e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2a5e-106">Syntax</span></span>


```C++
typedef struct _FILTEROBJECT {
  FILTERACTIONTYPE     Action;
  HPROPERTY            hProperty;
  union {
    VALUETYPE           Value;
    HPROTOCOL           hProtocol;
    LPVOID              lpArray;
    LPPROTOCOLTABLETYPE lpProtocolTable;
    LPADDRESS           lpAddress;
    ULPLARGEINT         lpLargeInt;
    ULPTIME             lpTime;
    LPOBJECT_IDENTIFIER lpOID;
  };
  union {
    WORD ByteCount;
    WORD ByteOffset;
  };
  struct _FILTEROBJECT  *pNext;
} FILTEROBJECT, *LPFILTEROBJECT;
```



## <a name="members"></a><span data-ttu-id="c2a5e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c2a5e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c2a5e-108">**Действие**</span><span class="sxs-lookup"><span data-stu-id="c2a5e-108">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="c2a5e-109">Флаг, указывающий действие **филтеробжект** .</span><span class="sxs-lookup"><span data-stu-id="c2a5e-109">Flag that specifies the **FILTEROBJECT** action.</span></span> <span data-ttu-id="c2a5e-110">Флаг может указывать свойство, значение или оператор.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-110">A flag can specify a property, value, or operator.</span></span>

<span data-ttu-id="c2a5e-111">В следующей таблице перечислены флаги свойств члена действия.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-111">The following table lists Action member property flags.</span></span>



| <span data-ttu-id="c2a5e-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c2a5e-112">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="c2a5e-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c2a5e-113">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="FILTERACTION_PROPERTY"></span><span id="filteraction_property"></span><dl> <span data-ttu-id="c2a5e-114"><dt>**свойство действия фильтра \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-114"><dt>**FILTERACTION\_PROPERTY**</dt></span></span> </dl>                | <span data-ttu-id="c2a5e-115">Содержит это свойство.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-115">Contains this property.</span></span><br/>                                     |
| <span id="FILTERACTION_PROPERTYEXIST"></span><span id="filteraction_propertyexist"></span><dl> <span data-ttu-id="c2a5e-116"><dt>**ДЕЙСТВИЕ фильтра \_ пропертексист**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-116"><dt>**FILTERACTION\_PROPERTYEXIST**</dt></span></span> </dl> | <span data-ttu-id="c2a5e-117">Указывает, что свойство действия фильтра уже определено.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-117">Indicates that a filter action property is already defined.</span></span><br/> |



 

<span data-ttu-id="c2a5e-118">В следующей таблице перечислены флаги значений членов действий.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-118">The following table lists Action member value flags.</span></span>



| <span data-ttu-id="c2a5e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c2a5e-119">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="c2a5e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c2a5e-120">Meaning</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="FILTERACTION_VALUE"></span><span id="filteraction_value"></span><dl> <span data-ttu-id="c2a5e-121"><dt>**значение действия фильтра \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-121"><dt>**FILTERACTION\_VALUE**</dt></span></span> </dl>                 | <span data-ttu-id="c2a5e-122">Содержит это значение.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-122">Contains this value.</span></span><br/>                                             |
| <span id="FILTERACTION_STRING"></span><span id="filteraction_string"></span><dl> <span data-ttu-id="c2a5e-123"><dt>**Строка действия фильтра \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-123"><dt>**FILTERACTION\_STRING**</dt></span></span> </dl>              | <span data-ttu-id="c2a5e-124">Содержит эту строку.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-124">Contains this string.</span></span><br/>                                            |
| <span id="FILTERACTION_ARRAY"></span><span id="filteraction_array"></span><dl> <span data-ttu-id="c2a5e-125"><dt>**\_массив фильтра**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-125"><dt>**FILTERACTION\_ARRAY**</dt></span></span> </dl>                 | <span data-ttu-id="c2a5e-126">Содержит этот массив.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-126">Contains this array.</span></span><br/>                                             |
| <span id="FILTERACTION_CONTAINSNC"></span><span id="filteraction_containsnc"></span><dl> <span data-ttu-id="c2a5e-127"><dt>**ДЕЙСТВИЕ фильтра \_ контаинснк**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-127"><dt>**FILTERACTION\_CONTAINSNC**</dt></span></span> </dl>  | <span data-ttu-id="c2a5e-128">Указывает, что свойство содержит подстроку без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-128">Indicates that a property contains a case-insensitive substring.</span></span><br/> |
| <span id="FILTERACTION_CONTAINS"></span><span id="filteraction_contains"></span><dl> <span data-ttu-id="c2a5e-129"><dt>**ДЕЙСТВИЕ фильтра \_ содержит**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-129"><dt>**FILTERACTION\_CONTAINS**</dt></span></span> </dl>        | <span data-ttu-id="c2a5e-130">Указывает, что свойство содержит подстроку с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-130">Indicates that a property contains a case sensitive substring.</span></span><br/>   |
| <span id="FILTERACTION_ADDRESS"></span><span id="filteraction_address"></span><dl> <span data-ttu-id="c2a5e-131"><dt>**адрес действия фильтра \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-131"><dt>**FILTERACTION\_ADDRESS**</dt></span></span> </dl>           | <span data-ttu-id="c2a5e-132">Содержит MAC-адрес.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-132">Contains the MAC address.</span></span><br/>                                        |
| <span id="FILTERACTION_ADDRESSANY"></span><span id="filteraction_addressany"></span><dl> <span data-ttu-id="c2a5e-133"><dt>**ДЕЙСТВИЕ фильтра \_ аддрессани**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-133"><dt>**FILTERACTION\_ADDRESSANY**</dt></span></span> </dl>  | <span data-ttu-id="c2a5e-134">Соответствует любому MAC-адресу.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-134">Matches any MAC address.</span></span><br/>                                         |
| <span id="FILTERACTION_FROM"></span><span id="filteraction_from"></span><dl> <span data-ttu-id="c2a5e-135"><dt>**ДЕЙСТВИЕ фильтра \_ из**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-135"><dt>**FILTERACTION\_FROM**</dt></span></span> </dl>                    | <span data-ttu-id="c2a5e-136">Указывает **MAC-** адрес.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-136">Indicates the **From MAC** address.</span></span><br/>                              |
| <span id="FILTERACTION_TO"></span><span id="filteraction_to"></span><dl> <span data-ttu-id="c2a5e-137"><dt>**ДЕЙСТВИЕ фильтра \_ для**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-137"><dt>**FILTERACTION\_TO**</dt></span></span> </dl>                          | <span data-ttu-id="c2a5e-138">Указывает **MAC-** адрес.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-138">Indicates the **To MAC** address.</span></span><br/>                                |
| <span id="FILTERACTION_FROMTO"></span><span id="filteraction_fromto"></span><dl> <span data-ttu-id="c2a5e-139"><dt>**ДЕЙСТВИЕ фильтра \_ фромто**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-139"><dt>**FILTERACTION\_FROMTO**</dt></span></span> </dl>              | <span data-ttu-id="c2a5e-140">Указывает на связывание MAC-адресов **от или к** .</span><span class="sxs-lookup"><span data-stu-id="c2a5e-140">Indicates a **From/To** pairing of MAC addresses.</span></span><br/>                |
| <span id="FILTERACTION_LARGEINT"></span><span id="filteraction_largeint"></span><dl> <span data-ttu-id="c2a5e-141"><dt>**ДЕЙСТВИЕ фильтра \_ ларжеинт**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-141"><dt>**FILTERACTION\_LARGEINT**</dt></span></span> </dl>        | <span data-ttu-id="c2a5e-142">Содержит большое целое число.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-142">Contains a large integer.</span></span><br/>                                        |
| <span id="FILTERACTION_TIME"></span><span id="filteraction_time"></span><dl> <span data-ttu-id="c2a5e-143"><dt>**время действия фильтра \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-143"><dt>**FILTERACTION\_TIME**</dt></span></span> </dl>                    | <span data-ttu-id="c2a5e-144">Содержит структуру **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="c2a5e-144">Contains a **SYSTEMTIME** structure.</span></span><br/>                             |
| <span id="FILTERACTION_ADDR_ETHER"></span><span id="filteraction_addr_ether"></span><dl> <span data-ttu-id="c2a5e-145"><dt>**\_ETHER адрес действия фильтра \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-145"><dt>**FILTERACTION\_ADDR\_ETHER**</dt></span></span> </dl> | <span data-ttu-id="c2a5e-146">Содержит MAC-адрес Ethernet.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-146">Contains an Ethernet MAC address.</span></span><br/>                                |
| <span id="FILTERACTION_ADDR_TOKEN"></span><span id="filteraction_addr_token"></span><dl> <span data-ttu-id="c2a5e-147"><dt>**\_маркер адреса в действии фильтра \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-147"><dt>**FILTERACTION\_ADDR\_TOKEN**</dt></span></span> </dl> | <span data-ttu-id="c2a5e-148">Содержит MAC-адрес Token Ring.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-148">Contains a token ring MAC address.</span></span><br/>                               |
| <span id="FILTERACTION_ADDR_FDDI"></span><span id="filteraction_addr_fddi"></span><dl> <span data-ttu-id="c2a5e-149"><dt>**адрес действия фильтра \_ \_ FDDI**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-149"><dt>**FILTERACTION\_ADDR\_FDDI**</dt></span></span> </dl>    | <span data-ttu-id="c2a5e-150">Содержит MAC-адрес FDDI.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-150">Contains a FDDI MAC address.</span></span><br/>                                     |
| <span id="FILTERACTION_ADDR_IPX"></span><span id="filteraction_addr_ipx"></span><dl> <span data-ttu-id="c2a5e-151"><dt>**адрес действия фильтра ( \_ \_ IPX)**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-151"><dt>**FILTERACTION\_ADDR\_IPX**</dt></span></span> </dl>       | <span data-ttu-id="c2a5e-152">Содержит MAC-адрес IPX.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-152">Contains an IPX MAC address.</span></span><br/>                                     |
| <span id="FILTERACTION_ADDR_IP"></span><span id="filteraction_addr_ip"></span><dl> <span data-ttu-id="c2a5e-153"><dt>**\_ \_ IP-адрес получателя фильтра**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-153"><dt>**FILTERACTION\_ADDR\_IP**</dt></span></span> </dl>          | <span data-ttu-id="c2a5e-154">Содержит IP-адрес MAC.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-154">Contains an IP MAC address.</span></span><br/>                                      |
| <span id="FILTERACTION_OID"></span><span id="filteraction_oid"></span><dl> <span data-ttu-id="c2a5e-155"><dt>**\_идентификатор объекта действия фильтра**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-155"><dt>**FILTERACTION\_OID**</dt></span></span> </dl>                       | <span data-ttu-id="c2a5e-156">Содержит идентификатор объекта (OID).</span><span class="sxs-lookup"><span data-stu-id="c2a5e-156">Contains an Object Identifier (OID).</span></span><br/>                             |



 

<span data-ttu-id="c2a5e-157">В следующей таблице перечислены флаги операторов члена действия.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-157">The following table lists Action member operator flags.</span></span>



| <span data-ttu-id="c2a5e-158">Значение</span><span class="sxs-lookup"><span data-stu-id="c2a5e-158">Value</span></span>                                                                                                                                                                                                        | <span data-ttu-id="c2a5e-159">Значение</span><span class="sxs-lookup"><span data-stu-id="c2a5e-159">Meaning</span></span>                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILTERACTION_INVALID"></span><span id="filteraction_invalid"></span><dl> <span data-ttu-id="c2a5e-160"><dt>**\_недопустимое действие фильтра**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-160"><dt>**FILTERACTION\_INVALID**</dt></span></span> </dl>                           | <span data-ttu-id="c2a5e-161">Указывает на недопустимое действие фильтра.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-161">Indicates an invalid filter action.</span></span><br/>                                                                                  |
| <span id="FILTERACTION_AND"></span><span id="filteraction_and"></span><dl> <span data-ttu-id="c2a5e-162"><dt>**ДЕЙСТВИЕ фильтра \_ и**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-162"><dt>**FILTERACTION\_AND**</dt></span></span> </dl>                                       | <span data-ttu-id="c2a5e-163">Указывает логическую инструкцию **и** .</span><span class="sxs-lookup"><span data-stu-id="c2a5e-163">Indicates a logical **AND** statement.</span></span><br/>                                                                               |
| <span id="FILTERACTION_OR"></span><span id="filteraction_or"></span><dl> <span data-ttu-id="c2a5e-164"><dt>**ДЕЙСТВИЕ фильтра \_ или**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-164"><dt>**FILTERACTION\_OR**</dt></span></span> </dl>                                          | <span data-ttu-id="c2a5e-165">Указывает на логический оператор **или** .</span><span class="sxs-lookup"><span data-stu-id="c2a5e-165">Indicates a logical **OR** statement.</span></span><br/>                                                                                |
| <span id="FILTERACTION_XOR"></span><span id="filteraction_xor"></span><dl> <span data-ttu-id="c2a5e-166"><dt>**ДЕЙСТВИЕ фильтра \_ XOR**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-166"><dt>**FILTERACTION\_XOR**</dt></span></span> </dl>                                       | <span data-ttu-id="c2a5e-167">Указывает на логическую исключающую инструкцию **или** (XOR).</span><span class="sxs-lookup"><span data-stu-id="c2a5e-167">Indicates a logical exclusive **OR** (XOR) statement.</span></span><br/>                                                                |
| <span id="FILTERACTION_NOT"></span><span id="filteraction_not"></span><dl> <span data-ttu-id="c2a5e-168"><dt>**ДЕЙСТВИЕ фильтра \_ не**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-168"><dt>**FILTERACTION\_NOT**</dt></span></span> </dl>                                       | <span data-ttu-id="c2a5e-169">Указывает на логическую инструкцию **Not** .</span><span class="sxs-lookup"><span data-stu-id="c2a5e-169">Indicates a logical **NOT** statement.</span></span><br/>                                                                               |
| <span id="FILTERACTION_EQUALNC"></span><span id="filteraction_equalnc"></span><dl> <span data-ttu-id="c2a5e-170"><dt>**ДЕЙСТВИЕ фильтра \_ екуалнк**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-170"><dt>**FILTERACTION\_EQUALNC**</dt></span></span> </dl>                           | <span data-ttu-id="c2a5e-171">Действие фильтра равно и не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-171">Filter action is equal and case insensitive.</span></span><br/>                                                                         |
| <span id="FILTERACTION_EQUAL"></span><span id="filteraction_equal"></span><dl> <span data-ttu-id="c2a5e-172"><dt>**ДЕЙСТВИЕ фильтра \_ равно**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-172"><dt>**FILTERACTION\_EQUAL**</dt></span></span> </dl>                                 | <span data-ttu-id="c2a5e-173">Действие фильтра равно и учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-173">Filter action is equal and case sensitive.</span></span><br/>                                                                           |
| <span id="FILTERACTION_NOTEQUALNC"></span><span id="filteraction_notequalnc"></span><dl> <span data-ttu-id="c2a5e-174"><dt>**ДЕЙСТВИЕ фильтра \_ нотекуалнк**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-174"><dt>**FILTERACTION\_NOTEQUALNC**</dt></span></span> </dl>                  | <span data-ttu-id="c2a5e-175">Оператор логического **не** равен и не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-175">Logical **NOT** statement is equal and case insensitive.</span></span><br/>                                                             |
| <span id="FILTERACTION_NOTEQUAL"></span><span id="filteraction_notequal"></span><dl> <span data-ttu-id="c2a5e-176"><dt>**ДЕЙСТВИЕ фильтра \_ NOTEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-176"><dt>**FILTERACTION\_NOTEQUAL**</dt></span></span> </dl>                        | <span data-ttu-id="c2a5e-177">Оператор логического **не** равен и учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-177">Logical **NOT** statement is equal and is case sensitive.</span></span><br/>                                                            |
| <span id="FILTERACTION_GREATERNC"></span><span id="filteraction_greaternc"></span><dl> <span data-ttu-id="c2a5e-178"><dt>**ДЕЙСТВИЕ фильтра \_ греатернк**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-178"><dt>**FILTERACTION\_GREATERNC**</dt></span></span> </dl>                     | <span data-ttu-id="c2a5e-179">Действие фильтра больше (>) и не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-179">Filter action is greater than (>) and case insensitive.</span></span><br/>                                                           |
| <span id="FILTERACTION_GREATER"></span><span id="filteraction_greater"></span><dl> <span data-ttu-id="c2a5e-180"><dt>**ДЕЙСТВИЕ фильтра \_ выше**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-180"><dt>**FILTERACTION\_GREATER**</dt></span></span> </dl>                           | <span data-ttu-id="c2a5e-181">Действие фильтра больше (>) и с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-181">Filter action is greater than (>) and case sensitive.</span></span><br/>                                                             |
| <span id="FILTERACTION_LESSNC"></span><span id="filteraction_lessnc"></span><dl> <span data-ttu-id="c2a5e-182"><dt>**ДЕЙСТВИЕ фильтра \_ лесснк**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-182"><dt>**FILTERACTION\_LESSNC**</dt></span></span> </dl>                              | <span data-ttu-id="c2a5e-183">Действие фильтра меньше (<) и не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-183">Filter action is less than (<) and case insensitive.</span></span><br/>                                                              |
| <span id="FILTERACTION_LESS"></span><span id="filteraction_less"></span><dl> <span data-ttu-id="c2a5e-184"><dt>**ДЕЙСТВИЕ фильтра \_ меньше**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-184"><dt>**FILTERACTION\_LESS**</dt></span></span> </dl>                                    | <span data-ttu-id="c2a5e-185">Действие фильтра меньше (<) и с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-185">Filter action is less than (<) and case sensitive.</span></span><br/>                                                                |
| <span id="FILTERACTION_GREATEREQUALNC"></span><span id="filteraction_greaterequalnc"></span><dl> <span data-ttu-id="c2a5e-186"><dt>**ДЕЙСТВИЕ фильтра \_ греатерекуалнк**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-186"><dt>**FILTERACTION\_GREATEREQUALNC**</dt></span></span> </dl>      | <span data-ttu-id="c2a5e-187">Действие фильтра больше или равно (>=) и не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-187">Filter action is greater than or equal to (>=) and case insensitive.</span></span><br/>                                              |
| <span id="FILTERACTION_GREATEREQUAL"></span><span id="filteraction_greaterequal"></span><dl> <span data-ttu-id="c2a5e-188"><dt>**ДЕЙСТВИЕ фильтра \_ загруженность**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-188"><dt>**FILTERACTION\_GREATEREQUAL**</dt></span></span> </dl>            | <span data-ttu-id="c2a5e-189">Действие фильтра больше или равно (>=) и с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-189">Filter action is greater than or equal to (>=) and case sensitive.</span></span><br/>                                                |
| <span id="FILTERACTION_LESSEQUALNC"></span><span id="filteraction_lessequalnc"></span><dl> <span data-ttu-id="c2a5e-190"><dt>**ДЕЙСТВИЕ фильтра \_ лессекуалнк**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-190"><dt>**FILTERACTION\_LESSEQUALNC**</dt></span></span> </dl>               | <span data-ttu-id="c2a5e-191">Действие фильтра меньше или равно (<=) и не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-191">Filter action is less than or equal to (<=) and case insensitive.</span></span><br/>                                                 |
| <span id="FILTERACTION_LESSEQUAL"></span><span id="filteraction_lessequal"></span><dl> <span data-ttu-id="c2a5e-192"><dt>**ДЕЙСТВИЕ фильтра \_ лессекуал**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-192"><dt>**FILTERACTION\_LESSEQUAL**</dt></span></span> </dl>                     | <span data-ttu-id="c2a5e-193">Действие фильтра меньше или равно (<=) и учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-193">Filter action is less than or equal to (<=) and is case sensitive.</span></span><br/>                                                |
| <span id="FILTERACTION_PLUS"></span><span id="filteraction_plus"></span><dl> <span data-ttu-id="c2a5e-194"><dt>**ДЕЙСТВИЕ фильтра \_ плюс**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-194"><dt>**FILTERACTION\_PLUS**</dt></span></span> </dl>                                    | <span data-ttu-id="c2a5e-195">Добавить оператор (+).</span><span class="sxs-lookup"><span data-stu-id="c2a5e-195">Add operator (+).</span></span><br/>                                                                                                    |
| <span id="FILTERACTION_MINUS"></span><span id="filteraction_minus"></span><dl> <span data-ttu-id="c2a5e-196"><dt>**ДЕЙСТВИЕ фильтра \_ минус**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-196"><dt>**FILTERACTION\_MINUS**</dt></span></span> </dl>                                 | <span data-ttu-id="c2a5e-197">Оператор вычитания (-).</span><span class="sxs-lookup"><span data-stu-id="c2a5e-197">Subtract operator (-).</span></span><br/>                                                                                               |
| <span id="FILTERACTION_AREBITSON"></span><span id="filteraction_arebitson"></span><dl> <span data-ttu-id="c2a5e-198"><dt>**ДЕЙСТВИЕ фильтра \_ аребитсон**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-198"><dt>**FILTERACTION\_AREBITSON**</dt></span></span> </dl>                     | <span data-ttu-id="c2a5e-199">Указывает побитовую операцию.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-199">Indicates a bitwise operation.</span></span><br/>                                                                                       |
| <span id="FILTERACTION_AREBITSOFF"></span><span id="filteraction_arebitsoff"></span><dl> <span data-ttu-id="c2a5e-200"><dt>**ДЕЙСТВИЕ фильтра \_ аребитсофф**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-200"><dt>**FILTERACTION\_AREBITSOFF**</dt></span></span> </dl>                  | <span data-ttu-id="c2a5e-201">Указывает на побитовую операцию.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-201">Indicates a non-bitwise operation.</span></span><br/>                                                                                   |
| <span id="FILTERACTION_PROTOCOLSEXIST"></span><span id="filteraction_protocolsexist"></span><dl> <span data-ttu-id="c2a5e-202"><dt>**ДЕЙСТВИЕ фильтра \_ протоколсексист**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-202"><dt>**FILTERACTION\_PROTOCOLSEXIST**</dt></span></span> </dl>      | <span data-ttu-id="c2a5e-203">Указывает, что выбранные протоколы существуют.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-203">Indicates that the selected protocols exist.</span></span><br/>                                                                         |
| <span id="FILTERACTION_PROTOCOLEXIST"></span><span id="filteraction_protocolexist"></span><dl> <span data-ttu-id="c2a5e-204"><dt>**ДЕЙСТВИЕ фильтра \_ протоколексист**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-204"><dt>**FILTERACTION\_PROTOCOLEXIST**</dt></span></span> </dl>         | <span data-ttu-id="c2a5e-205">Указывает, что выбранный протокол существует.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-205">Indicates that the selected protocol exists.</span></span><br/>                                                                         |
| <span id="FILTERACTION_ARRAYEQUAL"></span><span id="filteraction_arrayequal"></span><dl> <span data-ttu-id="c2a5e-206"><dt>**ДЕЙСТВИЕ фильтра \_ аррайекуал**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-206"><dt>**FILTERACTION\_ARRAYEQUAL**</dt></span></span> </dl>                  | <span data-ttu-id="c2a5e-207">Указывает, что содержимое массива равно.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-207">Indicates that array contents are equal.</span></span> <span data-ttu-id="c2a5e-208">Флаг должен использоваться с структурой **\_ массива фильтра** .</span><span class="sxs-lookup"><span data-stu-id="c2a5e-208">The flag must be used with a **FILTERACTION\_ARRAY** structure.</span></span><br/>             |
| <span id="FILTERACTION_DEREFPROPERTY"></span><span id="filteraction_derefproperty"></span><dl> <span data-ttu-id="c2a5e-209"><dt>**ДЕЙСТВИЕ фильтра \_ дерефпроперти**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-209"><dt>**FILTERACTION\_DEREFPROPERTY**</dt></span></span> </dl>         | <span data-ttu-id="c2a5e-210">Описывает соответствие шаблона по смещению (в байтах) от протокола.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-210">Describes a pattern match at an offset (in bytes), from the protocol.</span></span><br/>                                                |
| <span id="FILTERACTION_OID_CONTAINS"></span><span id="filteraction_oid_contains"></span><dl> <span data-ttu-id="c2a5e-211"><dt>**\_идентификатор объекта действия фильтра \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-211"><dt>**FILTERACTION\_OID\_CONTAINS**</dt></span></span> </dl>           | <span data-ttu-id="c2a5e-212">Вычисляет подстроку в пределах идентификатора объекта.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-212">Evaluates a substring within an object identifier.</span></span> <span data-ttu-id="c2a5e-213">Действие должно использоваться с структурой **\_ OID объекта фильтра** .</span><span class="sxs-lookup"><span data-stu-id="c2a5e-213">The action must be used with the **FILTERACTION\_OID** structure.</span></span><br/> |
| <span id="FILTERACTION_OID_BEGINS_WITH"></span><span id="filteraction_oid_begins_with"></span><dl> <span data-ttu-id="c2a5e-214"><dt>**Идентификатор объекта действия фильтра ( \_ OID) \_ начинается \_ с**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-214"><dt>**FILTERACTION\_OID\_BEGINS\_WITH**</dt></span></span> </dl> | <span data-ttu-id="c2a5e-215">Вычисляет подстроку, которая начинает идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-215">Evaluates a substring that begins an object identifier.</span></span> <span data-ttu-id="c2a5e-216">Флаг должен использоваться с **\_ идентификатором объекта действия фильтра**.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-216">The flag must be used with **FILTERACTION\_OID**.</span></span><br/>            |
| <span id="FILTERACTION_OID_ENDS_WITH"></span><span id="filteraction_oid_ends_with"></span><dl> <span data-ttu-id="c2a5e-217"><dt>**\_идентификатор объекта действия фильтра \_ заканчивается \_ на**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-217"><dt>**FILTERACTION\_OID\_ENDS\_WITH**</dt></span></span> </dl>       | <span data-ttu-id="c2a5e-218">Вычисляет подстроку, которая завершает идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-218">Evaluates a substring that ends an object identifier.</span></span> <span data-ttu-id="c2a5e-219">Флаг должен использоваться с **\_ идентификатором объекта действия фильтра**.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-219">The flag must be used with **FILTERACTION\_OID**.</span></span><br/>              |
| <span id="FILTERACTION_ADDR_VINES"></span><span id="filteraction_addr_vines"></span><dl> <span data-ttu-id="c2a5e-220"><dt>**\_приемники \_ фильтра**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-220"><dt>**FILTERACTION\_ADDR\_VINES**</dt></span></span> </dl>                 | <span data-ttu-id="c2a5e-221">Содержит MAC-адрес Vines.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-221">Contains a Vines MAC address.</span></span><br/>                                                                                        |
| <span id="FILTERACTION_EXPRESSION"></span><span id="filteraction_expression"></span><dl> <span data-ttu-id="c2a5e-222"><dt>**выражение действия фильтра \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-222"><dt>**FILTERACTION\_EXPRESSION**</dt></span></span> </dl>                  | <span data-ttu-id="c2a5e-223">Содержит выражение действия.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-223">Contains an action expression.</span></span><br/>                                                                                       |
| <span id="FILTERACTION_BOOL"></span><span id="filteraction_bool"></span><dl> <span data-ttu-id="c2a5e-224"><dt>**Логическое значение действия фильтра \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-224"><dt>**FILTERACTION\_BOOL**</dt></span></span> </dl>                                    | <span data-ttu-id="c2a5e-225">Содержит тип данных **bool** .</span><span class="sxs-lookup"><span data-stu-id="c2a5e-225">Contains a **BOOL** data type.</span></span><br/>                                                                                       |
| <span id="FILTER_DIRECTION_NEXT"></span><span id="filter_direction_next"></span><dl> <span data-ttu-id="c2a5e-226"><dt>**\_направление фильтра \_ Далее**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-226"><dt>**FILTER\_DIRECTION\_NEXT**</dt></span></span> </dl>                       | <span data-ttu-id="c2a5e-227">Управляет последовательным направлением (следующий кадр) в файле записи.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-227">Controls sequential direction (Next frame) within a capture file.</span></span><br/>                                                    |
| <span id="FILTER_DIRECTION_PREV"></span><span id="filter_direction_prev"></span><dl> <span data-ttu-id="c2a5e-228"><dt>**\_ \_ предыдущее направление фильтра**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-228"><dt>**FILTER\_DIRECTION\_PREV**</dt></span></span> </dl>                       | <span data-ttu-id="c2a5e-229">Управляет последовательным направлением (предыдущий кадр) в файле записи.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-229">Controls sequential direction (Previous frame) within a capture file.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="c2a5e-230">**хпроперти**</span><span class="sxs-lookup"><span data-stu-id="c2a5e-230">**hProperty**</span></span>
</dt> <dd>

<span data-ttu-id="c2a5e-231">Обработчик для ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-231">Handle to a property key.</span></span>

</dd> <dt>

<span data-ttu-id="c2a5e-232">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c2a5e-232">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="c2a5e-233">Значение объекта.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-233">Value of an object.</span></span>

</dd> <dt>

<span data-ttu-id="c2a5e-234">**хпротокол**</span><span class="sxs-lookup"><span data-stu-id="c2a5e-234">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="c2a5e-235">Маркер для протокола фильтра просмотра.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-235">Handle to display filter protocol.</span></span>

</dd> <dt>

<span data-ttu-id="c2a5e-236">**lpArray**</span><span class="sxs-lookup"><span data-stu-id="c2a5e-236">**lpArray**</span></span>
</dt> <dd>

<span data-ttu-id="c2a5e-237">Указатель на массив.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-237">Pointer to an array.</span></span>

</dd> <dt>

<span data-ttu-id="c2a5e-238">**лппротоколтабле**</span><span class="sxs-lookup"><span data-stu-id="c2a5e-238">**lpProtocolTable**</span></span>
</dt> <dd>

<span data-ttu-id="c2a5e-239">Указатель на список протоколов, предназначенный для проверки существования протокола в кадре.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-239">Pointer to a protocol list designed to test the existence of protocol in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="c2a5e-240">**лпаддресс**</span><span class="sxs-lookup"><span data-stu-id="c2a5e-240">**lpAddress**</span></span>
</dt> <dd>

<span data-ttu-id="c2a5e-241">Указатель на адрес типа ядра.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-241">Pointer to the kernel type address.</span></span> <span data-ttu-id="c2a5e-242">Например, MAC или IP.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-242">For example, MAC or IP.</span></span>

</dd> <dt>

<span data-ttu-id="c2a5e-243">**лпларжеинт**</span><span class="sxs-lookup"><span data-stu-id="c2a5e-243">**lpLargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="c2a5e-244">Двойное **слово DWORD** , используемое в приложении Windows NT или Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-244">Double **DWORD** used in a Windows NT or Windows 2000 application.</span></span>

</dd> <dt>

<span data-ttu-id="c2a5e-245">**лптиме**</span><span class="sxs-lookup"><span data-stu-id="c2a5e-245">**lpTime**</span></span>
</dt> <dd>

<span data-ttu-id="c2a5e-246">Указатель на структуру **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="c2a5e-246">A pointer to a **SYSTEMTIME** structure.</span></span>

</dd> <dt>

<span data-ttu-id="c2a5e-247">**лпоид**</span><span class="sxs-lookup"><span data-stu-id="c2a5e-247">**lpOID**</span></span>
</dt> <dd>

<span data-ttu-id="c2a5e-248">Указатель на структуру **\_ идентификатора объекта** (OID).</span><span class="sxs-lookup"><span data-stu-id="c2a5e-248">A pointer to the **OBJECT\_IDENTIFIER** (OID) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c2a5e-249">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="c2a5e-249">**ByteCount**</span></span>
</dt> <dd>

<span data-ttu-id="c2a5e-250">Число в байтах в кадре.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-250">The number, in bytes, in the frame.</span></span>

</dd> <dt>

<span data-ttu-id="c2a5e-251">**ByteOffset**</span><span class="sxs-lookup"><span data-stu-id="c2a5e-251">**ByteOffset**</span></span>
</dt> <dd>

<span data-ttu-id="c2a5e-252">Значение байта смещения структуры ФИЛТЕРОБЖЕКТ, используемое для сравнения массивов.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-252">The offset byte value of the FILTEROBJECT structure used to compare arrays.</span></span>

</dd> <dt>

<span data-ttu-id="c2a5e-253">**пнекст**</span><span class="sxs-lookup"><span data-stu-id="c2a5e-253">**pNext**</span></span>
</dt> <dd>

<span data-ttu-id="c2a5e-254">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="c2a5e-254">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2a5e-255">Требования</span><span class="sxs-lookup"><span data-stu-id="c2a5e-255">Requirements</span></span>



| <span data-ttu-id="c2a5e-256">Требование</span><span class="sxs-lookup"><span data-stu-id="c2a5e-256">Requirement</span></span> | <span data-ttu-id="c2a5e-257">Значение</span><span class="sxs-lookup"><span data-stu-id="c2a5e-257">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a5e-258">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2a5e-258">Minimum supported client</span></span><br/> | <span data-ttu-id="c2a5e-259">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c2a5e-259">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c2a5e-260">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2a5e-260">Minimum supported server</span></span><br/> | <span data-ttu-id="c2a5e-261">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c2a5e-261">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c2a5e-262">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c2a5e-262">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2a5e-263"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2a5e-263"><dt>Netmon.h</dt></span></span> </dl> |



 

 




