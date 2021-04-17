---
description: Буферы для конкретных устройств могут быть частью реализации расширенных операций поставщика услуг. Значение этих буферов определяется поставщиком услуг.
ms.assetid: 5783f892-ec11-4340-afad-44f2ef55fd18
title: Буфер конкретного устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 628ee93e4f88fc733e744b3c52af3c0a1c31ecf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673719"
---
# <a name="device-specific-buffer"></a><span data-ttu-id="f195b-104">Буфер конкретного устройства</span><span class="sxs-lookup"><span data-stu-id="f195b-104">Device-specific Buffer</span></span>

<span data-ttu-id="f195b-105">Буферы для конкретных устройств могут быть частью реализации расширенных операций поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="f195b-105">Device-specific buffers may be part of a service provider's implementation of extended operations.</span></span> <span data-ttu-id="f195b-106">Значение этих буферов определяется поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="f195b-106">The service provider defines the meaning of these buffers.</span></span>

<span data-ttu-id="f195b-107">Не все поставщики служб поддерживают использование этих сведений.</span><span class="sxs-lookup"><span data-stu-id="f195b-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="f195b-108">**Интерфейс TAPI 2. x:** См. раздел [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**двдевспеЦификсизе** and **двдевспеЦификоффсет** Members of [**линекаллинфо**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span><span class="sxs-lookup"><span data-stu-id="f195b-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwDevSpecificSize** and **dwDevSpecificOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span></span>

<span data-ttu-id="f195b-109">**Интерфейс TAPI 3. x:** См. раздел [**иткаллинфо:: жеткаллинфобуффер**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer) (**ЦИБ \_ девспеЦификбуффер** Member в [**каллинфо \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span><span class="sxs-lookup"><span data-stu-id="f195b-109">**TAPI 3.x:** See [**ITCallInfo::GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer) (**CIB\_DEVSPECIFICBUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span></span>

 

 
