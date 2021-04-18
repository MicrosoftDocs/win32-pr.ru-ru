---
title: Константы TF_IAS_ (Мсктф. h)
description: '\_ \_ Константы TF IAS \ используются в качестве флагов битовых знаков в методах, которые вставляют текст или внедренные объекты в выделенном фрагменте или точке вставки.'
ms.assetid: adc5c539-fdb1-4829-ad17-2f54ec179c47
topic_type:
- apiref
api_name:
- TF_IAS_NOQUERY
- TF_IAS_QUERYONLY
- TF_IAS_NO_DEFAULT_COMPOSITION
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a025e295d80ac9a58625c221c4b4c224233fbb26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681874"
---
# <a name="tf_ias_-constants"></a><span data-ttu-id="0f2bc-103">TF \_ IAS \_ \* константы</span><span class="sxs-lookup"><span data-stu-id="0f2bc-103">TF\_IAS\_\* Constants</span></span>

<span data-ttu-id="0f2bc-104">\_ \_ \* Константы TF IAS используются в качестве флагов битовых знаков в методах, которые вставляют текст или внедренные объекты в выделенном фрагменте или точке вставки.</span><span class="sxs-lookup"><span data-stu-id="0f2bc-104">The TF\_IAS\_\* constants are used as bitfield flags in methods that insert text or embedded objects at a selection or insertion point.</span></span>



| <span data-ttu-id="0f2bc-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="0f2bc-105">Constant/value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="0f2bc-106">Описание</span><span class="sxs-lookup"><span data-stu-id="0f2bc-106">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_IAS_NOQUERY"></span><span id="tf_ias_noquery"></span><dl> <span data-ttu-id="0f2bc-107"><dt>**Tf \_ \_НЕЗАПРОС IAS**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0f2bc-107"><dt>**TF\_IAS\_NOQUERY**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                                       | <span data-ttu-id="0f2bc-108">Текст вставляется, а при выходе в качестве указателя на диапазон устанавливается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="0f2bc-108">Text is inserted and the range pointer is set to **NULL** upon exit.</span></span> <span data-ttu-id="0f2bc-109">Не может использоваться вместе с \_ \_ флагом TF IAS куерйонли.</span><span class="sxs-lookup"><span data-stu-id="0f2bc-109">Cannot be combined with the TF\_IAS\_QUERYONLY flag.</span></span><br/>       |
| <span id="TF_IAS_QUERYONLY"></span><span id="tf_ias_queryonly"></span><dl> <span data-ttu-id="0f2bc-110"><dt>**Tf \_ IAS \_ куерйонли**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0f2bc-110"><dt>**TF\_IAS\_QUERYONLY**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                                 | <span data-ttu-id="0f2bc-111">Не выполняйте вставку.</span><span class="sxs-lookup"><span data-stu-id="0f2bc-111">Do not perform the insert.</span></span> <span data-ttu-id="0f2bc-112">Вызывающий объект требует, чтобы был установлен только указатель на диапазон.</span><span class="sxs-lookup"><span data-stu-id="0f2bc-112">Caller only requires the range pointer to be set.</span></span> <span data-ttu-id="0f2bc-113">Параметр не может использоваться вместе с \_ флагом "TF IAS- \_ запрос".</span><span class="sxs-lookup"><span data-stu-id="0f2bc-113">Cannot be combined with the TF\_IAS\_NOQUERY flag.</span></span><br/> |
| <span id="TF_IAS_NO_DEFAULT_COMPOSITION"></span><span id="tf_ias_no_default_composition"></span><dl> <span data-ttu-id="0f2bc-114"><dt>**Tf \_ Служба \_ IAS \_ без \_ композиции по умолчанию**</dt> <dt>(0x80000000)</dt></span><span class="sxs-lookup"><span data-stu-id="0f2bc-114"><dt>**TF\_IAS\_NO\_DEFAULT\_COMPOSITION**</dt> <dt>( 0x80000000 )</dt></span></span> </dl> | <span data-ttu-id="0f2bc-115">Если требуется композиция, TSF не создаст композицию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f2bc-115">TSF will not create a default composition if a composition is required.</span></span> <span data-ttu-id="0f2bc-116">Вызывающий объект должен начать композицию в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="0f2bc-116">Caller must start a composition over the range.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="0f2bc-117">Требования</span><span class="sxs-lookup"><span data-stu-id="0f2bc-117">Requirements</span></span>



| <span data-ttu-id="0f2bc-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0f2bc-118">Requirement</span></span> | <span data-ttu-id="0f2bc-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0f2bc-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0f2bc-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f2bc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0f2bc-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0f2bc-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0f2bc-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f2bc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0f2bc-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0f2bc-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0f2bc-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0f2bc-124">Redistributable</span></span><br/>          | <span data-ttu-id="0f2bc-125">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="0f2bc-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="0f2bc-126">Header</span><span class="sxs-lookup"><span data-stu-id="0f2bc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f2bc-127"><dt>Мсктф. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f2bc-127"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f2bc-128">IDL</span><span class="sxs-lookup"><span data-stu-id="0f2bc-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f2bc-129"><dt>Мсктф. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f2bc-129"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f2bc-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f2bc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f2bc-131">ITextStoreACP:: Инсертембеддедатселектион</span><span class="sxs-lookup"><span data-stu-id="0f2bc-131">ITextStoreACP::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="0f2bc-132">ITextStoreACP:: Инсерттекстатселектион</span><span class="sxs-lookup"><span data-stu-id="0f2bc-132">ITextStoreACP::InsertTextAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection)
</dt> <dt>

[<span data-ttu-id="0f2bc-133">Итекстстореанчор:: Инсертембеддедатселектион</span><span class="sxs-lookup"><span data-stu-id="0f2bc-133">ITextStoreAnchor::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="0f2bc-134">Итекстстореанчор:: Инсерттекстатселектион</span><span class="sxs-lookup"><span data-stu-id="0f2bc-134">ITextStoreAnchor::InsertTextAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection)
</dt> <dt>

[<span data-ttu-id="0f2bc-135">Итфинсертатселектион:: Инсертембеддедатселектион</span><span class="sxs-lookup"><span data-stu-id="0f2bc-135">ITfInsertAtSelection::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="0f2bc-136">Итфинсертатселектион:: Инсерттекстатселектион</span><span class="sxs-lookup"><span data-stu-id="0f2bc-136">ITfInsertAtSelection::InsertTextAtSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-inserttextatselection)
</dt> </dl>

 

 





