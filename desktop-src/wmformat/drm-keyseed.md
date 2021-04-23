---
title: DRM_KeySeed
description: Свойство DRM \_ кэйсид содержит начальное значение ключа, которое будет использоваться в сочетании с KeyID для создания ключа.
ms.assetid: 38613d50-89c2-4422-9265-5e89de030ae9
keywords:
- DRM_KeySeed формат Windows Media
topic_type:
- apiref
api_name:
- DRM_KeySeed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 698db5fe5a1123af0a7b4623d304bf0569bbf253
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105672251"
---
# <a name="drm_keyseed"></a><span data-ttu-id="faa62-104">\_КЭЙСИД DRM</span><span class="sxs-lookup"><span data-stu-id="faa62-104">DRM\_KeySeed</span></span>

<span data-ttu-id="faa62-105">Свойство **DRM \_ кэйсид** содержит начальное значение ключа, которое будет использоваться в сочетании с KeyID для создания ключа.</span><span class="sxs-lookup"><span data-stu-id="faa62-105">The **DRM\_KeySeed** property contains the key seed that will be used in conjunction with the KeyID to create the key.</span></span>

## <a name="global-constant"></a><span data-ttu-id="faa62-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="faa62-106">Global Constant</span></span>

<span data-ttu-id="faa62-107">g \_ всзвмдрм \_ кэйсид</span><span class="sxs-lookup"><span data-stu-id="faa62-107">g\_wszWMDRM\_KeySeed</span></span>

## <a name="data-type"></a><span data-ttu-id="faa62-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="faa62-108">Data Type</span></span>

<span data-ttu-id="faa62-109">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="faa62-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="faa62-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="faa62-110">Remarks</span></span>

<span data-ttu-id="faa62-111">Это свойство можно задать с помощью [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span><span class="sxs-lookup"><span data-stu-id="faa62-111">This property can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span> <span data-ttu-id="faa62-112">Он недоступен для объекта Reader.</span><span class="sxs-lookup"><span data-stu-id="faa62-112">It is not accessible by the reader object.</span></span>

<span data-ttu-id="faa62-113">Начальное значение обычно используется для защиты нескольких файлов или наборов файлов, например всех файлов, выданных сервером лицензирования, или, возможно, всех файлов определенным исполнителем.</span><span class="sxs-lookup"><span data-stu-id="faa62-113">A key seed is typically used to protect multiple files or sets of files, for example all the files issued by a license server, or perhaps all the files by a particular artist.</span></span> <span data-ttu-id="faa62-114">Однако KeyID уникальны для каждого файла.</span><span class="sxs-lookup"><span data-stu-id="faa62-114">The KeyID, however, is unique for each file.</span></span>

<span data-ttu-id="faa62-115">Начальное значение ключа должно оставаться секретом, который является общим только для создателя содержимого и распространителя лицензий.</span><span class="sxs-lookup"><span data-stu-id="faa62-115">The key seed must remain a secret that is shared only between the content creator and the license distributor.</span></span> <span data-ttu-id="faa62-116">Это значение не хранится в заголовке DRM и не является ни необходимым, ни недоступным для приложений проигрывателя DRM.</span><span class="sxs-lookup"><span data-stu-id="faa62-116">This value is not stored in the DRM header and it is neither needed by nor accessible to DRM player applications.</span></span>

<span data-ttu-id="faa62-117">Новое начальное значение ключа можно создать с помощью метода [**ивмдрмвритер:: женератекэйсид**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) или любых других подходящих средств.</span><span class="sxs-lookup"><span data-stu-id="faa62-117">A new key seed can be generated using the [**IWMDRMWriter::GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) method or by any other suitable means.</span></span>

## <a name="see-also"></a><span data-ttu-id="faa62-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="faa62-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faa62-119">**Свойства DRM**</span><span class="sxs-lookup"><span data-stu-id="faa62-119">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




