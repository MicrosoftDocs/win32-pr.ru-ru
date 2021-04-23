---
title: Типы данных WinSNMP
description: Стандартные типы данных WinSNMP определяются в WINSNMP. H файл.
ms.assetid: 20f1bbc3-5a08-4206-980d-22a794cda402
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7061ade6f9b69c63ba4718d9d79bbd4d39c67b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070499"
---
# <a name="winsnmp-data-types"></a><span data-ttu-id="69a9d-103">Типы данных WinSNMP</span><span class="sxs-lookup"><span data-stu-id="69a9d-103">WinSNMP Data Types</span></span>

<span data-ttu-id="69a9d-104">\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="69a9d-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="69a9d-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="69a9d-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="69a9d-106">Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="69a9d-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="69a9d-107">Стандартные типы данных WinSNMP определяются в WINSNMP. H файл.</span><span class="sxs-lookup"><span data-stu-id="69a9d-107">The standard WinSNMP data types are defined in the WINSNMP.H file.</span></span>

<span data-ttu-id="69a9d-108">Обратите внимание, что параметру WinSNMP указываются некоторые параметры с типом длинного целого числа со знаком **смиинт**.</span><span class="sxs-lookup"><span data-stu-id="69a9d-108">Note that WinSNMP specifies some parameters with the signed long integer type, **smiINT**.</span></span> <span data-ttu-id="69a9d-109">Это позволяет параметру WinSNMP соответствовать элементам данных, особенно компонентам PDU, определенным в соответствующих документах RFC.</span><span class="sxs-lookup"><span data-stu-id="69a9d-109">This enables WinSNMP to comply with the data elements, especially the PDU components, defined in the relevant RFCs.</span></span>

 

 