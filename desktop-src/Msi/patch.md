---
description: Установщик задает для свойства PATCH список примененных исправлений путем вызова Мсиапплипатч, Мсиапплимултиплепатчес или параметра командной строки/p.
ms.assetid: f2993544-2124-4fb0-8bb3-59f5d8e76b83
title: Свойство PATCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870c480c1fdff0f979701e059bfcd6eb187a4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652115"
---
# <a name="patch-property"></a><span data-ttu-id="c645c-103">Свойство PATCH</span><span class="sxs-lookup"><span data-stu-id="c645c-103">PATCH property</span></span>

<span data-ttu-id="c645c-104">Установщик задает для свойства **Patch** список примененных исправлений путем вызова [**мсиапплипатч**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha), [**мсиапплимултиплепатчес**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) или [параметра командной строки](command-line-options.md)/p.</span><span class="sxs-lookup"><span data-stu-id="c645c-104">The installer sets the **PATCH** property to a list of patches being applied by calling [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha), [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) or the /p [Command Line Option](command-line-options.md).</span></span> <span data-ttu-id="c645c-105">Можно также задать свойство **Patch** в командной строке при установке пакета с помощью [**Мсиинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) или параметра командной строки/i.</span><span class="sxs-lookup"><span data-stu-id="c645c-105">You can also set the **PATCH** property on the command line while installing a package using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) or the /i Command Line Option.</span></span>

<span data-ttu-id="c645c-106">Значение свойства **Patch** представляет собой список устанавливаемых исправлений.</span><span class="sxs-lookup"><span data-stu-id="c645c-106">The value of the **PATCH** property is a list of the patches that are being installed.</span></span> <span data-ttu-id="c645c-107">Каждое исправление в списке представлено полным путем к пакету исправления (MSP-файлу). Полные пути в списке разделяются точками с запятой.</span><span class="sxs-lookup"><span data-stu-id="c645c-107">Each patch in the list is represented by the full path to the patch's package (.msp file.) The full paths in the list are separated by semicolons.</span></span>

<span data-ttu-id="c645c-108">**Установщик Windows 2,0:** Несколько исправлений не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="c645c-108">**Windows Installer 2.0:** Multiple patches are not supported.</span></span> <span data-ttu-id="c645c-109">Для применения нескольких исправлений требуется установщик Windows 3,0.</span><span class="sxs-lookup"><span data-stu-id="c645c-109">Windows Installer 3.0 is required to apply multiple patches.</span></span>

## <a name="remarks"></a><span data-ttu-id="c645c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c645c-110">Remarks</span></span>

<span data-ttu-id="c645c-111">При создании пакета исправлений с помощью [Msimsp.exe](msimsp-exe.md) и [Patchwiz.dll](patchwiz-dll.md) можно указать, что действие или диалоговое окно следует запускать только при применении конкретного исправления.</span><span class="sxs-lookup"><span data-stu-id="c645c-111">If you create a patch package using [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) you can specify that an action or a dialog box only run when a particular patch is being applied.</span></span> <span data-ttu-id="c645c-112">При создании пакета исправлений, например Test. MSP, создается обновленный образ продукта и файл свойств создания исправления.</span><span class="sxs-lookup"><span data-stu-id="c645c-112">When you create the patch package, for example test.msp, you author an upgraded image of the product and a patch creation properties file.</span></span> <span data-ttu-id="c645c-113">При создании файла свойств создания исправления можно ввести имя свойства, например ПАТЧФОРТЕСТ, в поле Медиасркпропнаме таблицы [имажефамилиес](imagefamilies-table-patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="c645c-113">When authoring the patch creation properties file you can enter a property name, for example PATCHFORTEST, in the MediaSrcPropName field of the [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) table.</span></span> <span data-ttu-id="c645c-114">При создании таблиц последовательности обновленного образа продукта можно включить в столбец Condition (условие) в таблице последовательностей условный оператор для действия или диалогового окна, которое необходимо сделать условным.</span><span class="sxs-lookup"><span data-stu-id="c645c-114">When you author the sequence tables of the upgraded image of the product, you can include in the Condition column of the sequence table a conditional statement for the action or dialog box you want to make conditional.</span></span>

<span data-ttu-id="c645c-115">Например, можно использовать следующую условную инструкцию для запуска действия или диалогового окна только при применении Test. MSP.</span><span class="sxs-lookup"><span data-stu-id="c645c-115">For example, you can use the following conditional statement to run an action or dialog box only when test.msp is being applied.</span></span>

<dl> <span data-ttu-id="c645c-116">ИСПРАВЛЕНИЕ И ПАТЧФОРТЕСТ И ИСПРАВЛЕНИЕ >< ПАТЧФОРТЕСТ</span><span class="sxs-lookup"><span data-stu-id="c645c-116">PATCH AND PATCHFORTEST AND PATCH >< PATCHFORTEST</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="c645c-117">Поскольку свойство **Patch** может содержать несколько исправлений, используйте оператор substring "><" для проверки наличия конкретного исправления, а не оператора Equals "=".</span><span class="sxs-lookup"><span data-stu-id="c645c-117">Because the **PATCH** property can contain multiple patches, use the substring operator "><" to test for the presence of a particular patch rather than the equals operator "=".</span></span> <span data-ttu-id="c645c-118">Дополнительные сведения об условных инструкциях см. в разделе [Синтаксис условных](conditional-statement-syntax.md) инструкций.</span><span class="sxs-lookup"><span data-stu-id="c645c-118">For more information about conditional statements see the [Conditional Statement Syntax](conditional-statement-syntax.md) section.</span></span>

 

<span data-ttu-id="c645c-119">Установщик задает оба свойства, если вы применяете список исправлений, включающий Test. MSP.</span><span class="sxs-lookup"><span data-stu-id="c645c-119">The installer sets both properties if you apply a list of patches that includes test.msp.</span></span> <span data-ttu-id="c645c-120">Например, можно использовать [параметр командной строки](command-line-options.md) /p для применения списка двух исправлений.</span><span class="sxs-lookup"><span data-stu-id="c645c-120">For example, you can use the /p [Command Line Option](command-line-options.md) to apply a list of two patches.</span></span>

<span data-ttu-id="c645c-121">**msiexec/QB/p \\ \\ "Рабочая область" \\ \\ \\ . исправления: \\ Test. MSP; \\ \\ Вспомогательная \\ Рабочая \\ \\ область XYZ. MSP**</span><span class="sxs-lookup"><span data-stu-id="c645c-121">**msiexec /qb /p \\\\scratch\\scratch\\XYZ\\Patches\\test.msp;\\\\scratch\\scratch\\XYZ\\bar.msp**</span></span>

<span data-ttu-id="c645c-122">Установщик задает свойства **Patch** и патчфортест следующим образом.</span><span class="sxs-lookup"><span data-stu-id="c645c-122">The installer sets the **PATCH** and PATCHFORTEST properties as follows.</span></span>

<dl> <span data-ttu-id="c645c-123">Исправление = "Рабочая область" — \\ \\ \\ \\ \\ исправления \\ . MSP; \\ \\ Вспомогательная \\ Рабочая \\ \\ область XYZ. MSP</span><span class="sxs-lookup"><span data-stu-id="c645c-123">PATCH=\\\\scratch\\scratch\\XYZ\\Patches\\test.msp;\\\\scratch\\scratch\\XYZ\\bar.msp</span></span>  
<span data-ttu-id="c645c-124">ПАТЧФОРТЕСТ = "Рабочая область" — \\ \\ \\ \\ \\ исправления \\ . MSP</span><span class="sxs-lookup"><span data-stu-id="c645c-124">PATCHFORTEST=\\\\scratch\\scratch\\XYZ\\Patches\\test.msp</span></span>  
</dl>

<span data-ttu-id="c645c-125">В этом случае условие имеет значение TRUE, и для каждого устанавливаемого исправления может выполняться указанное выше условное действие или диалоговое окно. Проверьте MSP-и Bar. MSP.</span><span class="sxs-lookup"><span data-stu-id="c645c-125">In this case, the condition is TRUE and the above conditional action or dialog box can run for each patch being installed, test.msp and bar.msp.</span></span>

<span data-ttu-id="c645c-126">Если не применяется Test. MSP, установщик не включает его в свойство **Patch** и не устанавливает патчфортест.</span><span class="sxs-lookup"><span data-stu-id="c645c-126">If test.msp is not being applied, the installer does not include it in the **PATCH** property and does not set PATCHFORTEST.</span></span> <span data-ttu-id="c645c-127">В этом случае условие выше имеет значение FALSE, а условное действие или диалоговое окно не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c645c-127">In this case, the condition above is FALSE and the conditional action or dialog box does not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="c645c-128">Требования</span><span class="sxs-lookup"><span data-stu-id="c645c-128">Requirements</span></span>



| <span data-ttu-id="c645c-129">Требование</span><span class="sxs-lookup"><span data-stu-id="c645c-129">Requirement</span></span> | <span data-ttu-id="c645c-130">Значение</span><span class="sxs-lookup"><span data-stu-id="c645c-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c645c-131">Версия</span><span class="sxs-lookup"><span data-stu-id="c645c-131">Version</span></span><br/> | <span data-ttu-id="c645c-132">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c645c-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c645c-133">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c645c-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c645c-134">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c645c-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c645c-135">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c645c-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c645c-136">См. также</span><span class="sxs-lookup"><span data-stu-id="c645c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c645c-137">Свойства</span><span class="sxs-lookup"><span data-stu-id="c645c-137">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="c645c-138">Синтаксис условных операторов</span><span class="sxs-lookup"><span data-stu-id="c645c-138">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> <dt>

[<span data-ttu-id="c645c-139">Примеры синтаксиса условных операторов</span><span class="sxs-lookup"><span data-stu-id="c645c-139">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)
</dt> </dl>

 

 




