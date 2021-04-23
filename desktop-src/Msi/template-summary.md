---
description: Для пакета установки свойство сводка по шаблону указывает на версии платформы и языка, совместимые с этой базой данных установки.
ms.assetid: a1015ddb-8d5c-40f7-97ac-4a1347644ae6
title: Свойство сводки шаблона
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b3949e7028fd0b1b5f9ff3112f1a3d03c9b87e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675187"
---
# <a name="template-summary-property"></a><span data-ttu-id="ed2e9-103">Свойство сводки шаблона</span><span class="sxs-lookup"><span data-stu-id="ed2e9-103">Template Summary property</span></span>

<span data-ttu-id="ed2e9-104">Для пакета установки свойство сводка по **шаблону** указывает на версии платформы и языка, совместимые с этой базой данных установки.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-104">For an installation package, the **Template Summary** property indicates the platform and language versions that are compatible with this installation database.</span></span> <span data-ttu-id="ed2e9-105">Ниже приведен синтаксис сведений о свойстве **сводки шаблона** для базы данных установки.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-105">The syntax of the **Template Summary** property information for an installation database is the following:</span></span>

<span data-ttu-id="ed2e9-106">\[*свойство платформы* \] ; \[ *идентификатор языка* \] \[ ,*идентификатор языка* \] \[ ,... \] .</span><span class="sxs-lookup"><span data-stu-id="ed2e9-106">\[*platform property*\];\[*language id*\]\[,*language id*\]\[,...\].</span></span>

<span data-ttu-id="ed2e9-107">Следующие примеры являются допустимыми значениями для свойства **сводки шаблона** :</span><span class="sxs-lookup"><span data-stu-id="ed2e9-107">The following examples are valid values for the **Template Summary** property:</span></span>

-   <span data-ttu-id="ed2e9-108">x64; 1033</span><span class="sxs-lookup"><span data-stu-id="ed2e9-108">x64;1033</span></span>
-   <span data-ttu-id="ed2e9-109">Intel; 1033</span><span class="sxs-lookup"><span data-stu-id="ed2e9-109">Intel;1033</span></span>
-   <span data-ttu-id="ed2e9-110">Intel64; 1033</span><span class="sxs-lookup"><span data-stu-id="ed2e9-110">Intel64;1033</span></span>
-   <span data-ttu-id="ed2e9-111">; 1033</span><span class="sxs-lookup"><span data-stu-id="ed2e9-111">;1033</span></span>
-   <span data-ttu-id="ed2e9-112">Intel; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="ed2e9-112">Intel ;1033,2046</span></span>
-   <span data-ttu-id="ed2e9-113">Intel64; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="ed2e9-113">Intel64;1033,2046</span></span>
-   <span data-ttu-id="ed2e9-114">Intel; 0</span><span class="sxs-lookup"><span data-stu-id="ed2e9-114">Intel;0</span></span>
-   <span data-ttu-id="ed2e9-115">ARM; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="ed2e9-115">Arm;1033,2046</span></span>
-   <span data-ttu-id="ed2e9-116">ARM; 0</span><span class="sxs-lookup"><span data-stu-id="ed2e9-116">Arm;0</span></span>
-   <span data-ttu-id="ed2e9-117">Arm64; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="ed2e9-117">Arm64;1033,2046</span></span>
-   <span data-ttu-id="ed2e9-118">Arm64; 0</span><span class="sxs-lookup"><span data-stu-id="ed2e9-118">Arm64;0</span></span>

<span data-ttu-id="ed2e9-119">Свойство **Сводка шаблона** преобразования указывает версии платформы и языка, совместимые с преобразованием.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-119">The **Template Summary** property of a transform indicates the platform and language versions compatible with the transform.</span></span> <span data-ttu-id="ed2e9-120">В файле преобразования может быть указан только один язык.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-120">In a transform file, only one language may be specified.</span></span> <span data-ttu-id="ed2e9-121">Указанная платформа и язык определяют, можно ли применить преобразование к определенной базе данных.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-121">The specified platform and language determine whether a transform can be applied to a particular database.</span></span> <span data-ttu-id="ed2e9-122">Свойство Platform и свойство Language можно оставить пустыми, если для проверки преобразования не используются ограничения преобразования.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-122">The platform property and the language property can be left blank if no transform restriction relies on them to validate the transform.</span></span>

<span data-ttu-id="ed2e9-123">Свойство **Сводка шаблона** пакета исправлений представляет собой разделенный точками с запятой список кодов продуктов, которые могут принять исправление.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-123">The **Template Summary** property of a patch package is a semicolon-delimited list of the product codes that can accept the patch.</span></span> <span data-ttu-id="ed2e9-124">Если для создания пакета обновления используется [Msimsp.exe](msimsp-exe.md) и [Patchwiz.dll](patchwiz-dll.md) , этот список получается из [таблицы таржетимажес](targetimages-table-patchwiz-dll-.md) файла создания исправления.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-124">If you use [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) to generate the patch package, this list is obtained from the [TargetImages table](targetimages-table-patchwiz-dll-.md) of the patch creation file.</span></span>

<span data-ttu-id="ed2e9-125">Это свойство сводки является обязательным.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-125">This summary property is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed2e9-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed2e9-126">Remarks</span></span>

<span data-ttu-id="ed2e9-127">Если текущая платформа не соответствует одной из платформ, указанных в свойстве **сводки шаблона** , установщик не обрабатывает пакет.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-127">If the current platform does not match one of the platforms specified in the **Template Summary** property then the installer does not process the package.</span></span>

<span data-ttu-id="ed2e9-128">Если спецификация платформы отсутствует в значении свойства **сводки шаблона** , установщик предполагает, что архитектура Intel.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-128">If the platform specification is missing in the **Template Summary** property value, the installer assumes the Intel architecture.</span></span>

<span data-ttu-id="ed2e9-129">Если это 64-разрядный пакет установщик Windows выполняется на платформе Intel64 (Itanium), введите Intel64 в свойстве **сводки шаблона** .</span><span class="sxs-lookup"><span data-stu-id="ed2e9-129">If this is a 64-bit Windows Installer package being run on an Intel64 (Itanium) platform, enter Intel64 in the **Template Summary** property.</span></span>

<span data-ttu-id="ed2e9-130">Если это 64-разрядный пакет установщик Windows выполняется на платформе x64, введите x64 в свойстве **сводки шаблона** .</span><span class="sxs-lookup"><span data-stu-id="ed2e9-130">If this is a 64-bit Windows Installer package being run on a x64 platform, enter x64 in the **Template Summary** property.</span></span>

<span data-ttu-id="ed2e9-131">Если это 64-разрядный установщик Windowsный пакет, который выполняется на Arm64 платформе, введите Arm64 в свойстве **сводки шаблона** .</span><span class="sxs-lookup"><span data-stu-id="ed2e9-131">If this is a 64-bit Windows Installer package being run on an Arm64 platform, enter Arm64 in the **Template Summary** property.</span></span>

<span data-ttu-id="ed2e9-132">Пакет установщик Windows не может быть помечен как поддерживающий как Intel64, так и x64; Например, значение свойства " **Сводка" шаблона** Intel64, x64 является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-132">A Windows Installer package cannot be marked as supporting both Intel64 and x64; for example, the **Template Summary** property value of Intel64,x64 is invalid.</span></span>

<span data-ttu-id="ed2e9-133">Пакет установщик Windows не может быть помечен как поддерживающий как 32-разрядную, так и 64-разрядную платформу. Например, значения свойств **сводки шаблона** , такие как Intel, x64 или Intel, Intel64 являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-133">A Windows Installer package cannot be marked as supporting both 32-bit and 64-bit platforms; for example, **Template Summary** property values such as Intel,x64 or Intel,Intel64 are invalid.</span></span>

<span data-ttu-id="ed2e9-134">Если ввести 0 (ноль) в поле Идентификатор языка свойства **Сводка по шаблону** или оставьте это поле пустым, это означает, что пакет не является нейтральным к языку.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-134">Entering 0 (zero) in the language ID field of the **Template Summary** property, or leaving this field empty, indicates that the package is language neutral.</span></span>

<span data-ttu-id="ed2e9-135">Если это установщик Windows пакет, который выполняется в Windows RT, введите значение ARM в свойстве **Сводка шаблона** .</span><span class="sxs-lookup"><span data-stu-id="ed2e9-135">If this is a Windows Installer package being run on Windows RT, enter the value Arm in the **Template Summary** property.</span></span>

<span data-ttu-id="ed2e9-136">Модули слияния — это единственные пакеты, которые могут иметь несколько языков.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-136">Merge Modules are the only packages that may have multiple languages.</span></span> <span data-ttu-id="ed2e9-137">В исходной базе данных установщика можно указать только один язык.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-137">Only one language can be specified in a source installer database.</span></span> <span data-ttu-id="ed2e9-138">Дополнительные сведения см. в разделе [модули слияния с несколькими языками](multiple-language-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="ed2e9-138">For more information, see [Multiple Language Merge Modules](multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="ed2e9-139">Платформа Alpha не поддерживается установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-139">The Alpha platform is not supported by Windows Installer.</span></span>

<span data-ttu-id="ed2e9-140">**Установщик Windows:** Следующий синтаксис не поддерживается:</span><span class="sxs-lookup"><span data-stu-id="ed2e9-140">**Windows Installer:** The following syntax is not supported:</span></span>

<span data-ttu-id="ed2e9-141">\[*свойство Platform* \] \[ , \] \[ ,... \] свойства \[ платформы *идентификатор языка* \] \[ ,*идентификатор языка* \] \[ ,... \] .</span><span class="sxs-lookup"><span data-stu-id="ed2e9-141">\[*platform property*\]\[,*platform property*\]\[,...\]\[*language id*\]\[,*language id*\]\[,...\].</span></span>

<span data-ttu-id="ed2e9-142">Следующие примеры не являются допустимыми значениями для свойства **сводки шаблона** :</span><span class="sxs-lookup"><span data-stu-id="ed2e9-142">The following examples are not valid values for the **Template Summary** property:</span></span>

-   <span data-ttu-id="ed2e9-143">Альфа, Intel; 1033</span><span class="sxs-lookup"><span data-stu-id="ed2e9-143">Alpha,Intel;1033</span></span>
-   <span data-ttu-id="ed2e9-144">Intel, Альфа; 1033</span><span class="sxs-lookup"><span data-stu-id="ed2e9-144">Intel,Alpha;1033</span></span>
-   <span data-ttu-id="ed2e9-145">Альфа; 1033</span><span class="sxs-lookup"><span data-stu-id="ed2e9-145">Alpha;1033</span></span>
-   <span data-ttu-id="ed2e9-146">Альфа; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="ed2e9-146">Alpha;1033,2046</span></span>

## <a name="requirements"></a><span data-ttu-id="ed2e9-147">Требования</span><span class="sxs-lookup"><span data-stu-id="ed2e9-147">Requirements</span></span>



| <span data-ttu-id="ed2e9-148">Требование</span><span class="sxs-lookup"><span data-stu-id="ed2e9-148">Requirement</span></span> | <span data-ttu-id="ed2e9-149">Значение</span><span class="sxs-lookup"><span data-stu-id="ed2e9-149">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed2e9-150">Версия</span><span class="sxs-lookup"><span data-stu-id="ed2e9-150">Version</span></span><br/> | <span data-ttu-id="ed2e9-151">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-151">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ed2e9-152">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ed2e9-152">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ed2e9-153">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="ed2e9-153">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed2e9-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed2e9-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed2e9-155">Описания свойств сводки</span><span class="sxs-lookup"><span data-stu-id="ed2e9-155">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




