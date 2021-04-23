---
description: Указывает, что типы единиц уровня абстрагирования сети (NAL) следует перенаправлять в выходные образцы с помощью декодера.
ms.assetid: 2A1D8629-EB66-4F72-9AD7-93123D941BB0
title: Атрибут MF_MT_FORWARD_CUSTOM_NALU (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a318523f52ab7d65450c4c2f35b7bfbf63d5f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546623"
---
# <a name="mf_mt_forward_custom_nalu-attribute"></a><span data-ttu-id="c1de4-103">MF \_ \_ \_ настраиваемый \_ атрибут налу</span><span class="sxs-lookup"><span data-stu-id="c1de4-103">MF\_MT\_FORWARD\_CUSTOM\_NALU attribute</span></span>

<span data-ttu-id="c1de4-104">Указывает, что типы единиц уровня абстрагирования сети (NAL) следует перенаправлять в выходные образцы с помощью декодера.</span><span class="sxs-lookup"><span data-stu-id="c1de4-104">Specifies that network abstraction layer (NAL) unit types should be forwarded on output samples by the decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="c1de4-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c1de4-105">Data type</span></span>

<span data-ttu-id="c1de4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c1de4-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c1de4-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1de4-107">Remarks</span></span>

<span data-ttu-id="c1de4-108">Если декодер анализирует налу, он не будет перенаправлен.</span><span class="sxs-lookup"><span data-stu-id="c1de4-108">If the decoder parses a NALU then it will not be forwarded.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1de4-109">Требования</span><span class="sxs-lookup"><span data-stu-id="c1de4-109">Requirements</span></span>



| <span data-ttu-id="c1de4-110">Требование</span><span class="sxs-lookup"><span data-stu-id="c1de4-110">Requirement</span></span> | <span data-ttu-id="c1de4-111">Значение</span><span class="sxs-lookup"><span data-stu-id="c1de4-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1de4-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1de4-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c1de4-113">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="c1de4-113">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c1de4-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1de4-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c1de4-115">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="c1de4-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c1de4-116">Header</span><span class="sxs-lookup"><span data-stu-id="c1de4-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1de4-117"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1de4-117"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




