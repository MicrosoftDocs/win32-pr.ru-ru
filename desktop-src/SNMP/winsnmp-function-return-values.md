---
title: Возвращаемые значения функции WinSNMP
description: Возвращаемое значение вызова функции WinSNMP может быть маркером для ресурса, который выделяется реализацией Microsoft WinSNMP для приложения WinSNMP.
ms.assetid: f0723cc7-fa3b-4a72-93a0-49d40a1fedd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a8e42e7d27b1079398efb2970b385bfc4e732c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070498"
---
# <a name="winsnmp-function-return-values"></a><span data-ttu-id="ac9f4-103">Возвращаемые значения функции WinSNMP</span><span class="sxs-lookup"><span data-stu-id="ac9f4-103">WinSNMP Function Return Values</span></span>

<span data-ttu-id="ac9f4-104">\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="ac9f4-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ac9f4-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="ac9f4-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="ac9f4-106">Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="ac9f4-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="ac9f4-107">Возвращаемое значение вызова функции WinSNMP может быть маркером для ресурса, который выделяется реализацией Microsoft WinSNMP для приложения WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="ac9f4-107">The return value from a WinSNMP function call can be a handle to a resource that the Microsoft WinSNMP implementation allocates for the WinSNMP application.</span></span>

<span data-ttu-id="ac9f4-108">В следующей таблице перечислены пять типов дескрипторов ресурсов, которые выделяет реализация.</span><span class="sxs-lookup"><span data-stu-id="ac9f4-108">The following table lists the five types of resource handles that the implementation allocates.</span></span>



| <span data-ttu-id="ac9f4-109">Тип обработчика</span><span class="sxs-lookup"><span data-stu-id="ac9f4-109">Handle type</span></span>    | <span data-ttu-id="ac9f4-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ac9f4-110">Description</span></span>                       |
|----------------|-----------------------------------|
| <span data-ttu-id="ac9f4-111">\_сеанс хснмп</span><span class="sxs-lookup"><span data-stu-id="ac9f4-111">HSNMP\_SESSION</span></span> | <span data-ttu-id="ac9f4-112">Обработчик для сеанса WinSNMP</span><span class="sxs-lookup"><span data-stu-id="ac9f4-112">Handle to a WinSNMP session</span></span>       |
| <span data-ttu-id="ac9f4-113">\_сущность хснмп</span><span class="sxs-lookup"><span data-stu-id="ac9f4-113">HSNMP\_ENTITY</span></span>  | <span data-ttu-id="ac9f4-114">Обработчик для объекта SNMP</span><span class="sxs-lookup"><span data-stu-id="ac9f4-114">Handle to an SNMP entity</span></span>          |
| <span data-ttu-id="ac9f4-115">\_контекст хснмп</span><span class="sxs-lookup"><span data-stu-id="ac9f4-115">HSNMP\_CONTEXT</span></span> | <span data-ttu-id="ac9f4-116">Обработчик контекста SNMP</span><span class="sxs-lookup"><span data-stu-id="ac9f4-116">Handle to an SNMP context</span></span>         |
| <span data-ttu-id="ac9f4-117">ХСНМП \_ PDU</span><span class="sxs-lookup"><span data-stu-id="ac9f4-117">HSNMP\_PDU</span></span>     | <span data-ttu-id="ac9f4-118">Обработчик для единицы данных протокола</span><span class="sxs-lookup"><span data-stu-id="ac9f4-118">Handle to a protocol data unit</span></span>    |
| <span data-ttu-id="ac9f4-119">ХСНМП \_ вбл</span><span class="sxs-lookup"><span data-stu-id="ac9f4-119">HSNMP\_VBL</span></span>     | <span data-ttu-id="ac9f4-120">Handle в список привязок переменных</span><span class="sxs-lookup"><span data-stu-id="ac9f4-120">Handle to a variable binding list</span></span> |



 

<span data-ttu-id="ac9f4-121">Дополнительные сведения см. в разделе [объекты обработчика ресурсов](resource-handle-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ac9f4-121">For more information, see [Resource Handle Objects](resource-handle-objects.md).</span></span>

<span data-ttu-id="ac9f4-122">Возвращаемое значение также может быть целочисленным значением без знака типа **smiUINT32** , представляющим \_ значение состояния снмпапи.</span><span class="sxs-lookup"><span data-stu-id="ac9f4-122">The return value can also be an unsigned long integer value of the **smiUINT32** type that represents an SNMPAPI\_STATUS value.</span></span>

<span data-ttu-id="ac9f4-123">В следующей таблице перечислены значения состояния WinSNMP и их значение.</span><span class="sxs-lookup"><span data-stu-id="ac9f4-123">The following table lists the WinSNMP status values and their meaning.</span></span>



| <span data-ttu-id="ac9f4-124">Состояние</span><span class="sxs-lookup"><span data-stu-id="ac9f4-124">Status</span></span>           | <span data-ttu-id="ac9f4-125">Описание</span><span class="sxs-lookup"><span data-stu-id="ac9f4-125">Description</span></span>                                                                      |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ac9f4-126">\_сбой снмпапи</span><span class="sxs-lookup"><span data-stu-id="ac9f4-126">SNMPAPI\_FAILURE</span></span> | <span data-ttu-id="ac9f4-127">Указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="ac9f4-127">Indicates an error.</span></span> <span data-ttu-id="ac9f4-128">Эквивалентно 0 или **null**.</span><span class="sxs-lookup"><span data-stu-id="ac9f4-128">Equates to 0 or **NULL**.</span></span>                                    |
| <span data-ttu-id="ac9f4-129">СНМПАПИ \_ успешно</span><span class="sxs-lookup"><span data-stu-id="ac9f4-129">SNMPAPI\_SUCCESS</span></span> | <span data-ttu-id="ac9f4-130">Указывает, что функция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="ac9f4-130">Indicates the function completed successfully.</span></span> <span data-ttu-id="ac9f4-131">Эквивалентно 1 или положительному числу.</span><span class="sxs-lookup"><span data-stu-id="ac9f4-131">Equates to 1 or a positive count.</span></span> |



 

 

 