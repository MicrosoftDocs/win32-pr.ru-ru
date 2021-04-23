---
description: Указывает, как загрузчик топологии подключает этот узел топологии и является ли этот узел необязательным.
ms.assetid: 8d70e1af-607b-47c3-9808-091c95fd05b7
title: Атрибут MF_TOPONODE_CONNECT_METHOD (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3db5fef529ef451fa02ac4a29e62002b0a1996a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272107"
---
# <a name="mf_toponode_connect_method-attribute"></a><span data-ttu-id="0e838-103">\_ \_ Атрибут метода Connect топоноде MF \_</span><span class="sxs-lookup"><span data-stu-id="0e838-103">MF\_TOPONODE\_CONNECT\_METHOD attribute</span></span>

<span data-ttu-id="0e838-104">Указывает, как загрузчик топологии подключает этот узел топологии и является ли этот узел необязательным.</span><span class="sxs-lookup"><span data-stu-id="0e838-104">Specifies how the topology loader connects this topology node, and whether this node is optional.</span></span>

## <a name="data-type"></a><span data-ttu-id="0e838-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0e838-105">Data type</span></span>

<span data-ttu-id="0e838-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0e838-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0e838-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e838-107">Remarks</span></span>

<span data-ttu-id="0e838-108">Этот атрибут применяется ко всем типам узлов.</span><span class="sxs-lookup"><span data-stu-id="0e838-108">This attribute applies to all node types.</span></span>

<span data-ttu-id="0e838-109">Значение атрибута представляет собой побитовое **или** для флагов из перечисления [**\_ \_ метода MF Connect**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) .</span><span class="sxs-lookup"><span data-stu-id="0e838-109">The attribute value is a bitwise **OR** of flags from the [**MF\_CONNECT\_METHOD**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) enumeration.</span></span> <span data-ttu-id="0e838-110">Если этот атрибут не задан, по умолчанию используется значение **MF \_ Connect \_ Разрешить \_ декодер**.</span><span class="sxs-lookup"><span data-stu-id="0e838-110">If this attribute is not set, the default value is **MF\_CONNECT\_ALLOW\_DECODER**.</span></span>

<span data-ttu-id="0e838-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="0e838-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e838-112">Требования</span><span class="sxs-lookup"><span data-stu-id="0e838-112">Requirements</span></span>



| <span data-ttu-id="0e838-113">Требование</span><span class="sxs-lookup"><span data-stu-id="0e838-113">Requirement</span></span> | <span data-ttu-id="0e838-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0e838-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e838-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e838-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0e838-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e838-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0e838-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e838-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0e838-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0e838-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0e838-119">Header</span><span class="sxs-lookup"><span data-stu-id="0e838-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e838-120"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e838-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e838-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e838-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e838-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0e838-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0e838-123">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="0e838-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0e838-124">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0e838-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0e838-125">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="0e838-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="0e838-126">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="0e838-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




