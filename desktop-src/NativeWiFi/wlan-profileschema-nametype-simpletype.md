---
description: Содержит либо имя, либо описание профиля беспроводной локальной сети.
ms.assetid: cb30d76f-051f-4b90-a0e0-24088a99ca9b
title: Простой тип Наметипе (LAN_policy) (профиль)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e73e8bd013836767e2a943616407aea9f563fea2
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187833"
---
# <a name="nametype-simple-type-lan_policy-for-profileschema"></a><span data-ttu-id="a1a42-103">Простой тип Наметипе (LAN_policy) для профилесчема</span><span class="sxs-lookup"><span data-stu-id="a1a42-103">nameType Simple Type (LAN_policy) for profileschema</span></span>

<span data-ttu-id="a1a42-104">Простой тип Наметипе может содержать либо имя, либо описание профиля беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="a1a42-104">The nameType simple type can contain either the name or a description of a wireless LAN profile.</span></span> <span data-ttu-id="a1a42-105">Это строковое значение должно содержать от 1 до 255 символов.</span><span class="sxs-lookup"><span data-stu-id="a1a42-105">This string value must be between 1 and 255 characters long.</span></span>

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="a1a42-106">Требования</span><span class="sxs-lookup"><span data-stu-id="a1a42-106">Requirements</span></span>



| <span data-ttu-id="a1a42-107">Требование</span><span class="sxs-lookup"><span data-stu-id="a1a42-107">Requirement</span></span> | <span data-ttu-id="a1a42-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a1a42-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a1a42-109">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1a42-109">Minimum supported client</span></span><br/> | <span data-ttu-id="a1a42-110">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a1a42-110">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a1a42-111">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1a42-111">Minimum supported server</span></span><br/> | <span data-ttu-id="a1a42-112">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a1a42-112">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a1a42-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a1a42-113">Redistributable</span></span><br/>          | <span data-ttu-id="a1a42-114">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="a1a42-114">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



 

 




