---
description: Инструментарий WMI использует пути к объектам в ссылочных свойствах классов ассоциаций для обнаружения связанных объектов, а также для использования путей к объектам в входных или выходных параметрах для нескольких методов.
ms.assetid: 07fee6f8-810e-4dec-8f0f-787756ee3beb
ms.tgt_platform: multiple
title: Требования к пути к объектам WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b46195eae3e8351c9c611a34c28cc9d5dd58d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423837"
---
# <a name="wmi-object-path-requirements"></a><span data-ttu-id="df6ac-103">Требования к пути к объектам WMI</span><span class="sxs-lookup"><span data-stu-id="df6ac-103">WMI Object Path Requirements</span></span>

<span data-ttu-id="df6ac-104">Инструментарий WMI использует пути к объектам в ссылочных свойствах классов ассоциаций для обнаружения связанных объектов, а также для использования путей к объектам в входных или выходных параметрах для нескольких методов.</span><span class="sxs-lookup"><span data-stu-id="df6ac-104">WMI uses object paths in the reference properties of association classes to identify related objects, as well as using object paths in input or output parameters for several methods.</span></span> <span data-ttu-id="df6ac-105">Поскольку пути к объектам обрабатываются как строки для поиска и сравнения, значение пути к объекту при использовании в качестве ссылочного свойства всегда является самой строкой, а не объектом разыменования.</span><span class="sxs-lookup"><span data-stu-id="df6ac-105">Because object paths are treated as strings for the purpose of lookup and comparison, the value of an object path when used as a reference property is always the string itself and not the dereferenced object.</span></span> <span data-ttu-id="df6ac-106">При сравнении строк, которые работают с путями объектов, всегда учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="df6ac-106">String comparisons that deal with object paths are always case-insensitive.</span></span>

<span data-ttu-id="df6ac-107">Путь к объекту может использовать следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="df6ac-107">An object path can use the following syntax:</span></span>

-   <span data-ttu-id="df6ac-108">Строки, содержащиеся в одинарных кавычках.</span><span class="sxs-lookup"><span data-stu-id="df6ac-108">Strings contained in single quotation marks.</span></span>
-   <span data-ttu-id="df6ac-109">Косые черты в качестве разделителей.</span><span class="sxs-lookup"><span data-stu-id="df6ac-109">Forward slashes as separators.</span></span>
-   <span data-ttu-id="df6ac-110">Символы обратной косой черты в качестве разделителей.</span><span class="sxs-lookup"><span data-stu-id="df6ac-110">Backslashes as separators.</span></span>
-   <span data-ttu-id="df6ac-111">Шестнадцатеричные константы для целых чисел.</span><span class="sxs-lookup"><span data-stu-id="df6ac-111">Hexadecimal constants for integers.</span></span>
-   <span data-ttu-id="df6ac-112">Логические константы для классов с ключами, принимающими логические значения.</span><span class="sxs-lookup"><span data-stu-id="df6ac-112">Boolean constants for classes with keys that take Boolean values.</span></span>
-   <span data-ttu-id="df6ac-113">Нотация URL-адреса для представления непечатаемых символов, например %20, для пустого пространства.</span><span class="sxs-lookup"><span data-stu-id="df6ac-113">URL notation to represent nonprinting characters, such as %20 for a blank space.</span></span>

<span data-ttu-id="df6ac-114">Кроме того, строка пути к объекту должна соблюдать следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="df6ac-114">In addition, an object path string must obey the following restrictions:</span></span>

-   <span data-ttu-id="df6ac-115">Предполагается, что локальный сервер с частичным путем к пространству имен.</span><span class="sxs-lookup"><span data-stu-id="df6ac-115">An assumed local server with a partial namespace path.</span></span> <span data-ttu-id="df6ac-116">Таким словами, Указание корневого и пространства имен по умолчанию подразумевает корневое и пространство имен по умолчанию на локальном сервере.</span><span class="sxs-lookup"><span data-stu-id="df6ac-116">Thus, specifying the root and default namespace implies the root and default namespace on the local server.</span></span>
-   <span data-ttu-id="df6ac-117">Нет пробелов ни в одном элементе, ни между элементами.</span><span class="sxs-lookup"><span data-stu-id="df6ac-117">No white space either within an element or between elements.</span></span>
-   <span data-ttu-id="df6ac-118">Внедренные кавычки в путях к объектам разрешены, но они должны разделять кавычки escape-символами, как в приложениях C или C++.</span><span class="sxs-lookup"><span data-stu-id="df6ac-118">Embedded quotation marks in object paths are allowed but must delimit the quotation mark with escape characters, as in a C or C++ application.</span></span>
-   <span data-ttu-id="df6ac-119">Только десятичные значения распознаются как числовые части ключей.</span><span class="sxs-lookup"><span data-stu-id="df6ac-119">Only decimal values are recognized as numeric portions of keys.</span></span>

 

 



