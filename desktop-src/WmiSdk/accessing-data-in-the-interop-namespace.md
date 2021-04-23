---
description: Поставщики ассоциаций позволяют клиентам инструментарий управления Windows (WMI) (WMI) просматривать и получать профили и связанные экземпляры классов из разных пространств имен.
ms.assetid: 00c654d1-a5de-40c5-a190-99382949486a
ms.tgt_platform: multiple
title: Доступ к данным в пространстве имен Interop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a217a7a44651b1a6c94476b53193eedac7f0d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999378"
---
# <a name="accessing-data-in-the-interop-namespace"></a><span data-ttu-id="fdbe6-103">Доступ к данным в пространстве имен Interop</span><span class="sxs-lookup"><span data-stu-id="fdbe6-103">Accessing Data in the Interop Namespace</span></span>

<span data-ttu-id="fdbe6-104">Поставщики ассоциаций позволяют клиентам инструментарий управления Windows (WMI) (WMI) просматривать и получать профили и связанные экземпляры классов из разных пространств имен.</span><span class="sxs-lookup"><span data-stu-id="fdbe6-104">Association providers enable Windows Management Instrumentation (WMI) clients to traverse and retrieve profiles and associated class instances from different namespaces.</span></span>

<span data-ttu-id="fdbe6-105">Поставщики ассоциаций и классы находятся в \\ \\ корневом \\ пространстве имен взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="fdbe6-105">Association providers and classes reside in the \\\\root\\interop namespace.</span></span> <span data-ttu-id="fdbe6-106">Дополнительные сведения см. в разделе [перекрестное сопоставление связей между пространствами имен](cross-namespace-association-traversal.md) и [запись поставщика взаимосвязей](writing-an-association-provider-for-interop.md).</span><span class="sxs-lookup"><span data-stu-id="fdbe6-106">For more information, see [Cross Namespace Association Traversal](cross-namespace-association-traversal.md) and [Writing an Association Provider](writing-an-association-provider-for-interop.md).</span></span>

<span data-ttu-id="fdbe6-107">Поставщики ассоциаций предоставляют стандартные профили, например профиль питания.</span><span class="sxs-lookup"><span data-stu-id="fdbe6-107">Association providers expose standard profiles, like a power profile.</span></span> <span data-ttu-id="fdbe6-108">В следующих примерах используется профиль управления питанием для демонстрации обнаружения и доступа к данным через пространство имен Interop.</span><span class="sxs-lookup"><span data-stu-id="fdbe6-108">The following examples use the power profile to illustrate how to discover and access data through the interop namespace.</span></span>

<span data-ttu-id="fdbe6-109">Windows PowerShell предоставляет простой механизм для прохода по соответствующей ассоциации, получения профиля устройства и вызова метода.</span><span class="sxs-lookup"><span data-stu-id="fdbe6-109">Windows PowerShell provides a simple mechanism to traverse through the appropriate association, retrieve a device profile, and call a method.</span></span>

## <a name="enumerating-profiles-in-the-rootinterop-namespace"></a><span data-ttu-id="fdbe6-110">Перечисление профилей в пространстве имен root или Interop</span><span class="sxs-lookup"><span data-stu-id="fdbe6-110">Enumerating profiles in the root/interop namespace</span></span>

<span data-ttu-id="fdbe6-111">Следующая команда Windows PowerShell перечисляет поддерживаемые профили распределенного управления Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) на компьютере с Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fdbe6-111">The following Windows PowerShell command enumerates the Distributed Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman))-supported profiles on a Windows 7 computer:</span></span>


```PowerShell
Get-WmiObject CIM_RegisteredProfile  -namespace root\interop
```



## <a name="retrieving-instances-of-a-specific-device-profile"></a><span data-ttu-id="fdbe6-112">Получение экземпляров определенного профиля устройства</span><span class="sxs-lookup"><span data-stu-id="fdbe6-112">Retrieving instances of a specific device profile</span></span>

<span data-ttu-id="fdbe6-113">Следующая команда Windows PowerShell возвращает все экземпляры указанного профиля через [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="fdbe6-113">The following Windows PowerShell command returns all instances of a specified profile through [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)):</span></span>


```PowerShell
Get-WmiObject -namespace root\interop -query "Associators of {CIM_RegisteredProfile.InstanceID='Power Supply'}"
```



## <a name="assigning-the-power-profile-to-a-variable"></a><span data-ttu-id="fdbe6-114">Назначение профиля питания переменной</span><span class="sxs-lookup"><span data-stu-id="fdbe6-114">Assigning the power profile to a variable</span></span>

<span data-ttu-id="fdbe6-115">Следующая команда Windows PowerShell присваивает экземпляр профиля управления питанием переменной:</span><span class="sxs-lookup"><span data-stu-id="fdbe6-115">The following Windows PowerShell command assigns the power profile instance to a variable:</span></span>


```PowerShell
$pplan = Get-WmiObject -query "Select * from Win32_PowerPlan" -Namespace root\cimv2\power
```



## <a name="enumerating-the-power-plans-on-a-computer"></a><span data-ttu-id="fdbe6-116">Перечисление схем управления питанием на компьютере</span><span class="sxs-lookup"><span data-stu-id="fdbe6-116">Enumerating the power plans on a computer</span></span>

<span data-ttu-id="fdbe6-117">Следующая команда Windows PowerShell перечисляет доступные планы профиля управления питанием:</span><span class="sxs-lookup"><span data-stu-id="fdbe6-117">The following Windows PowerShell command enumerates the available power profile plans:</span></span>


```PowerShell
$pplan
```



## <a name="calling-a-method"></a><span data-ttu-id="fdbe6-118">Вызов метода</span><span class="sxs-lookup"><span data-stu-id="fdbe6-118">Calling a method</span></span>

<span data-ttu-id="fdbe6-119">Следующая команда Windows PowerShell вызывает метод [**Activate**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) для схемы управления питанием:</span><span class="sxs-lookup"><span data-stu-id="fdbe6-119">The following Windows PowerShell command calls the [**Activate**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) method for the power plan:</span></span>


```PowerShell
$pplan[2].Activate()
```



## <a name="related-topics"></a><span data-ttu-id="fdbe6-120">См. также</span><span class="sxs-lookup"><span data-stu-id="fdbe6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdbe6-121">Просмотр связей между пространствами имен</span><span class="sxs-lookup"><span data-stu-id="fdbe6-121">Cross Namespace Association Traversal</span></span>](cross-namespace-association-traversal.md)
</dt> <dt>

[<span data-ttu-id="fdbe6-122">Написание поставщика ассоциаций</span><span class="sxs-lookup"><span data-stu-id="fdbe6-122">Writing an Association Provider</span></span>](writing-an-association-provider-for-interop.md)
</dt> <dt>

<span data-ttu-id="fdbe6-123">[**\_РЕГИСТЕРЕДПРОФИЛЕ CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fdbe6-123">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="fdbe6-124">[**\_PowerPlan Win32**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fdbe6-124">[**Win32\_PowerPlan**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))</span></span>
</dt> </dl>

 

 
