---
title: DRM_KeyID
description: '\_Атрибут KEYID DRM содержит идентификатор ключа.'
ms.assetid: 90406809-76d9-4559-afe8-6812efbc1477
keywords:
- DRM_KeyID формат Windows Media
topic_type:
- apiref
api_name:
- DRM_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a60afa330a7cf967b42a4d06009d9c921d8f56
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069600"
---
# <a name="drm_keyid"></a><span data-ttu-id="0eae2-104">\_KEYID DRM</span><span class="sxs-lookup"><span data-stu-id="0eae2-104">DRM\_KeyID</span></span>

<span data-ttu-id="0eae2-105">Атрибут **\_ KeyID DRM** содержит идентификатор ключа.</span><span class="sxs-lookup"><span data-stu-id="0eae2-105">The **DRM\_KeyID** attribute contains the key identifier.</span></span>

## <a name="global-constant"></a><span data-ttu-id="0eae2-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="0eae2-106">Global Constant</span></span>

<span data-ttu-id="0eae2-107">g \_ всзвмдрм \_ KeyID</span><span class="sxs-lookup"><span data-stu-id="0eae2-107">g\_wszWMDRM\_KeyID</span></span>

## <a name="data-type"></a><span data-ttu-id="0eae2-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0eae2-108">Data Type</span></span>

<span data-ttu-id="0eae2-109">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="0eae2-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="0eae2-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0eae2-110">Remarks</span></span>

<span data-ttu-id="0eae2-111">Этот атрибут имеется только для содержимого версии 7 DRM.</span><span class="sxs-lookup"><span data-stu-id="0eae2-111">This attribute is present for DRM Version 7 content only.</span></span> <span data-ttu-id="0eae2-112">Его можно задать с помощью [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , и его можно получить при помощи [**Ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="0eae2-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="0eae2-113">Один и тот же атрибут файла можно получить с помощью [**\_ Дрмхеадер \_ KeyID DRM**](drm-drmheader-keyid.md).</span><span class="sxs-lookup"><span data-stu-id="0eae2-113">The same file attribute can be retrieved using [**DRM\_DRMHeader\_KeyID**](drm-drmheader-keyid.md).</span></span>

<span data-ttu-id="0eae2-114">Идентификатор ключа используется в сочетании с начальным значением ключа для создания ключа содержимого, который используется для шифрования и расшифровки файла.</span><span class="sxs-lookup"><span data-stu-id="0eae2-114">The key ID is used in conjunction with the key seed to create the content key which is used to encrypt and decrypt the file.</span></span> <span data-ttu-id="0eae2-115">Приложение для записи использует идентификатор ключа для шифрования файла, а затем сохраняет идентификатор ключа в заголовке файла.</span><span class="sxs-lookup"><span data-stu-id="0eae2-115">The writer application uses the key ID to encrypt the file and then it stores the key ID in the file header.</span></span> <span data-ttu-id="0eae2-116">Когда приложение Player запрашивает лицензию для файла, компонент DRM отправляет идентификатор ключа (вместе с остальной частью заголовка DRM) на сервер лицензирования.</span><span class="sxs-lookup"><span data-stu-id="0eae2-116">When a player application requests a license for a file, the DRM component sends the key ID (along with the rest of the DRM header) to the license server.</span></span> <span data-ttu-id="0eae2-117">Сервер лицензирования, который имеет начальное значение секретного ключа, использует его и идентификатор ключа для создания ключа для файла, который затем вставляется в лицензию вместе с различными правами, которые будут применены к файлу.</span><span class="sxs-lookup"><span data-stu-id="0eae2-117">The license server, which has the secret key seed, uses it and the key ID to create a key for the file, which it then inserts into a license along with the various rights that will be applied to the file.</span></span>

<span data-ttu-id="0eae2-118">Как правило, одно начальное значение ключа используется с множеством идентификаторов ключей.</span><span class="sxs-lookup"><span data-stu-id="0eae2-118">Typically, one key seed is used with many key IDs.</span></span> <span data-ttu-id="0eae2-119">Начальное значение ключа — это секрет, который предоставляется только создателю содержимого и распространителю лицензий.</span><span class="sxs-lookup"><span data-stu-id="0eae2-119">The key seed is a secret shared only by the content creator and the license distributor.</span></span> <span data-ttu-id="0eae2-120">Идентификатор ключа используется клиентскими приложениями DRM и хранится в заголовке DRM в окне Clear.</span><span class="sxs-lookup"><span data-stu-id="0eae2-120">The key ID is used by DRM client applications and is stored in the DRM header in the clear.</span></span>

<span data-ttu-id="0eae2-121">Этот атрибут совпадает с [**DRM \_ дрмхеадер \_ KeyID**](drm-drmheader-keyid.md).</span><span class="sxs-lookup"><span data-stu-id="0eae2-121">This attribute is the same as [**DRM\_DRMHeader\_KeyID**](drm-drmheader-keyid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0eae2-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0eae2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eae2-123">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="0eae2-123">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




