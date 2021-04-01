---
description: Идентификатор, который можно задать для Имфаутпутполици.
ms.assetid: 89da33c8-97af-4c56-8bdb-2ac588810d77
title: MF_POLICY_ID (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787195b20980164d7534bccc267781cdbb7510e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081506"
---
# <a name="mf_policy_id-attribute"></a><span data-ttu-id="00176-103">\_ \_ Атрибут идентификатора политики MF</span><span class="sxs-lookup"><span data-stu-id="00176-103">MF\_POLICY\_ID attribute</span></span>

<span data-ttu-id="00176-104">Идентификатор, который можно задать для [имфаутпутполици](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy).</span><span class="sxs-lookup"><span data-stu-id="00176-104">An identifier that can be set on an [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy).</span></span>

## <a name="data-type"></a><span data-ttu-id="00176-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="00176-105">Data type</span></span>

<span data-ttu-id="00176-106">**UINT32** (рассматривается как **bool**)</span><span class="sxs-lookup"><span data-stu-id="00176-106">**UINT32** (treated as **BOOL**)</span></span>

## <a name="remarks"></a><span data-ttu-id="00176-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00176-107">Remarks</span></span>

<span data-ttu-id="00176-108">Значение может быть получено из события мультимедиа [меполицисет](./mepolicyset.md) .</span><span class="sxs-lookup"><span data-stu-id="00176-108">The value can be recieved from the [MEPolicySet](./mepolicyset.md) media event.</span></span> <span data-ttu-id="00176-109">Он сохраняется как полезная нагрузка типа **VT_UI4** в событии **меполицисет** .</span><span class="sxs-lookup"><span data-stu-id="00176-109">It is stored as a **VT_UI4** type payload in the **MEPolicySet** event.</span></span>


## <a name="requirements"></a><span data-ttu-id="00176-110">Требования</span><span class="sxs-lookup"><span data-stu-id="00176-110">Requirements</span></span>



| <span data-ttu-id="00176-111">Требование</span><span class="sxs-lookup"><span data-stu-id="00176-111">Requirement</span></span> | <span data-ttu-id="00176-112">Значение</span><span class="sxs-lookup"><span data-stu-id="00176-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="00176-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00176-113">Minimum supported client</span></span><br/> | <span data-ttu-id="00176-114">Обновление Windows 10 от апреля 2020</span><span class="sxs-lookup"><span data-stu-id="00176-114">Windows 10 April 2020 Update</span></span>   <br/>                                      |
| <span data-ttu-id="00176-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00176-115">Minimum supported server</span></span><br/> | <span data-ttu-id="00176-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="00176-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="00176-117">Header</span><span class="sxs-lookup"><span data-stu-id="00176-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="00176-118"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="00176-118"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00176-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00176-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00176-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="00176-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>



 

 
