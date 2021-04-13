---
description: Задает локальную политику управления подключаемым модулем.
ms.assetid: 2936F3C9-3BCB-452A-8C03-35D73A200CE2
title: Атрибут MF_LOCAL_PLUGIN_CONTROL_POLICY (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1bdaee17651cebfdc844bb5b6998907b1cd295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647735"
---
# <a name="mf_local_plugin_control_policy-attribute"></a><span data-ttu-id="6aea2-103">\_ \_ \_ Атрибут политики управления локальным подключаемым модулем MF \_</span><span class="sxs-lookup"><span data-stu-id="6aea2-103">MF\_LOCAL\_PLUGIN\_CONTROL\_POLICY attribute</span></span>

<span data-ttu-id="6aea2-104">Задает локальную политику управления подключаемым модулем.</span><span class="sxs-lookup"><span data-stu-id="6aea2-104">Specifies a local plugin control policy.</span></span>

## <a name="data-type"></a><span data-ttu-id="6aea2-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6aea2-105">Data type</span></span>

<span data-ttu-id="6aea2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6aea2-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6aea2-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6aea2-107">Remarks</span></span>

<span data-ttu-id="6aea2-108">Присвойте этому атрибуту одно из [**значений \_ \_ \_ политики управления подключаемым модулем MF**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) .</span><span class="sxs-lookup"><span data-stu-id="6aea2-108">Set this attribute to one of the [**MF\_PLUGIN\_CONTROL\_POLICY**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) values.</span></span>

<span data-ttu-id="6aea2-109">Эти атрибуты позволяют приложению указать более ограниченную локальную политику по сравнению с политикой уровня процесса, настроенной [**имфплугинконтрол**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol).</span><span class="sxs-lookup"><span data-stu-id="6aea2-109">This attributes allows the app to specify a more restrictive local policy than the process-wide policy configured by [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol).</span></span>

## <a name="requirements"></a><span data-ttu-id="6aea2-110">Требования</span><span class="sxs-lookup"><span data-stu-id="6aea2-110">Requirements</span></span>



| <span data-ttu-id="6aea2-111">Требование</span><span class="sxs-lookup"><span data-stu-id="6aea2-111">Requirement</span></span> | <span data-ttu-id="6aea2-112">Значение</span><span class="sxs-lookup"><span data-stu-id="6aea2-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6aea2-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6aea2-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6aea2-114">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6aea2-114">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6aea2-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6aea2-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6aea2-116">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6aea2-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6aea2-117">Header</span><span class="sxs-lookup"><span data-stu-id="6aea2-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="6aea2-118"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6aea2-118"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6aea2-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6aea2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aea2-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6aea2-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6aea2-121">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="6aea2-121">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




