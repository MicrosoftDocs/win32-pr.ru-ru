---
description: Поставщик SNMP использует следующие квалификаторы класса CIM при сопоставлении определений объектов MIB с определениями классов CIM.
ms.assetid: 458167dc-562e-47b8-8760-797ae13f9459
ms.tgt_platform: multiple
title: Квалификаторы класса CIM для объектов MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60fe97debc7fd81b48a6daf0f5a955374546458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266226"
---
# <a name="cim-class-qualifiers-for-mib-objects"></a><span data-ttu-id="43d0a-103">Квалификаторы класса CIM для объектов MIB</span><span class="sxs-lookup"><span data-stu-id="43d0a-103">CIM Class Qualifiers for MIB Objects</span></span>

<span data-ttu-id="43d0a-104">Поставщик SNMP использует следующие квалификаторы класса CIM при сопоставлении определений объектов MIB с определениями классов CIM.</span><span class="sxs-lookup"><span data-stu-id="43d0a-104">The SNMP Provider uses the following CIM class qualifiers when mapping MIB object definitions to CIM class definitions.</span></span> <span data-ttu-id="43d0a-105">Чтобы поставщик SNMP полностью разрешил объект группы, должен присутствовать обязательный квалификатор.</span><span class="sxs-lookup"><span data-stu-id="43d0a-105">A mandatory qualifier must be present for the SNMP Provider to fully resolve a group object.</span></span> <span data-ttu-id="43d0a-106">Ошибка при определении обязательного квалификатора возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="43d0a-106">Failure to define a mandatory qualifier returns an error.</span></span> <span data-ttu-id="43d0a-107">Указание недопустимого значения квалификатора также возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="43d0a-107">Specifying an illegal qualifier value also returns an error.</span></span>

> [!Note]  
> <span data-ttu-id="43d0a-108">Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="43d0a-108">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 



| <span data-ttu-id="43d0a-109">Квалификатор</span><span class="sxs-lookup"><span data-stu-id="43d0a-109">Qualifier</span></span>           | <span data-ttu-id="43d0a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="43d0a-110">Description</span></span>                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43d0a-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="43d0a-111">**Description**</span></span>     | <span data-ttu-id="43d0a-112">**строка** Используемых</span><span class="sxs-lookup"><span data-stu-id="43d0a-112">**string** Optional</span></span><br/> <span data-ttu-id="43d0a-113">Описание класса.</span><span class="sxs-lookup"><span data-stu-id="43d0a-113">Description of the class.</span></span><br/>                                                                      |
| <span data-ttu-id="43d0a-114">**\_ObjectID группы**</span><span class="sxs-lookup"><span data-stu-id="43d0a-114">**Group\_Objectid**</span></span> | <span data-ttu-id="43d0a-115">**строка** Является обязательным, если класс предназначен для поставщика класса SNMP.</span><span class="sxs-lookup"><span data-stu-id="43d0a-115">**string** Mandatory, if the class is for the SNMP class provider.</span></span><br/> <span data-ttu-id="43d0a-116">Идентификатор объекта собранной коллекции.</span><span class="sxs-lookup"><span data-stu-id="43d0a-116">Object identifier of the fabricated collection.</span></span><br/> |
| <span data-ttu-id="43d0a-117">**\_Импорты модулей**</span><span class="sxs-lookup"><span data-stu-id="43d0a-117">**Module\_Imports**</span></span> | <span data-ttu-id="43d0a-118">**строка** Используемых</span><span class="sxs-lookup"><span data-stu-id="43d0a-118">**string** Optional</span></span><br/> <span data-ttu-id="43d0a-119">Разделенный запятыми список имен модулей MIB, используемых для разрешения операций импорта.</span><span class="sxs-lookup"><span data-stu-id="43d0a-119">Comma-separated list of MIB module names used to resolve imports.</span></span><br/>                              |
| <span data-ttu-id="43d0a-120">**\_Имя модуля**</span><span class="sxs-lookup"><span data-stu-id="43d0a-120">**Module\_Name**</span></span>    | <span data-ttu-id="43d0a-121">**строка** Используемых</span><span class="sxs-lookup"><span data-stu-id="43d0a-121">**string** Optional</span></span><br/> <span data-ttu-id="43d0a-122">Имя удостоверения модуля MIB.</span><span class="sxs-lookup"><span data-stu-id="43d0a-122">Identity name of a MIB module.</span></span><br/>                                                                 |
| <span data-ttu-id="43d0a-123">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="43d0a-123">**Reference**</span></span>       | <span data-ttu-id="43d0a-124">**строка** Используемых</span><span class="sxs-lookup"><span data-stu-id="43d0a-124">**string** Optional</span></span><br/> <span data-ttu-id="43d0a-125">Ссылается на другой документ, содержащий дополнительные сведения о классе.</span><span class="sxs-lookup"><span data-stu-id="43d0a-125">Refers to another document that contains more information about the class.</span></span><br/>                     |
| <span data-ttu-id="43d0a-126">**Одноэлементный**</span><span class="sxs-lookup"><span data-stu-id="43d0a-126">**Singleton**</span></span>       | <span data-ttu-id="43d0a-127">**Bool (логическое** ) Обязателен для классов, сопоставленных из скалярных коллекций.</span><span class="sxs-lookup"><span data-stu-id="43d0a-127">**Bool** Mandatory for classes mapped from scalar collections.</span></span><br/> <span data-ttu-id="43d0a-128">Указывает класс, который может иметь только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="43d0a-128">Indicates a class that can only have one instance.</span></span><br/>  |



 

 

 




