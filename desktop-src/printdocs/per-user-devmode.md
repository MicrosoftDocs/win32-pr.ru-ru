---
description: Пользователь может указать параметры документа по умолчанию для принтера. Это называется DEVMODE для каждого пользователя, так как он влияет только на значения по умолчанию для конкретного пользователя, а сведения для каждого принтера определяются в отдельной структуре DEVMODE.
ms.assetid: f791f847-c31e-4a06-93cb-49117d8f0cb8
title: Per-User DEVMODE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dee5a79d314e0f9ab89210ba4d2644d2b8ec99c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702209"
---
# <a name="per-user-devmode"></a><span data-ttu-id="3a034-104">Per-User DEVMODE</span><span class="sxs-lookup"><span data-stu-id="3a034-104">Per-User DEVMODE</span></span>

<span data-ttu-id="3a034-105">Пользователь может указать параметры документа по умолчанию для принтера.</span><span class="sxs-lookup"><span data-stu-id="3a034-105">A user can specify the default document settings for a printer.</span></span> <span data-ttu-id="3a034-106">Это называется DEVMODE для *каждого пользователя* , так как он влияет только на значения по умолчанию для конкретного пользователя, а сведения для каждого принтера определяются в отдельной структуре [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .</span><span class="sxs-lookup"><span data-stu-id="3a034-106">This is called the *per-user DEVMODE* because it only affects the defaults for a particular user, and the information for each printer is defined in a separate [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>

<span data-ttu-id="3a034-107">Чтобы задать DEVMODE для каждого пользователя, вызовите [**сетпринтер**](setprinter.md) со структурой [**Printer \_ info \_ 2**](printer-info-2.md) или [**Printer \_ info \_ 9**](printer-info-9.md) .</span><span class="sxs-lookup"><span data-stu-id="3a034-107">To set the per-user DEVMODE, call [**SetPrinter**](setprinter.md) with either the [**PRINTER\_INFO\_2**](printer-info-2.md) or the [**PRINTER\_INFO\_9**](printer-info-9.md) structure.</span></span> <span data-ttu-id="3a034-108">Чтобы сбросить DEVMODE для каждого пользователя до глобального [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)по умолчанию, вызовите **сетпринтер** с помощью структуры [**Printer \_ info \_ 8**](printer-info-8.md) .</span><span class="sxs-lookup"><span data-stu-id="3a034-108">To reset the per-user DEVMODE to the global default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), call **SetPrinter** with the [**PRINTER\_INFO\_8**](printer-info-8.md) structure.</span></span>

 

 



