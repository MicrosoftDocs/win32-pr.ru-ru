---
description: В этом разделе описываются вспомогательные функции, которые можно использовать для разработки пользовательских мониторов.
ms.assetid: 2c019183-9823-4e34-bb41-cf35f2731b8f
title: Мониторинг функций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9391927104196e282d4438c0b047e233d61f3619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897622"
---
# <a name="monitor-functions"></a><span data-ttu-id="b6142-103">Мониторинг функций</span><span class="sxs-lookup"><span data-stu-id="b6142-103">Monitor Functions</span></span>

<span data-ttu-id="b6142-104">В этом разделе описываются вспомогательные функции, которые можно использовать для разработки пользовательских мониторов.</span><span class="sxs-lookup"><span data-stu-id="b6142-104">This section describes the helper functions you can use to develop custom monitors.</span></span>



| <span data-ttu-id="b6142-105">Функция</span><span class="sxs-lookup"><span data-stu-id="b6142-105">Function</span></span>                                       | <span data-ttu-id="b6142-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b6142-106">Description</span></span>                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6142-107">дллжетмониторобжект</span><span class="sxs-lookup"><span data-stu-id="b6142-107">DllGetMonitorObject</span></span>](dllgetmonitorobject.md) | <span data-ttu-id="b6142-108">Создает экземпляр монитора.</span><span class="sxs-lookup"><span data-stu-id="b6142-108">Creates an instance of the monitor.</span></span>                                                                                                                              |
| [<span data-ttu-id="b6142-109">хтмлвалуетауникоде</span><span class="sxs-lookup"><span data-stu-id="b6142-109">HTMLValueToUnicode</span></span>](htmlvaluetounicode.md)   | <span data-ttu-id="b6142-110">Преобразует \_ строку версии HTML CP UTF8 в Юникод.</span><span class="sxs-lookup"><span data-stu-id="b6142-110">Converts an HTML CP\_UTF8 version string to Unicode.</span></span>                                                                                                             |
| [<span data-ttu-id="b6142-111">лоаддворд</span><span class="sxs-lookup"><span data-stu-id="b6142-111">LoadDWORD</span></span>](loaddword.md)                     | <span data-ttu-id="b6142-112">Загружает **DWORD** из строки конфигурации HTML.</span><span class="sxs-lookup"><span data-stu-id="b6142-112">Loads a **DWORD** from an HTML configuration string.</span></span>                                                                                                             |
| [<span data-ttu-id="b6142-113">лоадипаддрессес</span><span class="sxs-lookup"><span data-stu-id="b6142-113">LoadIPAddresses</span></span>](loadipaddresses.md)         | <span data-ttu-id="b6142-114">Загружает список IP-адресов из строки конфигурации HTML TEXTAREA.</span><span class="sxs-lookup"><span data-stu-id="b6142-114">Loads an IP address list from an HTML TEXTAREA configuration string.</span></span>                                                                                             |
| [<span data-ttu-id="b6142-115">лоадипксаддрессес</span><span class="sxs-lookup"><span data-stu-id="b6142-115">LoadIPXAddresses</span></span>](loadipxaddresses.md)       | <span data-ttu-id="b6142-116">Загружает список IPX-адресов из строки конфигурации HTML TEXTAREA.</span><span class="sxs-lookup"><span data-stu-id="b6142-116">Loads an IPX address list from an HTML TEXTAREA configuration string.</span></span>                                                                                            |
| [<span data-ttu-id="b6142-117">лоадмакаддрессес</span><span class="sxs-lookup"><span data-stu-id="b6142-117">LoadMACAddresses</span></span>](loadmacaddresses.md)       | <span data-ttu-id="b6142-118">Загружает список MAC-адресов из строки конфигурации HTML-элемента TEXTAREA.</span><span class="sxs-lookup"><span data-stu-id="b6142-118">Loads a MAC address list from an HTML TEXTAREA configuration string.</span></span>                                                                                             |
| [<span data-ttu-id="b6142-119">лоадстрингаддр</span><span class="sxs-lookup"><span data-stu-id="b6142-119">LoadStringAddr</span></span>](loadstringaddr.md)           | <span data-ttu-id="b6142-120">Преобразует строку (например, "157.54.32.45") в адрес **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b6142-120">Transforms a string (such as "157.54.32.45") to a **DWORD** address.</span></span>                                                                                             |
| [<span data-ttu-id="b6142-121">лоадтчар</span><span class="sxs-lookup"><span data-stu-id="b6142-121">LoadTCHAR</span></span>](loadtchar.md)                     | <span data-ttu-id="b6142-122">Выполняет поиск запрошенного имени переменной в строке конфигурации и выделяет достаточно места (с помощью **хеапаллокмемори**) для сохранения, копирования и возврата.</span><span class="sxs-lookup"><span data-stu-id="b6142-122">Searches for a requested variable name in the configuration string, and allocates sufficient space (by using **HeapAllocMemory**) to store, copy, and return it.</span></span> |
| [<span data-ttu-id="b6142-123">онлоадингдлл</span><span class="sxs-lookup"><span data-stu-id="b6142-123">OnLoadingDLL</span></span>](onloadingdll.md)               | <span data-ttu-id="b6142-124">Указывает, что библиотека DLL начала загрузку.</span><span class="sxs-lookup"><span data-stu-id="b6142-124">Indicates that the DLL has begun to load.</span></span> <span data-ttu-id="b6142-125">МКСВК вызывает эту функцию при первой загрузке библиотеки DLL монитора.</span><span class="sxs-lookup"><span data-stu-id="b6142-125">The MCSVC calls this function when it first loads the monitor DLL.</span></span>                                                     |



 

 

 



