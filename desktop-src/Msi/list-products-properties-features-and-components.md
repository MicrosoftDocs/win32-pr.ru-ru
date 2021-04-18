---
description: Файл WiLstPrd.vbs VBScript предоставляется в Windows SDK компонентов для установщик Windows разработчиков. Пример скрипта подключается к объекту установщика и перечисляет зарегистрированные продукты и сведения о продукте.
ms.assetid: 13615dc2-ebc7-4536-9dd8-9bb1dbf3cfaf
title: Вывод списка продуктов, свойств, компонентов и компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20d2f563efad42108f763b909e7a1118e255dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682702"
---
# <a name="list-products-properties-features-and-components"></a><span data-ttu-id="d0472-104">Вывод списка продуктов, свойств, компонентов и компонентов</span><span class="sxs-lookup"><span data-stu-id="d0472-104">List Products, Properties, Features, and Components</span></span>

<span data-ttu-id="d0472-105">Файл WiLstPrd.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="d0472-105">The VBScript file WiLstPrd.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="d0472-106">Пример скрипта подключается к объекту [**установщика**](installer-object.md) и перечисляет зарегистрированные продукты и сведения о продукте.</span><span class="sxs-lookup"><span data-stu-id="d0472-106">The sample script connects to an [**Installer**](installer-object.md) object and enumerates registered products and product information.</span></span>

<span data-ttu-id="d0472-107">В этом примере демонстрируется использование:</span><span class="sxs-lookup"><span data-stu-id="d0472-107">This sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="d0472-108">**ProductInfo, свойство**</span><span class="sxs-lookup"><span data-stu-id="d0472-108">**ProductInfo property**</span></span>](installer-productinfo.md)
-   [<span data-ttu-id="d0472-109">**Свойство Продуктстате (объект установщика)**</span><span class="sxs-lookup"><span data-stu-id="d0472-109">**ProductState property (Installer object)**</span></span>](installer-productstate-property.md)
-   [<span data-ttu-id="d0472-110">**Products, свойство**</span><span class="sxs-lookup"><span data-stu-id="d0472-110">**Products property**</span></span>](installer-products.md)
-   [<span data-ttu-id="d0472-111">**Свойство Features**</span><span class="sxs-lookup"><span data-stu-id="d0472-111">**Features property**</span></span>](installer-features.md)
-   [<span data-ttu-id="d0472-112">**Феатурепарент, свойство**</span><span class="sxs-lookup"><span data-stu-id="d0472-112">**FeatureParent property**</span></span>](installer-featureparent.md)
-   [<span data-ttu-id="d0472-113">**Феатурестате, свойство**</span><span class="sxs-lookup"><span data-stu-id="d0472-113">**FeatureState property**</span></span>](installer-featurestate.md)
-   [<span data-ttu-id="d0472-114">**Components, свойство**</span><span class="sxs-lookup"><span data-stu-id="d0472-114">**Components property**</span></span>](installer-components.md)
-   [<span data-ttu-id="d0472-115">**Компонентклиентс, свойство**</span><span class="sxs-lookup"><span data-stu-id="d0472-115">**ComponentClients property**</span></span>](installer-componentclients.md)
-   [<span data-ttu-id="d0472-116">**Компонентпас, свойство**</span><span class="sxs-lookup"><span data-stu-id="d0472-116">**ComponentPath property**</span></span>](installer-componentpath.md)
-   [<span data-ttu-id="d0472-117">**Метод Ластерроррекорд**</span><span class="sxs-lookup"><span data-stu-id="d0472-117">**LastErrorRecord method**</span></span>](installer-lasterrorrecord.md)
-   <span data-ttu-id="d0472-118">[**Метод RegistryValue**](installer-registryvalue.md) [ **объекта установщика**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="d0472-118">[**RegistryValue method**](installer-registryvalue.md) of the [**Installer object**](installer-object.md)</span></span>

<span data-ttu-id="d0472-119">Для использования этого примера потребуется CScript.exe или WScript.exe версию сервера сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="d0472-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="d0472-120">Чтобы использовать CScript.exe для запуска этого образца, введите командную строку в командной строке, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="d0472-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="d0472-121">Если первый аргумент имеет значение/?, отображается справка.</span><span class="sxs-lookup"><span data-stu-id="d0472-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="d0472-122">или, если указано слишком мало аргументов.</span><span class="sxs-lookup"><span data-stu-id="d0472-122">or if too few arguments are specified.</span></span> <span data-ttu-id="d0472-123">Чтобы перенаправить выходные данные в файл, завершите командную строку с помощью VBS > \[ путь к файлу \] .</span><span class="sxs-lookup"><span data-stu-id="d0472-123">To redirect the output to a file, end the command line with VBS > \[path to file\].</span></span> <span data-ttu-id="d0472-124">Пример возвращает значение 0 для успешного выполнения, 1, если вызывается Справка, и 2 в случае сбоя сценария.</span><span class="sxs-lookup"><span data-stu-id="d0472-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="d0472-125">**\[Параметры имени продукта cscript WiLstPrd.vbs \] \[\]**</span><span class="sxs-lookup"><span data-stu-id="d0472-125">**cscript WiLstPrd.vbs \[Product Name\] \[options\]**</span></span>

<span data-ttu-id="d0472-126">Укажите имя продукта, не зависящее от регистра, или идентификатор GUID продукта установленного или объявленного продукта.</span><span class="sxs-lookup"><span data-stu-id="d0472-126">Specify the case-insensitive product name or the product ID GUID of the installed or advertised product.</span></span> <span data-ttu-id="d0472-127">Если продукт или параметры не указаны, установщик выводит список всех установленных или объявленных продуктов в системе.</span><span class="sxs-lookup"><span data-stu-id="d0472-127">If no product or options are specified, the installer lists all the products installed or advertised on the system.</span></span>

<span data-ttu-id="d0472-128">Обратите внимание, что эти параметры не являются переключателями, поэтому не следует ставить их в префикс с косой чертой (/) в командной строке.</span><span class="sxs-lookup"><span data-stu-id="d0472-128">Note that these options are not switches so you should not prefix them with a slash (/) on the commandline.</span></span> <span data-ttu-id="d0472-129">Следующие параметры можно объединять путем сцепления букв.</span><span class="sxs-lookup"><span data-stu-id="d0472-129">The following options may be combined by concatenating the letters.</span></span> <span data-ttu-id="d0472-130">Например, "PC", чтобы получить список свойств продуктов и установленных компонентов.</span><span class="sxs-lookup"><span data-stu-id="d0472-130">For example, "pc" to list both the products' properties and installed components.</span></span>



| <span data-ttu-id="d0472-131">Параметр</span><span class="sxs-lookup"><span data-stu-id="d0472-131">Option</span></span>               | <span data-ttu-id="d0472-132">Описание</span><span class="sxs-lookup"><span data-stu-id="d0472-132">Description</span></span>                                                                                                                           |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0472-133">параметры не указаны</span><span class="sxs-lookup"><span data-stu-id="d0472-133">no options specified</span></span> | <span data-ttu-id="d0472-134">Список свойств продуктов.</span><span class="sxs-lookup"><span data-stu-id="d0472-134">List the products' properties.</span></span>                                                                                                        |
| <span data-ttu-id="d0472-135">p</span><span class="sxs-lookup"><span data-stu-id="d0472-135">p</span></span>                    | <span data-ttu-id="d0472-136">Список свойств продуктов.</span><span class="sxs-lookup"><span data-stu-id="d0472-136">List the products' properties.</span></span>                                                                                                        |
| <span data-ttu-id="d0472-137">f</span><span class="sxs-lookup"><span data-stu-id="d0472-137">f</span></span>                    | <span data-ttu-id="d0472-138">Перечисление функций продуктов, родительских компонентов и состояний установки</span><span class="sxs-lookup"><span data-stu-id="d0472-138">List the products' features, feature parents, and installation states</span></span>                                                                 |
| <span data-ttu-id="d0472-139">c</span><span class="sxs-lookup"><span data-stu-id="d0472-139">c</span></span>                    | <span data-ttu-id="d0472-140">Вывод списка установленных компонентов продуктов.</span><span class="sxs-lookup"><span data-stu-id="d0472-140">List the products' installed components.</span></span>                                                                                              |
| <span data-ttu-id="d0472-141">d</span><span class="sxs-lookup"><span data-stu-id="d0472-141">d</span></span>                    | <span data-ttu-id="d0472-142">Перечислите значения в разделе **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ SharedDlls** для ключевых файлов компонента Products.</span><span class="sxs-lookup"><span data-stu-id="d0472-142">List the value under **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\SharedDlls** for the key files of the products' component.</span></span> |



 

<span data-ttu-id="d0472-143">Дополнительные сведения см. в статье [установщик Windows примеры сценариев](windows-installer-scripting-examples.md) для дополнительных примеров сценариев.</span><span class="sxs-lookup"><span data-stu-id="d0472-143">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) for additional scripting examples.</span></span> <span data-ttu-id="d0472-144">Примеры служебных программ, для которых не требуется сервер сценариев Windows, см. в разделе [установщик Windows средства разработки](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d0472-144">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



