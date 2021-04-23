---
title: DRM_HeaderSignPrivKey
description: Свойство DRM \_ хеадерсигнпривкэй содержит закрытый ключ, используемый для подписи заголовка ASF.
ms.assetid: 0f32e63d-d416-4a1d-b10c-2534b747adf3
keywords:
- DRM_HeaderSignPrivKey формат Windows Media
topic_type:
- apiref
api_name:
- DRM_HeaderSignPrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af73ea90acca6c20817f35a035f8f297aa56e90b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788755"
---
# <a name="drm_headersignprivkey"></a><span data-ttu-id="0cea2-104">\_ХЕАДЕРСИГНПРИВКЭЙ DRM</span><span class="sxs-lookup"><span data-stu-id="0cea2-104">DRM\_HeaderSignPrivKey</span></span>

<span data-ttu-id="0cea2-105">Свойство **DRM \_ хеадерсигнпривкэй** содержит закрытый ключ, используемый для подписи заголовка ASF.</span><span class="sxs-lookup"><span data-stu-id="0cea2-105">The **DRM\_HeaderSignPrivKey** property contains the private key used to sign the ASF header.</span></span>

## <a name="global-constant"></a><span data-ttu-id="0cea2-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="0cea2-106">Global Constant</span></span>

<span data-ttu-id="0cea2-107">g \_ всзвмдрм \_ хеадерсигнпривкэй</span><span class="sxs-lookup"><span data-stu-id="0cea2-107">g\_wszWMDRM\_HeaderSignPrivKey</span></span>

## <a name="data-type"></a><span data-ttu-id="0cea2-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0cea2-108">Data Type</span></span>

<span data-ttu-id="0cea2-109">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="0cea2-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="0cea2-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0cea2-110">Remarks</span></span>

<span data-ttu-id="0cea2-111">Это свойство создается с помощью [**ивмдрмвритер:: женератесигнингкэйпаир**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).</span><span class="sxs-lookup"><span data-stu-id="0cea2-111">This property is generated using the [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).</span></span> <span data-ttu-id="0cea2-112">Обеспечьте секрет ключа и поделитесь открытым ключом только со службой лицензирования.</span><span class="sxs-lookup"><span data-stu-id="0cea2-112">Keep this key secret and share the public key only with the license service.</span></span> <span data-ttu-id="0cea2-113">После установки этого ключа компонент DRM будет использовать его для подписи заголовка ASF-файла (а не заголовка DRM, который подписан с помощью значений объектов цифровых подписей, таких как DRM \_ ласигнатурепривкэй).</span><span class="sxs-lookup"><span data-stu-id="0cea2-113">After you set this key, the DRM component will use it to sign the ASF file header (not the DRM header which is signed with the digital signature object values such as DRM\_LASignaturePrivKey).</span></span> <span data-ttu-id="0cea2-114">Очевидно, **\_ хеадерсигнпривкэй DRM** не включается в заголовок файла.</span><span class="sxs-lookup"><span data-stu-id="0cea2-114">Obviously, **DRM\_HeaderSignPrivKey** is not included in the file headert.</span></span>

<span data-ttu-id="0cea2-115">Это свойство недоступно из объекта модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="0cea2-115">This property is not accessible from the reader object.</span></span> <span data-ttu-id="0cea2-116">Его можно задать из объекта модуля записи с помощью [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span><span class="sxs-lookup"><span data-stu-id="0cea2-116">It can be set from the writer object using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span>

## <a name="see-also"></a><span data-ttu-id="0cea2-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0cea2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cea2-118">**Свойства DRM**</span><span class="sxs-lookup"><span data-stu-id="0cea2-118">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




