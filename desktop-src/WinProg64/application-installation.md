---
title: Установка приложения в 64-разрядных системах
description: 64-разрядная установщик Windows может легко установить 32-разрядные приложения на основе MSI в 64-bit Windows.
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- Установка приложения 64-разрядное программирование для Windows
- Установка 64-разрядное программирование для Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13a5f8f623776ffa637718fc0d565f2c71a7b8e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134139"
---
# <a name="application-installation-on-64-bit-systems"></a><span data-ttu-id="763f7-105">Установка приложения в 64-разрядных системах</span><span class="sxs-lookup"><span data-stu-id="763f7-105">Application Installation on 64-bit Systems</span></span>

<span data-ttu-id="763f7-106">[64-разрядная установщик Windows](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) может легко установить 32-разрядные приложения на основе MSI в 64-bit Windows.</span><span class="sxs-lookup"><span data-stu-id="763f7-106">The [64-bit Windows Installer](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) can seamlessly install 32-bit MSI-based applications on 64-bit Windows.</span></span> <span data-ttu-id="763f7-107">Для более старых приложений, использующих 16-разрядную заглушку для запуска 32-разрядного модуля установки, 64-разрядная версия Windows распознает определенные 16-разрядные программы установки и под32 ставляет побайтовую отправку.</span><span class="sxs-lookup"><span data-stu-id="763f7-107">For older applications that use a 16-bit stub to launch a 32-bit installation engine, 64-bit Windows recognizes specific 16-bit installer programs and substitutes a ported 32-bit version.</span></span>

<span data-ttu-id="763f7-108">16-разрядные приложения DOS, Windows или OS/2 часто используют 16-разрядную заглушку для проверки типа компьютера, а затем запуска подсистему установки 32-bit для фактического выполнения установки.</span><span class="sxs-lookup"><span data-stu-id="763f7-108">16-bit DOS, Windows, or OS/2 applications often use a 16-bit stub to check the machine type, then launch a 32-bit installation engine to actually perform the installation.</span></span> <span data-ttu-id="763f7-109">Чтобы разрешить установку приложений, использующих этот метод, 64-разрядная ОС Windows подставляет 32-разрядные версии для следующих 16-разрядных программ установщика:</span><span class="sxs-lookup"><span data-stu-id="763f7-109">To enable installation of applications that use this technique, 64-bit Windows substitutes 32-bit versions for the following 16-bit installer programs:</span></span>

* <span data-ttu-id="763f7-110">Программа установки Microsoft для Windows 1,2</span><span class="sxs-lookup"><span data-stu-id="763f7-110">Microsoft Setup for Windows 1.2</span></span>  
* <span data-ttu-id="763f7-111">Программа установки Microsoft для Windows 2,6</span><span class="sxs-lookup"><span data-stu-id="763f7-111">Microsoft Setup for Windows 2.6</span></span>  
* <span data-ttu-id="763f7-112">Программа установки Microsoft для Windows 3,0</span><span class="sxs-lookup"><span data-stu-id="763f7-112">Microsoft Setup for Windows 3.0</span></span>  
* <span data-ttu-id="763f7-113">Программа установки Microsoft для Windows 3,01</span><span class="sxs-lookup"><span data-stu-id="763f7-113">Microsoft Setup for Windows 3.01</span></span>  
* <span data-ttu-id="763f7-114">InstallShield 5. x</span><span class="sxs-lookup"><span data-stu-id="763f7-114">InstallShield 5.x</span></span>  

<span data-ttu-id="763f7-115">Список подстановок хранится в реестре в следующем разделе: **hKey \_ Local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64**.</span><span class="sxs-lookup"><span data-stu-id="763f7-115">The list of substitutions is stored in the registry under the following key: **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\NtVdm64**.</span></span>

> [!Note]  
> <span data-ttu-id="763f7-116">Этот механизм предоставляется только для обеспечения совместимости с 32-разрядными приложениями, которые используют 16-разрядные программы установщика Майкрософт, перечисленные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="763f7-116">This mechanism is provided only for compatibility with 32-bit applications that use the 16-bit Microsoft installer programs listed in this topic.</span></span> <span data-ttu-id="763f7-117">Добавление программ сторонних разработчиков не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="763f7-117">Addition of third-party installer programs is not supported.</span></span>

 

> [!Note]  
> <span data-ttu-id="763f7-118">Этот механизм не включен в Windows 10 на ARM.</span><span class="sxs-lookup"><span data-stu-id="763f7-118">This mechanism is not included on Windows 10 on ARM.</span></span>

 

 

 