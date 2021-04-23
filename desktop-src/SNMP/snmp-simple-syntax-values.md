---
title: Простые синтаксические значения SNMP (SNMP. h)
description: Простые значения синтаксиса SNMP используются для указания типа переменной SNMP.
ms.assetid: 42b681e5-721d-4d41-bc1a-c9f0005cde87
topic_type:
- apiref
api_name:
- ASN_INTEGER
- ASN_BITS
- ASN_OCTETSTRING
- ASN_NULL
- ASN_OBJECTIDENTIFIER
- ASN_INTEGER32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee6a40b4f63b7ce701b8232b310b2f73bac42d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136362"
---
# <a name="snmp-simple-syntax-values"></a><span data-ttu-id="7b6f6-103">Простые синтаксические значения SNMP</span><span class="sxs-lookup"><span data-stu-id="7b6f6-103">SNMP Simple Syntax Values</span></span>

<span data-ttu-id="7b6f6-104">\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="7b6f6-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7b6f6-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="7b6f6-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7b6f6-106">Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="7b6f6-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="7b6f6-107">Простые значения синтаксиса SNMP используются для указания типа переменной SNMP.</span><span class="sxs-lookup"><span data-stu-id="7b6f6-107">The SNMP Simple Syntax Values are used to indicate an SNMP variable type.</span></span>



| <span data-ttu-id="7b6f6-108">Константа</span><span class="sxs-lookup"><span data-stu-id="7b6f6-108">Constant</span></span>                                                                                                                                                                           | <span data-ttu-id="7b6f6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7b6f6-109">Description</span></span>                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="ASN_INTEGER"></span><span id="asn_integer"></span><dl> <span data-ttu-id="7b6f6-110"><dt>**ASN, \_ целое**</dt></span><span class="sxs-lookup"><span data-stu-id="7b6f6-110"><dt>**ASN\_INTEGER**</dt></span></span> </dl>                            | <span data-ttu-id="7b6f6-111">Указывает переменную с 32-битным целым числом со знаком.</span><span class="sxs-lookup"><span data-stu-id="7b6f6-111">Indicates a 32-bit signed integer variable.</span></span><br/>                |
| <span id="ASN_BITS"></span><span id="asn_bits"></span><dl> <span data-ttu-id="7b6f6-112"><dt>**\_биты ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="7b6f6-112"><dt>**ASN\_BITS**</dt></span></span> </dl>                                     | <span data-ttu-id="7b6f6-113">Указывает переменную, которая является перечислением именованных битов.</span><span class="sxs-lookup"><span data-stu-id="7b6f6-113">Indicates a variable that is an enumeration of named bits.</span></span><br/> |
| <span id="ASN_OCTETSTRING"></span><span id="asn_octetstring"></span><dl> <span data-ttu-id="7b6f6-114"><dt>**ASN \_ октетстринг**</dt></span><span class="sxs-lookup"><span data-stu-id="7b6f6-114"><dt>**ASN\_OCTETSTRING**</dt></span></span> </dl>                | <span data-ttu-id="7b6f6-115">Указывает переменную строки октета.</span><span class="sxs-lookup"><span data-stu-id="7b6f6-115">Indicates an octet string variable.</span></span><br/>                        |
| <span id="ASN_NULL"></span><span id="asn_null"></span><dl> <span data-ttu-id="7b6f6-116"><dt>**ASN \_ null**</dt></span><span class="sxs-lookup"><span data-stu-id="7b6f6-116"><dt>**ASN\_NULL**</dt></span></span> </dl>                                     | <span data-ttu-id="7b6f6-117">Указывает значение **null** .</span><span class="sxs-lookup"><span data-stu-id="7b6f6-117">Indicates a **NULL** value.</span></span><br/>                                |
| <span id="ASN_OBJECTIDENTIFIER"></span><span id="asn_objectidentifier"></span><dl> <span data-ttu-id="7b6f6-118"><dt>**ASN \_ OBJECTIDENTIFIER**</dt></span><span class="sxs-lookup"><span data-stu-id="7b6f6-118"><dt>**ASN\_OBJECTIDENTIFIER**</dt></span></span> </dl> | <span data-ttu-id="7b6f6-119">Указывает переменную идентификатора объекта.</span><span class="sxs-lookup"><span data-stu-id="7b6f6-119">Indicates an object identifier variable.</span></span><br/>                   |
| <span id="ASN_INTEGER32"></span><span id="asn_integer32"></span><dl> <span data-ttu-id="7b6f6-120"><dt>**ASN \_ INTEGER32**</dt></span><span class="sxs-lookup"><span data-stu-id="7b6f6-120"><dt>**ASN\_INTEGER32**</dt></span></span> </dl>                      | <span data-ttu-id="7b6f6-121">Указывает значение 32-битового целого числа со знаком.</span><span class="sxs-lookup"><span data-stu-id="7b6f6-121">Indicates a 32-bit signed integer value.</span></span><br/>                   |



## <a name="requirements"></a><span data-ttu-id="7b6f6-122">Требования</span><span class="sxs-lookup"><span data-stu-id="7b6f6-122">Requirements</span></span>



| <span data-ttu-id="7b6f6-123">Требование</span><span class="sxs-lookup"><span data-stu-id="7b6f6-123">Requirement</span></span> | <span data-ttu-id="7b6f6-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7b6f6-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7b6f6-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b6f6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7b6f6-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7b6f6-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="7b6f6-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b6f6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7b6f6-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7b6f6-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7b6f6-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7b6f6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b6f6-130"><dt>Протокол SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b6f6-130"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b6f6-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b6f6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b6f6-132">Обзор протокола SNMP</span><span class="sxs-lookup"><span data-stu-id="7b6f6-132">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="7b6f6-133">Справочник по SNMP</span><span class="sxs-lookup"><span data-stu-id="7b6f6-133">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="7b6f6-134">Константы SNMP</span><span class="sxs-lookup"><span data-stu-id="7b6f6-134">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

