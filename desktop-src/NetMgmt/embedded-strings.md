---
title: Внедренные строки
description: Информационные структуры не будут содержать встроенные строки. Это улучшает выравнивание информационных структур и обеспечивает гибкость в основных функциях для OEM.
ms.assetid: a3272a0a-5352-4847-84fd-113b4467c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c71ed50971661f9ad06855024ecba2796f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777114"
---
# <a name="embedded-strings"></a><span data-ttu-id="26982-104">Внедренные строки</span><span class="sxs-lookup"><span data-stu-id="26982-104">Embedded Strings</span></span>

<span data-ttu-id="26982-105">Информационные структуры не будут содержать встроенные строки.</span><span class="sxs-lookup"><span data-stu-id="26982-105">Information structures will not contain embedded strings.</span></span> <span data-ttu-id="26982-106">Это улучшает выравнивание информационных структур и обеспечивает гибкость в основных функциях для OEM.</span><span class="sxs-lookup"><span data-stu-id="26982-106">This improves the alignment of the information structures and allows for OEM flexibility in the core functions.</span></span>

<span data-ttu-id="26982-107">Любое информационное поле, возвращаемое в вызове перечисления, которое может быть впоследствии использовано в качестве ключа для вызова функции управления сетью с подробными данными, гарантированно находится в буфере перечисления.</span><span class="sxs-lookup"><span data-stu-id="26982-107">Any information field that is returned in an enumeration call that can be subsequently used as a key for the call to a GetInfo network management function is guaranteed to be present in the enumeration buffer.</span></span> <span data-ttu-id="26982-108">Если строка со строкой переменной длины, указывающая значение ключевого поля, не будет помещаться, вся структура фиксированной длины для записи не возвращается.</span><span class="sxs-lookup"><span data-stu-id="26982-108">If the variable-length information string that would specify the key field value will not fit, then the entire fixed-length structure for the entry is not returned.</span></span> <span data-ttu-id="26982-109">Другие поля переменной длины будут возвращены как указатель **null** для случая, в котором строка не умещается.</span><span class="sxs-lookup"><span data-stu-id="26982-109">Other variable-length fields will be returned as a **NULL** pointer for the case in which the string does not fit.</span></span>

 

 




