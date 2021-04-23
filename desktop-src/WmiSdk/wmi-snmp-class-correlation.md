---
description: Корреляция влияет на набор классов, возвращаемых из Смир.
ms.assetid: 799a0866-e7a0-492f-956e-b13bf591babe
ms.tgt_platform: multiple
title: Корреляция классов SNMP WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc0ca4740c90563fce05e1b6352ef33b0e3ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263921"
---
# <a name="wmi-snmp-class-correlation"></a><span data-ttu-id="7dcea-103">Корреляция классов SNMP WMI</span><span class="sxs-lookup"><span data-stu-id="7dcea-103">WMI SNMP Class Correlation</span></span>

<span data-ttu-id="7dcea-104">Корреляция влияет на набор классов, возвращаемых из Смир.</span><span class="sxs-lookup"><span data-stu-id="7dcea-104">Correlation affects the set of classes returned from the SMIR.</span></span> <span data-ttu-id="7dcea-105">Коррелированные классы — это те, которые поддерживаются данным устройством SNMP при перечислении времени.</span><span class="sxs-lookup"><span data-stu-id="7dcea-105">Correlated classes are those that a given SNMP device is known to support at the time enumeration occurs.</span></span> <span data-ttu-id="7dcea-106">Некоррелированное перечисление возвращает все классы, находящиеся в Смир, независимо от того, поддерживает ли устройство их.</span><span class="sxs-lookup"><span data-stu-id="7dcea-106">Noncorrelated enumeration returns all classes present within the SMIR, regardless of whether the device supports them.</span></span> <span data-ttu-id="7dcea-107">Корреляция является функцией поставщика WMI SNMP и может быть выключена или включена (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="7dcea-107">Correlation is a feature of the WMI SNMP provider and can be turned off or on (default).</span></span>

> [!Note]  
> <span data-ttu-id="7dcea-108">Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="7dcea-108">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="7dcea-109">Корреляция может препятствовать просмотру всех классов, которые на самом деле поддерживаются устройством.</span><span class="sxs-lookup"><span data-stu-id="7dcea-109">Correlation might prevent you from seeing all of the classes that are actually supported by a device.</span></span> <span data-ttu-id="7dcea-110">Если известно, что конкретный класс поддерживается, но не отображается в Смир, это может быть вызвано несколькими причинами, одним из которых является корреляция.</span><span class="sxs-lookup"><span data-stu-id="7dcea-110">If you know that a particular class is supported but it does not appear in the SMIR, this could be due to several reasons, one of which is correlation.</span></span> <span data-ttu-id="7dcea-111">Рассмотрите возможность отключения корреляции перед записью на рассматриваемое устройство.</span><span class="sxs-lookup"><span data-stu-id="7dcea-111">Consider turning correlation off before writing to the device in question.</span></span> <span data-ttu-id="7dcea-112">Однако отключение корреляции приводит к невозможности, что многие классы, не поддерживаемые устройством, будут отображаться в Смир.</span><span class="sxs-lookup"><span data-stu-id="7dcea-112">However, turning correlation off results in the likelihood that many classes not supported by the device will appear in the SMIR.</span></span> <span data-ttu-id="7dcea-113">Кроме того, при использовании корреляции возникает снижение производительности, так как на устройстве запрашиваются сведения о поддерживаемых классах.</span><span class="sxs-lookup"><span data-stu-id="7dcea-113">Also, there is a performance cost in using correlation because the device is queried to see what classes it supports.</span></span> <span data-ttu-id="7dcea-114">Если функция корреляции включена, поставщик SNMP вызывает перечисление классов, поддерживаемых устройствами, подобно результату выполнения средства *анализа MIB* .</span><span class="sxs-lookup"><span data-stu-id="7dcea-114">When correlation is turned on, the SNMP provider causes an enumeration of device-supported classes similar to the result of running a *mib walk* tool.</span></span>

<span data-ttu-id="7dcea-115">Например, диспетчер сети хочет узнать несколько ключевых фрагментов данных обо всех управляемых концентраторах в определенной сети.</span><span class="sxs-lookup"><span data-stu-id="7dcea-115">For example, a network manager wants to know several key pieces of data about all the managed hubs in a particular network.</span></span> <span data-ttu-id="7dcea-116">База данных текущих устройств и их поддерживаемые MIB уже существуют, поэтому нет необходимости полагаться на функцию корреляции устройства для предоставления поддерживаемых элементов данных.</span><span class="sxs-lookup"><span data-stu-id="7dcea-116">A database of the current devices and their supported MIBs already exists, so there is no need to rely on the correlation function of the device to provide the supported data elements.</span></span> <span data-ttu-id="7dcea-117">В этом случае может быть отключена корреляция.</span><span class="sxs-lookup"><span data-stu-id="7dcea-117">In this case, correlation could be turned off.</span></span>

<span data-ttu-id="7dcea-118">В следующем примере показано, как отключить корреляцию.</span><span class="sxs-lookup"><span data-stu-id="7dcea-118">The following example shows how to turn off correlation.</span></span>


```VB
set objNamedValueSet = CreateObject( _
    "WbemScripting.SWbemNamedValueSet") 
objNamedValueSet.Add "Correlate", FALSE, 0
```



<span data-ttu-id="7dcea-119">С другой стороны, другим диспетчером сети может потребоваться мониторинг всех дисков компьютера UNIX в сети, но не знаком с данными MIB на этих компьютерах.</span><span class="sxs-lookup"><span data-stu-id="7dcea-119">On the other hand, another network manager may want to monitor all the UNIX machine disk drives on the network but is unfamiliar with the MIB data on those machines.</span></span> <span data-ttu-id="7dcea-120">В этом случае будет включена корреляция.</span><span class="sxs-lookup"><span data-stu-id="7dcea-120">In that case, correlation would be turned on.</span></span>

 

 



