---
description: Определяет строковый тип для элемента Иконфилепас в профиле мобильного широкополосного подключения.
ms.assetid: 053bc5b8-fab2-4abe-97f8-ed98aea880b1
title: Простой тип Иконфилетипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- iconFileType
api_type:
- Schema
ms.openlocfilehash: 168c2709f8b3049270711e286a35fbbd11e1ffef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144797"
---
# <a name="iconfiletype-simple-type"></a><span data-ttu-id="33647-103">Простой тип Иконфилетипе</span><span class="sxs-lookup"><span data-stu-id="33647-103">iconFileType Simple Type</span></span>

<span data-ttu-id="33647-104">Простой тип **иконфилетипе** определяет строковый тип для элемента [**иконфилепас**](schema-iconfilepath-mbnprofile-element.md) в профиле мобильного широкополосного подключения.</span><span class="sxs-lookup"><span data-stu-id="33647-104">The **iconFileType** simple type defines a string type for the [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md) element in the Mobile Broadband profile.</span></span> <span data-ttu-id="33647-105">Эта строка состоит по меньшей мере из одного символа и не длиннее 1024 символов.</span><span class="sxs-lookup"><span data-stu-id="33647-105">This string is at least one character long and at most 1024 characters long.</span></span>

``` syntax
<xs:simpleType name="iconFileType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="1024"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="33647-106">Требования</span><span class="sxs-lookup"><span data-stu-id="33647-106">Requirements</span></span>



| <span data-ttu-id="33647-107">Требование</span><span class="sxs-lookup"><span data-stu-id="33647-107">Requirement</span></span> | <span data-ttu-id="33647-108">Значение</span><span class="sxs-lookup"><span data-stu-id="33647-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="33647-109">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33647-109">Minimum supported client</span></span><br/> | <span data-ttu-id="33647-110">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="33647-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="33647-111">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33647-111">Minimum supported server</span></span><br/> | <span data-ttu-id="33647-112">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="33647-112">None supported</span></span><br/>                         |



 

 




