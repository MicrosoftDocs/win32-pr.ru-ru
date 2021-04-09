---
description: Указывает, использует ли приемник мультимедиа Digital живая Network Alliance (DLNA) службу планировщика классов мультимедиа (MMCSS).
ms.assetid: 4c27e2ec-624a-4b1f-bea9-3aaad1534c9b
title: Атрибут MF_MP2DLNA_USE_MMCSS (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfdaf36ce51f1158e110dcb3682a5b072c060dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080868"
---
# <a name="mf_mp2dlna_use_mmcss-attribute"></a><span data-ttu-id="7b945-103">MF \_ MP2DLNA \_ использовать \_ атрибут MMCSS</span><span class="sxs-lookup"><span data-stu-id="7b945-103">MF\_MP2DLNA\_USE\_MMCSS attribute</span></span>

<span data-ttu-id="7b945-104">Указывает, использует ли приемник мультимедиа Digital живая Network Alliance (DLNA) службу планировщика классов мультимедиа (MMCSS).</span><span class="sxs-lookup"><span data-stu-id="7b945-104">Specifies whether the Digital Living Network Alliance (DLNA) media sink uses the Multimedia Class Scheduler Service (MMCSS).</span></span>

## <a name="data-type"></a><span data-ttu-id="7b945-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7b945-105">Data type</span></span>

<span data-ttu-id="7b945-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="7b945-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="7b945-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="7b945-107">Get/set</span></span>

<span data-ttu-id="7b945-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="7b945-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7b945-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="7b945-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="7b945-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b945-110">Remarks</span></span>

<span data-ttu-id="7b945-111">Чтобы задать этот атрибут для приемника мультимедиа DLNA, запросите приемник мультимедиа для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="7b945-111">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="7b945-112">Задайте атрибут перед началом потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="7b945-112">Set the attribute before streaming begins.</span></span>

<span data-ttu-id="7b945-113">Если этот атрибут имеет **значение true**, приемник мультимедиа DLNA регистрируется в службе MMCSS.</span><span class="sxs-lookup"><span data-stu-id="7b945-113">If this attribute is **TRUE**, the DLNA media sink registers itself with MMCSS.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b945-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7b945-114">Requirements</span></span>



| <span data-ttu-id="7b945-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7b945-115">Requirement</span></span> | <span data-ttu-id="7b945-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7b945-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b945-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b945-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7b945-118">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7b945-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7b945-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b945-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7b945-120">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7b945-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7b945-121">Header</span><span class="sxs-lookup"><span data-stu-id="7b945-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b945-122"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b945-122"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b945-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b945-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b945-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7b945-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




