---
description: Указывает, зарегистрировано ли преобразование Media Foundation (MFT) только в процессе приложений.
ms.assetid: e10d6378-8e85-4f73-9fa3-a2e954fc8249
title: Атрибут MFT_PROCESS_LOCAL_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d3595ef530008b8d09f27e3e76fad81a06039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811608"
---
# <a name="mft_process_local_attribute-attribute"></a><span data-ttu-id="2dc89-103">\_ \_ Атрибут локального атрибута процесса MFT \_</span><span class="sxs-lookup"><span data-stu-id="2dc89-103">MFT\_PROCESS\_LOCAL\_Attribute attribute</span></span>

<span data-ttu-id="2dc89-104">Указывает, регистрируется ли преобразование Media Foundation (MFT) только в процессе приложения.</span><span class="sxs-lookup"><span data-stu-id="2dc89-104">Specifies whether a Media Foundation transform (MFT) is registered only in the application's process.</span></span>

## <a name="data-type"></a><span data-ttu-id="2dc89-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2dc89-105">Data type</span></span>

<span data-ttu-id="2dc89-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2dc89-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="2dc89-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="2dc89-107">Get/set</span></span>

<span data-ttu-id="2dc89-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="2dc89-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="2dc89-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="2dc89-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="2dc89-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2dc89-110">Remarks</span></span>

<span data-ttu-id="2dc89-111">Этот атрибут используется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2dc89-111">This attribute is used as follows:</span></span>

1.  <span data-ttu-id="2dc89-112">Приложение регистрирует локальную таблицу MFT, вызывая функцию [**мфтрегистерлокал**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) или [**мфтрегистерлокалбиклсид**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) .</span><span class="sxs-lookup"><span data-stu-id="2dc89-112">The application registers a local MFT by calling either the [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) function.</span></span> <span data-ttu-id="2dc89-113">Эти функции регистрируют MFT в процессе приложения.</span><span class="sxs-lookup"><span data-stu-id="2dc89-113">These functions register the MFT in the application's process.</span></span>
2.  <span data-ttu-id="2dc89-114">Функция [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) вызывается для перечисления МФТС, соответствующих определенному набору критериев.</span><span class="sxs-lookup"><span data-stu-id="2dc89-114">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function is called to enumerate MFTs that match a particular set of criteria.</span></span> <span data-ttu-id="2dc89-115">Приложение может напрямую вызывать функцию **мфтенумекс** , но чаще эта функция вызывается загрузчиком топологии.</span><span class="sxs-lookup"><span data-stu-id="2dc89-115">The application might call the **MFTEnumEx** function directly, but more often this function is called by the topology loader.</span></span>
3.  <span data-ttu-id="2dc89-116">Функция [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) извлекает массив указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , каждый из которых представляет объект активации для MFT.</span><span class="sxs-lookup"><span data-stu-id="2dc89-116">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function retrieves an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, each representing an activation object for an MFT.</span></span> <span data-ttu-id="2dc89-117">Если таблица MFT зарегистрирована локально, \_ \_ атрибут локального атрибута процесса MFT \_ имеет значение **true** для соответствующего объекта активации.</span><span class="sxs-lookup"><span data-stu-id="2dc89-117">If an MFT is registered locally, the MFT\_PROCESS\_LOCAL\_Attribute attribute is set to **TRUE** on the corresponding activation object.</span></span>

<span data-ttu-id="2dc89-118">Значение по умолчанию для этого атрибута — **false**.</span><span class="sxs-lookup"><span data-stu-id="2dc89-118">The default value for this attribute is **FALSE**.</span></span>

<span data-ttu-id="2dc89-119">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="2dc89-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dc89-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2dc89-120">Requirements</span></span>



| <span data-ttu-id="2dc89-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2dc89-121">Requirement</span></span> | <span data-ttu-id="2dc89-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2dc89-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc89-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2dc89-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2dc89-124">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="2dc89-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="2dc89-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2dc89-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2dc89-126">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="2dc89-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2dc89-127">Header</span><span class="sxs-lookup"><span data-stu-id="2dc89-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dc89-128"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dc89-128"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dc89-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2dc89-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dc89-130">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2dc89-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2dc89-131">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="2dc89-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




