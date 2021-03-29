---
description: Описание параметров политики управления питанием, составляющих схему управления питанием.
ms.assetid: cd515cd6-67f4-45d0-b769-3abc7a56faa8
title: Параметры политики электропитания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f490c758a890faf314be1ddffe9ac7a503bd473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813785"
---
# <a name="power-policy-settings"></a><span data-ttu-id="a7e53-103">Параметры политики электропитания</span><span class="sxs-lookup"><span data-stu-id="a7e53-103">Power Policy Settings</span></span>

<span data-ttu-id="a7e53-104">Планы и схемы управления питанием состоят из предпочтений и параметров политики.</span><span class="sxs-lookup"><span data-stu-id="a7e53-104">Power plans and schemes consist of preferences and policy settings.</span></span>

<span data-ttu-id="a7e53-105">Схема управления питанием состоит из группы параметров питания.</span><span class="sxs-lookup"><span data-stu-id="a7e53-105">A power plan consists of a group of power setting preferences.</span></span> <span data-ttu-id="a7e53-106">Эти настройки состоят из значений AC и DC для каждого параметра питания.</span><span class="sxs-lookup"><span data-stu-id="a7e53-106">These preferences consist of both an AC and DC value for each of the power settings.</span></span> <span data-ttu-id="a7e53-107">Каждая схема управления питанием определяется с помощью уникального **идентификатора GUID** , а также понятного имени.</span><span class="sxs-lookup"><span data-stu-id="a7e53-107">Each power plan is identified through a unique **GUID** as well as a friendly name.</span></span> <span data-ttu-id="a7e53-108">В Windows Vista предусмотрено три схемы управления питанием по умолчанию: экономия энергии, сбалансированная и высокая производительность.</span><span class="sxs-lookup"><span data-stu-id="a7e53-108">Windows Vista has three default power plans: Power Saver, Balanced, and High Performance.</span></span> <span data-ttu-id="a7e53-109">Эти планы можно настраивать, а также создавать дополнительные планы.</span><span class="sxs-lookup"><span data-stu-id="a7e53-109">These plans can be customized, and additional plans can be created.</span></span> <span data-ttu-id="a7e53-110">Все схемы управления питанием имеют атрибут «индивидуальность», указывающий общее поведение энергосбережения плана.</span><span class="sxs-lookup"><span data-stu-id="a7e53-110">All power plans have a personality attribute that indicates the overall power savings behavior of the plan.</span></span>

<span data-ttu-id="a7e53-111">В следующей таблице показаны три персональные схемы управления питанием.</span><span class="sxs-lookup"><span data-stu-id="a7e53-111">The following table shows the three power plan personalities.</span></span> 

| <span data-ttu-id="a7e53-112">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a7e53-112">Display name</span></span>     | <span data-ttu-id="a7e53-113">Описание</span><span class="sxs-lookup"><span data-stu-id="a7e53-113">Description</span></span>                                                                   | <span data-ttu-id="a7e53-114">**GUID**</span><span class="sxs-lookup"><span data-stu-id="a7e53-114">**GUID**</span></span>                             |
|------------------|-------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="a7e53-115">Экономия энергии</span><span class="sxs-lookup"><span data-stu-id="a7e53-115">Power Saver</span></span>      | <span data-ttu-id="a7e53-116">Обеспечивает снижение производительности, что может привести к увеличению энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="a7e53-116">Delivers reduced performance which may increase power savings.</span></span>                | <span data-ttu-id="a7e53-117">a1841308-3541-4fab-bc81-f71556f20b4a</span><span class="sxs-lookup"><span data-stu-id="a7e53-117">a1841308-3541-4fab-bc81-f71556f20b4a</span></span> |
| <span data-ttu-id="a7e53-118">Balanced</span><span class="sxs-lookup"><span data-stu-id="a7e53-118">Balanced</span></span>         | <span data-ttu-id="a7e53-119">Автоматически распределяет производительность и энергопотребление в соответствии с потребностями.</span><span class="sxs-lookup"><span data-stu-id="a7e53-119">Automatically balances performance and power consumption according to demand.</span></span> | <span data-ttu-id="a7e53-120">381b4222-f694-41f0-9685-ff5bb260df2e</span><span class="sxs-lookup"><span data-stu-id="a7e53-120">381b4222-f694-41f0-9685-ff5bb260df2e</span></span> |
| <span data-ttu-id="a7e53-121">Высокая производительность</span><span class="sxs-lookup"><span data-stu-id="a7e53-121">High Performance</span></span> | <span data-ttu-id="a7e53-122">Обеспечивает максимальную производительность за счет повышения энергопотребления.</span><span class="sxs-lookup"><span data-stu-id="a7e53-122">Delivers maximum performance at the expense of higher power consumption.</span></span>      | <span data-ttu-id="a7e53-123">8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c</span><span class="sxs-lookup"><span data-stu-id="a7e53-123">8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c</span></span> |



 

> [!Note]  
> <span data-ttu-id="a7e53-124">Устройства, поддерживающие [современный ждущий](/windows-hardware/design/device-experiences/modern-standby) режим, поддерживают только **сбалансированную** схему управления питанием.</span><span class="sxs-lookup"><span data-stu-id="a7e53-124">Devices that support [Modern Standby](/windows-hardware/design/device-experiences/modern-standby) mode only allow the **Balanced** power plan.</span></span> <span data-ttu-id="a7e53-125">**Современный** переход — это более новое, более рациональное решение для управления параметрами управления питанием.</span><span class="sxs-lookup"><span data-stu-id="a7e53-125">**Modern Standby** is the newer, more streamlined solution to power settings management.</span></span>

 

<span data-ttu-id="a7e53-126">Каждый компьютер имеет одну активную схему управления питанием.</span><span class="sxs-lookup"><span data-stu-id="a7e53-126">Each computer has a single, active power plan.</span></span> <span data-ttu-id="a7e53-127">По умолчанию непривилегированные пользователи могут получить доступ к параметрам питания системы.</span><span class="sxs-lookup"><span data-stu-id="a7e53-127">By default, nonprivileged users are able to access system power settings.</span></span> <span data-ttu-id="a7e53-128">Доступ ко всем или индивидуальным параметрам управления питанием можно контролировать с помощью списков управления доступом в параметрах управления питанием или с помощью групповая политика.</span><span class="sxs-lookup"><span data-stu-id="a7e53-128">Access to all or individual power settings can be controlled through ACLs on the power settings or through Group Policy.</span></span> <span data-ttu-id="a7e53-129">Приложения должны вызывать [**поверсеттингакцессчекк**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) , чтобы определить, имеет ли пользователь доступ к параметру питания.</span><span class="sxs-lookup"><span data-stu-id="a7e53-129">Applications should call [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) to determine if the user has access to the power setting.</span></span>

<span data-ttu-id="a7e53-130">Каждый параметр питания определяется уникальным **идентификатором GUID** и включает понятное имя, описание, допустимые значения и значения по умолчанию для AC и DC.</span><span class="sxs-lookup"><span data-stu-id="a7e53-130">Each power setting is identified by a unique **GUID** and includes a friendly name, description, allowable values, and default values for AC and DC.</span></span> <span data-ttu-id="a7e53-131">Пользовательские параметры питания можно создать с помощью функции [**поверкреатесеттинг**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) .</span><span class="sxs-lookup"><span data-stu-id="a7e53-131">Custom power settings can be created using the [**PowerCreateSetting**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7e53-132">См. также</span><span class="sxs-lookup"><span data-stu-id="a7e53-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7e53-133">Схемы управления питанием</span><span class="sxs-lookup"><span data-stu-id="a7e53-133">Power Schemes</span></span>](power-schemes.md)
</dt> </dl>

 

 
