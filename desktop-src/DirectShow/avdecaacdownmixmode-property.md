---
description: Указывает, использует ли декодер AAC стандартные уравнения MPEG-2/MPEG-4 стерео довнмикс или использует нестандартный довнмикс.
ms.assetid: a384d24e-07e2-45e7-84b8-e791feb64a83
title: Свойство Авдекаакдовнмиксмоде (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 388d1437dfe396d5072ef09082c4ad17ddb75953
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682288"
---
# <a name="avdecaacdownmixmode-property"></a><span data-ttu-id="d9f42-103">Авдекаакдовнмиксмоде, свойство</span><span class="sxs-lookup"><span data-stu-id="d9f42-103">AVDecAACDownmixMode property</span></span>

<span data-ttu-id="d9f42-104">Указывает, использует ли декодер AAC стандартные уравнения MPEG-2/MPEG-4 стерео довнмикс или использует нестандартный довнмикс.</span><span class="sxs-lookup"><span data-stu-id="d9f42-104">Specifies whether an AAC decoder uses standard MPEG-2/MPEG-4 stereo downmix equations, or uses a non-standard downmix.</span></span>

<span data-ttu-id="d9f42-105">Примером нестандартного довнмикс является тот, который определен документом АРИБ STD-B21 версии 4,4.</span><span class="sxs-lookup"><span data-stu-id="d9f42-105">An example of a non-standard downmix is the one defined by ARIB document STD-B21 version 4.4.</span></span>

<span data-ttu-id="d9f42-106">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d9f42-106">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d9f42-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d9f42-107">Data type</span></span>

<span data-ttu-id="d9f42-108">**UINT32** (**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="d9f42-108">**UINT32** (**VT\_UI4**</span></span>

## <a name="property-guid"></a><span data-ttu-id="d9f42-109">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="d9f42-109">Property GUID</span></span>

<span data-ttu-id="d9f42-110">**КОДЕКАПИ \_ авдекаакдовнмиксмоде**</span><span class="sxs-lookup"><span data-stu-id="d9f42-110">**CODECAPI\_AVDecAACDownmixMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="d9f42-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d9f42-111">Property value</span></span>

<span data-ttu-id="d9f42-112">Значение этого свойства является членом перечисления [**еавдекаакдовнмиксмоде**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) .</span><span class="sxs-lookup"><span data-stu-id="d9f42-112">The value of this property is a member of the [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9f42-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d9f42-113">Requirements</span></span>



| <span data-ttu-id="d9f42-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d9f42-114">Requirement</span></span> | <span data-ttu-id="d9f42-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d9f42-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f42-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9f42-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d9f42-117">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d9f42-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d9f42-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9f42-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d9f42-119">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="d9f42-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d9f42-120">Header</span><span class="sxs-lookup"><span data-stu-id="d9f42-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9f42-121"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9f42-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9f42-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9f42-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f42-123">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="d9f42-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d9f42-124">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="d9f42-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

