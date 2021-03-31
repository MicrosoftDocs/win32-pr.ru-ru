---
title: Типы данных DNS (Винднс. h)
ms.assetid: 652012a5-e45d-4ea6-896a-17e8b1ed4a05
description: 'Дополнительные сведения: типы данных DNS'
keywords:
- IP4_ADDRESS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2caa113670a749029b70df9772d6e2707684b7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264518"
---
# <a name="dns-data-types"></a><span data-ttu-id="c3840-104">Типы данных DNS</span><span class="sxs-lookup"><span data-stu-id="c3840-104">DNS Data Types</span></span>

<span data-ttu-id="c3840-105">Для DNS определены следующие типы данных:</span><span class="sxs-lookup"><span data-stu-id="c3840-105">The following data types are defined for DNS:</span></span>


```C++
typedef DWORD IP4_ADDRESS;
```



<dl> <dt>

<span data-ttu-id="c3840-106">**IP4- \_ адрес**</span><span class="sxs-lookup"><span data-stu-id="c3840-106">**IP4\_ADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="c3840-107">Значение, представляющее адрес протокола IP версии 4 (IPv4).</span><span class="sxs-lookup"><span data-stu-id="c3840-107">A value that represents an Internet Protocol version 4 (IPv4) address.</span></span> <span data-ttu-id="c3840-108">Например, разделенный точками десятичный IPv4-адрес ( **127.0.0.1**) представлен в порядке байтов узла как **0x7F000001**.</span><span class="sxs-lookup"><span data-stu-id="c3840-108">For example, the dotted decimal IPv4 address, **127.0.0.1**, is represented in host byte order as **0x7F000001**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3840-109">Требования</span><span class="sxs-lookup"><span data-stu-id="c3840-109">Requirements</span></span>



| <span data-ttu-id="c3840-110">Требование</span><span class="sxs-lookup"><span data-stu-id="c3840-110">Requirement</span></span> | <span data-ttu-id="c3840-111">Значение</span><span class="sxs-lookup"><span data-stu-id="c3840-111">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c3840-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3840-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c3840-113">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c3840-113">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c3840-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3840-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c3840-115">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c3840-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c3840-116">Header</span><span class="sxs-lookup"><span data-stu-id="c3840-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3840-117"><dt>Винднс. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3840-117"><dt>Windns.h</dt></span></span> </dl> |



 

 





