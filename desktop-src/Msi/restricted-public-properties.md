---
description: В некоторых случаях пользователь, не являющийся системным администратором, может переопределять только утвержденный список ограниченных установщик Windows открытых свойств.
ms.assetid: e16e8187-75b6-4104-a53c-928a56fcee6b
title: Ограниченные открытые свойства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f08be7f625cd45cdb48373eb0107ade708949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651032"
---
# <a name="restricted-public-properties"></a><span data-ttu-id="b1b3a-103">Ограниченные открытые свойства</span><span class="sxs-lookup"><span data-stu-id="b1b3a-103">Restricted Public Properties</span></span>

<span data-ttu-id="b1b3a-104">В случае управляемой установки разработчику пакета может потребоваться ограничить количество [общедоступных свойств](public-properties.md) , передаваемых на серверную часть, и изменить их может пользователь, не являющийся системным администратором.</span><span class="sxs-lookup"><span data-stu-id="b1b3a-104">In the case of a managed installation, the package author may need to limit which [public properties](public-properties.md) are passed to the server side and can be changed by a user that is not a system administrator.</span></span> <span data-ttu-id="b1b3a-105">Некоторые ограничения обычно необходимы для обеспечения безопасной среды, когда установка требует, чтобы установщик использовал повышенные привилегии.</span><span class="sxs-lookup"><span data-stu-id="b1b3a-105">Some restrictions are commonly necessary to maintain a secure environment when the installation requires the installer to use elevated privileges.</span></span> <span data-ttu-id="b1b3a-106">Если выполняются все перечисленные ниже условия, пользователь, не являющийся системным администратором, может переопределить только утвержденный список ограниченных общих свойств.</span><span class="sxs-lookup"><span data-stu-id="b1b3a-106">If all of the following conditions are met, a user that is not a system administrator can only override an approved list of restricted public properties:</span></span>

-   <span data-ttu-id="b1b3a-107">Система Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b1b3a-107">The system is Windows 2000.</span></span>
-   <span data-ttu-id="b1b3a-108">Пользователь не является системным администратором.</span><span class="sxs-lookup"><span data-stu-id="b1b3a-108">The user is not a system administrator.</span></span>
-   <span data-ttu-id="b1b3a-109">Приложение или продукт устанавливаются с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="b1b3a-109">The application or product is being installed with elevated privileges.</span></span>

<span data-ttu-id="b1b3a-110">Если все приведенные выше условия имеют значение true, установщик по умолчанию имеет следующий список ограниченных общедоступных свойств, которые могут быть изменены любым пользователем.</span><span class="sxs-lookup"><span data-stu-id="b1b3a-110">If all of the above conditions are true, the installer defaults to the following list of restricted public properties that can be changed by any user:</span></span>

-   [<span data-ttu-id="b1b3a-111">**ПОДДЕРЖКИ**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-111">**ACTION**</span></span>](action.md)
-   [<span data-ttu-id="b1b3a-112">**афтерребут**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-112">**AFTERREBOOT**</span></span>](afterreboot.md)
-   [<span data-ttu-id="b1b3a-113">**ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-113">**ALLUSERS**</span></span>](allusers.md)
-   [<span data-ttu-id="b1b3a-114">**EXECUTEACTION**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-114">**EXECUTEACTION**</span></span>](executeaction.md)
-   [<span data-ttu-id="b1b3a-115">**ексекутемоде**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-115">**EXECUTEMODE**</span></span>](executemode.md)
-   [<span data-ttu-id="b1b3a-116">**филеадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-116">**FILEADDDEFAULT**</span></span>](fileadddefault.md)
-   [<span data-ttu-id="b1b3a-117">**филеаддлокал**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-117">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
-   [<span data-ttu-id="b1b3a-118">**филеаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-118">**FILEADDSOURCE**</span></span>](fileaddsource.md)
-   [<span data-ttu-id="b1b3a-119">**инсталллевел**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-119">**INSTALLLEVEL**</span></span>](installlevel.md)
-   [<span data-ttu-id="b1b3a-120">**лимитуи**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-120">**LIMITUI**</span></span>](limitui.md)
-   [<span data-ttu-id="b1b3a-121">**логактион**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-121">**LOGACTION**</span></span>](logaction.md)
-   [<span data-ttu-id="b1b3a-122">**нокомпанинаме**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-122">**NOCOMPANYNAME**</span></span>](nocompanyname.md)
-   [<span data-ttu-id="b1b3a-123">**ИМЯ пользователя**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-123">**NOUSERNAME**</span></span>](nousername.md)
-   [<span data-ttu-id="b1b3a-124">**мсиенфорцеупградекомпонентрулес**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-124">**MSIENFORCEUPGRADECOMPONENTRULES**</span></span>](msienforceupgradecomponentrules.md)
-   [<span data-ttu-id="b1b3a-125">**мсиинстанцегуид**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-125">**MSIINSTANCEGUID**</span></span>](msiinstanceguid.md)
-   [<span data-ttu-id="b1b3a-126">**мсиневинстанце**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-126">**MSINEWINSTANCE**</span></span>](msinewinstance.md)
-   [<span data-ttu-id="b1b3a-127">**мсипатчремове**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-127">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
-   [<span data-ttu-id="b1b3a-128">**PATCH**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-128">**PATCH**</span></span>](patch.md)
-   [<span data-ttu-id="b1b3a-129">**примарифолдер**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-129">**PRIMARYFOLDER**</span></span>](primaryfolder.md)
-   [<span data-ttu-id="b1b3a-130">**промптроллбакккост**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-130">**PROMPTROLLBACKCOST**</span></span>](promptrollbackcost.md)
-   [<span data-ttu-id="b1b3a-131">**ОБНОВИТ**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-131">**REBOOT**</span></span>](reboot.md)
-   [<span data-ttu-id="b1b3a-132">**КАКОМУ**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-132">**REINSTALL**</span></span>](reinstall.md)
-   [<span data-ttu-id="b1b3a-133">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-133">**REINSTALLMODE**</span></span>](reinstallmode.md)
-   [<span data-ttu-id="b1b3a-134">**ВЫХОД**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-134">**RESUME**</span></span>](resume.md)
-   [<span data-ttu-id="b1b3a-135">**SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-135">**SEQUENCE**</span></span>](sequence.md)
-   [<span data-ttu-id="b1b3a-136">**шортфиленамес**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-136">**SHORTFILENAMES**</span></span>](shortfilenames.md)
-   [<span data-ttu-id="b1b3a-137">**ПРЕОБРАЗОВАНИЯ**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-137">**TRANSFORMS**</span></span>](transforms.md)
-   [<span data-ttu-id="b1b3a-138">**трансформсатсаурце**</span><span class="sxs-lookup"><span data-stu-id="b1b3a-138">**TRANSFORMSATSOURCE**</span></span>](transformsatsource.md)

<span data-ttu-id="b1b3a-139">Автор пакета установки может расширить этот список по умолчанию, чтобы включить дополнительные общие свойства с помощью свойства [**секурекустомпропертиес**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="b1b3a-139">The author of an installation package can extend this default list to include additional public properties by using the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

<span data-ttu-id="b1b3a-140">Установка свойства [**енаблеусерконтрол**](-enableusercontrol.md) или [системной политики](system-policy.md) [енаблеусерконтрол](enableusercontrol.md)расширяет список до всех общедоступных свойств.</span><span class="sxs-lookup"><span data-stu-id="b1b3a-140">Setting the [**EnableUserControl**](-enableusercontrol.md) property or the [EnableUserControl](enableusercontrol.md)[system policy](system-policy.md) extends the list to all public properties.</span></span> <span data-ttu-id="b1b3a-141">Затем все пользователи могут изменить любое общее свойство.</span><span class="sxs-lookup"><span data-stu-id="b1b3a-141">All users can then change any public property.</span></span>

<span data-ttu-id="b1b3a-142">Установщик задает свойство [**рестриктедусерконтрол**](restrictedusercontrol.md) всякий раз, когда список открытых свойств, передаваемых на сервер пользователями, не являющимися администраторами, ограничен.</span><span class="sxs-lookup"><span data-stu-id="b1b3a-142">The installer sets the [**RestrictedUserControl**](restrictedusercontrol.md) property whenever the list of public properties passed to the server by non-administrator users is restricted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1b3a-143">См. также</span><span class="sxs-lookup"><span data-stu-id="b1b3a-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1b3a-144">Сведения о свойствах</span><span class="sxs-lookup"><span data-stu-id="b1b3a-144">About Properties</span></span>](about-properties.md)
</dt> </dl>

 

 



