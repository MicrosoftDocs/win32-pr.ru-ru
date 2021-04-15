---
description: Указывает, поддерживает ли Media Foundationное преобразование (MFT) трехмерное видео стереоскопик.
ms.assetid: DE96FD14-5C7E-4560-99AC-B1EBDA1EBB2B
title: Атрибут MFT_SUPPORT_3DVIDEO (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdbc7208f9bbcf2c638ae83e988c6e541a4be2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701803"
---
# <a name="mft_support_3dvideo-attribute"></a><span data-ttu-id="7a0f5-103">Таблица MFT \_ поддерживает \_ атрибут 3DVIDEO</span><span class="sxs-lookup"><span data-stu-id="7a0f5-103">MFT\_SUPPORT\_3DVIDEO attribute</span></span>

<span data-ttu-id="7a0f5-104">Указывает, поддерживает ли Media Foundationное преобразование (MFT) трехмерное видео стереоскопик.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-104">Specifies whether a Media Foundation transform (MFT) supports 3D stereoscopic video.</span></span>

## <a name="data-type"></a><span data-ttu-id="7a0f5-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7a0f5-105">Data type</span></span>

<span data-ttu-id="7a0f5-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="7a0f5-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7a0f5-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a0f5-107">Remarks</span></span>

<span data-ttu-id="7a0f5-108">Чтобы запросить этот атрибут, вызовите [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) , чтобы получить глобальное хранилище атрибутов MFT.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-108">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span> <span data-ttu-id="7a0f5-109">Если методы **InAttribute** выполнены, вызовите [**ИМФАТТРИБУТЕС:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="7a0f5-109">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7a0f5-110">Значение этого атрибута по умолчанию равно **false**.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-110">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="7a0f5-111">Рассматривайте этот атрибут как доступный только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-111">Treat this attribute as read-only.</span></span> <span data-ttu-id="7a0f5-112">Не изменяйте значение. в MFT все изменения в значении будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-112">Do not change the value; the MFT will ignore any changes to the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a0f5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7a0f5-113">Requirements</span></span>



| <span data-ttu-id="7a0f5-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7a0f5-114">Requirement</span></span> | <span data-ttu-id="7a0f5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7a0f5-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a0f5-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a0f5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7a0f5-117">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="7a0f5-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="7a0f5-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a0f5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7a0f5-119">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="7a0f5-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="7a0f5-120">Header</span><span class="sxs-lookup"><span data-stu-id="7a0f5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a0f5-121"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a0f5-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a0f5-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a0f5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a0f5-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7a0f5-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




