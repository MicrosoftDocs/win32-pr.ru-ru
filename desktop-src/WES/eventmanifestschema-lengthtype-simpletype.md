---
title: Простой тип Ленгстипе
description: Определяет тип длины, используемый для указания числа байтов или символов в элементе данных переменной длины, например двоичных данных или строки ANSI или Юникод.
ms.assetid: a15e4241-cce3-4f62-bc1c-f70fb1ea5d38
keywords:
- Журнал событий простого типа Ленгстипе
topic_type:
- apiref
api_name:
- LengthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dbb0720c2e26fa73056ccffdd17392e93e491c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341205"
---
# <a name="lengthtype-simple-type"></a><span data-ttu-id="9ad76-104">Простой тип Ленгстипе</span><span class="sxs-lookup"><span data-stu-id="9ad76-104">LengthType Simple Type</span></span>

<span data-ttu-id="9ad76-105">Определяет тип длины, используемый для указания числа байтов или символов в элементе данных переменной длины, например двоичных данных или строки ANSI или Юникод.</span><span class="sxs-lookup"><span data-stu-id="9ad76-105">Defines a length type that is used to specify the number of bytes or characters in a variable length data item such as binary data or an ANSI or Unicode string.</span></span> <span data-ttu-id="9ad76-106">Значение может быть указано в виде значения xs: Унсигнедшорт или в виде строки, ссылающейся на имя узла элемента данных, который содержит короткое значение без знака.</span><span class="sxs-lookup"><span data-stu-id="9ad76-106">The value can be specified as an xs:unsignedShort value or as a string that references the name of data item node that contains the unsigned short value.</span></span>

``` syntax
<xs:simpleType name="LengthType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="9ad76-107">Требования</span><span class="sxs-lookup"><span data-stu-id="9ad76-107">Requirements</span></span>



| <span data-ttu-id="9ad76-108">Требование</span><span class="sxs-lookup"><span data-stu-id="9ad76-108">Requirement</span></span> | <span data-ttu-id="9ad76-109">Значение</span><span class="sxs-lookup"><span data-stu-id="9ad76-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9ad76-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ad76-110">Minimum supported client</span></span><br/> | <span data-ttu-id="9ad76-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ad76-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9ad76-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ad76-112">Minimum supported server</span></span><br/> | <span data-ttu-id="9ad76-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9ad76-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





