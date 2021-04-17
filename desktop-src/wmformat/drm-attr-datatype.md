---
title: Перечисление DRM_ATTR_DATATYPE (Вмдрмсдк. h)
description: '\_ \_ Перечисление DATATYPE attr DRM определяет типы данных, используемые для атрибутов и свойств DRM.'
ms.assetid: ccad16e2-475d-4cc7-b773-f17038d2754a
keywords:
- Формат Windows Media DRM_ATTR_DATATYPE перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- DRM_ATTR_DATATYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e684ba1c09a86c65a13adbd189bb185f65598b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708518"
---
# <a name="drm_attr_datatype-enumeration"></a><span data-ttu-id="724bd-105">\_ \_ Перечисление DATATYPE атрибутов DRM</span><span class="sxs-lookup"><span data-stu-id="724bd-105">DRM\_ATTR\_DATATYPE enumeration</span></span>

<span data-ttu-id="724bd-106">Перечисление **\_ \_ DATATYPE attr DRM** определяет типы данных, используемые для атрибутов и свойств DRM.</span><span class="sxs-lookup"><span data-stu-id="724bd-106">The **DRM\_ATTR\_DATATYPE** enumeration defines the data types used for DRM attributes and properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="724bd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="724bd-107">Syntax</span></span>


```C++
typedef enum DRM_ATTR_DATATYPE { 
  DRM_TYPE_DWORD   = 0,
  DRM_TYPE_STRING  = 1,
  DRM_TYPE_BINARY  = 2,
  DRM_TYPE_BOOL    = 3,
  DRM_TYPE_QWORD   = 4,
  DRM_TYPE_WORD    = 5,
  DRM_TYPE_GUID    = 6
} ;
```



## <a name="constants"></a><span data-ttu-id="724bd-108">Константы</span><span class="sxs-lookup"><span data-stu-id="724bd-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="724bd-109"><span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**\_тип DRM типа \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="724bd-109"><span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**DRM\_TYPE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="724bd-110">Свойство является 4-байтовым значением **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="724bd-110">The property is a 4-byte **DWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="724bd-111"><span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**\_Строка типа \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="724bd-111"><span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**DRM\_TYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="724bd-112">Свойство является строкой в Юникоде, завершающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="724bd-112">The property is a null-terminated Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="724bd-113"><span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**\_ \_ двоичный тип DRM**</span><span class="sxs-lookup"><span data-stu-id="724bd-113"><span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**DRM\_TYPE\_BINARY**</span></span>
</dt> <dd>

<span data-ttu-id="724bd-114">Свойство представляет собой массив байтов.</span><span class="sxs-lookup"><span data-stu-id="724bd-114">The property is an array of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="724bd-115"><span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**\_тип логического типа DRM \_**</span><span class="sxs-lookup"><span data-stu-id="724bd-115"><span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**DRM\_TYPE\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="724bd-116">Свойство является 4-байтовым логическим значением.</span><span class="sxs-lookup"><span data-stu-id="724bd-116">The property is a 4-byte Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="724bd-117"><span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**Тип управления цифровыми правами ( \_ \_ QWORD)**</span><span class="sxs-lookup"><span data-stu-id="724bd-117"><span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**DRM\_TYPE\_QWORD**</span></span>
</dt> <dd>

<span data-ttu-id="724bd-118">Свойство является 8-байтовым значением **QWORD** .</span><span class="sxs-lookup"><span data-stu-id="724bd-118">The property is an 8-byte **QWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="724bd-119"><span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**\_слово типа \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="724bd-119"><span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**DRM\_TYPE\_WORD**</span></span>
</dt> <dd>

<span data-ttu-id="724bd-120">Свойство является 2-байтовым значением **слова** .</span><span class="sxs-lookup"><span data-stu-id="724bd-120">The property is a 2-byte **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="724bd-121"><span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**\_GUID типа \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="724bd-121"><span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**DRM\_TYPE\_GUID**</span></span>
</dt> <dd>

<span data-ttu-id="724bd-122">Свойство является 128-битным (6-байтовым) значением GUID.</span><span class="sxs-lookup"><span data-stu-id="724bd-122">The property is a 128-bit (6-byte) GUID value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="724bd-123">Требования</span><span class="sxs-lookup"><span data-stu-id="724bd-123">Requirements</span></span>



| <span data-ttu-id="724bd-124">Требование</span><span class="sxs-lookup"><span data-stu-id="724bd-124">Requirement</span></span> | <span data-ttu-id="724bd-125">Значение</span><span class="sxs-lookup"><span data-stu-id="724bd-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="724bd-126">Header</span><span class="sxs-lookup"><span data-stu-id="724bd-126">Header</span></span><br/> | <dl> <span data-ttu-id="724bd-127"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="724bd-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="724bd-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="724bd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="724bd-129">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="724bd-129">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





