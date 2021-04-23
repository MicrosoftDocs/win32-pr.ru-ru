---
description: Библиотека DbgHelp реализуется DbgHelp.dll.
ms.assetid: 8ef1740d-c791-4fbd-8297-7207a987c09d
title: Версии DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811e92ba88bf38cb46274e2d2c716a620ea83b16
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806958"
---
# <a name="dbghelp-versions"></a><span data-ttu-id="bbc78-103">Версии DbgHelp</span><span class="sxs-lookup"><span data-stu-id="bbc78-103">DbgHelp Versions</span></span>

<span data-ttu-id="bbc78-104">Библиотека DbgHelp реализуется DbgHelp.dll.</span><span class="sxs-lookup"><span data-stu-id="bbc78-104">The DbgHelp library is implemented by DbgHelp.dll.</span></span> <span data-ttu-id="bbc78-105">Хотя эта библиотека DLL включена во все поддерживаемые версии Windows, она редко является самой актуальной версией DbgHelp.</span><span class="sxs-lookup"><span data-stu-id="bbc78-105">Although this DLL is included in all supported versions of Windows, it is rarely the most current version of DbgHelp available.</span></span> <span data-ttu-id="bbc78-106">Более того, версия DbgHelp, входящая в состав Windows, обладает ограниченной функциональностью других выпусков. в частности, она не поддерживает сервер символов и исходный сервер.</span><span class="sxs-lookup"><span data-stu-id="bbc78-106">Furthermore, the version of DbgHelp that ships in Windows has reduced functionality from the other releases-- specifically, it lacks support for Symbol Server and Source Server.</span></span>

<span data-ttu-id="bbc78-107">Новейшие версии DbgHelp.dll, SymSrv.dll и SrcSrv.dll доступны в составе пакета [средств отладки для Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) .</span><span class="sxs-lookup"><span data-stu-id="bbc78-107">The most current versions of DbgHelp.dll, SymSrv.dll, and SrcSrv.dll are available as a part of the [Debugging Tools For Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) package.</span></span> <span data-ttu-id="bbc78-108">Политики распространения для этих включенных библиотек DLL были специально разработаны для того, чтобы пользователи могли включать эти файлы в свои пакеты и выпуски.</span><span class="sxs-lookup"><span data-stu-id="bbc78-108">The redistribution policies for these included DLLs were specifically designed to make it as easy as possible for people to include these files in their own packages and releases.</span></span>

> [!Caution]  
> <span data-ttu-id="bbc78-109">Пользователи никогда не должны пытаться установить [средства отладки для версий windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) DbgHelp.dll в системные каталоги Windows, так как они не проверяются в этом сценарии и, скорее всего, будут дестабилизировать систему.</span><span class="sxs-lookup"><span data-stu-id="bbc78-109">Users should never attempt to install the [Debugging Tools For Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) versions of DbgHelp.dll into the Windows system directories because they are untested in this scenario and likely to destabilize the system.</span></span> <span data-ttu-id="bbc78-110">Существуют отдельные версии пакета отладки x64 и x86, и они необходимы для тех, кто заинтересован в поддержке обеих платформ.</span><span class="sxs-lookup"><span data-stu-id="bbc78-110">There are separate X64 and X86 versions of the debugging package and both are necessary for people interested in supporting both platforms.</span></span>

<span data-ttu-id="bbc78-111">Чтобы получить последнюю версию DbgHelp.dll, перейдите на страницу [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) и скачайте средства отладки для Windows.</span><span class="sxs-lookup"><span data-stu-id="bbc78-111">To obtain the latest version of DbgHelp.dll, go to [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) and download Debugging Tools for Windows.</span></span> <span data-ttu-id="bbc78-112">Сведения о правильной установке см. в разделе [вызов библиотеки DBGHELP](calling-the-dbghelp-library.md) .</span><span class="sxs-lookup"><span data-stu-id="bbc78-112">Refer to [Calling the DbgHelp Library](calling-the-dbghelp-library.md) for information on proper installation.</span></span>

> [!Note]  
> <span data-ttu-id="bbc78-113">Файл DbgHelp.dll, поставляемый в составе Windows, не является распространяемым.</span><span class="sxs-lookup"><span data-stu-id="bbc78-113">The DbgHelp.dll file that ships in Windows is not redistributable.</span></span>

<span data-ttu-id="bbc78-114">Многие версии DbgHelp включают дополнительные функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="bbc78-114">Many versions of DbgHelp include additional functionality.</span></span> <span data-ttu-id="bbc78-115">Чтобы убедиться, что для приложения доступна правильная версия DbgHelp, ознакомьтесь со сведениями о требованиях в конкретной справочной документации по API.</span><span class="sxs-lookup"><span data-stu-id="bbc78-115">To ensure that the correct version of DbgHelp is available for your application, review the Requirements information in the specific API reference documentation.</span></span>
