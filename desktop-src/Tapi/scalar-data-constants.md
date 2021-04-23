---
description: Для расширяемых скалярных констант данных поставщик поставщика услуг может определять новые значения в указанном диапазоне.
ms.assetid: 62280b71-9bec-4a9d-abd2-d3e1c2cee43f
title: Константы скалярных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3187d2064501727614dfcbf0b8e11c136fea13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819424"
---
# <a name="scalar-data-constants"></a><span data-ttu-id="9a47e-103">Константы скалярных данных</span><span class="sxs-lookup"><span data-stu-id="9a47e-103">Scalar Data Constants</span></span>

<span data-ttu-id="9a47e-104">Для расширяемых скалярных констант данных поставщик поставщика услуг может определять новые значения в указанном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="9a47e-104">For extensible scalar data constants, a service-provider vendor can define new values in a specified range.</span></span> <span data-ttu-id="9a47e-105">Поскольку большинство констант данных имеют значение **DWORD**, то диапазон от 0X00000000 до 0x7FFFFFFF обычно резервируется для распространенных будущих расширений, а 0X80000000 по 0xFFFFFFFF доступен для расширений, зависящих от поставщика.</span><span class="sxs-lookup"><span data-stu-id="9a47e-105">Because most data constants are **DWORD** s, the range 0x00000000 through 0x7FFFFFFF is typically reserved for common future extensions, while 0x80000000 through 0xFFFFFFFF is available for vendor-specific extensions.</span></span> <span data-ttu-id="9a47e-106">Предполагается, что поставщик определит значения, которые являются естественными расширениями типов данных, определенных API.</span><span class="sxs-lookup"><span data-stu-id="9a47e-106">The assumption is that a vendor would define values that are natural extensions of the datatypes defined by the API.</span></span>

 

 



