---
description: Указывает, как приемник мультимедиа ASF должен применять Windows Media DRM.
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: Свойство MFPKEY_ASFMEDIASINK_DRMACTION (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80906a5ac6e5d12bd59dd57445d33b100fee1aef
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820325"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a><span data-ttu-id="c052c-103">МФПКЭЙ \_ асфмедиасинк \_ дрмактион, свойство</span><span class="sxs-lookup"><span data-stu-id="c052c-103">MFPKEY\_ASFMEDIASINK\_DRMACTION property</span></span>

<span data-ttu-id="c052c-104">Указывает, как приемник мультимедиа ASF должен применять Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="c052c-104">Specifies how the ASF media sink should apply Windows Media DRM.</span></span>



<span data-ttu-id="c052c-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c052c-105">Data type</span></span>

<span data-ttu-id="c052c-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="c052c-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="c052c-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="c052c-107">PROPVARIANT member</span></span>

<span data-ttu-id="c052c-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="c052c-108">**ULONG**</span></span>

<span data-ttu-id="c052c-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="c052c-109">VT\_UI4</span></span>

<span data-ttu-id="c052c-110">**улвал**</span><span class="sxs-lookup"><span data-stu-id="c052c-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="c052c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c052c-111">Remarks</span></span>

<span data-ttu-id="c052c-112">Значение этого свойства является членом перечисления [**мфсинк \_ вмдрмактион**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) .</span><span class="sxs-lookup"><span data-stu-id="c052c-112">The value of this property is a member of the [**MFSINK\_WMDRMACTION**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) enumeration.</span></span>

<span data-ttu-id="c052c-113">Этот атрибут можно использовать для настройки приемника мультимедиа ASF.</span><span class="sxs-lookup"><span data-stu-id="c052c-113">You can use this attribute to configure the ASF media sink.</span></span> <span data-ttu-id="c052c-114">Использование зависит от того, какая функция вызывается для создания приемника мультимедиа ASF:</span><span class="sxs-lookup"><span data-stu-id="c052c-114">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="c052c-115">[**Мфкреатеасфмедиасинк**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): запросите полученный указатель [**Имфмедиасинк**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) для интерфейса **ипропертисторе** .</span><span class="sxs-lookup"><span data-stu-id="c052c-115">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="c052c-116">[**Мфкреатеасфмедиасинкактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): вызов [**Имфасфконтентинфо:: жетенкодингконфигуратионпропертисторе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) в указателе [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , указанном в параметре *pContentInfo* .</span><span class="sxs-lookup"><span data-stu-id="c052c-116">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c052c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c052c-117">Requirements</span></span>



| <span data-ttu-id="c052c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c052c-118">Requirement</span></span> | <span data-ttu-id="c052c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c052c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c052c-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c052c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c052c-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c052c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c052c-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c052c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c052c-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c052c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c052c-124">Header</span><span class="sxs-lookup"><span data-stu-id="c052c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c052c-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c052c-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c052c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c052c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c052c-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c052c-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
