---
description: Показывает, как использовать интерфейсы VSS для создания поставщика оборудования VSS.
ms.assetid: 4d3c3f3c-22d2-4246-afef-aee2a0bd52d6
title: Средство Всссамплепровидер и пример
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fceaa65b851e5469a3e82323da92d8bde0651a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692350"
---
# <a name="vsssampleprovider-tool-and-sample"></a><span data-ttu-id="54c70-103">Средство Всссамплепровидер и пример</span><span class="sxs-lookup"><span data-stu-id="54c70-103">VssSampleProvider Tool and Sample</span></span>

<span data-ttu-id="54c70-104">Показывает, как использовать [интерфейсы](volume-shadow-copy-api-interfaces.md) VSS для создания поставщика оборудования VSS.</span><span class="sxs-lookup"><span data-stu-id="54c70-104">Shows how to use the VSS [interfaces](volume-shadow-copy-api-interfaces.md) to create a VSS hardware provider.</span></span>

> [!Note]  
> <span data-ttu-id="54c70-105">Средство Всссамплепровидер и пример включены в пакет средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="54c70-105">The VssSampleProvider tool and sample are included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="54c70-106">Вы можете скачать Windows SDK из [пакета средств разработки программного обеспечения (SDK) для Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).</span><span class="sxs-lookup"><span data-stu-id="54c70-106">You can download the Windows SDK from [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).</span></span>

 

<span data-ttu-id="54c70-107">В Windows SDK установки средство Всссамплепровидер можно найти в `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (для 64-разрядной версии Windows) и `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (для 32-разрядной версии Windows).</span><span class="sxs-lookup"><span data-stu-id="54c70-107">In the Windows SDK installation, the VssSampleProvider tool can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

> [!Note]  
> <span data-ttu-id="54c70-108">Поставщики оборудования поддерживаются только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="54c70-108">Hardware providers are only supported on Windows Server operating systems.</span></span> <span data-ttu-id="54c70-109">В клиентской операционной системе Windows можно скомпилировать пример Всссамплепровидер, но нельзя зарегистрировать его в качестве поставщика оборудования.</span><span class="sxs-lookup"><span data-stu-id="54c70-109">On a Windows Client operating system, you can compile the VssSampleProvider sample, but you can't register it as a hardware provider.</span></span>

 

<span data-ttu-id="54c70-110">Средство Всссамплепровидер состоит из следующих файлов:</span><span class="sxs-lookup"><span data-stu-id="54c70-110">The VssSampleProvider tool consists of the following files:</span></span>

-   <span data-ttu-id="54c70-111">Virtualstorage.sys</span><span class="sxs-lookup"><span data-stu-id="54c70-111">Virtualstorage.sys</span></span>
-   <span data-ttu-id="54c70-112">Vstorcontrol.exe</span><span class="sxs-lookup"><span data-stu-id="54c70-112">Vstorcontrol.exe</span></span>
-   <span data-ttu-id="54c70-113">Vssampleprovider.dll</span><span class="sxs-lookup"><span data-stu-id="54c70-113">Vssampleprovider.dll</span></span>
-   <span data-ttu-id="54c70-114">Vstorinterface.dll</span><span class="sxs-lookup"><span data-stu-id="54c70-114">Vstorinterface.dll</span></span>

<span data-ttu-id="54c70-115">Пример Всссамплепровидер включает следующие скрипты установки и удаления:</span><span class="sxs-lookup"><span data-stu-id="54c70-115">The VssSampleProvider sample includes the following installation and uninstallation scripts:</span></span>

-   <span data-ttu-id="54c70-116">Инсталл-самплепровидер. cmd</span><span class="sxs-lookup"><span data-stu-id="54c70-116">Install-sampleprovider.cmd</span></span>
-   <span data-ttu-id="54c70-117">Унинсталл-самплепровидер. cmd</span><span class="sxs-lookup"><span data-stu-id="54c70-117">Uninstall-sampleprovider.cmd</span></span>
-   <span data-ttu-id="54c70-118">Регистрация \_app.vbs</span><span class="sxs-lookup"><span data-stu-id="54c70-118">Register\_app.vbs</span></span>

<span data-ttu-id="54c70-119">**Установка и использование образца Всссамплепровидер**</span><span class="sxs-lookup"><span data-stu-id="54c70-119">**To install and use the VssSampleProvider sample**</span></span>

1.  <span data-ttu-id="54c70-120">Перейдите к каталогу `Program Files (x86)\Windows Kits\8.0\bin\`.</span><span class="sxs-lookup"><span data-stu-id="54c70-120">Navigate to the `Program Files (x86)\Windows Kits\8.0\bin\` directory.</span></span> <span data-ttu-id="54c70-121">Этот каталог содержит virtualstoragevss.sys и vstorcontrol.exe.</span><span class="sxs-lookup"><span data-stu-id="54c70-121">This directory contains virtualstoragevss.sys and vstorcontrol.exe.</span></span>
2.  <span data-ttu-id="54c70-122">Откройте окно командной строки в указанном каталоге.</span><span class="sxs-lookup"><span data-stu-id="54c70-122">Open a command prompt window in the specified directory.</span></span>
3.  <span data-ttu-id="54c70-123">Чтобы установить драйвер виртуального хранилища, в окне командной строки введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="54c70-123">To install the virtual storage driver, in the command prompt window, type the following command:</span></span>

    ```cmd
    vstorcontrol.exe install
    ```

    

4.  <span data-ttu-id="54c70-124">Чтобы установить пример поставщика VSS, в окне командной строки введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="54c70-124">To install the VSS sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    install-sampleprovider.cmd
    ```

    

5.  <span data-ttu-id="54c70-125">Чтобы создать виртуальный LUN, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="54c70-125">To create a virtual LUN, do the following.</span></span>

    1.  <span data-ttu-id="54c70-126">В окне командной строки введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="54c70-126">In the command prompt window, type the following command:</span></span>

        ```cmd
        vstorcontrol.exe create fixeddisk -
        newimage C:\disk1.image -size 20M -storid "VSS Sample HW Provider"
        ```

        

        <span data-ttu-id="54c70-127">Эта команда создает виртуальный LUN, идентификатор хранения которого является **примером поставщика оборудования VSS**.</span><span class="sxs-lookup"><span data-stu-id="54c70-127">This command creates a virtual LUN whose storage identifier is **VSS Sample HW Provider**.</span></span> <span data-ttu-id="54c70-128">Чтобы создать дополнительные виртуальные LUN, повторите этот шаг.</span><span class="sxs-lookup"><span data-stu-id="54c70-128">To create additional virtual LUNs, repeat this step.</span></span>

        <span data-ttu-id="54c70-129">Пример поставщика VSS распознает LUN только в том случае, если **образец VSS поставщика оборудования** является частью идентификатора хранилища.</span><span class="sxs-lookup"><span data-stu-id="54c70-129">The VSS sample provider recognizes a LUN only if **VSS Sample HW Provider** is a part of the storage identifier.</span></span> <span data-ttu-id="54c70-130">Дополнительные сведения об идентификаторе хранилища см. в следующей записи блога.</span><span class="sxs-lookup"><span data-stu-id="54c70-130">For more information about the storage identifier, see the following blog post.</span></span>

        [<span data-ttu-id="54c70-131">LUN. Повторная синхронизация с Diskshadow и виртуальным хранилищем</span><span class="sxs-lookup"><span data-stu-id="54c70-131">LUN - Resync with Diskshadow and Virtual Storage</span></span>](https://blogs.msdn.microsoft.com/b/himanshu_kale/archive/2009/06/02/lun-resync-with-diskshadow-virtual-storage.aspx)

    2.  <span data-ttu-id="54c70-132">В окне командной строки используйте diskpart.exe, чтобы отформатировать виртуальный диск и назначить ему букву диска.</span><span class="sxs-lookup"><span data-stu-id="54c70-132">In the command prompt window, use diskpart.exe to format the virtual disk and assign a drive letter to it.</span></span>

        <span data-ttu-id="54c70-133">Ниже приведен пример сценария для выполнения в командной строке DiskPart.</span><span class="sxs-lookup"><span data-stu-id="54c70-133">Here is a sample script to run at the diskpart command prompt.</span></span>

        ```cmd
        Select disk 
        Create partition primary size=<size>
        Format FS=NTFS quick
        Assign Letter=<letter>
        Exit
        ```

        

6.  <span data-ttu-id="54c70-134">Чтобы запустить пример поставщика, в окне командной строки введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="54c70-134">To run the sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    Run vshadow.exe -p -nw <drive>
    ```

    

    <span data-ttu-id="54c70-135">*<drive>* представляет букву диска виртуального LUN.</span><span class="sxs-lookup"><span data-stu-id="54c70-135">*<drive>* represents the drive letter of the virtual LUN.</span></span>

7.  <span data-ttu-id="54c70-136">Чтобы удалить пример поставщика VSS, в окне командной строки введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="54c70-136">To uninstall the VSS sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    uninstall-sampleprovider.cmd
    ```

    

8.  <span data-ttu-id="54c70-137">Чтобы удалить драйвер виртуального хранилища, в окне командной строки введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="54c70-137">To uninstall the virtual storage driver, in the command prompt window, type the following command:</span></span>

    ```cmd
    vstorcontrol.exe uninstall
    ```

    

 

 



