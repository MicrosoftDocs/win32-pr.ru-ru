---
description: Указывает, когда преобразуются преобразования.
ms.assetid: 68332106-d1fe-467b-8baa-1e592b9cc243
title: Атрибут MF_TOPONODE_DRAIN (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b87d626738b82f4504673392bd0fe159e2722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711296"
---
# <a name="mf_toponode_drain-attribute"></a><span data-ttu-id="8c6b8-103">\_ \_ Атрибут слива MF топоноде</span><span class="sxs-lookup"><span data-stu-id="8c6b8-103">MF\_TOPONODE\_DRAIN attribute</span></span>

<span data-ttu-id="8c6b8-104">Указывает, когда преобразуются преобразования.</span><span class="sxs-lookup"><span data-stu-id="8c6b8-104">Specifies when a transform is drained.</span></span>

## <a name="data-type"></a><span data-ttu-id="8c6b8-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8c6b8-105">Data type</span></span>

<span data-ttu-id="8c6b8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8c6b8-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="8c6b8-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c6b8-107">Remarks</span></span>

<span data-ttu-id="8c6b8-108">Этот атрибут применяется к узлам преобразования (**\_ \_ \_ узел преобразования топологии MF**).</span><span class="sxs-lookup"><span data-stu-id="8c6b8-108">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="8c6b8-109">Значение атрибута является членом перечисления [**\_ \_ \_ режима стока топоноде**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_drain_mode) .</span><span class="sxs-lookup"><span data-stu-id="8c6b8-109">The value of the attribute is a member of the [**MF\_TOPONODE\_DRAIN\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_drain_mode) enumeration.</span></span> <span data-ttu-id="8c6b8-110">Если этот атрибут не задан, по умолчанию используется значение **MF \_ топоноде \_ сток \_ по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="8c6b8-110">If this attribute is not set, the default value is **MF\_TOPONODE\_DRAIN\_DEFAULT**.</span></span>

<span data-ttu-id="8c6b8-111">Сток выполняется путем вызова [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) в преобразовании с сообщением о [**\_ \_ \_ стоке команды сообщения MFT**](mft-message-command-drain.md) .</span><span class="sxs-lookup"><span data-stu-id="8c6b8-111">Draining is performed by calling [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) on the transform with the [**MFT\_MESSAGE\_COMMAND\_DRAIN**](mft-message-command-drain.md) message.</span></span> <span data-ttu-id="8c6b8-112">Дополнительные сведения см. в статье перечисление [**\_ \_ типов сообщений MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) .</span><span class="sxs-lookup"><span data-stu-id="8c6b8-112">For more information, see [**MFT\_MESSAGE\_TYPE**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) enumeration.</span></span>

<span data-ttu-id="8c6b8-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="8c6b8-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c6b8-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8c6b8-114">Requirements</span></span>



| <span data-ttu-id="8c6b8-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8c6b8-115">Requirement</span></span> | <span data-ttu-id="8c6b8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8c6b8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8c6b8-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c6b8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8c6b8-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c6b8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8c6b8-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c6b8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8c6b8-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8c6b8-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8c6b8-121">Header</span><span class="sxs-lookup"><span data-stu-id="8c6b8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c6b8-122"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c6b8-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c6b8-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c6b8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c6b8-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8c6b8-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8c6b8-125">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="8c6b8-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="8c6b8-126">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8c6b8-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="8c6b8-127">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="8c6b8-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="8c6b8-128">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="8c6b8-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




