---
title: Простой тип Версионтипе
description: Определяет шаблон, указывающий версию задачи.
ms.assetid: e9eebbc1-5465-4af6-8b97-f1fd5827442e
keywords:
- планировщик задач простого типа Версионтипе
topic_type:
- apiref
api_name:
- versionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df7010c6ecba29ad0ade80ce403018dd626d01cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340485"
---
# <a name="versiontype-simple-type"></a><span data-ttu-id="818a8-104">Простой тип Версионтипе</span><span class="sxs-lookup"><span data-stu-id="818a8-104">versionType Simple Type</span></span>

<span data-ttu-id="818a8-105">Определяет шаблон, указывающий версию задачи.</span><span class="sxs-lookup"><span data-stu-id="818a8-105">Defines a pattern that specifies a version of a task.</span></span>

``` syntax
<xs:simpleType name="versionType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\d+(\.\d+){1,3}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="818a8-106">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="818a8-106">Patterns</span></span>

<span data-ttu-id="818a8-107">Простой тип **версионтипе** — это **строка** , которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="818a8-107">The **versionType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `\d+(\.\d+){1,3}`

    <span data-ttu-id="818a8-108">Double, за которым следует один, два или три типа Double.</span><span class="sxs-lookup"><span data-stu-id="818a8-108">A double followed by one, two, or three doubles.</span></span> <span data-ttu-id="818a8-109">Например, 1,2 или 1.2.3.</span><span class="sxs-lookup"><span data-stu-id="818a8-109">For example, 1.2, or 1.2.3.</span></span>

## <a name="requirements"></a><span data-ttu-id="818a8-110">Требования</span><span class="sxs-lookup"><span data-stu-id="818a8-110">Requirements</span></span>



| <span data-ttu-id="818a8-111">Требование</span><span class="sxs-lookup"><span data-stu-id="818a8-111">Requirement</span></span> | <span data-ttu-id="818a8-112">Значение</span><span class="sxs-lookup"><span data-stu-id="818a8-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="818a8-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="818a8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="818a8-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="818a8-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="818a8-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="818a8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="818a8-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="818a8-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





