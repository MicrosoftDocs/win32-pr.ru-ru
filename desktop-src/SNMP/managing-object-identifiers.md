---
title: Управление идентификаторами объектов
description: API-интерфейс WinSNMP предоставляет несколько служебных функций WinSNMP, упрощающих обработку идентификаторов объектов для WinSNMP Applications.
ms.assetid: 6ca5f5bc-aa49-4826-97a7-2ea4a882dc2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9745cb8018b6833a1ef0569e69f201c621aa38e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486984"
---
# <a name="managing-object-identifiers"></a><span data-ttu-id="4e085-103">Управление идентификаторами объектов</span><span class="sxs-lookup"><span data-stu-id="4e085-103">Managing Object Identifiers</span></span>

<span data-ttu-id="4e085-104">API-интерфейс WinSNMP предоставляет несколько [служебных функций WinSNMP](winsnmp-functions.md) , упрощающих обработку идентификаторов объектов для WinSNMP Applications.</span><span class="sxs-lookup"><span data-stu-id="4e085-104">The WinSNMP API provides several [WinSNMP utility functions](winsnmp-functions.md) that simplify the manipulation of object identifiers for WinSNMP applications.</span></span>

<span data-ttu-id="4e085-105">Функция [**снмпоидтостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) преобразует внутреннее двоичное представление идентификатора объекта в формат числовой строки с точками.</span><span class="sxs-lookup"><span data-stu-id="4e085-105">The [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) function converts the internal binary representation of an object identifier to its dotted numeric string format.</span></span> <span data-ttu-id="4e085-106">При вызове [**снмпоидтостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)укажите БУФЕР строки максобжидстрсизе length (1408 байт), чтобы размер выходного буфера был достаточно большим, чтобы вместить преобразованную строку.</span><span class="sxs-lookup"><span data-stu-id="4e085-106">When you call [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr), specify a string buffer of MAXOBJIDSTRSIZE length (1408 bytes) to ensure that the output buffer is large enough to hold the converted string.</span></span> <span data-ttu-id="4e085-107">Чтобы преобразовать идентификатор объекта из числового формата, разделенного точками, во внутреннее двоичное представление, вызовите функцию [**снмпстртуид**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) .</span><span class="sxs-lookup"><span data-stu-id="4e085-107">To convert an object identifier from the dotted numeric string format to its internal binary representation, call the [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) function.</span></span>

<span data-ttu-id="4e085-108">Чтобы скопировать идентификатор объекта SNMP, вызовите функцию [**снмпоидкопи**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) .</span><span class="sxs-lookup"><span data-stu-id="4e085-108">To copy an SNMP object identifier call the [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) function.</span></span> <span data-ttu-id="4e085-109">Эта функция выделяет необходимую память для нового идентификатора объекта.</span><span class="sxs-lookup"><span data-stu-id="4e085-109">This function allocates any necessary memory for the new object identifier.</span></span>

<span data-ttu-id="4e085-110">Для освобождения ресурсов, выделенных для элемента **ptr** структуры [**смиоид**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) , заданной в функциях [**Снмпстртуид**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) и [**Снмпоидкопи**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) , приложение WinSNMP должно вызывать функцию [**снмпфридескриптор**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) .</span><span class="sxs-lookup"><span data-stu-id="4e085-110">A WinSNMP application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to free resources allocated for the **ptr** member of the [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure specified by both the [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) and the [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) functions.</span></span>

<span data-ttu-id="4e085-111">Функция [**снмпоидкомпаре**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) сравнивает два идентификатора объектов SNMP.</span><span class="sxs-lookup"><span data-stu-id="4e085-111">The [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) function compares two SNMP object identifiers.</span></span> <span data-ttu-id="4e085-112">В приложении WinSNMP можно указать количество подидентификаторов для сравнения.</span><span class="sxs-lookup"><span data-stu-id="4e085-112">The WinSNMP application can specify the number of subidentifiers to compare.</span></span> <span data-ttu-id="4e085-113">Вызовите **снмпоидкомпаре** , чтобы определить, имеют ли два идентификатора объектов общие префиксы.</span><span class="sxs-lookup"><span data-stu-id="4e085-113">Call **SnmpOidCompare** to determine whether two object identifiers have common prefixes.</span></span>

<span data-ttu-id="4e085-114">Дополнительные сведения об управлении памятью, выделенной для идентификаторов объектов, см. в разделе [выделение объектов WinSNMP Memory](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4e085-114">For additional information about managing the memory allocated for object identifiers, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




