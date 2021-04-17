---
title: Перечисление WMDM_TAG_DATATYPE
description: '\_ \_ Тип перечисления DATATYPE тега вмдм определяет тип данных.'
ms.assetid: 9c300814-5610-4e46-b441-e7f2fc78a47b
keywords:
- WMDM_TAG_DATATYPE перечисление Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDM_TAG_DATATYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad04f0d220809f6bd13d8ae29cc36d52ff6e599
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694600"
---
# <a name="wmdm_tag_datatype-enumeration"></a><span data-ttu-id="99658-104">\_ \_ Перечисление DATATYPE тега вмдм</span><span class="sxs-lookup"><span data-stu-id="99658-104">WMDM\_TAG\_DATATYPE enumeration</span></span>

<span data-ttu-id="99658-105">Тип **перечисления \_ \_ DATATYPE тега вмдм** определяет тип данных.</span><span class="sxs-lookup"><span data-stu-id="99658-105">The **WMDM\_TAG\_DATATYPE** enumeration type defines a data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="99658-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99658-106">Syntax</span></span>


```C++
typedef enum tagWMDM_TAG_DATATYPE { 
  WMDM_TYPE_DWORD,
  WMDM_TYPE_STRING,
  WMDM_TYPE_BINARY,
  WMDM_TYPE_BOOL,
  WMDM_TYPE_QWORD,
  WMDM_TYPE_WORD,
  WMDM_TYPE_GUID,
  WMDM_TYPE_DATE
} WMDM_TAG_DATATYPE;
```



## <a name="constants"></a><span data-ttu-id="99658-107">Константы</span><span class="sxs-lookup"><span data-stu-id="99658-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="99658-108"><span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**ВМДМ, \_ тип \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="99658-108"><span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**WMDM\_TYPE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="99658-109">Задает 4-байтовое значение **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="99658-109">Specifies a 4-byte **DWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="99658-110"><span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**\_Строка типа \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="99658-110"><span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**WMDM\_TYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="99658-111">Указывает строку в Юникоде, заканчивающуюся нулем (2 байта на символ).</span><span class="sxs-lookup"><span data-stu-id="99658-111">Specifies a null-terminated Unicode string (2 bytes per character).</span></span>

</dd> <dt>

<span data-ttu-id="99658-112"><span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**\_ \_ двоичный тип вмдм**</span><span class="sxs-lookup"><span data-stu-id="99658-112"><span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**WMDM\_TYPE\_BINARY**</span></span>
</dt> <dd>

<span data-ttu-id="99658-113">Указывает массив байтов.</span><span class="sxs-lookup"><span data-stu-id="99658-113">Specifies an array of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="99658-114"><span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**\_bool типа \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="99658-114"><span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**WMDM\_TYPE\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="99658-115">Задает 4-байтовое логическое значение.</span><span class="sxs-lookup"><span data-stu-id="99658-115">Specifies a 4-byte Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="99658-116"><span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**ВМДМ \_ тип \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="99658-116"><span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**WMDM\_TYPE\_QWORD**</span></span>
</dt> <dd>

<span data-ttu-id="99658-117">Задает 8-байтовое значение **QWORD** .</span><span class="sxs-lookup"><span data-stu-id="99658-117">Specifies an 8-byte **QWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="99658-118"><span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**\_слово типа \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="99658-118"><span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**WMDM\_TYPE\_WORD**</span></span>
</dt> <dd>

<span data-ttu-id="99658-119">Задает 2-байтовое значение **слова** .</span><span class="sxs-lookup"><span data-stu-id="99658-119">Specifies a 2-byte **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="99658-120"><span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**\_GUID типа \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="99658-120"><span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**WMDM\_TYPE\_GUID**</span></span>
</dt> <dd>

<span data-ttu-id="99658-121">Задает 128-разрядный (16-байтный) GUID.</span><span class="sxs-lookup"><span data-stu-id="99658-121">Specifies a 128-bit (16-byte) GUID.</span></span>

</dd> <dt>

<span data-ttu-id="99658-122"><span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**ВМДМ \_ тип \_ даты**</span><span class="sxs-lookup"><span data-stu-id="99658-122"><span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**WMDM\_TYPE\_DATE**</span></span>
</dt> <dd>

<span data-ttu-id="99658-123">Указывает дату.</span><span class="sxs-lookup"><span data-stu-id="99658-123">Specifies a date.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99658-124">Требования</span><span class="sxs-lookup"><span data-stu-id="99658-124">Requirements</span></span>



| <span data-ttu-id="99658-125">Требование</span><span class="sxs-lookup"><span data-stu-id="99658-125">Requirement</span></span> | <span data-ttu-id="99658-126">Значение</span><span class="sxs-lookup"><span data-stu-id="99658-126">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="99658-127">Header</span><span class="sxs-lookup"><span data-stu-id="99658-127">Header</span></span><br/> | <dl> <span data-ttu-id="99658-128"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="99658-128"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99658-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99658-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99658-130">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="99658-130">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





