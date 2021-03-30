---
description: Непрозрачные дескрипторы используются в ТСПИ для ссылки на структуры данных, представляющие линии, телефоны и внешний вид вызовов.
ms.assetid: aa1742aa-6cd4-461a-ad92-972eefcf637f
title: Непрозрачные дескрипторы и закрытые структуры данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cd8c7b911de5f85f84b56a8e25e28eb805c5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991290"
---
# <a name="opaque-handles-and-private-data-structures"></a><span data-ttu-id="b5601-103">Непрозрачные дескрипторы и закрытые структуры данных</span><span class="sxs-lookup"><span data-stu-id="b5601-103">Opaque Handles and Private Data Structures</span></span>

<span data-ttu-id="b5601-104">Непрозрачные дескрипторы используются в ТСПИ для ссылки на структуры данных, представляющие линии, телефоны и внешний вид вызовов.</span><span class="sxs-lookup"><span data-stu-id="b5601-104">Opaque handles are used in TSPI to refer to the data structures representing lines, phones, and call appearances.</span></span> <span data-ttu-id="b5601-105">Они отображаются как параметры большинства функций и обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="b5601-105">These appear as parameters to most of the functions and callbacks.</span></span> <span data-ttu-id="b5601-106">Существует несколько функций, которые ссылаются на устройство, используя идентификатор устройства вместо непрозрачного маркера.</span><span class="sxs-lookup"><span data-stu-id="b5601-106">There are few functions that refer to the device using a device identifier instead of an opaque handle.</span></span> <span data-ttu-id="b5601-107">В этом случае ссылка указывает на само устройство, а не на структуру данных.</span><span class="sxs-lookup"><span data-stu-id="b5601-107">In such a case, the reference is to the device itself rather than to a data structure.</span></span> <span data-ttu-id="b5601-108">Функции, которые работают таким образом, обычно вызываются на ранних этапах инициализации до создания структур данных и обмена непрозрачными дескрипторами.</span><span class="sxs-lookup"><span data-stu-id="b5601-108">Functions that work in this fashion are typically those called at early initialization times before data structures are created and opaque handles are exchanged.</span></span>

<span data-ttu-id="b5601-109">Поставщик услуг должен решить, как интерпретировать эти дескрипторы.</span><span class="sxs-lookup"><span data-stu-id="b5601-109">The service provider must decide how to interpret these handles.</span></span> <span data-ttu-id="b5601-110">Поставщик услуг обычно использует указатель на структуру данных или индекс в массиве структур данных в качестве непрозрачного маркера.</span><span class="sxs-lookup"><span data-stu-id="b5601-110">A service provider typically uses the pointer to its data structure or to the index into an array of data structures as its opaque handle.</span></span> <span data-ttu-id="b5601-111">Единственное ограничение заключается в том, что поставщик услуг не может использовать значение 0 в качестве [хдрвлине](hdrvline.md), Хдрвкалл или [хдрвфоне](hdrvphone.md).</span><span class="sxs-lookup"><span data-stu-id="b5601-111">The only restriction is that the service provider cannot use the value 0 as an [HDRVLINE](hdrvline.md), HDRVCALL, or [HDRVPHONE](hdrvphone.md).</span></span> <span data-ttu-id="b5601-112">Значение 0 или **null** для маркера имеет специальное значение в некоторых операциях.</span><span class="sxs-lookup"><span data-stu-id="b5601-112">The value 0 or **NULL** for a handle has a special meaning in some operations.</span></span>

 

 



