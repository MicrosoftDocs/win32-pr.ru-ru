---
title: DRM_LASignaturePrivKey
description: Свойство DRM \_ ласигнатурепривкэй содержит закрытый ключ, используемый для шифрования заголовка DRM.
ms.assetid: b7083237-da11-4f31-a143-c0278a54b5a6
keywords:
- DRM_LASignaturePrivKey формат Windows Media
topic_type:
- apiref
api_name:
- DRM_LASignaturePrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdb22f3abc57fc2331ff87bd05bc05d580d607c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412557"
---
# <a name="drm_lasignatureprivkey"></a><span data-ttu-id="e8b7c-104">\_ЛАСИГНАТУРЕПРИВКЭЙ DRM</span><span class="sxs-lookup"><span data-stu-id="e8b7c-104">DRM\_LASignaturePrivKey</span></span>

<span data-ttu-id="e8b7c-105">Свойство **DRM \_ ласигнатурепривкэй** содержит закрытый ключ, используемый для шифрования заголовка DRM.</span><span class="sxs-lookup"><span data-stu-id="e8b7c-105">The **DRM\_LASignaturePrivKey** property contains the private key that is used to encrypt the DRM header.</span></span>

## <a name="global-constant"></a><span data-ttu-id="e8b7c-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="e8b7c-106">Global Constant</span></span>

<span data-ttu-id="e8b7c-107">g \_ всзвмдрм \_ ласигнатурепривкэй</span><span class="sxs-lookup"><span data-stu-id="e8b7c-107">g\_wszWMDRM\_LASignaturePrivKey</span></span>

## <a name="data-type"></a><span data-ttu-id="e8b7c-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e8b7c-108">Data Type</span></span>

<span data-ttu-id="e8b7c-109">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="e8b7c-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="e8b7c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8b7c-110">Remarks</span></span>

<span data-ttu-id="e8b7c-111">Это свойство может быть создано с помощью метода [**ивмдрмвритер:: женератесигнингкэйпаир**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) .</span><span class="sxs-lookup"><span data-stu-id="e8b7c-111">This property can be generated using the [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) method.</span></span> <span data-ttu-id="e8b7c-112">Это свойство должно оставаться секретом, известным только создателю содержимого.</span><span class="sxs-lookup"><span data-stu-id="e8b7c-112">This property should remain a secret known only by the content creator.</span></span> <span data-ttu-id="e8b7c-113">Это свойство можно задать с помощью метода [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) .</span><span class="sxs-lookup"><span data-stu-id="e8b7c-113">This property can be set with the [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) method.</span></span> <span data-ttu-id="e8b7c-114">Он недоступен для объекта Reader.</span><span class="sxs-lookup"><span data-stu-id="e8b7c-114">It is not accessible to the reader object.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8b7c-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8b7c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8b7c-116">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="e8b7c-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




