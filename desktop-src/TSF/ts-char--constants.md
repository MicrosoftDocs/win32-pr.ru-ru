---
title: Константы TS_CHAR_ (Текстстор. h)
description: '\_ \_ Константы TS char \ описывают тип символа.'
ms.assetid: b40ca931-d45c-4101-9380-bb2b3ad25fba
topic_type:
- apiref
api_name:
- TS_CHAR_EMBEDDED
- TS_CHAR_REGION
- TS_CHAR_REPLACEMENT
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25f66006dcb37e2504785b2b28ca1f328edfcfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415245"
---
# <a name="ts_char_-constants"></a><span data-ttu-id="98fd2-103">\_Константы char служб терминалов \_ \*</span><span class="sxs-lookup"><span data-stu-id="98fd2-103">TS\_CHAR\_\* Constants</span></span>

<span data-ttu-id="98fd2-104">\_Константы char служб терминалов \_ \* описывают тип символа.</span><span class="sxs-lookup"><span data-stu-id="98fd2-104">The TS\_CHAR\_\* constants describe the type of character.</span></span>



| <span data-ttu-id="98fd2-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="98fd2-105">Constant/value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="98fd2-106">Описание</span><span class="sxs-lookup"><span data-stu-id="98fd2-106">Description</span></span>                                                                                         |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| <span id="TS_CHAR_EMBEDDED"></span><span id="ts_char_embedded"></span><dl> <span data-ttu-id="98fd2-107"><dt>**TS \_ CHAR \_ Embedded**</dt> <dt>(0xfffc)</dt></span><span class="sxs-lookup"><span data-stu-id="98fd2-107"><dt>**TS\_CHAR\_EMBEDDED**</dt> <dt>( 0xfffc )</dt></span></span> </dl>          | <span data-ttu-id="98fd2-108">Символ представляет собой символ замены объекта в Юникоде 2,1.</span><span class="sxs-lookup"><span data-stu-id="98fd2-108">The character is a Unicode 2.1 object-replacement character.</span></span><br/>                             |
| <span id="TS_CHAR_REGION"></span><span id="ts_char_region"></span><dl> <span data-ttu-id="98fd2-109"><dt>**TS \_ \_Область char**</dt> <dt>(0)</dt></span><span class="sxs-lookup"><span data-stu-id="98fd2-109"><dt>**TS\_CHAR\_REGION**</dt> <dt>( 0 )</dt></span></span> </dl>                     | <span data-ttu-id="98fd2-110">Символ является границей области.</span><span class="sxs-lookup"><span data-stu-id="98fd2-110">The character is a region boundary.</span></span><br/>                                                      |
| <span id="TS_CHAR_REPLACEMENT"></span><span id="ts_char_replacement"></span><dl> <span data-ttu-id="98fd2-111"><dt>**TS \_ \_Замена символов**</dt> <dt>(0xfffd)</dt></span><span class="sxs-lookup"><span data-stu-id="98fd2-111"><dt>**TS\_CHAR\_REPLACEMENT**</dt> <dt>( 0xfffd )</dt></span></span> </dl> | <span data-ttu-id="98fd2-112">Символ является символом-заполнителем скрытого текста или символом замены в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="98fd2-112">The character is a hidden-text placeholder character or a Unicode replacement character.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="98fd2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="98fd2-113">Requirements</span></span>



| <span data-ttu-id="98fd2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="98fd2-114">Requirement</span></span> | <span data-ttu-id="98fd2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="98fd2-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98fd2-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98fd2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="98fd2-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="98fd2-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="98fd2-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98fd2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="98fd2-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="98fd2-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="98fd2-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="98fd2-120">Redistributable</span></span><br/>          | <span data-ttu-id="98fd2-121">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="98fd2-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="98fd2-122">Header</span><span class="sxs-lookup"><span data-stu-id="98fd2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="98fd2-123"><dt>Текстстор. h</dt></span><span class="sxs-lookup"><span data-stu-id="98fd2-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="98fd2-124">IDL</span><span class="sxs-lookup"><span data-stu-id="98fd2-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="98fd2-125"><dt>Текстстор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="98fd2-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98fd2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98fd2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98fd2-127">Внедренные объекты</span><span class="sxs-lookup"><span data-stu-id="98fd2-127">Embedded Objects</span></span>](embedded-objects.md)
</dt> </dl>

 

 





