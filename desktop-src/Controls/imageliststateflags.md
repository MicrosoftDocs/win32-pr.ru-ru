---
title: ИМАЖЕЛИСТСТАТЕФЛАГС (Коммктрл. h)
description: Следующие флаги передаются в метод Draw IImageList в элементе Фстате элемента ИМАЖЕЛИСТДРАВПАРАМС.
ms.assetid: a22b4acf-c290-44b2-9216-b006d0326236
topic_type:
- apiref
api_name:
- ILS_NORMAL
- ILS_GLOW
- ILS_SHADOW
- ILS_SATURATE
- ILS_ALPHA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea580294f54b6e2fc5c3e5b6aee1119811c22e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071459"
---
# <a name="imageliststateflags"></a><span data-ttu-id="34cb8-103">имажелистстатефлагс</span><span class="sxs-lookup"><span data-stu-id="34cb8-103">IMAGELISTSTATEFLAGS</span></span>

<span data-ttu-id="34cb8-104">Следующие флаги передаются в метод [**IImageList::D RAW**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) в элементе **фстате** элемента [**имажелистдравпарамс**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).</span><span class="sxs-lookup"><span data-stu-id="34cb8-104">The following flags are passed to the [**IImageList::Draw**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) method in the **fState** member of [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).</span></span>



| <span data-ttu-id="34cb8-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="34cb8-105">Constant/value</span></span>                                                                                                                                                                                                             | <span data-ttu-id="34cb8-106">Описание</span><span class="sxs-lookup"><span data-stu-id="34cb8-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILS_NORMAL"></span><span id="ils_normal"></span><dl> <span data-ttu-id="34cb8-107"><dt>**ILS \_ Обычная**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="34cb8-107"><dt>**ILS\_NORMAL**</dt> <dt>0x00000000</dt></span></span> </dl>       | <span data-ttu-id="34cb8-108">Состояние изображения не изменяется.</span><span class="sxs-lookup"><span data-stu-id="34cb8-108">The image state is not modified.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ILS_GLOW"></span><span id="ils_glow"></span><dl> <span data-ttu-id="34cb8-109"><dt>**ILS \_ СВЕЧЕНИе**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="34cb8-109"><dt>**ILS\_GLOW**</dt> <dt>0x00000001</dt></span></span> </dl>             | <span data-ttu-id="34cb8-110">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="34cb8-110">Not supported.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SHADOW"></span><span id="ils_shadow"></span><dl> <span data-ttu-id="34cb8-111"><dt>**ILS \_ ТЕНЕВая**</dt> версия <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="34cb8-111"><dt>**ILS\_SHADOW**</dt> <dt>0x00000002</dt></span></span> </dl>       | <span data-ttu-id="34cb8-112">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="34cb8-112">Not supported.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SATURATE"></span><span id="ils_saturate"></span><dl> <span data-ttu-id="34cb8-113"><dt>**ILS \_ НАСЫЩЕНность**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="34cb8-113"><dt>**ILS\_SATURATE**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="34cb8-114">Уменьшает насыщенность цвета значка до оттенков серого.</span><span class="sxs-lookup"><span data-stu-id="34cb8-114">Reduces the color saturation of the icon to grayscale.</span></span> <span data-ttu-id="34cb8-115">Это относится только к образам 32 бита.</span><span class="sxs-lookup"><span data-stu-id="34cb8-115">This only affects 32bpp images.</span></span> <br/>                                                                                                                                                                                                                                                                                            |
| <span id="ILS_ALPHA"></span><span id="ils_alpha"></span><dl> <span data-ttu-id="34cb8-116"><dt>**ILS \_ Альфа**</dt> - <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="34cb8-116"><dt>**ILS\_ALPHA**</dt> <dt>0x00000008</dt></span></span> </dl>          | <span data-ttu-id="34cb8-117">Альфа-смешение значка.</span><span class="sxs-lookup"><span data-stu-id="34cb8-117">Alpha blends the icon.</span></span> <span data-ttu-id="34cb8-118">Альфа-смешение определяет уровень прозрачности значка в соответствии со значением его альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="34cb8-118">Alpha blending controls the transparency level of an icon, according to the value of its alpha channel.</span></span> <span data-ttu-id="34cb8-119">Значение альфа-канала обозначается элементом **Frame** в методе [**имажелистдравпарамс**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) .</span><span class="sxs-lookup"><span data-stu-id="34cb8-119">The value of the alpha channel is indicated by the **frame** member in the [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) method.</span></span> <span data-ttu-id="34cb8-120">Альфа-канал может принимать значение от 0 до 255, при этом 0 становится полностью прозрачным, а 255 — полностью непрозрачным.</span><span class="sxs-lookup"><span data-stu-id="34cb8-120">The alpha channel can be from 0 to 255, with 0 being completely transparent, and 255 being completely opaque.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="34cb8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="34cb8-121">Requirements</span></span>



| <span data-ttu-id="34cb8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="34cb8-122">Requirement</span></span> | <span data-ttu-id="34cb8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="34cb8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34cb8-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34cb8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="34cb8-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="34cb8-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="34cb8-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34cb8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="34cb8-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="34cb8-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="34cb8-128">Header</span><span class="sxs-lookup"><span data-stu-id="34cb8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="34cb8-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="34cb8-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

