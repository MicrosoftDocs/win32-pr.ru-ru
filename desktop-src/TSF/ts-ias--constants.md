---
title: Константы TS_IAS_ (Текстстор. h)
description: '\_ \_ Константы TS IAS \ используются в качестве флагов битов для управления вставкой текста или внедренных объектов в выделенном фрагменте или точке вставки.'
ms.assetid: 58e0d13c-d90c-41d2-bd93-4eba5fe0a69a
topic_type:
- apiref
api_name:
- TS_IAS_NOQUERY
- TS_IAS_QUERYONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d59584295567c586ebd8db7e5f63366fd8272f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135990"
---
# <a name="ts_ias_-constants"></a><span data-ttu-id="82ea8-103">\_Константы IAS служб терминалов \_ \*</span><span class="sxs-lookup"><span data-stu-id="82ea8-103">TS\_IAS\_\* Constants</span></span>

<span data-ttu-id="82ea8-104">\_Константы IAS служб терминалов \_ \* используются как флаги битов для управления вставкой текста или внедренных объектов в выделенном фрагменте или точке вставки.</span><span class="sxs-lookup"><span data-stu-id="82ea8-104">The TS\_IAS\_\* constants are used as bitfield flags to control insertion of text or embedded objects at a selection or insertion point.</span></span>



| <span data-ttu-id="82ea8-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="82ea8-105">Constant/value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="82ea8-106">Описание</span><span class="sxs-lookup"><span data-stu-id="82ea8-106">Description</span></span>                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IAS_NOQUERY"></span><span id="ts_ias_noquery"></span><dl> <span data-ttu-id="82ea8-107"><dt>**TS \_ \_НЕЗАПРОС IAS**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="82ea8-107"><dt>**TS\_IAS\_NOQUERY**</dt> <dt>( 0x1 )</dt></span></span> </dl>       | <span data-ttu-id="82ea8-108">Текст вставляется, а при выходе в качестве указателя на диапазон устанавливается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="82ea8-108">Text is inserted and the range pointer is set to **NULL** upon exit.</span></span> <span data-ttu-id="82ea8-109">Не может сочетаться с \_ \_ флагом TS IAS куерйонли.</span><span class="sxs-lookup"><span data-stu-id="82ea8-109">Cannot be combined with the TS\_IAS\_QUERYONLY flag.</span></span><br/>          |
| <span id="TS_IAS_QUERYONLY"></span><span id="ts_ias_queryonly"></span><dl> <span data-ttu-id="82ea8-110"><dt>**TS \_ IAS \_ куерйонли**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="82ea8-110"><dt>**TS\_IAS\_QUERYONLY**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="82ea8-111">Не выполняйте вставку.</span><span class="sxs-lookup"><span data-stu-id="82ea8-111">Do not perform the insertion.</span></span> <span data-ttu-id="82ea8-112">Вызывающий объект требует, чтобы был установлен только указатель на диапазон.</span><span class="sxs-lookup"><span data-stu-id="82ea8-112">Caller only requires the range pointer to be set.</span></span> <span data-ttu-id="82ea8-113">Не может использоваться вместе с \_ \_ флагом незапроса IAS служб терминалов.</span><span class="sxs-lookup"><span data-stu-id="82ea8-113">Cannot be combined with the TS\_IAS\_NOQUERY flag.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="82ea8-114">Требования</span><span class="sxs-lookup"><span data-stu-id="82ea8-114">Requirements</span></span>



| <span data-ttu-id="82ea8-115">Требование</span><span class="sxs-lookup"><span data-stu-id="82ea8-115">Requirement</span></span> | <span data-ttu-id="82ea8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="82ea8-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82ea8-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82ea8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="82ea8-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="82ea8-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="82ea8-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82ea8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="82ea8-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="82ea8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="82ea8-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="82ea8-121">Redistributable</span></span><br/>          | <span data-ttu-id="82ea8-122">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="82ea8-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="82ea8-123">Header</span><span class="sxs-lookup"><span data-stu-id="82ea8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="82ea8-124"><dt>Текстстор. h</dt></span><span class="sxs-lookup"><span data-stu-id="82ea8-124"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="82ea8-125">IDL</span><span class="sxs-lookup"><span data-stu-id="82ea8-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="82ea8-126"><dt>Текстстор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="82ea8-126"><dt>Textstor.idl</dt></span></span> </dl> |



 

 





