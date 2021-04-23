---
description: Тип данных ХКРИПТКЭЙ используется для представления дескрипторов криптографических ключей.
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: ХКРИПТКЭЙ (Винкрипт. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56bda14169aa2f4d7c6e502d3444473ea0f00408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664120"
---
# <a name="hcryptkey"></a><span data-ttu-id="2f751-103">хкрипткэй</span><span class="sxs-lookup"><span data-stu-id="2f751-103">HCRYPTKEY</span></span>

<span data-ttu-id="2f751-104">Тип данных **хкрипткэй** используется для представления дескрипторов [*криптографических ключей*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2f751-104">The **HCRYPTKEY** data type is used to represent handles to [*cryptographic keys*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="2f751-105">Эти дескрипторы используются для указания модулю CSP, какой ключ используется в конкретной операции.</span><span class="sxs-lookup"><span data-stu-id="2f751-105">These handles are used to indicate to the CSP module which key is being used in a specific operation.</span></span> <span data-ttu-id="2f751-106">Модуль CSP не обеспечивает прямой доступ к значениям ключей.</span><span class="sxs-lookup"><span data-stu-id="2f751-106">The CSP module does not enable direct access to the key values.</span></span> <span data-ttu-id="2f751-107">Вместо этого пользователь выполняет функции, используя значение ключа через маркер ключа.</span><span class="sxs-lookup"><span data-stu-id="2f751-107">Instead, the user performs functions by using the key value through the key handle.</span></span>


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a><span data-ttu-id="2f751-108">Требования</span><span class="sxs-lookup"><span data-stu-id="2f751-108">Requirements</span></span>



| <span data-ttu-id="2f751-109">Требование</span><span class="sxs-lookup"><span data-stu-id="2f751-109">Requirement</span></span> | <span data-ttu-id="2f751-110">Значение</span><span class="sxs-lookup"><span data-stu-id="2f751-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f751-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f751-111">Minimum supported client</span></span><br/> | <span data-ttu-id="2f751-112">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2f751-112">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2f751-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f751-113">Minimum supported server</span></span><br/> | <span data-ttu-id="2f751-114">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2f751-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f751-115">Header</span><span class="sxs-lookup"><span data-stu-id="2f751-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f751-116"><dt>Винкрипт. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f751-116"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
