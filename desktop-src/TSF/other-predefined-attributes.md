---
title: Другие предопределенные атрибуты (Тсаттрид. h)
description: Следующие значения указывают различные атрибуты, полученные с помощью метода ITfContext Жетапппроперти. В него включаются формат данных и содержимое каждого типа свойства.
ms.assetid: 8536938b-98a1-415b-b5f2-45b90215c270
keywords:
- Другие предопределенные атрибуты платформа текстовых служб
topic_type:
- apiref
api_name:
- Other Predefined Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0d0a3ff72a5ea84a6b9e5b47106012a945dbf45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682048"
---
# <a name="other-predefined-attributes"></a><span data-ttu-id="ac5d2-105">Другие предопределенные атрибуты</span><span class="sxs-lookup"><span data-stu-id="ac5d2-105">Other Predefined Attributes</span></span>

<span data-ttu-id="ac5d2-106">Следующие значения указывают различные атрибуты, полученные с помощью метода [ITfContext:: жетапппроперти](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) .</span><span class="sxs-lookup"><span data-stu-id="ac5d2-106">The following values identify miscellaneous attributes obtained with the [ITfContext::GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) method.</span></span> <span data-ttu-id="ac5d2-107">В него включаются формат данных и содержимое каждого типа свойства.</span><span class="sxs-lookup"><span data-stu-id="ac5d2-107">The data format and contents of each property type are included.</span></span>

## <a name="properties"></a><span data-ttu-id="ac5d2-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="ac5d2-108">Properties</span></span>



| <span data-ttu-id="ac5d2-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="ac5d2-109">Property</span></span>                             | <span data-ttu-id="ac5d2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ac5d2-110">Description</span></span>                                                                       |
|--------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ac5d2-111">**\_Приложение тсаттрид**</span><span class="sxs-lookup"><span data-stu-id="ac5d2-111">**TSATTRID\_App**</span></span>                    | <span data-ttu-id="ac5d2-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ac5d2-112">Not used.</span></span>                                                                         |
| <span data-ttu-id="ac5d2-113">**\_Инкорректграммар приложения \_ тсаттрид**</span><span class="sxs-lookup"><span data-stu-id="ac5d2-113">**TSATTRID\_App\_IncorrectGrammar**</span></span>  | <span data-ttu-id="ac5d2-114">Содержит ненулевое значение, если текст содержит грамматическую ошибку или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ac5d2-114">Contains a nonzero value if the text contains a grammar error or zero otherwise.</span></span>  |
| <span data-ttu-id="ac5d2-115">**\_Инкорректспеллинг приложения \_ тсаттрид**</span><span class="sxs-lookup"><span data-stu-id="ac5d2-115">**TSATTRID\_App\_IncorrectSpelling**</span></span> | <span data-ttu-id="ac5d2-116">Содержит ненулевое значение, если текст содержит орфографические ошибки или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ac5d2-116">Contains a nonzero value if the text contains a spelling error or zero otherwise.</span></span> |
| <span data-ttu-id="ac5d2-117">**ТСАТТРИД \_ другие**</span><span class="sxs-lookup"><span data-stu-id="ac5d2-117">**TSATTRID\_OTHERS**</span></span>                 | <span data-ttu-id="ac5d2-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ac5d2-118">Not used.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="ac5d2-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ac5d2-119">Requirements</span></span>



| <span data-ttu-id="ac5d2-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ac5d2-120">Requirement</span></span> | <span data-ttu-id="ac5d2-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ac5d2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac5d2-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac5d2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ac5d2-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ac5d2-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ac5d2-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac5d2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ac5d2-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ac5d2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac5d2-126">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="ac5d2-126">Redistributable</span></span><br/>          | <span data-ttu-id="ac5d2-127">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="ac5d2-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="ac5d2-128">Header</span><span class="sxs-lookup"><span data-stu-id="ac5d2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac5d2-129"><dt>Тсаттрид. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac5d2-129"><dt>TsAttrid.h</dt></span></span> </dl> |



 

