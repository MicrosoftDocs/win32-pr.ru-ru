---
description: Mergemod.dll предоставляет COM-объект, который реализует операции слияния и создание образов источника для модулей слияния. Основной объект реализует интерфейсы для программ C/C++ и клиентов автоматизации, включая Visual Basic и VBScript.
ms.assetid: 877d3691-948f-4aea-89d8-0ff008126ccc
title: Автоматизация модуля слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ae27370b2ad898cf9413567285afc41d117815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651173"
---
# <a name="merge-module-automation"></a><span data-ttu-id="ea314-104">Автоматизация модуля слияния</span><span class="sxs-lookup"><span data-stu-id="ea314-104">Merge Module Automation</span></span>

<span data-ttu-id="ea314-105">Mergemod.dll предоставляет COM-объект, который реализует операции слияния и создание образов источника для модулей слияния.</span><span class="sxs-lookup"><span data-stu-id="ea314-105">Mergemod.dll provides a COM object that implements merge operations and source image generation for merge modules.</span></span> <span data-ttu-id="ea314-106">Основной объект реализует интерфейсы для программ C/C++ и клиентов автоматизации, включая Visual Basic и VBScript.</span><span class="sxs-lookup"><span data-stu-id="ea314-106">The main object implements interfaces for C/C++ programs and automation clients, including Visual Basic and VBScript.</span></span>

<span data-ttu-id="ea314-107">Предпочтительный метод установки Mergemod.dll — с помощью установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="ea314-107">The preferred method for installing Mergemod.dll is by using the Windows Installer.</span></span> <span data-ttu-id="ea314-108">Идентификатор компонента для компонента, содержащего COM-интерфейс Mergemod.dll, — {FD153241-37EC-11D2-8892-00A0C981B015}.</span><span class="sxs-lookup"><span data-stu-id="ea314-108">The Component ID for the component containing the Mergemod.dll COM interface is {FD153241-37EC-11D2-8892-00A0C981B015}.</span></span> <span data-ttu-id="ea314-109">Один и тот же двоичный файл можно использовать во всех системах Windows, и библиотека DLL будет самостоятельно регистрироваться с помощью программы regsvr32 в старых системах.</span><span class="sxs-lookup"><span data-stu-id="ea314-109">The same binary can be used on all Windows systems and the dll will self-register through regsvr32 on older systems.</span></span>

<span data-ttu-id="ea314-110">Обратите внимание, что Mergemod.dll требует, чтобы Msvcrt.dll была установлена в системе.</span><span class="sxs-lookup"><span data-stu-id="ea314-110">Note that Mergemod.dll requires that the Msvcrt.dll be installed on the system.</span></span>

<span data-ttu-id="ea314-111">Обратите внимание, что для создания [настраиваемых модулей слияния](configurable-merge-modules.md)требуется Mergemod.dll 2,0.</span><span class="sxs-lookup"><span data-stu-id="ea314-111">Note that Mergemod.dll 2.0 is required to create [Configurable Merge Modules](configurable-merge-modules.md).</span></span> <span data-ttu-id="ea314-112">Mergemod.dll версии 2,0 предоставляет расширенную функциональность во время сборки через интерфейс [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) .</span><span class="sxs-lookup"><span data-stu-id="ea314-112">Mergemod.dll version 2.0 provides extended functionality at build time through the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) Interface.</span></span> <span data-ttu-id="ea314-113">Этот CLSID поддерживает все существующие функции интерфейса [**имсммерже**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) , предоставляемые Mergemod.dll версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="ea314-113">This CLSID supports all the existing functionality of the [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) Interface provided by Mergemod.dll version 1.0.</span></span> <span data-ttu-id="ea314-114">Интерфейсом по умолчанию для объекта [**слияния**](merge-object.md) Mergemod.dll 2,0 является интерфейс **IMsmMerge2** , а не интерфейс **имсммерже** .</span><span class="sxs-lookup"><span data-stu-id="ea314-114">The default interface on the [**Merge**](merge-object.md) object of Mergemod.dll 2.0 is the **IMsmMerge2** interface instead of the **IMsmMerge** interface.</span></span>

[<span data-ttu-id="ea314-115">Объектная модель для Mergemod.dll версии 1,0</span><span class="sxs-lookup"><span data-stu-id="ea314-115">Object Model for Mergemod.dll Version 1.0</span></span>](object-model-for-mergemod-dll-version-1-0.md)

[<span data-ttu-id="ea314-116">Объектная модель для Mergemod.dll версии 2,0</span><span class="sxs-lookup"><span data-stu-id="ea314-116">Object Model for Mergemod.dll Version 2.0</span></span>](object-model-for-mergemod-dll-version-2-0.md)

 

 
