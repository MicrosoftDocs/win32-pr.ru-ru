---
title: Типы переменных SNMP и запросы типов PDU
description: Определения некоторых типов переменных SNMP и типов PDU запросов изменились. Файл SNMP. h сопоставляет старые типы с соответствующими новыми типами.
ms.assetid: 2d87aeee-6fcb-4837-b091-6a9def8a9acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d656add1b177b50e24b30a11d9fe008dcdfdf9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792865"
---
# <a name="snmp-variable-types-and-request-pdu-types"></a><span data-ttu-id="6c7ab-104">Типы переменных SNMP и запросы типов PDU</span><span class="sxs-lookup"><span data-stu-id="6c7ab-104">SNMP Variable Types and Request PDU Types</span></span>

<span data-ttu-id="6c7ab-105">\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="6c7ab-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6c7ab-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="6c7ab-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6c7ab-107">Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="6c7ab-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="6c7ab-108">Определения некоторых типов переменных SNMP и типов PDU запросов изменились.</span><span class="sxs-lookup"><span data-stu-id="6c7ab-108">The definitions for some SNMP variable types and request PDU types have changed.</span></span> <span data-ttu-id="6c7ab-109">Файл SNMP. h сопоставляет старые типы с соответствующими новыми типами.</span><span class="sxs-lookup"><span data-stu-id="6c7ab-109">The Snmp.h file maps old types to the corresponding new types.</span></span>

## <a name="modified-snmp-variable-types"></a><span data-ttu-id="6c7ab-110">Измененные типы переменных SNMP</span><span class="sxs-lookup"><span data-stu-id="6c7ab-110">Modified SNMP Variable Types</span></span>

<span data-ttu-id="6c7ab-111">При разработке приложений Manager, использующих API управления Microsoft SNMP, следует использовать новые типы переменных SNMP, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6c7ab-111">You should use the new SNMP variable types listed in the following table when you develop manager applications that use the Microsoft SNMP Management API.</span></span> <span data-ttu-id="6c7ab-112">В таблице перечислены старые типы переменных SNMP с соответствующими новыми типами переменных.</span><span class="sxs-lookup"><span data-stu-id="6c7ab-112">The table lists the old SNMP variable types with the corresponding new variable types.</span></span>

| <span data-ttu-id="6c7ab-113">Старый тип переменной</span><span class="sxs-lookup"><span data-stu-id="6c7ab-113">Old variable type</span></span>        | <span data-ttu-id="6c7ab-114">Новый тип переменной</span><span class="sxs-lookup"><span data-stu-id="6c7ab-114">New variable type</span></span> |
|--------------------------|-------------------|
| <span data-ttu-id="6c7ab-115">ASN \_ RFC1155 \_ IPAddress</span><span class="sxs-lookup"><span data-stu-id="6c7ab-115">ASN\_RFC1155\_IPADDRESS</span></span>  | <span data-ttu-id="6c7ab-116">ASN \_ IPAddress</span><span class="sxs-lookup"><span data-stu-id="6c7ab-116">ASN\_IPADDRESS</span></span>    |
| <span data-ttu-id="6c7ab-117">\_Счетчик ASN RFC1155 \_</span><span class="sxs-lookup"><span data-stu-id="6c7ab-117">ASN\_RFC1155\_COUNTER</span></span>    | <span data-ttu-id="6c7ab-118">ASN \_ COUNTER32</span><span class="sxs-lookup"><span data-stu-id="6c7ab-118">ASN\_COUNTER32</span></span>    |
| <span data-ttu-id="6c7ab-119">\_Датчик RFC1155 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="6c7ab-119">ASN\_RFC1155\_GAUGE</span></span>      | <span data-ttu-id="6c7ab-120">ASN \_ значение Gauge32</span><span class="sxs-lookup"><span data-stu-id="6c7ab-120">ASN\_GAUGE32</span></span>      |
| <span data-ttu-id="6c7ab-121">ASN \_ RFC1155 \_ значение TIMETICKS</span><span class="sxs-lookup"><span data-stu-id="6c7ab-121">ASN\_RFC1155\_TIMETICKS</span></span>  | <span data-ttu-id="6c7ab-122">ASN \_ значение TIMETICKS</span><span class="sxs-lookup"><span data-stu-id="6c7ab-122">ASN\_TIMETICKS</span></span>    |
| <span data-ttu-id="6c7ab-123">ASN \_ RFC1155 \_ непрозрачный</span><span class="sxs-lookup"><span data-stu-id="6c7ab-123">ASN\_RFC1155\_OPAQUE</span></span>     | <span data-ttu-id="6c7ab-124">непрозрачный ASN \_</span><span class="sxs-lookup"><span data-stu-id="6c7ab-124">ASN\_OPAQUE</span></span>       |
| <span data-ttu-id="6c7ab-125">ASN \_ RFC1213 \_ диспстринг</span><span class="sxs-lookup"><span data-stu-id="6c7ab-125">ASN\_RFC1213\_DISPSTRING</span></span> | <span data-ttu-id="6c7ab-126">ASN \_ октетстринг</span><span class="sxs-lookup"><span data-stu-id="6c7ab-126">ASN\_OCTETSTRING</span></span>  |



 

## <a name="modified-snmp-pdu-request-types"></a><span data-ttu-id="6c7ab-127">Измененные типы запросов PDU SNMP</span><span class="sxs-lookup"><span data-stu-id="6c7ab-127">Modified SNMP PDU Request Types</span></span>

<span data-ttu-id="6c7ab-128">При разработке приложений диспетчера, использующих API управления Microsoft SNMP, следует использовать новые типы PDU SNMP, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6c7ab-128">You should use the new SNMP PDU types listed in the following table when you develop manager applications that use the Microsoft SNMP Management API.</span></span> <span data-ttu-id="6c7ab-129">В таблице перечислены старые типы PDU SNMP с соответствующими новыми типами PDU.</span><span class="sxs-lookup"><span data-stu-id="6c7ab-129">The table lists the old SNMP PDU types with the corresponding new PDU types.</span></span>

| <span data-ttu-id="6c7ab-130">Старый тип PDU</span><span class="sxs-lookup"><span data-stu-id="6c7ab-130">Old PDU type</span></span>                 | <span data-ttu-id="6c7ab-131">Новый тип PDU</span><span class="sxs-lookup"><span data-stu-id="6c7ab-131">New PDU type</span></span>        |
|------------------------------|---------------------|
| <span data-ttu-id="6c7ab-132">\_Запрос ASN RFC1157 \_</span><span class="sxs-lookup"><span data-stu-id="6c7ab-132">ASN\_RFC1157\_GETREQUEST</span></span>     | <span data-ttu-id="6c7ab-133">\_Получение PDU \_ SNMP</span><span class="sxs-lookup"><span data-stu-id="6c7ab-133">SNMP\_PDU\_GET</span></span>      |
| <span data-ttu-id="6c7ab-134">ASN \_ RFC1157 \_ жетнекстрекуест</span><span class="sxs-lookup"><span data-stu-id="6c7ab-134">ASN\_RFC1157\_GETNEXTREQUEST</span></span> | <span data-ttu-id="6c7ab-135">SNMP- \_ PDU- \_ следующее</span><span class="sxs-lookup"><span data-stu-id="6c7ab-135">SNMP\_PDU\_GETNEXT</span></span>  |
| <span data-ttu-id="6c7ab-136">ASN \_ RFC1157 \_ GetResponse</span><span class="sxs-lookup"><span data-stu-id="6c7ab-136">ASN\_RFC1157\_GETRESPONSE</span></span>    | <span data-ttu-id="6c7ab-137">отклик SNMP- \_ PDU \_</span><span class="sxs-lookup"><span data-stu-id="6c7ab-137">SNMP\_PDU\_RESPONSE</span></span> |
| <span data-ttu-id="6c7ab-138">ASN \_ RFC1157 \_ сетрекуест</span><span class="sxs-lookup"><span data-stu-id="6c7ab-138">ASN\_RFC1157\_SETREQUEST</span></span>     | <span data-ttu-id="6c7ab-139">\_набор PDU \_ SNMP</span><span class="sxs-lookup"><span data-stu-id="6c7ab-139">SNMP\_PDU\_SET</span></span>      |
| <span data-ttu-id="6c7ab-140">\_ \_ Ловушка RFC1157 ASN</span><span class="sxs-lookup"><span data-stu-id="6c7ab-140">ASN\_RFC1157\_TRAP</span></span>           | <span data-ttu-id="6c7ab-141">\_V1TRAP PDU \_ SNMP</span><span class="sxs-lookup"><span data-stu-id="6c7ab-141">SNMP\_PDU\_V1TRAP</span></span>   |



 

 

 