---
title: Настройка службы имен для Windows 3. x или MS-DOS
description: Удаленный вызов процедур (RPC) и Настройка службы имен для Windows 3. x или MS-DOS.
ms.assetid: 7b22a12e-43d0-4e32-a191-d63a56559143
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533a0d8556f9cc51d0842768d0df1bdd0d553b5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068130"
---
# <a name="configuring-the-name-service-for-windows-3x-or-ms-dos"></a><span data-ttu-id="cbcc8-103">Настройка службы имен для Windows 3. x или MS-DOS</span><span class="sxs-lookup"><span data-stu-id="cbcc8-103">Configuring the Name Service for Windows 3.x or MS-DOS</span></span>

<span data-ttu-id="cbcc8-104">При запуске Setup.exe для установки 16-разрядной библиотеки времени выполнения RPC выводится запрос на выбор поставщика службы имен:</span><span class="sxs-lookup"><span data-stu-id="cbcc8-104">When you run Setup.exe to install the 16-bit RPC run-time library, it prompts you to select a name service provider:</span></span>

-   <span data-ttu-id="cbcc8-105">Если выбран вариант **установить поставщик службы имен по умолчанию**, устанавливается по умолчанию NSP, локатор Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="cbcc8-105">If you choose **Install Default Name Service Provider**, the default NSP, Microsoft Locator, is installed.</span></span>
-   <span data-ttu-id="cbcc8-106">Если выбран вариант **установить поставщик службы настраиваемых имен**, заполните диалоговое окно **Определение сетевого адреса** , чтобы установить службу каталогов ЯЧЕЕК DCE в качестве NSP.</span><span class="sxs-lookup"><span data-stu-id="cbcc8-106">If you choose **Install Custom Name Service Provider**, complete the **Define Network Address** dialog box to install the DCE Cell Directory Service as your NSP.</span></span> <span data-ttu-id="cbcc8-107">Служба каталогов ячеек DCE — это NSP, используемый с серверами DCE.</span><span class="sxs-lookup"><span data-stu-id="cbcc8-107">The DCE Cell Directory Service is the NSP used with DCE servers.</span></span>

<span data-ttu-id="cbcc8-108">Сетевой адрес — это имя главного компьютера, на котором работает управляющая программа NSI (нсид).</span><span class="sxs-lookup"><span data-stu-id="cbcc8-108">The network address is the name of the host computer that runs the NSI daemon (nsid).</span></span> <span data-ttu-id="cbcc8-109">Этот компьютер выступает в качестве шлюза для службы каталогов ячеек DCE и передает вызовы функций NSI между компьютерами, на которых работают операционные системы Майкрософт и компьютеры DCE.</span><span class="sxs-lookup"><span data-stu-id="cbcc8-109">This computer acts as a gateway to the DCE Cell Directory Service, passing NSI function calls between computers that run Microsoft operating systems and DCE computers.</span></span> <span data-ttu-id="cbcc8-110">Сетевой адрес может содержать не более 80 символов, например, 11.1.9.169 является допустимым адресом.</span><span class="sxs-lookup"><span data-stu-id="cbcc8-110">The network address can be 80 characters or less—for example, 11.1.9.169 is a valid address.</span></span>

 

 




