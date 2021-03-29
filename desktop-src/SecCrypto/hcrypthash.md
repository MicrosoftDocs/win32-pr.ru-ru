---
description: Тип данных ХКРИПСАШ используется для представления дескрипторов для хэш-объектов.
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: ХКРИПСАШ (Винкрипт. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a009350ed910627c1e6ec9ae33997ed20c7fec2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912031"
---
# <a name="hcrypthash"></a><span data-ttu-id="a2b0c-103">хкрипсаш</span><span class="sxs-lookup"><span data-stu-id="a2b0c-103">HCRYPTHASH</span></span>

<span data-ttu-id="a2b0c-104">Тип данных **хкрипсаш** используется для представления дескрипторов для [*хэш-объектов*](../secgloss/h-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a2b0c-104">The **HCRYPTHASH** data type is used to represent handles to [*hash objects*](../secgloss/h-gly.md).</span></span> <span data-ttu-id="a2b0c-105">Эти дескрипторы указывают модулю CSP, какой хэш используется в определенной операции.</span><span class="sxs-lookup"><span data-stu-id="a2b0c-105">These handles indicate to the CSP module which hash is being used in a particular operation.</span></span> <span data-ttu-id="a2b0c-106">Модуль CSP не включает прямую обработку хэш-значений.</span><span class="sxs-lookup"><span data-stu-id="a2b0c-106">The CSP module does not enable direct manipulation of the hash values.</span></span> <span data-ttu-id="a2b0c-107">Вместо этого пользователь управляет хэш-значениями с помощью хэш-маркера.</span><span class="sxs-lookup"><span data-stu-id="a2b0c-107">Instead, the user manipulates the hash values through the hash handle.</span></span>


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a><span data-ttu-id="a2b0c-108">Требования</span><span class="sxs-lookup"><span data-stu-id="a2b0c-108">Requirements</span></span>



| <span data-ttu-id="a2b0c-109">Требование</span><span class="sxs-lookup"><span data-stu-id="a2b0c-109">Requirement</span></span> | <span data-ttu-id="a2b0c-110">Значение</span><span class="sxs-lookup"><span data-stu-id="a2b0c-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2b0c-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2b0c-111">Minimum supported client</span></span><br/> | <span data-ttu-id="a2b0c-112">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a2b0c-112">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a2b0c-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2b0c-113">Minimum supported server</span></span><br/> | <span data-ttu-id="a2b0c-114">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a2b0c-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a2b0c-115">Header</span><span class="sxs-lookup"><span data-stu-id="a2b0c-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2b0c-116"><dt>Винкрипт. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2b0c-116"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
