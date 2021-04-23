---
title: show cachestate
description: Перечисляет все ресурсы и связанные с ними свойства, которые кэшируются в кэше HTTP-ответов, или отображает один ресурс и связанные с ним свойства.
ms.assetid: 9daa445e-dd2f-4b73-8938-58df931c015b
keywords:
- показывать качестате HTTP
topic_type:
- apiref
api_name:
- show cachestate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 088a59eaa92db8ed9e8cbe59075d540507e51535
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "104335048"
---
# <a name="show-cachestate"></a><span data-ttu-id="3d2d8-104">show cachestate</span><span class="sxs-lookup"><span data-stu-id="3d2d8-104">show cachestate</span></span>

<span data-ttu-id="3d2d8-105">Перечисляет все ресурсы и связанные с ними свойства, которые кэшируются в кэше HTTP-ответов, или отображает один ресурс и связанные с ним свойства.</span><span class="sxs-lookup"><span data-stu-id="3d2d8-105">Lists all resources and their associated properties that are cached in the HTTP response cache or displays a single resource and its associated properties.</span></span>

``` syntax
show cachestate [[url=]string]
 
```

## <a name="parameters"></a><span data-ttu-id="3d2d8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d2d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d2d8-107"><span id="__url__string_"></span><span id="__URL__STRING_"></span>**\[\[URL-адрес = \] ***строка***\]**</span><span class="sxs-lookup"><span data-stu-id="3d2d8-107"><span id="__url__string_"></span><span id="__URL__STRING_"></span>**\[\[url=\]***string***\]**</span></span>
</dt> <dd>

<span data-ttu-id="3d2d8-108">Полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="3d2d8-108">Fully qualified URL.</span></span> <span data-ttu-id="3d2d8-109">Если не указано, подразумевает использование всех URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="3d2d8-109">If unspecified, implies all URLs.</span></span> <span data-ttu-id="3d2d8-110">URL-адрес также может быть префиксом для зарегистрированных URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="3d2d8-110">The URL can also be a prefix to registered URLs.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="3d2d8-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="3d2d8-111">Examples</span></span>

<span data-ttu-id="3d2d8-112">**показывать URL-адрес качестате =https://www.contoso.com:80/myresource**</span><span class="sxs-lookup"><span data-stu-id="3d2d8-112">**show cachestate url=https://www.contoso.com:80/myresource**</span></span>

 

 




