---
description: Определяет строковый тип для элемента ProviderName в профиле мобильного широкополосного подключения.
ms.assetid: 1644ded2-f931-4920-848d-e0405d8723e3
title: Простой тип Провидернаметипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerNameType
api_type:
- Schema
ms.openlocfilehash: df61473358a9ed4453bc28f1b5c7974082e515bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541386"
---
# <a name="providernametype-simple-type"></a><span data-ttu-id="57b5f-103">Простой тип Провидернаметипе</span><span class="sxs-lookup"><span data-stu-id="57b5f-103">providerNameType Simple Type</span></span>

<span data-ttu-id="57b5f-104">Простой тип **провидернаметипе** определяет строковый тип для элемента [**providerName**](schema-providername-providertype-element.md) в профиле мобильного широкополосного подключения.</span><span class="sxs-lookup"><span data-stu-id="57b5f-104">The **providerNameType** simple type defines a string type for the [**ProviderName**](schema-providername-providertype-element.md) element in the Mobile Broadband profile.</span></span> <span data-ttu-id="57b5f-105">Эта строка состоит по меньшей мере из одного символа и не длиннее 20 символов.</span><span class="sxs-lookup"><span data-stu-id="57b5f-105">This string is at least one character long and at most 20 characters long.</span></span>

``` syntax
<xs:simpleType name="providerNameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="20"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="57b5f-106">Требования</span><span class="sxs-lookup"><span data-stu-id="57b5f-106">Requirements</span></span>



| <span data-ttu-id="57b5f-107">Требование</span><span class="sxs-lookup"><span data-stu-id="57b5f-107">Requirement</span></span> | <span data-ttu-id="57b5f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="57b5f-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="57b5f-109">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57b5f-109">Minimum supported client</span></span><br/> | <span data-ttu-id="57b5f-110">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="57b5f-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="57b5f-111">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57b5f-111">Minimum supported server</span></span><br/> | <span data-ttu-id="57b5f-112">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="57b5f-112">None supported</span></span><br/>                         |



 

 




