---
title: show urlacl
description: Список DACL для указанного зарезервированного URL-адреса или всех зарезервированных URL-адресов.
ms.assetid: 8428583c-b420-408f-974f-670b6809fa3c
keywords:
- показывать urlacl HTTP
topic_type:
- apiref
api_name:
- show urlacl
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86f7856e70a1be327297bb3fd4b892b3bf39789
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "103987031"
---
# <a name="show-urlacl"></a><span data-ttu-id="a3d70-104">show urlacl</span><span class="sxs-lookup"><span data-stu-id="a3d70-104">show urlacl</span></span>

<span data-ttu-id="a3d70-105">Список DACL для указанного зарезервированного URL-адреса или всех зарезервированных URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="a3d70-105">Lists DACLs for the specified reserved URL or all reserved URLs.</span></span>

``` syntax
show urlacl [url=]string
 
```

## <a name="parameters"></a><span data-ttu-id="a3d70-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3d70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3d70-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[URL = \] \* \* \* строка*</span><span class="sxs-lookup"><span data-stu-id="a3d70-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[url=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="a3d70-108">Указывает полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="a3d70-108">Specifies the fully qualified URL.</span></span> <span data-ttu-id="a3d70-109">Если не указано, подразумевает использование всех URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="a3d70-109">If unspecified, implies all URLs.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="a3d70-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="a3d70-110">Examples</span></span>

<span data-ttu-id="a3d70-111">**показывать URL-адрес urlacl =https://+:80/MyUrl**</span><span class="sxs-lookup"><span data-stu-id="a3d70-111">**show urlacl url=https://+:80/MyUrl**</span></span>

<span data-ttu-id="a3d70-112">**показывать URL-адрес urlacl =https://www.contoso.com:80/MyUrl**</span><span class="sxs-lookup"><span data-stu-id="a3d70-112">**show urlacl url=https://www.contoso.com:80/MyUrl**</span></span>

 

 




