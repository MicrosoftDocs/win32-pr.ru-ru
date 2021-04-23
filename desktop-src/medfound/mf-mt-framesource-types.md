---
description: Значение, указывающее тип датчика, предоставляемого источником кадра, например цвет, инфракрасная связь или глубина.
ms.assetid: F327B9E9-C01C-4F5B-9A26-6404ECD7F27F
title: Атрибут MF_MT_FRAMESOURCE_TYPES (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4475d66aea245ac9295a7996da2c37cabdb9627
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656568"
---
# <a name="mf_mt_framesource_types-attribute"></a><span data-ttu-id="9e1ce-103">\_ \_ Атрибут типа MF MT фрамесаурце \_</span><span class="sxs-lookup"><span data-stu-id="9e1ce-103">MF\_MT\_FRAMESOURCE\_TYPES attribute</span></span>

<span data-ttu-id="9e1ce-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="9e1ce-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9e1ce-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="9e1ce-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9e1ce-106">Значение, указывающее тип датчика, предоставляемого источником кадра, например цвет, инфракрасная связь или глубина.</span><span class="sxs-lookup"><span data-stu-id="9e1ce-106">A value that indicates the type of sensor provided by a frame source, such as color, infrared, or depth.</span></span>

## <a name="data-type"></a><span data-ttu-id="9e1ce-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9e1ce-107">Data type</span></span>

<span data-ttu-id="9e1ce-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9e1ce-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9e1ce-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e1ce-109">Remarks</span></span>

<span data-ttu-id="9e1ce-110">Это значение должно быть членом перечисления [**\_ мффрамесаурцетипес**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9e1ce-110">This value should be a member of the [**\_MFFrameSourceTypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) enumeration.</span></span> <span data-ttu-id="9e1ce-111">Для обеспечения обратной совместимости, если этот атрибут не определен для типа мультимедиа, предполагается, что это **\_ мффрамесаурцетес:: Color**.</span><span class="sxs-lookup"><span data-stu-id="9e1ce-111">For backward compatibility, when this attribute is not defined on a media type, it's assumed to be **\_MFFrameSourceTyes::Color**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e1ce-112">Требования</span><span class="sxs-lookup"><span data-stu-id="9e1ce-112">Requirements</span></span>



| <span data-ttu-id="9e1ce-113">Требование</span><span class="sxs-lookup"><span data-stu-id="9e1ce-113">Requirement</span></span> | <span data-ttu-id="9e1ce-114">Значение</span><span class="sxs-lookup"><span data-stu-id="9e1ce-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9e1ce-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e1ce-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9e1ce-116">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="9e1ce-116">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9e1ce-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e1ce-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9e1ce-118">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="9e1ce-118">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="9e1ce-119">Header</span><span class="sxs-lookup"><span data-stu-id="9e1ce-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e1ce-120"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e1ce-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
