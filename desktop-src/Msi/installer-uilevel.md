---
description: Свойство Duilevel объекта установщика — это свойство, доступное для чтения и записи, которое указывает тип пользовательского интерфейса, используемого при открытии и обработке последующих пакетов в пределах текущего пространства процесса.
ms.assetid: c89545b5-aeb7-4b05-94b0-d6e2a237152e
title: Свойство Installer. Duilevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UILevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: de6bda93b5607e00544a69c917a6a238b596c581
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652264"
---
# <a name="installeruilevel-property"></a><span data-ttu-id="c5508-103">Свойство Installer. Duilevel</span><span class="sxs-lookup"><span data-stu-id="c5508-103">Installer.UILevel property</span></span>

<span data-ttu-id="c5508-104">Свойство **duilevel** объекта [**установщика**](installer-object.md) — это свойство, доступное для чтения и записи, которое указывает тип пользовательского интерфейса, используемого при открытии и обработке последующих пакетов в пределах текущего пространства процесса.</span><span class="sxs-lookup"><span data-stu-id="c5508-104">The **UILevel** property of the [**Installer**](installer-object.md) object is a read-write property that indicates the type of user interface to be used when opening and processing subsequent packages within the current process space.</span></span>

<span data-ttu-id="c5508-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c5508-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5508-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5508-106">Syntax</span></span>


```JScript
propVal = Installer.UILevel
Installer.UILevel = propVal 
```



## <a name="property-value"></a><span data-ttu-id="c5508-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c5508-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="c5508-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5508-108">Remarks</span></span>



| <span data-ttu-id="c5508-109">Уровень пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="c5508-109">User interface level</span></span>   | <span data-ttu-id="c5508-110">Значение</span><span class="sxs-lookup"><span data-stu-id="c5508-110">Value</span></span> | <span data-ttu-id="c5508-111">Описание</span><span class="sxs-lookup"><span data-stu-id="c5508-111">Description</span></span>                                                                                                                                                                                        |
|------------------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5508-112">мсиуилевелночанже</span><span class="sxs-lookup"><span data-stu-id="c5508-112">msiUILevelNoChange</span></span>     | <span data-ttu-id="c5508-113">0</span><span class="sxs-lookup"><span data-stu-id="c5508-113">0</span></span>     | <span data-ttu-id="c5508-114">Не изменяет уровень пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c5508-114">Does not change UI level.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="c5508-115">мсиуилевелдефаулт</span><span class="sxs-lookup"><span data-stu-id="c5508-115">msiUILevelDefault</span></span>      | <span data-ttu-id="c5508-116">1</span><span class="sxs-lookup"><span data-stu-id="c5508-116">1</span></span>     | <span data-ttu-id="c5508-117">Использует уровень пользовательского интерфейса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c5508-117">Uses default UI level.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="c5508-118">мсиуилевелноне</span><span class="sxs-lookup"><span data-stu-id="c5508-118">msiUILevelNone</span></span>         | <span data-ttu-id="c5508-119">2</span><span class="sxs-lookup"><span data-stu-id="c5508-119">2</span></span>     | <span data-ttu-id="c5508-120">Автоматическая установка.</span><span class="sxs-lookup"><span data-stu-id="c5508-120">Silent installation.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="c5508-121">мсиуилевелбасик</span><span class="sxs-lookup"><span data-stu-id="c5508-121">msiUILevelBasic</span></span>        | <span data-ttu-id="c5508-122">3</span><span class="sxs-lookup"><span data-stu-id="c5508-122">3</span></span>     | <span data-ttu-id="c5508-123">Простой ход выполнения и обработка ошибок.</span><span class="sxs-lookup"><span data-stu-id="c5508-123">Simple progress and error handling.</span></span>                                                                                                                                                                |
| <span data-ttu-id="c5508-124">мсиуилевелредуцед</span><span class="sxs-lookup"><span data-stu-id="c5508-124">msiUILevelReduced</span></span>      | <span data-ttu-id="c5508-125">4</span><span class="sxs-lookup"><span data-stu-id="c5508-125">4</span></span>     | <span data-ttu-id="c5508-126">Созданные диалоговые окна пользовательского интерфейса и мастера подавлены.</span><span class="sxs-lookup"><span data-stu-id="c5508-126">Authored UI and wizard dialog boxes suppressed.</span></span>                                                                                                                                                    |
| <span data-ttu-id="c5508-127">мсиуилевелфулл</span><span class="sxs-lookup"><span data-stu-id="c5508-127">msiUILevelFull</span></span>         | <span data-ttu-id="c5508-128">5</span><span class="sxs-lookup"><span data-stu-id="c5508-128">5</span></span>     | <span data-ttu-id="c5508-129">Создан пользовательский интерфейс с мастерами, ходом выполнения и ошибками.</span><span class="sxs-lookup"><span data-stu-id="c5508-129">Authored UI with wizards, progress, and errors.</span></span>                                                                                                                                                    |
| <span data-ttu-id="c5508-130">мсиуилевелхидеканцел</span><span class="sxs-lookup"><span data-stu-id="c5508-130">msiUILevelHideCancel</span></span>   | <span data-ttu-id="c5508-131">32</span><span class="sxs-lookup"><span data-stu-id="c5508-131">32</span></span>    | <span data-ttu-id="c5508-132">В сочетании со значением Мсиуилевелбасик программа установки отображает диалоговые окна хода выполнения, но не отображает кнопку **Отмена** в диалоговом окне, чтобы запретить пользователям отменять установку.</span><span class="sxs-lookup"><span data-stu-id="c5508-132">If combined with the msiUILevelBasic value, the installer shows progress dialog boxes but does not display a **Cancel** button on the dialog box to prevent users from canceling the installation.</span></span> |
| <span data-ttu-id="c5508-133">мсиуилевелпрогрессонли</span><span class="sxs-lookup"><span data-stu-id="c5508-133">msiUILevelProgressOnly</span></span> | <span data-ttu-id="c5508-134">64</span><span class="sxs-lookup"><span data-stu-id="c5508-134">64</span></span>    | <span data-ttu-id="c5508-135">Если в сочетании со значением Мсиуилевелбасик, установщик отображает диалоговые окна хода выполнения, но не отображает модальные диалоговые окна или диалоговые окна ошибок.</span><span class="sxs-lookup"><span data-stu-id="c5508-135">If combined with the msiUILevelBasic value, the installer displays progress dialog boxes but does not display any modal dialog boxes or error dialog boxes.</span></span>                                        |
| <span data-ttu-id="c5508-136">мсиуилевеленддиалог</span><span class="sxs-lookup"><span data-stu-id="c5508-136">msiUILevelEndDialog</span></span>    | <span data-ttu-id="c5508-137">128</span><span class="sxs-lookup"><span data-stu-id="c5508-137">128</span></span>   | <span data-ttu-id="c5508-138">Если в сочетании с любым из указанных выше значений, установщик отображает модальное диалоговое окно в конце успешной установки или при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="c5508-138">If combined with any above value, the installer displays a modal dialog box at the end of a successful installation or if there has been an error.</span></span> <span data-ttu-id="c5508-139">Если пользователь отменяет операцию, диалоговое окно не отображается.</span><span class="sxs-lookup"><span data-stu-id="c5508-139">No dialog box is displayed if the user cancels.</span></span> |



 

<span data-ttu-id="c5508-140">См. также [Определение уровня пользовательского интерфейса из настраиваемого действия](determining-ui-level-from-a-custom-action.md).</span><span class="sxs-lookup"><span data-stu-id="c5508-140">See also, [Determining UI Level from a Custom Action](determining-ui-level-from-a-custom-action.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5508-141">Требования</span><span class="sxs-lookup"><span data-stu-id="c5508-141">Requirements</span></span>



| <span data-ttu-id="c5508-142">Требование</span><span class="sxs-lookup"><span data-stu-id="c5508-142">Requirement</span></span> | <span data-ttu-id="c5508-143">Значение</span><span class="sxs-lookup"><span data-stu-id="c5508-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5508-144">Версия</span><span class="sxs-lookup"><span data-stu-id="c5508-144">Version</span></span><br/> | <span data-ttu-id="c5508-145">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c5508-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c5508-146">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c5508-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c5508-147">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="c5508-147">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c5508-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c5508-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="c5508-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5508-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c5508-150">IID</span><span class="sxs-lookup"><span data-stu-id="c5508-150">IID</span></span><br/>     | <span data-ttu-id="c5508-151">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c5508-151">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




