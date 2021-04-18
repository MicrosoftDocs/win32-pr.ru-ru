---
description: Указывает, требуется ли Имфтрансформ получать уведомления о завершении Меполицисет.
title: MFT_POLICY_SET_AWARE (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2effa9eab2b0b126c2849d39ce7ffe3f62d81e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719464"
---
# <a name="mft_policy_set_aware-attribute"></a><span data-ttu-id="02144-103">\_Атрибут с \_ поддержкой набора политик \_ MFT</span><span class="sxs-lookup"><span data-stu-id="02144-103">MFT\_POLICY\_SET\_AWARE attribute</span></span>

<span data-ttu-id="02144-104">Если значение не равно нулю, указывает, что **имфтрансформ** хочет получать уведомления о завершении [меполицисет](./mepolicyset.md) .</span><span class="sxs-lookup"><span data-stu-id="02144-104">If non-zero, indicates that the **IMFTransform** wants to receive [MEPolicySet](./mepolicyset.md) completion notifications.</span></span>

## <a name="data-type"></a><span data-ttu-id="02144-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="02144-105">Data type</span></span>

<span data-ttu-id="02144-106">**UINT32** (рассматривается как **bool**)</span><span class="sxs-lookup"><span data-stu-id="02144-106">**UINT32** (treated as **BOOL**)</span></span>

## <a name="getset"></a><span data-ttu-id="02144-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="02144-107">Get/set</span></span>

<span data-ttu-id="02144-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="02144-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="02144-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="02144-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="02144-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="02144-110">Applies to</span></span>

[<span data-ttu-id="02144-111">**имфинпуттрустаусорити**</span><span class="sxs-lookup"><span data-stu-id="02144-111">**IMFInputTrustAuthority**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfinputtrustauthority)

## <a name="remarks"></a><span data-ttu-id="02144-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02144-112">Remarks</span></span>

<span data-ttu-id="02144-113">Этот атрибут может использоваться средством расшифровки **имфинпуттрустаусорити** .</span><span class="sxs-lookup"><span data-stu-id="02144-113">This attributet can be used by an **IMFInputTrustAuthority** decrypter.</span></span> <span data-ttu-id="02144-114">Реализация модуля расшифровки содержимого (CDM) может включать реализацию **имфинпуттрустаусорити**.</span><span class="sxs-lookup"><span data-stu-id="02144-114">An implementation of a Content Decryption Module (CDM) may include an implementation of **IMFInputTrustAuthority**.</span></span> <span data-ttu-id="02144-115">Доступ к объекту **имфинпуттрустаусорити** осуществляется через [Имфконтентдекриптионмодуле:: креатетрустединпут](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).</span><span class="sxs-lookup"><span data-stu-id="02144-115">The **IMFInputTrustAuthority** object is accessed through [IMFContentDecryptionModule::CreateTrustedInput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).</span></span>


<span data-ttu-id="02144-116">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="02144-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="02144-117">Требования</span><span class="sxs-lookup"><span data-stu-id="02144-117">Requirements</span></span>



| <span data-ttu-id="02144-118">Требование</span><span class="sxs-lookup"><span data-stu-id="02144-118">Requirement</span></span> | <span data-ttu-id="02144-119">Значение</span><span class="sxs-lookup"><span data-stu-id="02144-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="02144-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02144-120">Minimum supported client</span></span><br/> | <span data-ttu-id="02144-121">Обновление Windows 10 от апреля 2020</span><span class="sxs-lookup"><span data-stu-id="02144-121">Windows 10 April 2020 Update</span></span>   <br/>                                        |
| <span data-ttu-id="02144-122">Header</span><span class="sxs-lookup"><span data-stu-id="02144-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="02144-123"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="02144-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02144-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02144-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02144-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="02144-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[<span data-ttu-id="02144-126">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="02144-126">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
