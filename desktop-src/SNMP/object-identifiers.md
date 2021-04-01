---
title: Идентификаторы объектов (SNMP)
description: Идентификатор SNMP-объекта уникальным образом именует объект и определяет его расположение в древовидной структуре управляющей базы данных (MIB).
ms.assetid: b4552185-ef37-4e04-9b19-a226165e0b32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed1f54f67b85000e508dddb42b9c784628a53ab
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800647"
---
# <a name="object-identifiers-snmp"></a><span data-ttu-id="9c17a-103">Идентификаторы объектов (SNMP)</span><span class="sxs-lookup"><span data-stu-id="9c17a-103">Object Identifiers (SNMP)</span></span>

<span data-ttu-id="9c17a-104">Идентификатор SNMP-объекта уникальным образом именует объект и определяет его расположение в древовидной структуре управляющей базы данных (MIB).</span><span class="sxs-lookup"><span data-stu-id="9c17a-104">An SNMP object identifier uniquely names an object and identifies its location within a Management Information Base (MIB) tree structure.</span></span> <span data-ttu-id="9c17a-105">Идентификаторы объектов — это не зависящие от приложения синтаксические нотации одного (ASN. 1) типов данных, состоящие из последовательности неотрицательных целых чисел или субидентификаторов.</span><span class="sxs-lookup"><span data-stu-id="9c17a-105">Object identifiers are application-independent Abstract Syntax Notation One (ASN.1) data types that consist of a sequence of non-negative integers, or subidentifiers.</span></span> <span data-ttu-id="9c17a-106">Идентификаторы объектов должны иметь как минимум два подидентификатора и не должны превышать 128 подидентификаторов.</span><span class="sxs-lookup"><span data-stu-id="9c17a-106">Object identifiers must have a minimum of two subidentifiers and they must not exceed 128 subidentifiers.</span></span>

<span data-ttu-id="9c17a-107">В среде программирования WinSNMP используется структура [**смиоид**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) для управления идентификаторами объектов.</span><span class="sxs-lookup"><span data-stu-id="9c17a-107">The WinSNMP programming environment uses the [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure to manage object identifiers.</span></span> <span data-ttu-id="9c17a-108">Формат массива идентификаторов объектов в структуре **смиоид** является одним подидентификатором для каждого элемента массива.</span><span class="sxs-lookup"><span data-stu-id="9c17a-108">The format of the object identifier array in an **smiOID** structure is one subidentifier per array element.</span></span>

<span data-ttu-id="9c17a-109">Строковое представление числового значения идентификатора объекта разделяет его вложенные идентификаторы точками. Например, "1.2.3.4.5.6".</span><span class="sxs-lookup"><span data-stu-id="9c17a-109">The dotted numeric string representation of an object identifier separates its subidentifiers with periods; for example, "1.2.3.4.5.6".</span></span>

<span data-ttu-id="9c17a-110">Дополнительные сведения см. [в статье база данных SNMP Management Base (MIB)](the-snmp-management-information-base-mib-.md) и соответствующие RFC.</span><span class="sxs-lookup"><span data-stu-id="9c17a-110">For more information, see [The SNMP Management Information Base (MIB)](the-snmp-management-information-base-mib-.md) and the relevant RFCs.</span></span>

 

 




