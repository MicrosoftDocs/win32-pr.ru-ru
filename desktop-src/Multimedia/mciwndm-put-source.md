---
title: Сообщение MCIWNDM_PUT_SOURCE (VFW. h)
description: '\_ \_ Сообщение источника мЦивндм размещение переопределяет координаты исходного прямоугольника, используемого для обрезки изображений AVI в ходе воспроизведения. Это сообщение можно отправить явно или с помощью макроса МЦивндпутсаурце.'
ms.assetid: cff95139-0302-4db3-bf2e-559e75257e85
keywords:
- MCIWNDM_PUT_SOURCE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5407f420b8def6dda9795e87eb68943c9373b143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801012"
---
# <a name="mciwndm_put_source-message"></a><span data-ttu-id="a3f1c-105">МЦИВНДМ \_ Размещение \_ исходного сообщения</span><span class="sxs-lookup"><span data-stu-id="a3f1c-105">MCIWNDM\_PUT\_SOURCE message</span></span>

<span data-ttu-id="a3f1c-106">Сообщение **\_ \_ источника мЦивндм размещение** переопределяет координаты исходного прямоугольника, используемого для обрезки изображений AVI в ходе воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-106">The **MCIWNDM\_PUT\_SOURCE** message redefines the coordinates of the source rectangle used for cropping the images of an AVI file during playback.</span></span> <span data-ttu-id="a3f1c-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндпутсаурце**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) .</span><span class="sxs-lookup"><span data-stu-id="a3f1c-107">You can send this message explicitly or by using the [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) macro.</span></span>


```C++
MCIWNDM_PUT_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="a3f1c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3f1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3f1c-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="a3f1c-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="a3f1c-110">Указатель на структуру [Rect](/previous-versions//ms536136(v=vs.85)) , содержащую координаты исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-110">Pointer to a [RECT](/previous-versions//ms536136(v=vs.85)) structure containing the coordinates of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3f1c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3f1c-111">Return Value</span></span>

<span data-ttu-id="a3f1c-112">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3f1c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a3f1c-113">Requirements</span></span>



| <span data-ttu-id="a3f1c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a3f1c-114">Requirement</span></span> | <span data-ttu-id="a3f1c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a3f1c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a3f1c-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3f1c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a3f1c-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a3f1c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a3f1c-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3f1c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a3f1c-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a3f1c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a3f1c-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a3f1c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3f1c-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3f1c-121"><dt>Vfw.h</dt></span></span> </dl> |



 

