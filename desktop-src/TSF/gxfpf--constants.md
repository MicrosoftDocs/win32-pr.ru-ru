---
title: Константы GXFPF_ (Текстстор. h)
description: ГКСФПФ \_ \ константы задает позицию символа, возвращаемую в зависимости от экранных координат точки относительно ограничивающего прямоугольника символа.
ms.assetid: e69e5a4c-65e6-4d9b-8cb0-962524aa5d39
topic_type:
- apiref
api_name:
- GXFPF_ROUND_NEAREST
- GXFPF_NEAREST
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d2dfc5ce874a7c4ce5b205c9b92436040aa60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489705"
---
# <a name="gxfpf_-constants"></a><span data-ttu-id="77e97-103">\_ \* КОНСТАНТы гксфпф</span><span class="sxs-lookup"><span data-stu-id="77e97-103">GXFPF\_\* Constants</span></span>

<span data-ttu-id="77e97-104">\_ \* Константы гксфпф указывают позицию символа, возвращаемую в зависимости от координат экрана точки относительно ограничивающего прямоугольника символа.</span><span class="sxs-lookup"><span data-stu-id="77e97-104">GXFPF\_\* constants specify the character position to return based on the screen coordinates of the point relative to a character bounding box.</span></span>



| <span data-ttu-id="77e97-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="77e97-105">Constant/value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="77e97-106">Описание</span><span class="sxs-lookup"><span data-stu-id="77e97-106">Description</span></span>                                                                                                                                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GXFPF_ROUND_NEAREST"></span><span id="gxfpf_round_nearest"></span><dl> <span data-ttu-id="77e97-107"><dt>**Гксфпф \_ СКРУГЛЕНие \_ ближайшего**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="77e97-107"><dt>**GXFPF\_ROUND\_NEAREST**</dt> <dt>( 0x1 )</dt></span></span> </dl> | <span data-ttu-id="77e97-108">Если экранные координаты точки содержатся в прямоугольнике с ограничивающим символом, то возвращаемая точка символа является ограничивающим ребром, ближайшим к экранным координатам точки.</span><span class="sxs-lookup"><span data-stu-id="77e97-108">If the screen coordinates of the point are contained in a character bounding box, the character position returned is the bounding edge closest to the screen coordinates of the point.</span></span><br/> |
| <span id="GXFPF_NEAREST"></span><span id="gxfpf_nearest"></span><dl> <span data-ttu-id="77e97-109"><dt>**Гксфпф \_ БЛИЖАЙШЕе**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="77e97-109"><dt>**GXFPF\_NEAREST**</dt> <dt>( 0x2 )</dt></span></span> </dl>                    | <span data-ttu-id="77e97-110">Если экранные координаты точки не содержатся в прямоугольнике с ограничивающим символом, возвращается ближайшая символьная точка.</span><span class="sxs-lookup"><span data-stu-id="77e97-110">If the screen coordinates of the point are not contained in a character bounding box, the closest character position is returned.</span></span><br/>                                                      |



## <a name="remarks"></a><span data-ttu-id="77e97-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77e97-111">Remarks</span></span>

<span data-ttu-id="77e97-112">Параметры *dwFlags* методов [ITextStoreACP:: жетакпфромпоинт](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) и [итфконтекстовнер:: жетакпфромпоинт](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) используют эти константы.</span><span class="sxs-lookup"><span data-stu-id="77e97-112">The *dwflags* parameters of the [ITextStoreACP::GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) and [ITfContextOwner::GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) methods use these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="77e97-113">Требования</span><span class="sxs-lookup"><span data-stu-id="77e97-113">Requirements</span></span>



| <span data-ttu-id="77e97-114">Требование</span><span class="sxs-lookup"><span data-stu-id="77e97-114">Requirement</span></span> | <span data-ttu-id="77e97-115">Значение</span><span class="sxs-lookup"><span data-stu-id="77e97-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77e97-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77e97-116">Minimum supported client</span></span><br/> | <span data-ttu-id="77e97-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="77e97-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="77e97-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77e97-118">Minimum supported server</span></span><br/> | <span data-ttu-id="77e97-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="77e97-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77e97-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="77e97-120">Redistributable</span></span><br/>          | <span data-ttu-id="77e97-121">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="77e97-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="77e97-122">Header</span><span class="sxs-lookup"><span data-stu-id="77e97-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="77e97-123"><dt>Текстстор. h</dt></span><span class="sxs-lookup"><span data-stu-id="77e97-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="77e97-124">IDL</span><span class="sxs-lookup"><span data-stu-id="77e97-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="77e97-125"><dt>Текстстор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="77e97-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77e97-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77e97-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77e97-127">ITextStoreACP:: Жетакпфромпоинт</span><span class="sxs-lookup"><span data-stu-id="77e97-127">ITextStoreACP::GetACPFromPoint</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint)
</dt> <dt>

[<span data-ttu-id="77e97-128">Итфконтекстовнер:: Жетакпфромпоинт</span><span class="sxs-lookup"><span data-stu-id="77e97-128">ITfContextOwner::GetACPFromPoint</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint)
</dt> </dl>

 

 





