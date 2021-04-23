---
title: Простой тип filePath
description: Определяет строку, содержащую полный путь к файлу.
ms.assetid: a9b8f40a-fecd-4325-b068-a5aca3133134
keywords:
- Журнал событий простого типа filePath
topic_type:
- apiref
api_name:
- filePath
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 492580634c1a48c88df6f50de2582c215ec7ecb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489501"
---
# <a name="filepath-simple-type"></a><span data-ttu-id="19e62-104">Простой тип filePath</span><span class="sxs-lookup"><span data-stu-id="19e62-104">filePath Simple Type</span></span>

<span data-ttu-id="19e62-105">Определяет строку, содержащую полный путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="19e62-105">Defines a string that contains a fully qualified path to a file.</span></span> <span data-ttu-id="19e62-106">Путь может содержать переменные среды.</span><span class="sxs-lookup"><span data-stu-id="19e62-106">The path may contain environment variables.</span></span>

``` syntax
<xs:simpleType name="filePath">
    <xs:restriction
        base="xs:string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="19e62-107">Требования</span><span class="sxs-lookup"><span data-stu-id="19e62-107">Requirements</span></span>



| <span data-ttu-id="19e62-108">Требование</span><span class="sxs-lookup"><span data-stu-id="19e62-108">Requirement</span></span> | <span data-ttu-id="19e62-109">Значение</span><span class="sxs-lookup"><span data-stu-id="19e62-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="19e62-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19e62-110">Minimum supported client</span></span><br/> | <span data-ttu-id="19e62-111">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="19e62-111">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="19e62-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19e62-112">Minimum supported server</span></span><br/> | <span data-ttu-id="19e62-113">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="19e62-113">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





