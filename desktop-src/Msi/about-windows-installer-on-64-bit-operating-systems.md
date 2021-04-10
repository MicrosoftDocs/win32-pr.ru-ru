---
description: Установщик Windows работает как служба на компьютерах, использующих 32-разрядную или 64-разрядную версию Windows.
ms.assetid: c02fc401-0c9c-49f6-adcc-ed36bdb18fca
title: Сведения о установщик Windows в 64-разрядных операционных системах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe9969a3fc1ccd9b63f6bd75b145f9dbc7d8c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "104273129"
---
# <a name="about-windows-installer-on-64-bit-operating-systems"></a><span data-ttu-id="996b1-103">Сведения о установщик Windows в 64-разрядных операционных системах</span><span class="sxs-lookup"><span data-stu-id="996b1-103">About Windows Installer on 64-Bit Operating Systems</span></span>

<span data-ttu-id="996b1-104">Установщик Windows работает как служба на компьютерах, использующих 32-разрядную или 64-разрядную версию Windows.</span><span class="sxs-lookup"><span data-stu-id="996b1-104">Windows Installer runs as a service on computers using 32-bit or 64-bit Windows.</span></span> <span data-ttu-id="996b1-105">Версии установщика, предшествующие версии 2,0, могут устанавливать 32-разрядные пакеты установщик Windows и управлять ими только в 32-разрядных операционных системах.</span><span class="sxs-lookup"><span data-stu-id="996b1-105">Versions of the installer earlier than version 2.0 can install and manage 32-bit Windows Installer Packages only on 32-bit operating systems.</span></span> <span data-ttu-id="996b1-106">Обратите внимание, что невозможно объявить или установить 64-разрядное приложение в 32-разрядной операционной системе.</span><span class="sxs-lookup"><span data-stu-id="996b1-106">Note that you cannot advertise or install a 64-bit application on a 32-bit operating system.</span></span>

<span data-ttu-id="996b1-107">Пакет установщик Windows должен быть указан как 32-разрядный или 64-разрядный пакет; Он не может быть указан как нейтральный.</span><span class="sxs-lookup"><span data-stu-id="996b1-107">A Windows Installer package must be specified as either a 32-bit or a 64-bit package; it cannot be specified as neutral.</span></span> <span data-ttu-id="996b1-108">На компьютере, использующем 64-разрядную операционную систему, служба установщик Windows размещается в 64-разрядном процессе, который устанавливает как 32-разрядные, так и 64-разрядные пакеты.</span><span class="sxs-lookup"><span data-stu-id="996b1-108">On a computer using a 64-bit operating system, the Windows Installer service is hosted in a 64-bit process that installs both 32-bit and 64-bit packages.</span></span> <span data-ttu-id="996b1-109">Установщик Windows устанавливает три типа пакетов установщика Windows на компьютере, работающем под управлением 64-разрядной операционной системы:</span><span class="sxs-lookup"><span data-stu-id="996b1-109">Windows Installer installs three types of Windows installer packages on a computer running a 64-bit operating system:</span></span>

-   <span data-ttu-id="996b1-110">32-разрядные пакеты, содержащие только 32-разрядные компоненты.</span><span class="sxs-lookup"><span data-stu-id="996b1-110">32-bit packages that contain only 32-bit components.</span></span>
-   <span data-ttu-id="996b1-111">64-разрядные пакеты, содержащие некоторые 32-разрядные компоненты.</span><span class="sxs-lookup"><span data-stu-id="996b1-111">64-bit packages containing some 32-bit components.</span></span>
-   <span data-ttu-id="996b1-112">64-разрядные пакеты, содержащие только 64-разрядные компоненты.</span><span class="sxs-lookup"><span data-stu-id="996b1-112">64-bit packages containing only 64-bit components.</span></span>

<span data-ttu-id="996b1-113">В следующих разделах описываются два типа пакетов установщик Windows и новые свойства установщика, предоставляемые установщик Windows для 64-разрядных пакетов.</span><span class="sxs-lookup"><span data-stu-id="996b1-113">The follow sections describe the two types of Windows Installer packages and the new installer properties provided by Windows Installer for 64-bit packages.</span></span>

[<span data-ttu-id="996b1-114">32-разрядные пакеты установщик Windows</span><span class="sxs-lookup"><span data-stu-id="996b1-114">32-bit Windows Installer Packages</span></span>](32-bit-windows-installer-packages.md)

[<span data-ttu-id="996b1-115">64-разрядные пакеты установщик Windows</span><span class="sxs-lookup"><span data-stu-id="996b1-115">64-bit Windows Installer Packages</span></span>](64-bit-windows-installer-packages.md)

## <a name="related-topics"></a><span data-ttu-id="996b1-116">См. также</span><span class="sxs-lookup"><span data-stu-id="996b1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="996b1-117">Использование 64-разрядных пакетов установщик Windows</span><span class="sxs-lookup"><span data-stu-id="996b1-117">Using 64-Bit Windows Installer Packages</span></span>](using-64-bit-windows-installer-packages.md)
</dt> </dl>

 

 



