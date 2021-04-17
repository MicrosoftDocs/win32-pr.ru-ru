---
description: Вы можете указать все сведения, необходимые для настройки компонента "Установка и удаление программ" на панели управления, задав значения определенных свойств установщика в пакете установщик Windows приложения.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: Настройка установки и удаления программ с помощью установщик Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6850163e18af94aa9cceaf6c4bb2e8059dcf2121
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/30/2021
ms.locfileid: "105994506"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a><span data-ttu-id="aea48-103">Настройка установки и удаления программ с помощью установщик Windows</span><span class="sxs-lookup"><span data-stu-id="aea48-103">Configuring Add/Remove Programs with Windows Installer</span></span>

<span data-ttu-id="aea48-104">Вы можете указать все сведения, необходимые для настройки компонента "Установка и удаление программ" на панели управления, задав значения определенных свойств установщика в пакете установщик Windows приложения.</span><span class="sxs-lookup"><span data-stu-id="aea48-104">You can supply all of the information needed to configure Add/Remove Programs in Control Panel by setting the values of certain installer properties in your application's Windows Installer package.</span></span> <span data-ttu-id="aea48-105">При установке этих свойств соответствующие значения автоматически записываются в реестр.</span><span class="sxs-lookup"><span data-stu-id="aea48-105">Setting these properties automatically writes the corresponding values into the registry.</span></span> <span data-ttu-id="aea48-106">Если установщик обнаруживает, что продукт помечен для полного удаления, операции автоматически добавляются в сценарий для удаления папки "Установка и удаление программ" в окне "сведения о продукте" панели управления.</span><span class="sxs-lookup"><span data-stu-id="aea48-106">If the installer detects that the product is marked for complete removal, operations are automatically added to the script to remove the Add/Remove Programs folder in Control Panel information for the product.</span></span>

<span data-ttu-id="aea48-107">Если приложение не зарегистрировано, оно не отображается в окне Установка и удаление программ на панели управления.</span><span class="sxs-lookup"><span data-stu-id="aea48-107">If an application is not registered, it is not listed in Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="aea48-108">Дополнительные сведения см. [в разделах Добавление и удаление приложения и отсутствие трассировки в реестре](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="aea48-108">For more information, see [Adding and Removing an Application and Leaving No Trace in the Registry](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).</span></span>

<span data-ttu-id="aea48-109">Приложения, установленные в [контексте установки](installation-context.md) «на пользователя», отображаются в окне «Установка и удаление программ» текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="aea48-109">Applications that have been installed in the per-user [installation context](installation-context.md) are displayed in the Add/Remove Programs of the current user.</span></span> <span data-ttu-id="aea48-110">Приложения, установленные в контексте установки на компьютере, отображаются в окне "Установка и удаление программ" для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="aea48-110">Applications that have been installed in the per-machine installation context are displayed in the Add/Remove Programs of all users.</span></span> <span data-ttu-id="aea48-111">Приложения, которые не были установлены для каждого компьютера и установлены только как приложения для отдельных пользователей, кроме текущего пользователя, не отображаются в окне "Установка и удаление программ" текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="aea48-111">Applications that have not been installed per-machine, and have only been installed as per-user applications for users other than the current user, do not appear in the Add/Remove Programs of the current user.</span></span>

<span data-ttu-id="aea48-112">Обратите внимание, что пакеты установки, использующие свойство [**лимитуи**](limitui.md) , также должны содержать [**арпномодифи**](arpnomodify.md).</span><span class="sxs-lookup"><span data-stu-id="aea48-112">Note that installation packages that use the [**LIMITUI**](limitui.md) property must also contain the [**ARPNOMODIFY**](arpnomodify.md).</span></span> <span data-ttu-id="aea48-113">Это необходимо, чтобы пользователь получил правильное поведение из окна "Установка и удаление программ" в служебной программе "Панель управления" при попытке настроить продукт.</span><span class="sxs-lookup"><span data-stu-id="aea48-113">This is required for a user to obtain the correct behavior from Add/Remove Programs in Control Panel utility when attempting to configure a product.</span></span>

<span data-ttu-id="aea48-114">Установщик использует следующие [Общие свойства](public-properties.md) для управления компонентом "Установка и удаление программ" на панели управления.</span><span class="sxs-lookup"><span data-stu-id="aea48-114">The installer uses the following [public properties](public-properties.md) to manage Add/Remove Programs in Control Panel.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aea48-115">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="aea48-115">Property name</span></span></th>
<th><span data-ttu-id="aea48-116">Краткое описание свойства</span><span class="sxs-lookup"><span data-stu-id="aea48-116">Brief description of property</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aea48-117"><a href="arpauthorizedcdfprefix.md"><strong>арпаусоризедкдфпрефикс</strong></a></span><span class="sxs-lookup"><span data-stu-id="aea48-117"><a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a></span></span></td>
<td><span data-ttu-id="aea48-118">URL-адрес канала обновления для приложения.</span><span class="sxs-lookup"><span data-stu-id="aea48-118">URL of the update channel for the application.</span></span> <span data-ttu-id="aea48-119">Значение, записываемое установщиком в <a href="uninstall-registry-key.md">раздел реестра Uninstall</a>.</span><span class="sxs-lookup"><span data-stu-id="aea48-119">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aea48-120"><a href="arpcomments.md"><strong>арпкомментс</strong></a></span><span class="sxs-lookup"><span data-stu-id="aea48-120"><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></span></span></td>
<td><span data-ttu-id="aea48-121">Содержит комментарии для компонента «Установка и удаление программ» на панели управления.</span><span class="sxs-lookup"><span data-stu-id="aea48-121">Provides Comments for the Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="aea48-122">Значение, записываемое установщиком в <a href="uninstall-registry-key.md">раздел реестра Uninstall</a>.</span><span class="sxs-lookup"><span data-stu-id="aea48-122">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aea48-123"><a href="arpcontact.md"><strong>арпконтакт</strong></a></span><span class="sxs-lookup"><span data-stu-id="aea48-123"><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></span></span></td>
<td><span data-ttu-id="aea48-124">Предоставляет контакт для компонента "Установка и удаление программ" на панели управления.</span><span class="sxs-lookup"><span data-stu-id="aea48-124">Provides the Contact for Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="aea48-125">Значение, записываемое установщиком в <a href="uninstall-registry-key.md">раздел реестра Uninstall</a>.</span><span class="sxs-lookup"><span data-stu-id="aea48-125">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aea48-126"><a href="arpinstalllocation.md"><strong>арпинсталллокатион</strong></a></span><span class="sxs-lookup"><span data-stu-id="aea48-126"><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></span></span></td>
<td><span data-ttu-id="aea48-127">Полный путь к первичной папке приложения.</span><span class="sxs-lookup"><span data-stu-id="aea48-127">Fully qualified path to the application's primary folder.</span></span> <span data-ttu-id="aea48-128">Значение, записываемое установщиком в <a href="uninstall-registry-key.md">раздел реестра Uninstall</a>.</span><span class="sxs-lookup"><span data-stu-id="aea48-128">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aea48-129"><a href="arphelplink.md"><strong>арфелплинк</strong></a></span><span class="sxs-lookup"><span data-stu-id="aea48-129"><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></span></span></td>
<td><span data-ttu-id="aea48-130">Адрес в Интернете (или URL-адрес) для службы технической поддержки.</span><span class="sxs-lookup"><span data-stu-id="aea48-130">Internet address, or URL, for technical support.</span></span> <span data-ttu-id="aea48-131">Значение, записываемое установщиком в <a href="uninstall-registry-key.md">раздел реестра Uninstall</a>.</span><span class="sxs-lookup"><span data-stu-id="aea48-131">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aea48-132"><a href="arphelptelephone.md"><strong>арфелптелефоне</strong></a></span><span class="sxs-lookup"><span data-stu-id="aea48-132"><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></span></span></td>
<td><span data-ttu-id="aea48-133">Номера телефонов технической поддержки.</span><span class="sxs-lookup"><span data-stu-id="aea48-133">Technical support phone numbers.</span></span> <span data-ttu-id="aea48-134">Значение, записываемое установщиком в <a href="uninstall-registry-key.md">раздел реестра Uninstall</a>.</span><span class="sxs-lookup"><span data-stu-id="aea48-134">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aea48-135"><a href="arpnomodify.md"><strong>арпномодифи</strong></a></span><span class="sxs-lookup"><span data-stu-id="aea48-135"><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></span></span></td>
<td><span data-ttu-id="aea48-136">Предотвращает отображение кнопки изменения для продукта в окне Установка и удаление программ на панели управления.</span><span class="sxs-lookup"><span data-stu-id="aea48-136">Prevents display of a Change button for the product in Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="aea48-137">
<b>Примечание.</b> Это влияет только на отображение в ARP.</span><span class="sxs-lookup"><span data-stu-id="aea48-137">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="aea48-138">Установщик Windows по-прежнему поддерживает восстановление, установку по запросу и удаление приложений с помощью командной строки или программного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="aea48-138">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aea48-139"><a href="arpnoremove.md"><strong>арпноремове</strong></a></span><span class="sxs-lookup"><span data-stu-id="aea48-139"><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></span></span></td>
<td><span data-ttu-id="aea48-140">Предотвращает отображение кнопки Удалить для продукта в окне Установка и удаление программ на панели управления.</span><span class="sxs-lookup"><span data-stu-id="aea48-140">Prevents display of a Remove button for the product in the Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="aea48-141">Продукт по-прежнему можно удалить, нажав кнопку изменить, если установочный пакет был создан с помощью пользовательского интерфейса, который предоставляет возможность удаления продукта.</span><span class="sxs-lookup"><span data-stu-id="aea48-141">The product can still be removed by selecting the Change button if the installation package has been authored with a user interface that provides product removal as an option.</span></span>
<blockquote><span data-ttu-id="aea48-142">
<b>Примечание.</b> Это влияет только на отображение в ARP.</span><span class="sxs-lookup"><span data-stu-id="aea48-142">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="aea48-143">Установщик Windows по-прежнему поддерживает восстановление, установку по запросу и удаление приложений с помощью командной строки или программного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="aea48-143">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aea48-144"><a href="arpnorepair.md"><strong>арпнорепаир</strong></a></span><span class="sxs-lookup"><span data-stu-id="aea48-144"><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></span></span></td>
<td><span data-ttu-id="aea48-145">Отключает кнопку восстановить в окне Установка и удаление программ на панели управления.</span><span class="sxs-lookup"><span data-stu-id="aea48-145">Disables the Repair button in the Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="aea48-146">
<b>Примечание.</b> Это влияет только на отображение в ARP.</span><span class="sxs-lookup"><span data-stu-id="aea48-146">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="aea48-147">Установщик Windows по-прежнему поддерживает восстановление, установку по запросу и удаление приложений с помощью командной строки или программного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="aea48-147">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aea48-148"><a href="arpproducticon.md"><strong>арппродуктикон</strong></a></span><span class="sxs-lookup"><span data-stu-id="aea48-148"><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></span></span></td>
<td><span data-ttu-id="aea48-149">Определяет значок, отображаемый в окне "Установка и удаление программ".</span><span class="sxs-lookup"><span data-stu-id="aea48-149">Identifies the icon displayed in Add/Remove Programs.</span></span> <span data-ttu-id="aea48-150">Если это свойство не определено, то в окне Установка и удаление программ задается значок вывода.</span><span class="sxs-lookup"><span data-stu-id="aea48-150">If this property is not defined, Add/Remove Programs specifies the display icon.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aea48-151"><a href="arpreadme.md"><strong>арпреадме</strong></a></span><span class="sxs-lookup"><span data-stu-id="aea48-151"><a href="arpreadme.md"><strong>ARPREADME</strong></a></span></span></td>
<td><span data-ttu-id="aea48-152">Содержит файл сведений для компонента «Установка и удаление программ» на панели управления.</span><span class="sxs-lookup"><span data-stu-id="aea48-152">Provides the ReadMe for Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="aea48-153">Значение, записываемое установщиком в <a href="uninstall-registry-key.md">раздел реестра Uninstall</a>.</span><span class="sxs-lookup"><span data-stu-id="aea48-153">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aea48-154"><a href="arpsize.md"><strong>арпсизе</strong></a></span><span class="sxs-lookup"><span data-stu-id="aea48-154"><a href="arpsize.md"><strong>ARPSIZE</strong></a></span></span></td>
<td><span data-ttu-id="aea48-155">Предполагаемый размер приложения в КБ.</span><span class="sxs-lookup"><span data-stu-id="aea48-155">Estimated size of the application in KB.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aea48-156"><a href="arpsystemcomponent.md"><strong>арпсистемкомпонент</strong></a></span><span class="sxs-lookup"><span data-stu-id="aea48-156"><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="aea48-157">Предотвращает отображение приложения в списке "программы" окна "Установка и удаление программ" на панели управления.</span><span class="sxs-lookup"><span data-stu-id="aea48-157">Prevents display of the application in the Programs List of the Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="aea48-158">
<b>Примечание.</b> Это влияет только на отображение в ARP.</span><span class="sxs-lookup"><span data-stu-id="aea48-158">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="aea48-159">Установщик Windows по-прежнему поддерживает восстановление, установку по запросу и удаление приложений с помощью командной строки или программного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="aea48-159">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aea48-160"><a href="arpurlinfoabout.md"><strong>арпурлинфоабаут</strong></a></span><span class="sxs-lookup"><span data-stu-id="aea48-160"><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></span></span></td>
<td><span data-ttu-id="aea48-161">URL-адрес домашней страницы приложения.</span><span class="sxs-lookup"><span data-stu-id="aea48-161">URL for application's home page.</span></span> <span data-ttu-id="aea48-162">Значение, записываемое установщиком в <a href="uninstall-registry-key.md">раздел реестра Uninstall</a>.</span><span class="sxs-lookup"><span data-stu-id="aea48-162">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aea48-163"><a href="arpurlupdateinfo.md"><strong>арпурлупдатеинфо</strong></a></span><span class="sxs-lookup"><span data-stu-id="aea48-163"><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></span></span></td>
<td><span data-ttu-id="aea48-164">URL-адрес для сведений об обновлении приложения.</span><span class="sxs-lookup"><span data-stu-id="aea48-164">URL for application update information.</span></span> <span data-ttu-id="aea48-165">Значение, записываемое установщиком в <a href="uninstall-registry-key.md">раздел реестра Uninstall</a>.</span><span class="sxs-lookup"><span data-stu-id="aea48-165">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
</tbody>
</table>

> [!Note]  
> <span data-ttu-id="aea48-166">Сведения о средстве установки программы и значений по умолчанию см. в разделе [Работа с настройками доступа к программам и параметров по умолчанию для компьютера](/previous-versions//bb776877(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="aea48-166">For information regarding the Set Program and Defaults tool, refer to the section [Working with Set Program Access and Computer Defaults](/previous-versions//bb776877(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aea48-167">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="aea48-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aea48-168">Удалить раздел реестра</span><span class="sxs-lookup"><span data-stu-id="aea48-168">Uninstall Registry Key</span></span>](uninstall-registry-key.md)
</dt> </dl>
