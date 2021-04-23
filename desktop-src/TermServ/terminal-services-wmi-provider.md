---
title: Поставщик WMI службы удаленных рабочих столов
description: Поставщик WMI службы удаленных рабочих столов предоставляет программный доступ к сведениям и параметрам, предоставляемым оснасткой «Настройка службы удаленных рабочих столов/подключения консоли управления Майкрософт (MMC)».
ms.assetid: d205a3da-3f9a-4ee1-9c99-a39e9cce0a11
ms.tgt_platform: multiple
keywords:
- Службы удаленных рабочих столов службы удаленных рабочих столов, поставщик WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d947db18c0cde63bcb6c4c3954fc9811e0f0f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070167"
---
# <a name="remote-desktop-services-wmi-provider"></a><span data-ttu-id="0bb43-104">Поставщик WMI службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="0bb43-104">Remote Desktop Services WMI provider</span></span>

<span data-ttu-id="0bb43-105">Поставщик WMI службы удаленных рабочих столов предоставляет программный доступ к сведениям и параметрам, предоставляемым оснасткой «Настройка службы удаленных рабочих столов/подключения консоли управления Майкрософт (MMC)».</span><span class="sxs-lookup"><span data-stu-id="0bb43-105">The Remote Desktop Services WMI provider provides programmatic access to the information and settings that are exposed by the Remote Desktop Services Configuration/Connections Microsoft Management Console (MMC) snap-in.</span></span>

<span data-ttu-id="0bb43-106">Библиотека DLL поставщика загружается процессом управления Windows (Winmgmt.exe), когда клиент выполняет запрос к серверу.</span><span class="sxs-lookup"><span data-stu-id="0bb43-106">The provider DLL is loaded by the Windows Management process (Winmgmt.exe) when a client makes a request to the server.</span></span> <span data-ttu-id="0bb43-107">Администрирование возможно с помощью методов поставщика.</span><span class="sxs-lookup"><span data-stu-id="0bb43-107">Administration is possible by using the provider methods.</span></span> <span data-ttu-id="0bb43-108">Поставщик регистрируется как экземпляр и как поставщик метода.</span><span class="sxs-lookup"><span data-stu-id="0bb43-108">The provider is registered as both an instance and a method provider.</span></span>

<span data-ttu-id="0bb43-109">Поставщик WMI службы удаленных рабочих столов реализован как динамический поставщик, производный от базового класса [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) , который наследует все его свойства и методы, а также внутрипроцессный библиотеку динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="0bb43-109">The Remote Desktop Services WMI provider has been implemented as a dynamic provider derived from the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) base class, inheriting all of its properties and methods, and an in-process dynamic link library.</span></span>

<span data-ttu-id="0bb43-110">Дополнительные сведения см. в [справочнике по поставщику WMI службы удаленных рабочих столов](terminal-services-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="0bb43-110">For more information, see the [Remote Desktop Services WMI Provider reference](terminal-services-wmi-provider-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bb43-111">См. также</span><span class="sxs-lookup"><span data-stu-id="0bb43-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bb43-112">Справочник по поставщику службы удаленных рабочих столов WMI</span><span class="sxs-lookup"><span data-stu-id="0bb43-112">Remote Desktop Services WMI Provider Reference</span></span>](terminal-services-wmi-provider-reference.md)
</dt> </dl>

 

 