---
title: Регистрация расширений вспомогательного класса NDF
description: С каждым расширением вспомогательного класса связано несколько разделов реестра. Для модели COM требуются некоторые ключи, а для NDF требуются некоторые ключи.
ms.assetid: 9ff3266d-5ffc-4a00-be24-2f85461c6ea6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f211517a975bdef61db7937fffa95f13beddc156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780207"
---
# <a name="registering-ndf-helper-class-extensions"></a><span data-ttu-id="d5046-104">Регистрация расширений вспомогательного класса NDF</span><span class="sxs-lookup"><span data-stu-id="d5046-104">Registering NDF Helper Class Extensions</span></span>

<span data-ttu-id="d5046-105">С каждым расширением вспомогательного класса связано несколько разделов реестра.</span><span class="sxs-lookup"><span data-stu-id="d5046-105">Each helper class extension has a number of registry keys associated with it.</span></span> <span data-ttu-id="d5046-106">Для модели COM требуются некоторые ключи, а для NDF требуются некоторые ключи.</span><span class="sxs-lookup"><span data-stu-id="d5046-106">Some keys are required by COM, and some keys are required by NDF.</span></span>

## <a name="com-registry-keys"></a><span data-ttu-id="d5046-107">Разделы реестра COM</span><span class="sxs-lookup"><span data-stu-id="d5046-107">COM Registry Keys</span></span>

<span data-ttu-id="d5046-108">Расширения вспомогательных классов должны быть реализованы как серверы COM.</span><span class="sxs-lookup"><span data-stu-id="d5046-108">Helper class extensions must be implemented as COM servers.</span></span> <span data-ttu-id="d5046-109">Регистрация COM должна быть выполнена для каждого расширения вспомогательного класса.</span><span class="sxs-lookup"><span data-stu-id="d5046-109">COM registration must be completed for each helper class extension.</span></span> <span data-ttu-id="d5046-110">Необходимо зарегистрировать CLSID объекта, интерфейс [**инетдиагхелперинфо**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) и интерфейс [**инетдиагхелпер**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) .</span><span class="sxs-lookup"><span data-stu-id="d5046-110">The object's CLSID, the [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) interface, and the [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) interface must be registered.</span></span> <span data-ttu-id="d5046-111">Регистрация создает ряд разделов реестра, связанных с COM, для расширения вспомогательного класса NDF.</span><span class="sxs-lookup"><span data-stu-id="d5046-111">Registration creates a number of COM-related registry keys for the NDF helper class extension.</span></span>

## <a name="ndf-registry-keys"></a><span data-ttu-id="d5046-112">Ключи реестра NDF</span><span class="sxs-lookup"><span data-stu-id="d5046-112">NDF Registry Keys</span></span>

<span data-ttu-id="d5046-113">Расширения вспомогательных классов должны быть зарегистрированы до взаимодействия с инфраструктурой диагностики сети и с другими связанными вспомогательными классами.</span><span class="sxs-lookup"><span data-stu-id="d5046-113">Helper class extensions must be registered before interacting with the Network Diagnostics Framework and with other related helper classes.</span></span> <span data-ttu-id="d5046-114">Это достигается путем заполнения реестра.</span><span class="sxs-lookup"><span data-stu-id="d5046-114">This is accomplished by populating the registry.</span></span>

<span data-ttu-id="d5046-115">В следующей процедуре показано, как добавить расширения вспомогательных классов в реестр.</span><span class="sxs-lookup"><span data-stu-id="d5046-115">The following procedure shows how to add helper class extensions to the registry.</span></span>

1.  <span data-ttu-id="d5046-116">Опубликуйте имена вспомогательных классов, реализованных библиотекой DLL, и их зависимости, создав ключ для библиотеки DLL в разделе</span><span class="sxs-lookup"><span data-stu-id="d5046-116">Publish the names of helper classes implemented by the DLL and their dependencies by creating a key for the DLL under</span></span>

    <span data-ttu-id="d5046-117">**HKLM \\ System \\ CurrentControlSet \\ Control \\ нетдиагфкс** \\ *ИмяПоставщика* \\ **хостдллс** \\ *DLL Class вспомогательного класса* \\ **хелперклассес** \\ *имя вспомогательного класса*</span><span class="sxs-lookup"><span data-stu-id="d5046-117">**HKLM\\System\\CurrentControlSet\\Control\\NetDiagFx**\\*VendorName*\\**HostDLLs**\\*Helper Class DLL*\\**HelperClasses**\\*Helper Class Name*</span></span>

    <span data-ttu-id="d5046-118">Замените *ИмяПоставщика*, *вспомогательный класс DLL* и *имя вспомогательного класса* на определяемые пользователем значения, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="d5046-118">Replace *VendorName*, *Helper Class DLL*, and *Helper Class Name* with user-defined values as described below.</span></span>

    | <span data-ttu-id="d5046-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d5046-119">Value</span></span>               | <span data-ttu-id="d5046-120">Тип</span><span class="sxs-lookup"><span data-stu-id="d5046-120">Type</span></span>    | <span data-ttu-id="d5046-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d5046-121">Meaning</span></span>                                                                      |
    |---------------------|---------|------------------------------------------------------------------------------|
    | <span data-ttu-id="d5046-122">*ИмяПоставщика*</span><span class="sxs-lookup"><span data-stu-id="d5046-122">*VendorName*</span></span>        | <span data-ttu-id="d5046-123">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d5046-123">REG\_SZ</span></span> | <span data-ttu-id="d5046-124">Имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="d5046-124">The name of the vendor.</span></span>                                                      |
    | <span data-ttu-id="d5046-125">*DLL-библиотека вспомогательного класса*</span><span class="sxs-lookup"><span data-stu-id="d5046-125">*Helper Class DLL*</span></span>  | <span data-ttu-id="d5046-126">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d5046-126">REG\_SZ</span></span> | <span data-ttu-id="d5046-127">Имя библиотеки DLL без расширения.</span><span class="sxs-lookup"><span data-stu-id="d5046-127">Name of the DLL, without extension.</span></span>                                          |
    | <span data-ttu-id="d5046-128">*Имя вспомогательного класса*</span><span class="sxs-lookup"><span data-stu-id="d5046-128">*Helper Class Name*</span></span> | <span data-ttu-id="d5046-129">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d5046-129">REG\_SZ</span></span> | <span data-ttu-id="d5046-130">Имя вспомогательного класса, от которого зависит текущий вспомогательный класс.</span><span class="sxs-lookup"><span data-stu-id="d5046-130">The name of the helper class on which the current helper class is dependent.</span></span> |

    

     

2.  <span data-ttu-id="d5046-131">В каждом ключе *имени вспомогательного класса* опубликуйте следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="d5046-131">Under each *Helper Class Name* key, publish the following information.</span></span>

    

    | <span data-ttu-id="d5046-132">Значение</span><span class="sxs-lookup"><span data-stu-id="d5046-132">Value</span></span>         | <span data-ttu-id="d5046-133">Тип</span><span class="sxs-lookup"><span data-stu-id="d5046-133">Type</span></span>       | <span data-ttu-id="d5046-134">Значение</span><span class="sxs-lookup"><span data-stu-id="d5046-134">Meaning</span></span>                                                                                                                                                                 |
    |---------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d5046-135">**ЭТОМУ**</span><span class="sxs-lookup"><span data-stu-id="d5046-135">**CLSID**</span></span>     | <span data-ttu-id="d5046-136">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d5046-136">REG\_SZ</span></span>    | <span data-ttu-id="d5046-137">Строка, содержащая идентификатор COM-класса вспомогательного класса.</span><span class="sxs-lookup"><span data-stu-id="d5046-137">A string that contains the COM class ID of the helper class.</span></span>                                                                                                            |
    | <span data-ttu-id="d5046-138">**Version**</span><span class="sxs-lookup"><span data-stu-id="d5046-138">**Version**</span></span>   | <span data-ttu-id="d5046-139">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d5046-139">REG\_SZ</span></span>    | <span data-ttu-id="d5046-140">Строка, содержащая основную и дополнительную версии вспомогательного класса в формате <major> <minor> .</span><span class="sxs-lookup"><span data-stu-id="d5046-140">A string the contains the major and minor versions of the helper class in the format <major><minor>.</span></span>                                                        |
    | <span data-ttu-id="d5046-141">**Выпущен**</span><span class="sxs-lookup"><span data-stu-id="d5046-141">**Published**</span></span> | <span data-ttu-id="d5046-142">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="d5046-142">REG\_DWORD</span></span> | <span data-ttu-id="d5046-143">Значение 1 означает, что этот вспомогательный класс должен вызываться напрямую из клиента диагностики.</span><span class="sxs-lookup"><span data-stu-id="d5046-143">A value of 1 means that this helper class is expected to be directly invoked from the Diagnostics client.</span></span> <span data-ttu-id="d5046-144">значение 0 означает, что его можно вызывать только из другого вспомогательного класса.</span><span class="sxs-lookup"><span data-stu-id="d5046-144">0 means that it can be called only from another helper class.</span></span> |
    | <span data-ttu-id="d5046-145">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="d5046-145">**Parent**</span></span>    | <span data-ttu-id="d5046-146">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d5046-146">REG\_SZ</span></span>    | <span data-ttu-id="d5046-147">Строка, названная расширяемым вспомогательным классом Майкрософт, который расширяется.</span><span class="sxs-lookup"><span data-stu-id="d5046-147">A string that names the Microsoft extensible helper class that is being extended.</span></span>                                                                                       |

    

     

3.  <span data-ttu-id="d5046-148">Для каждого вспомогательного класса опубликуйте список соответствующих атрибутов, создав ключ в разделе.</span><span class="sxs-lookup"><span data-stu-id="d5046-148">For each helper class, publish the list of matching attributes by creating a key under</span></span>

    <span data-ttu-id="d5046-149">**HKLM \\ System \\ CurrentControlSet \\ Control \\ нетдиагфкс** \\ *ИмяПоставщика* \\ **хостдллс** \\ *DLL классов вспомогательного класса* \\ **хелперклассес** \\ *имя вспомогательного класса* \\ **матчаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="d5046-149">**HKLM\\System\\CurrentControlSet\\Control\\NetDiagFx**\\*VendorName*\\**HostDLLs**\\*Helper Class DLL*\\**HelperClasses**\\*Helper Class Name*\\**MatchAttributes**</span></span>

    <span data-ttu-id="d5046-150">Ключ должен содержать одно или несколько значений (по одному на каждый атрибут) следующего типа.</span><span class="sxs-lookup"><span data-stu-id="d5046-150">They key must contain one or more values (one per attribute) of the following type.</span></span>

    | <span data-ttu-id="d5046-151">Значение</span><span class="sxs-lookup"><span data-stu-id="d5046-151">Value</span></span>             | <span data-ttu-id="d5046-152">Тип</span><span class="sxs-lookup"><span data-stu-id="d5046-152">Type</span></span>                             | <span data-ttu-id="d5046-153">Значение</span><span class="sxs-lookup"><span data-stu-id="d5046-153">Meaning</span></span>                                                                    |
    |-------------------|----------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="d5046-154">**AttributeName**</span><span class="sxs-lookup"><span data-stu-id="d5046-154">**AttributeName**</span></span> | <span data-ttu-id="d5046-155">REG \_ SZ \| reg \_ \| \_ двоичный файл реестра</span><span class="sxs-lookup"><span data-stu-id="d5046-155">REG\_SZ\|REG\_DWORD\|REG\_BINARY</span></span> | <span data-ttu-id="d5046-156">Значение, которое завершает пару "имя-значение" для конкретного атрибута.</span><span class="sxs-lookup"><span data-stu-id="d5046-156">A value that completes the name and value pair for a particular attribute.</span></span> |

    

     

 

 




