---
description: Определяет типы беспроводных сетей.
ms.assetid: 03236db9-4f58-4fe3-82ff-d4b3a387490a
title: Простой тип Нетворктипетипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d0acb998c879e718a0e201418610bb0aa6db8c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684230"
---
# <a name="networktypetype-simple-type"></a><span data-ttu-id="afbd6-103">Простой тип Нетворктипетипе</span><span class="sxs-lookup"><span data-stu-id="afbd6-103">networkTypeType Simple Type</span></span>

<span data-ttu-id="afbd6-104">Простой тип Нетворктипетипе определяет типы беспроводных сетей.</span><span class="sxs-lookup"><span data-stu-id="afbd6-104">The networkTypeType simple type defines the wireless network types.</span></span> <span data-ttu-id="afbd6-105">Существует два типа сетей: сети инфраструктуры (ESS) и ad-hoc Network (ИБСС).</span><span class="sxs-lookup"><span data-stu-id="afbd6-105">There are two types of networks: infrastructure networks (ESS) and ad-hoc networks (IBSS).</span></span>

``` syntax
<xs:simpleType name="networkTypeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="IBSS"
         />
        <xs:enumeration
            value="ESS"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="afbd6-106">Значения перечисления</span><span class="sxs-lookup"><span data-stu-id="afbd6-106">Enumeration values</span></span>

<span data-ttu-id="afbd6-107">Простой тип **нетворктипетипе** определяет следующие значения.</span><span class="sxs-lookup"><span data-stu-id="afbd6-107">The **networkTypeType** simple type defines the following values.</span></span>



| <span data-ttu-id="afbd6-108">Значение</span><span class="sxs-lookup"><span data-stu-id="afbd6-108">Value</span></span> | <span data-ttu-id="afbd6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="afbd6-109">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="afbd6-110">ибсс</span><span class="sxs-lookup"><span data-stu-id="afbd6-110">IBSS</span></span>  |             |
| <span data-ttu-id="afbd6-111">ДИСТАНЦИОН</span><span class="sxs-lookup"><span data-stu-id="afbd6-111">ESS</span></span>   |             |



## <a name="requirements"></a><span data-ttu-id="afbd6-112">Требования</span><span class="sxs-lookup"><span data-stu-id="afbd6-112">Requirements</span></span>



| <span data-ttu-id="afbd6-113">Требование</span><span class="sxs-lookup"><span data-stu-id="afbd6-113">Requirement</span></span> | <span data-ttu-id="afbd6-114">Значение</span><span class="sxs-lookup"><span data-stu-id="afbd6-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="afbd6-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="afbd6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="afbd6-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="afbd6-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="afbd6-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="afbd6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="afbd6-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="afbd6-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




