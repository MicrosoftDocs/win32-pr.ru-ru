---
description: Значение, указывающее, захвачен ли кадр с помощью активного инфракрасного (IR) освещения.
ms.assetid: D84772C8-902F-4302-8288-0430892A1896
title: Атрибут MF_CAPTURE_METADATA_FRAME_ILLUMINATION (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9aa60b5e921e99ac4f4c56cb4643af8389aa91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692509"
---
# <a name="mf_capture_metadata_frame_illumination-attribute"></a><span data-ttu-id="04527-103">\_ \_ \_ Атрибут освещения захвата метаданных записи MF \_</span><span class="sxs-lookup"><span data-stu-id="04527-103">MF\_CAPTURE\_METADATA\_FRAME\_ILLUMINATION attribute</span></span>

<span data-ttu-id="04527-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="04527-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="04527-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="04527-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="04527-106">Значение, указывающее, захвачен ли кадр с помощью активного инфракрасного (IR) освещения.</span><span class="sxs-lookup"><span data-stu-id="04527-106">A value indicating whether a frame was captured using active infrared (IR) illumination.</span></span>

## <a name="data-type"></a><span data-ttu-id="04527-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="04527-107">Data type</span></span>

<span data-ttu-id="04527-108">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="04527-108">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="04527-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04527-109">Remarks</span></span>

<span data-ttu-id="04527-110">Этот атрибут является битовой маской.</span><span class="sxs-lookup"><span data-stu-id="04527-110">This attribute is a bitmask.</span></span> <span data-ttu-id="04527-111">Это 64-битное значение для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="04527-111">It is a 64 bit value for backward compatibility.</span></span>

<span data-ttu-id="04527-112">Active освещения — когда устройство имеет световой передатчик, близко к ИК-камере, порожденной лампочкой, для освещения сцены, как правило, выдается IR-сигнал, чтобы не беспокоить человеческих глаз.</span><span class="sxs-lookup"><span data-stu-id="04527-112">Active illumination is when a device has a light emitter close to the IR camera emitting a beam of light to illuminate the scene, typically emitting IR light so it won’t disturb human eyes.</span></span> <span data-ttu-id="04527-113">Задайте значение (значение & 0x1)! = 0, если кадр был захвачен при включении и задании активных освещения (значение & 0x1) = = 0, если активная освещения была отключена.</span><span class="sxs-lookup"><span data-stu-id="04527-113">Set value to (value & 0x1) != 0 if frame was captured when active illumination was on and set (value & 0x1) == 0 if active illumination was off.</span></span>

## <a name="requirements"></a><span data-ttu-id="04527-114">Требования</span><span class="sxs-lookup"><span data-stu-id="04527-114">Requirements</span></span>



| <span data-ttu-id="04527-115">Требование</span><span class="sxs-lookup"><span data-stu-id="04527-115">Requirement</span></span> | <span data-ttu-id="04527-116">Значение</span><span class="sxs-lookup"><span data-stu-id="04527-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="04527-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04527-117">Minimum supported client</span></span><br/> | <span data-ttu-id="04527-118">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="04527-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="04527-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04527-119">Minimum supported server</span></span><br/> | <span data-ttu-id="04527-120">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="04527-120">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="04527-121">Header</span><span class="sxs-lookup"><span data-stu-id="04527-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="04527-122"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="04527-122"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




