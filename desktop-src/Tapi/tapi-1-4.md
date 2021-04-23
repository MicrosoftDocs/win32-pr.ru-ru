---
description: TAPI 1,4 добавил ряд интерфейсов API, сообщений, констант и элементов структуры в спецификацию 1,3.
ms.assetid: 293f732f-0288-46d1-b542-d948c6179158
title: TAPI 1,4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32f4320043ada2e2ae5477a698bde63f28d2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998469"
---
# <a name="tapi-14"></a><span data-ttu-id="a19bf-103">TAPI 1,4</span><span class="sxs-lookup"><span data-stu-id="a19bf-103">TAPI 1.4</span></span>

<span data-ttu-id="a19bf-104">TAPI 1,4 добавил ряд интерфейсов API, сообщений, констант и элементов структуры в спецификацию 1,3.</span><span class="sxs-lookup"><span data-stu-id="a19bf-104">TAPI 1.4 added a number of APIs, messages, constants, and structure elements to the 1.3 specification.</span></span> <span data-ttu-id="a19bf-105">TAPI 1,4 поддерживает только 16-разрядные специалистами.</span><span class="sxs-lookup"><span data-stu-id="a19bf-105">TAPI 1.4 supports only 16-bit TSPs.</span></span> <span data-ttu-id="a19bf-106">Однако это позволяет разрабатывать 32-разрядные приложения, не беспокоясь об ограничениях для 16-разрядных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="a19bf-106">However, it does allow 32-bit applications to be developed without having to worry about the limitations of 16-bit Windows.</span></span>

<span data-ttu-id="a19bf-107">Файлы заголовков TAPI и ТСПИ используются для разработки обоих приложений как для TAPI 1,4, так и для TAPI 2. x.</span><span class="sxs-lookup"><span data-stu-id="a19bf-107">The TAPI and TSPI header files are used to develop both applications for both TAPI 1.4 and TAPI 2.x.</span></span> <span data-ttu-id="a19bf-108">Хотя в структурах между этими двумя спецификациями не было внесено много изменений, были внесены изменения в API (в частности, поддержка Юникода), которые делают то, что заголовки компилируются по-разному, в зависимости от \_ \_ константы текущей версии TAPI.</span><span class="sxs-lookup"><span data-stu-id="a19bf-108">While there were not many changes to the structures between these two specifications, there were changes to the API (specifically, Unicode support) that make it very important to note that the headers compile differently, depending on the TAPI\_CURRENT\_VERSION constant.</span></span> <span data-ttu-id="a19bf-109">Пример:</span><span class="sxs-lookup"><span data-stu-id="a19bf-109">For example:</span></span>

``` syntax
#define TAPI_CURRENT_VERSION 0x00010004
#include <tapi.h>
```

> [!Note]  
> <span data-ttu-id="a19bf-110">\_Текущая \_ версия TAPI должна быть определена для всех приложений TAPI.</span><span class="sxs-lookup"><span data-stu-id="a19bf-110">TAPI\_CURRENT\_VERSION should be defined for all TAPI applications.</span></span> <span data-ttu-id="a19bf-111">Хотя это и не является обязательным требованием для разработки TAPI 2. x, для этого могут возникнуть будущие изменения.</span><span class="sxs-lookup"><span data-stu-id="a19bf-111">While it is not strictly necessary for TAPI 2.x development, future changes could occur to require this.</span></span>

 

 

 



