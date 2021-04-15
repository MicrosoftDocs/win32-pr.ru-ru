---
description: Следующие константы используются с протоколом сертифицированной защиты выходных данных (Копп) для конкретных механизмов защиты выходных данных.
ms.assetid: a3cd63d8-22a5-473c-83c2-3499f3d32671
title: Флаги типа защиты Копп (Дксва. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPP_ProtectionType_Unknown
- COPP_ProtectionType_None
- COPP_ProtectionType_HDCP
- COPP_ProtectionType_ACP
- COPP_ProtectionType_CGMSA
- COPP_ProtectionType_Mask
- COPP_ProtectionType_Reserved
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 57e9ccc9420659ac09c19f2bbb7a18db519c07bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669472"
---
# <a name="copp-protection-type-flags"></a><span data-ttu-id="f34a7-103">Флаги типа защиты Копп</span><span class="sxs-lookup"><span data-stu-id="f34a7-103">COPP Protection Type Flags</span></span>

<span data-ttu-id="f34a7-104">Следующие константы используются с протоколом сертифицированной защиты выходных данных (Копп) для конкретных механизмов защиты выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f34a7-104">The follow constants are used with Certified Output Protection Protocol (COPP) to specific output protection mechanisms.</span></span>



| <span data-ttu-id="f34a7-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="f34a7-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="f34a7-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f34a7-106">Description</span></span>                                                     |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="COPP_ProtectionType_Unknown"></span><span id="copp_protectiontype_unknown"></span><span id="COPP_PROTECTIONTYPE_UNKNOWN"></span><dl> <span data-ttu-id="f34a7-107"><dt>**Копп \_ ProtectionType \_ неизвестный**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="f34a7-107"><dt>**COPP\_ProtectionType\_Unknown**</dt> <dt>0x80000000</dt></span></span> </dl>     | <span data-ttu-id="f34a7-108">Неизвестный механизм защиты.</span><span class="sxs-lookup"><span data-stu-id="f34a7-108">Unknown protection mechanism.</span></span><br/>                        |
| <span id="COPP_ProtectionType_None"></span><span id="copp_protectiontype_none"></span><span id="COPP_PROTECTIONTYPE_NONE"></span><dl> <span data-ttu-id="f34a7-109"><dt>**Копп \_ ProtectionType \_ нет**</dt> , <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="f34a7-109"><dt>**COPP\_ProtectionType\_None**</dt> <dt>0x00000000</dt></span></span> </dl>                 | <span data-ttu-id="f34a7-110">Нет механизмов защиты.</span><span class="sxs-lookup"><span data-stu-id="f34a7-110">No protection mechanisms.</span></span><br/>                            |
| <span id="COPP_ProtectionType_HDCP"></span><span id="copp_protectiontype_hdcp"></span><span id="COPP_PROTECTIONTYPE_HDCP"></span><dl> <span data-ttu-id="f34a7-111"><dt>**Копп \_ ProtectionType \_ HDCP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="f34a7-111"><dt>**COPP\_ProtectionType\_HDCP**</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="f34a7-112">High-Bandwidth цифровой Защита содержимого (HDCP).</span><span class="sxs-lookup"><span data-stu-id="f34a7-112">High-Bandwidth Digital Content Protection (HDCP).</span></span><br/>    |
| <span id="COPP_ProtectionType_ACP"></span><span id="copp_protectiontype_acp"></span><span id="COPP_PROTECTIONTYPE_ACP"></span><dl> <span data-ttu-id="f34a7-113"><dt>**Копп \_ ProtectionType \_ ACP**</dt> , <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="f34a7-113"><dt>**COPP\_ProtectionType\_ACP**</dt> <dt>0x00000002</dt></span></span> </dl>                     | <span data-ttu-id="f34a7-114">Аналоговая защита от копирования (ACP).</span><span class="sxs-lookup"><span data-stu-id="f34a7-114">Analog Copy Protection (ACP).</span></span><br/>                        |
| <span id="COPP_ProtectionType_CGMSA"></span><span id="copp_protectiontype_cgmsa"></span><span id="COPP_PROTECTIONTYPE_CGMSA"></span><dl> <span data-ttu-id="f34a7-115"><dt>**Копп \_ ProtectionType \_ кгмса**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="f34a7-115"><dt>**COPP\_ProtectionType\_CGMSA**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="f34a7-116">Аналоговая система управления копиями (CGMS-A).</span><span class="sxs-lookup"><span data-stu-id="f34a7-116">Copy Generation Management System   Analog (CGMS-A).</span></span><br/> |
| <span id="COPP_ProtectionType_Mask"></span><span id="copp_protectiontype_mask"></span><span id="COPP_PROTECTIONTYPE_MASK"></span><dl> <span data-ttu-id="f34a7-117"><dt>**Копп \_ 0x80000007 \_ Mask ProtectionType**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f34a7-117"><dt>**COPP\_ProtectionType\_Mask**</dt> <dt>0x80000007</dt></span></span> </dl>                 | <span data-ttu-id="f34a7-118">Битовая маска для изоляции допустимых флагов.</span><span class="sxs-lookup"><span data-stu-id="f34a7-118">Bitmask to isolate valid flags.</span></span><br/>                      |
| <span id="COPP_ProtectionType_Reserved"></span><span id="copp_protectiontype_reserved"></span><span id="COPP_PROTECTIONTYPE_RESERVED"></span><dl> <span data-ttu-id="f34a7-119"><dt>**Копп \_ ProtectionType \_ зарезервированный**</dt> <dt>0x7FFFFFF8</dt></span><span class="sxs-lookup"><span data-stu-id="f34a7-119"><dt>**COPP\_ProtectionType\_Reserved**</dt> <dt>0x7FFFFFF8</dt></span></span> </dl> | <span data-ttu-id="f34a7-120">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="f34a7-120">Reserved.</span></span> <span data-ttu-id="f34a7-121">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="f34a7-121">Must be zero.</span></span><br/>                              |



## <a name="remarks"></a><span data-ttu-id="f34a7-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f34a7-122">Remarks</span></span>

<span data-ttu-id="f34a7-123">Некоторые методы возвращают один флаг из этого типа перечисления, а некоторые методы возвращают побитовую операцию **или** для одного или нескольких флагов.</span><span class="sxs-lookup"><span data-stu-id="f34a7-123">Some methods return a single flag from this enumeration type, and some methods return a bitwise **OR** of one or more flags.</span></span>

<span data-ttu-id="f34a7-124">Эти флаги используются в следующих запросах и командах Копп.</span><span class="sxs-lookup"><span data-stu-id="f34a7-124">These flags are used in the following COPP queries and commands.</span></span>

-   <span data-ttu-id="f34a7-125">Глобальный уровень защиты</span><span class="sxs-lookup"><span data-stu-id="f34a7-125">Global Protection Level</span></span>
-   <span data-ttu-id="f34a7-126">Локальный уровень защиты</span><span class="sxs-lookup"><span data-stu-id="f34a7-126">Local Protection Level</span></span>
-   <span data-ttu-id="f34a7-127">Тип защиты</span><span class="sxs-lookup"><span data-stu-id="f34a7-127">Protection Type</span></span>
-   <span data-ttu-id="f34a7-128">Задать уровень защиты</span><span class="sxs-lookup"><span data-stu-id="f34a7-128">Set Protection Level</span></span>

## <a name="requirements"></a><span data-ttu-id="f34a7-129">Требования</span><span class="sxs-lookup"><span data-stu-id="f34a7-129">Requirements</span></span>



| <span data-ttu-id="f34a7-130">Требование</span><span class="sxs-lookup"><span data-stu-id="f34a7-130">Requirement</span></span> | <span data-ttu-id="f34a7-131">Значение</span><span class="sxs-lookup"><span data-stu-id="f34a7-131">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f34a7-132">Header</span><span class="sxs-lookup"><span data-stu-id="f34a7-132">Header</span></span><br/> | <dl> <span data-ttu-id="f34a7-133"><dt>Дксва. h</dt></span><span class="sxs-lookup"><span data-stu-id="f34a7-133"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f34a7-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f34a7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f34a7-135">Константы и идентификаторы GUID</span><span class="sxs-lookup"><span data-stu-id="f34a7-135">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="f34a7-136">Использование протокола сертифицированной выходной защиты (Копп)</span><span class="sxs-lookup"><span data-stu-id="f34a7-136">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




