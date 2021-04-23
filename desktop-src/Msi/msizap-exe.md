---
description: Msizap.exe — это служебная программа командной строки, которая удаляет установщик Windows все сведения о продукте или все продукты, установленные на компьютере. Продукты, установленные установщиком, могут не работать после использования Msizap.
ms.assetid: 0debb8ab-3ae7-447e-84fc-0466ec1b2f26
title: Msizap.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a89f2287443bc442ee767b01e975d6bcc118c1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080600"
---
# <a name="msizapexe"></a><span data-ttu-id="aba03-104">Msizap.exe</span><span class="sxs-lookup"><span data-stu-id="aba03-104">Msizap.exe</span></span>

<span data-ttu-id="aba03-105">Msizap.exe — это служебная программа командной строки, которая удаляет установщик Windows все сведения о продукте или все продукты, установленные на компьютере.</span><span class="sxs-lookup"><span data-stu-id="aba03-105">Msizap.exe is a command line utility that removes either all Windows Installer information for a product or all products installed on a computer.</span></span> <span data-ttu-id="aba03-106">Продукты, установленные установщиком, могут не работать после использования Msizap.</span><span class="sxs-lookup"><span data-stu-id="aba03-106">Products installed by the installer may fail to function after using Msizap.</span></span>

<span data-ttu-id="aba03-107">В Windows 2000 и Windows XP для использования Msizap.exe требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="aba03-107">On Windows 2000 and Windows XP, administrative privileges are required to use Msizap.exe.</span></span>

<span data-ttu-id="aba03-108">Это средство доступно только в [компонентах Windows SDK для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md) и не должно распространяться повторно.</span><span class="sxs-lookup"><span data-stu-id="aba03-108">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) and should not be redistributed.</span></span> <span data-ttu-id="aba03-109">Используйте последнюю версию Msizap.exe (версии 3.1.4000.2726 или выше), которая доступна в Windows SDK компонентов для установщик Windows разработчиков для Windows Vista или более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="aba03-109">Use the recent version of Msizap.exe (version 3.1.4000.2726 or greater) that is available in the Windows SDK Components for Windows Installer Developers for Windows Vista or greater.</span></span> <span data-ttu-id="aba03-110">Более ранние версии Msizap.exe могут удалять сведения обо всех обновлениях, примененных к другим приложениям на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="aba03-110">Lesser versions of Msizap.exe can remove information about all updates that have been applied to other applications on the user's computer.</span></span> <span data-ttu-id="aba03-111">Если эта информация будет удалена, для получения дополнительных обновлений может потребоваться удаление и повторная установка этих приложений.</span><span class="sxs-lookup"><span data-stu-id="aba03-111">If this information is removed, these other applications may need to be removed and reinstalled to receive additional updates.</span></span>

## <a name="syntax"></a><span data-ttu-id="aba03-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aba03-112">Syntax</span></span>

<span data-ttu-id="aba03-113">**Msizap T**_\[ Вашингтон! \] {код продукта}_</span><span class="sxs-lookup"><span data-stu-id="aba03-113">**msizap T**_\[WA!\]{product code}_</span></span>

<span data-ttu-id="aba03-114">**Msizap T**_\[ Вашингтон! \] <msi package>_</span><span class="sxs-lookup"><span data-stu-id="aba03-114">**msizap T**_\[WA!\]<msi package>_</span></span>

<span data-ttu-id="aba03-115">\**\* \*\*\* Msizap \[ WA! \]* **Аллпродуктс**</span><span class="sxs-lookup"><span data-stu-id="aba03-115">\**msizap \*\*\*\*\[WA!\]* **ALLPRODUCTS**</span></span>

<span data-ttu-id="aba03-116">**Msizap ПВСА?!**</span><span class="sxs-lookup"><span data-stu-id="aba03-116">**msizap PWSA?!**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="aba03-117">Параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="aba03-117">Command Line Options</span></span>

<span data-ttu-id="aba03-118">В Msizap.exe используются параметры командной строки без учета регистра, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="aba03-118">Msizap.exe uses case-insensitive command line options shown in the following table.</span></span>



| <span data-ttu-id="aba03-119">Параметр</span><span class="sxs-lookup"><span data-stu-id="aba03-119">Option</span></span> | <span data-ttu-id="aba03-120">Описание</span><span class="sxs-lookup"><span data-stu-id="aba03-120">Description</span></span>                                                                                                                                                                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*     | <span data-ttu-id="aba03-121">Удаляет все установщик Windows папки и разделы реестра, корректирует количество общих библиотек DLL и останавливает службу установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="aba03-121">Removes all Windows Installer folders and registry keys, adjusts shared DLL counts, and stops Windows Installer service.</span></span> <span data-ttu-id="aba03-122">Также удаляет ключ In-Progress и сведения о откате.</span><span class="sxs-lookup"><span data-stu-id="aba03-122">Also removes the In-Progress key and rollback information.</span></span>                                                                           |
| <span data-ttu-id="aba03-123">а</span><span class="sxs-lookup"><span data-stu-id="aba03-123">a</span></span>      | <span data-ttu-id="aba03-124">Только изменяет список ACL для административного полного доступа для любого указанного удаления.</span><span class="sxs-lookup"><span data-stu-id="aba03-124">Only changes ACLs to Admin Full Control for any specified removal.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="aba03-125">н</span><span class="sxs-lookup"><span data-stu-id="aba03-125">g</span></span>      | <span data-ttu-id="aba03-126">Для всех пользователей удаляет все кэшированные установщик Windows потерянные файлы данных.</span><span class="sxs-lookup"><span data-stu-id="aba03-126">For all users, removes any cached Windows Installer data files that have been orphaned.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="aba03-127">p</span><span class="sxs-lookup"><span data-stu-id="aba03-127">p</span></span>      | <span data-ttu-id="aba03-128">Удаляет ключ In-Progress.</span><span class="sxs-lookup"><span data-stu-id="aba03-128">Removes the In-Progress key.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="aba03-129">s</span><span class="sxs-lookup"><span data-stu-id="aba03-129">s</span></span>      | <span data-ttu-id="aba03-130">Удаляет сведения об откате.</span><span class="sxs-lookup"><span data-stu-id="aba03-130">Removes Rollback Information.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="aba03-131">t</span><span class="sxs-lookup"><span data-stu-id="aba03-131">t</span></span>      | <span data-ttu-id="aba03-132">Удаляет все сведения для указанного кода продукта.</span><span class="sxs-lookup"><span data-stu-id="aba03-132">Removes all information for the specified product code.</span></span> <span data-ttu-id="aba03-133">При использовании этого параметра код продукта следует заключать в фигурные скобки.</span><span class="sxs-lookup"><span data-stu-id="aba03-133">When using this option, enclose the Product Code in curly braces.</span></span> <span data-ttu-id="aba03-134">Этот параметр можно использовать с полным путем к MSI или с кодом продукта.</span><span class="sxs-lookup"><span data-stu-id="aba03-134">This option may be used with either the full path to the .msi file or with the product code.</span></span>                                        |
| <span data-ttu-id="aba03-135">w</span><span class="sxs-lookup"><span data-stu-id="aba03-135">w</span></span>      | <span data-ttu-id="aba03-136">Удаляет сведения о установщик Windows для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="aba03-136">Removes Windows Installer information for all users.</span></span> <span data-ttu-id="aba03-137">Если этот параметр не установлен, удаляются только сведения для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="aba03-137">When this option is not set, only the information for the current user is removed.</span></span> <span data-ttu-id="aba03-138">Для использования этого параметра необходимо, чтобы профиль пользователя был загружен, чтобы пользовательский куст реестра для пользователя был доступен.</span><span class="sxs-lookup"><span data-stu-id="aba03-138">Use of this option requires that the user's profile be loaded so that the user's per-user registry hive be available.</span></span> |
| <span data-ttu-id="aba03-139">?</span><span class="sxs-lookup"><span data-stu-id="aba03-139">?</span></span>      | <span data-ttu-id="aba03-140">Подробная Справка.</span><span class="sxs-lookup"><span data-stu-id="aba03-140">Verbose help.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="aba03-141">!</span><span class="sxs-lookup"><span data-stu-id="aba03-141">!</span></span>      | <span data-ttu-id="aba03-142">Принудительно выводит ответ "Да" на запрос.</span><span class="sxs-lookup"><span data-stu-id="aba03-142">Forces a 'yes' response to any prompt.</span></span>                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="aba03-143">См. также</span><span class="sxs-lookup"><span data-stu-id="aba03-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aba03-144">Выпущенные версии, средства и распространяемые пакеты</span><span class="sxs-lookup"><span data-stu-id="aba03-144">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



