---
title: Структура WinSNMP
description: Функции WinSNMP API используют следующие структуры.
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- WinSNMP-структуры SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b263f6078171c096eb7208ae4c7ef29847aead9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890840"
---
# <a name="winsnmp-structures"></a><span data-ttu-id="e3787-104">Структура WinSNMP</span><span class="sxs-lookup"><span data-stu-id="e3787-104">WinSNMP Structures</span></span>

<span data-ttu-id="e3787-105">\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="e3787-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e3787-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="e3787-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e3787-107">Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="e3787-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="e3787-108">Функции WinSNMP API используют следующие структуры.</span><span class="sxs-lookup"><span data-stu-id="e3787-108">The WinSNMP API functions use the following structures.</span></span>



| <span data-ttu-id="e3787-109">Структура</span><span class="sxs-lookup"><span data-stu-id="e3787-109">Structure</span></span>                                  | <span data-ttu-id="e3787-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e3787-110">Description</span></span>                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3787-111">**smiCNTR64**</span><span class="sxs-lookup"><span data-stu-id="e3787-111">**smiCNTR64**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | <span data-ttu-id="e3787-112">Содержит 64-битовое целочисленное значение без знака, представляющее счетчик.</span><span class="sxs-lookup"><span data-stu-id="e3787-112">Contains a 64-bit unsigned integer value that represents a counter.</span></span>                                                    |
| [<span data-ttu-id="e3787-113">**смиоктетс**</span><span class="sxs-lookup"><span data-stu-id="e3787-113">**smiOCTETS**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | <span data-ttu-id="e3787-114">Содержит указатель на строку октета SNMP с переменной длиной.</span><span class="sxs-lookup"><span data-stu-id="e3787-114">Contains a pointer to an SNMP octet string of variable length.</span></span>                                                         |
| [<span data-ttu-id="e3787-115">**смиоид**</span><span class="sxs-lookup"><span data-stu-id="e3787-115">**smiOID**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | <span data-ttu-id="e3787-116">Содержит указатель на массив переменной длины субидентификаторов, связанных с указанным именованным объектом.</span><span class="sxs-lookup"><span data-stu-id="e3787-116">Contains a pointer to a variable length array of the subidentifiers that are associated with a specified named object.</span></span> |
| [<span data-ttu-id="e3787-117">**смивалуе**</span><span class="sxs-lookup"><span data-stu-id="e3787-117">**smiVALUE**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | <span data-ttu-id="e3787-118">Представляет значение, связанное с именем переменной в записи привязки переменной.</span><span class="sxs-lookup"><span data-stu-id="e3787-118">Represents the value that is associated with a variable name in a variable binding entry.</span></span>                              |
| [<span data-ttu-id="e3787-119">**смивендоринфо**</span><span class="sxs-lookup"><span data-stu-id="e3787-119">**smiVENDORINFO**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | <span data-ttu-id="e3787-120">Содержит сведения о реализации WinSNMP в Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e3787-120">Contains information about the Microsoft implementation of WinSNMP.</span></span>                                                    |



 

 

 