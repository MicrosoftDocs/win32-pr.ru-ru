---
description: Определяет тип, используемый для указания допустимых значений цвета определенных элементов в XML-файле журнала.
ms.assetid: 10a19f28-d0aa-4126-b3f5-fde35fc5fdb0
title: Простой тип Колортипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ColorType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 883c34f42f8d31f3581599445b398b93676d416b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701352"
---
# <a name="colortype-simple-type"></a><span data-ttu-id="39e49-103">Простой тип Колортипе</span><span class="sxs-lookup"><span data-stu-id="39e49-103">ColorType Simple Type</span></span>

<span data-ttu-id="39e49-104">Определяет тип, используемый для указания допустимых значений цвета определенных элементов в XML-файле журнала.</span><span class="sxs-lookup"><span data-stu-id="39e49-104">Defines the type that is used to specify valid values for the color of certain elements in a Journal XML file.</span></span>

``` syntax
<xs:simpleType name="ColorType">
    <xs:restriction
        base="string"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="39e49-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39e49-105">Remarks</span></span>

<span data-ttu-id="39e49-106">Цвет может быть шестнадцатеричным значением RGB в формате \# RRGGBB.</span><span class="sxs-lookup"><span data-stu-id="39e49-106">A color can be a hexadecimal RGB value in the format \#RRGGBB.</span></span> <span data-ttu-id="39e49-107">Оно должно соответствовать следующему регулярному выражению: \# \[ 0-9a-fA-F \] {6} .</span><span class="sxs-lookup"><span data-stu-id="39e49-107">It must match the following regular expression: \#\[0-9a-fA-F\]{6}.</span></span> <span data-ttu-id="39e49-108">Например: " \# 4a79B5".</span><span class="sxs-lookup"><span data-stu-id="39e49-108">For example: "\#4a79B5".</span></span>

## <a name="requirements"></a><span data-ttu-id="39e49-109">Требования</span><span class="sxs-lookup"><span data-stu-id="39e49-109">Requirements</span></span>



| <span data-ttu-id="39e49-110">Требование</span><span class="sxs-lookup"><span data-stu-id="39e49-110">Requirement</span></span> | <span data-ttu-id="39e49-111">Значение</span><span class="sxs-lookup"><span data-stu-id="39e49-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="39e49-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39e49-112">Minimum supported client</span></span><br/> | <span data-ttu-id="39e49-113">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="39e49-113">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="39e49-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39e49-114">Minimum supported server</span></span><br/> | <span data-ttu-id="39e49-115">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="39e49-115">None supported</span></span><br/>                                     |



 

 




