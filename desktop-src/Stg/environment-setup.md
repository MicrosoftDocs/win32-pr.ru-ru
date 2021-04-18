---
title: Настройка среды
description: Установленный пакет средств разработки программного обеспечения платформы (SDK) предоставляет Setenv.bat файл, расположенный в корневом каталоге пакета SDK платформы, который можно запустить, чтобы настроить среду для создания приложений, использующих пакет SDK для платформы.
ms.assetid: 2dec3d7a-acac-4ff7-9d4a-d3540e6d441d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f752872b96e4b02cbfd1724d8a4a99ca1de13f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661537"
---
# <a name="environment-setup"></a><span data-ttu-id="82560-103">Настройка среды</span><span class="sxs-lookup"><span data-stu-id="82560-103">Environment Setup</span></span>

<span data-ttu-id="82560-104">Установленный пакет средств разработки программного обеспечения платформы (SDK) предоставляет Setenv.bat файл, расположенный в корневом каталоге пакета SDK платформы, который можно запустить, чтобы настроить среду для создания приложений, использующих пакет SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="82560-104">The installed Platform Software Development Kit (SDK) provides a Setenv.bat file located in the root directory of the Platform SDK that you can run to set up your environment for building applications that use the Platform SDK.</span></span>

## <a name="settings-and-variables"></a><span data-ttu-id="82560-105">Параметры и переменные</span><span class="sxs-lookup"><span data-stu-id="82560-105">Settings and Variables</span></span>

<span data-ttu-id="82560-106">Можно также вручную настроить среду, добавив в файл Autoexec.bat что-то вроде следующего:</span><span class="sxs-lookup"><span data-stu-id="82560-106">You can also manually set up your environment by adding something like the following to your Autoexec.bat file.</span></span> <span data-ttu-id="82560-107">С помощью Windows можно изменить файл Autoexec.bat, чтобы включить эти команды.</span><span class="sxs-lookup"><span data-stu-id="82560-107">Using Windows, you can edit the Autoexec.bat file to include these commands.</span></span> <span data-ttu-id="82560-108">С помощью Windows Server 2003, Windows XP, Windows 2000 или Windows NT можно изменить или добавить эти параметры в переменные среды с помощью диалогового окна система, которое можно запустить из панели управления.</span><span class="sxs-lookup"><span data-stu-id="82560-108">Using Windows Server 2003, Windows XP, Windows 2000, or Windows NT, you can edit or add these settings to your environment variables using the System dialog that you can run from the Control Panel.</span></span>


```cmd
  SET INCLUDE=D:\MSSDK\INCLUDE;C:\MSDEV\INCLUDE;C:\MSDEV\ATL\INCLUDE
  SET LIB=D:\MSSDK\LIB;C:\MSDEV\LIB
  SET MSSDK=D:\MSSDK
  SET MSTOOLS=D:\MSSDK
  SET CPU=i386
  SET PATH=C:\WIN95;C:\WIN95\COMMAND;C:\DOS;D:\MSSDK\BIN;C:\MSDEV\BIN
```



<span data-ttu-id="82560-109">Эти параметры подходят для платформы Intel 80386 или более поздней версии с Windows Me, Windows 98 или Windows 95 вместе с Microsoft Visual C++ и с установленным пакетом SDK платформы.</span><span class="sxs-lookup"><span data-stu-id="82560-109">These settings are appropriate for an Intel 80386 or later platform running Windows Me, Windows 98, or Windows 95 with both Microsoft Visual C++ and the Platform SDK installed.</span></span> <span data-ttu-id="82560-110">Например, в этой системе Visual C++ версии 5,0 устанавливается в каталог C: \\ мсдев.</span><span class="sxs-lookup"><span data-stu-id="82560-110">For example, on this system, Visual C++ version 5.0 is installed under the C:\\MSDEV directory.</span></span> <span data-ttu-id="82560-111">Пакет Platform SDK устанавливается в каталог D: \\ мссдк.</span><span class="sxs-lookup"><span data-stu-id="82560-111">The Platform SDK is installed under the D:\\MSSDK directory.</span></span> <span data-ttu-id="82560-112">Конфигурация диска может отличаться.</span><span class="sxs-lookup"><span data-stu-id="82560-112">Your disk configuration may be different.</span></span> <span data-ttu-id="82560-113">Каталоги пакета SDK для платформы (в данном примере — с D: \\ мссдк) являются более ранними в каждой последовательности путей.</span><span class="sxs-lookup"><span data-stu-id="82560-113">The Platform SDK directories (for this example, those with D:\\MSSDK in them) are all earlier in each path sequence.</span></span> <span data-ttu-id="82560-114">В этой последовательности предполагается, что компиляция из командной строки должна выполняться в окне Командная строка, а файлы библиотеки include и lib в Platform SDK являются предпочтительными для этих компиляций.</span><span class="sxs-lookup"><span data-stu-id="82560-114">This sequence assumes that command line compilations are intended to be run in the Command Prompt window and that the .h include and .lib library files in the Platform SDK are preferred for those compilations.</span></span>

<span data-ttu-id="82560-115">Переменная среды ЦП определяется для управления сборками Win32 в зависимости от платформы.</span><span class="sxs-lookup"><span data-stu-id="82560-115">The CPU environment variable is defined to control the Win32 builds, depending on the platform.</span></span> <span data-ttu-id="82560-116">К текущим возможным значениям относятся i386, MIPS, ALPHA и PPC.</span><span class="sxs-lookup"><span data-stu-id="82560-116">Current possible values include i386, MIPS, ALPHA, and PPC.</span></span> <span data-ttu-id="82560-117">Дополнительные сведения см. в файле Win32. MAK, приведенном в пакете Platform SDK, \\ в \\ каталоге мссдк include.</span><span class="sxs-lookup"><span data-stu-id="82560-117">For more information, see the Win32.mak file provided in the Platform SDK in the \\MSSDK\\INCLUDE directory.</span></span> <span data-ttu-id="82560-118">Все примеры файлов makefile с примером кода учебника COM включают Win32. MAK.</span><span class="sxs-lookup"><span data-stu-id="82560-118">All of the COM tutorial code sample makefiles include Win32.mak.</span></span>

 

 




