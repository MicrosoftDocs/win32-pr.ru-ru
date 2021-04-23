---
title: Коды ошибок WinSNMP
description: Коды ошибок WinSNMP
ms.assetid: 03b13b82-a31c-47e2-8b4d-17dcc4d19e56
keywords:
- Коды ошибок WinSNMP SNMP
- Коды ошибок SNMP, WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d3cff7bd1e534f5f9c1fb0ae2ea2687d2ba99a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488145"
---
# <a name="winsnmp-error-codes"></a><span data-ttu-id="9ec74-105">Коды ошибок WinSNMP</span><span class="sxs-lookup"><span data-stu-id="9ec74-105">WinSNMP Error Codes</span></span>

<span data-ttu-id="9ec74-106">\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="9ec74-106">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9ec74-107">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="9ec74-107">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="9ec74-108">Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="9ec74-108">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

> [!Note]  
> <span data-ttu-id="9ec74-109">Ошибки, описанные в этом разделе, отличаются от кодов ошибок SNMP, определенных соответствующими RFC.</span><span class="sxs-lookup"><span data-stu-id="9ec74-109">The errors described in this topic are distinct from the SNMP error codes defined by the relevant RFCs.</span></span>

 

<span data-ttu-id="9ec74-110">Все функции WinSNMP возвращают значение **снмпапи \_** в случае сбоя функции.</span><span class="sxs-lookup"><span data-stu-id="9ec74-110">All WinSNMP functions return the value **SNMPAPI\_FAILURE** if the function fails.</span></span> <span data-ttu-id="9ec74-111">Чтобы получить расширенные сведения об ошибке при сбое функции WinSNMP, приложение WinSNMP должно немедленно вызвать функцию [**снмпжетластеррор**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) .</span><span class="sxs-lookup"><span data-stu-id="9ec74-111">The WinSNMP application must immediately call the [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) function to retrieve extended error information when a WinSNMP function fails.</span></span> <span data-ttu-id="9ec74-112">В следующей таблице перечислены разделы, в которых обсуждаются коды расширенных ошибок, возвращаемые функциями WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="9ec74-112">The following table lists topics that discuss extended error codes returned by WinSNMP functions.</span></span>



| <span data-ttu-id="9ec74-113">Раздел</span><span class="sxs-lookup"><span data-stu-id="9ec74-113">Topic</span></span>                                                        | <span data-ttu-id="9ec74-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9ec74-114">Description</span></span>                                             |
|--------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="9ec74-115">Общие коды ошибок WinSNMP</span><span class="sxs-lookup"><span data-stu-id="9ec74-115">WinSNMP Common Error Codes</span></span>](winsnmp-common-error-codes.md) | <span data-ttu-id="9ec74-116">Описывает распространенные коды ошибок для API WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="9ec74-116">Describes common error codes for the WinSNMP API.</span></span>       |
| [<span data-ttu-id="9ec74-117">Ошибки сетевого транспорта</span><span class="sxs-lookup"><span data-stu-id="9ec74-117">Network Transport Errors</span></span>](network-transport-errors.md)     | <span data-ttu-id="9ec74-118">Описание ошибок сетевого транспорта для API WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="9ec74-118">Describes network transport errors for the WinSNMP API.</span></span> |



 

<span data-ttu-id="9ec74-119">Ошибки WinSNMP, которые содержат сведения, относящиеся к контексту, содержатся на странице справки по функциям.</span><span class="sxs-lookup"><span data-stu-id="9ec74-119">The WinSNMP errors that convey context-specific information are included in the function reference page.</span></span>

 

 