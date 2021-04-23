---
title: Сообщение MCIWNDM_GET_SOURCE (VFW. h)
description: '\_ \_ Сообщение источника мЦивндм Get получает координаты исходного прямоугольника, используемого для обрезки изображений файла AVI во время воспроизведения. Это сообщение можно отправить явно или с помощью макроса МЦивнджетсаурце.'
ms.assetid: d5f25926-5a3d-412e-8248-fbf307583757
keywords:
- MCIWNDM_GET_SOURCE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GET_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85147182d06386efed73229fcdd6c75372244fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415900"
---
# <a name="mciwndm_get_source-message"></a><span data-ttu-id="f2280-105">МЦИВНДМ \_ Получение \_ исходного сообщения</span><span class="sxs-lookup"><span data-stu-id="f2280-105">MCIWNDM\_GET\_SOURCE message</span></span>

<span data-ttu-id="f2280-106">Сообщение **\_ \_ источника мЦивндм Get** получает координаты исходного прямоугольника, используемого для обрезки изображений файла AVI во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="f2280-106">The **MCIWNDM\_GET\_SOURCE** message retrieves the coordinates of the source rectangle used for cropping the images of an AVI file during playback.</span></span> <span data-ttu-id="f2280-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетсаурце**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) .</span><span class="sxs-lookup"><span data-stu-id="f2280-107">You can send this message explicitly or by using the [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) macro.</span></span>


```C++
MCIWNDM_GET_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="f2280-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2280-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2280-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="f2280-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="f2280-110">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , в которой должны содержаться координаты исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="f2280-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to contain the coordinates of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2280-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2280-111">Return Value</span></span>

<span data-ttu-id="f2280-112">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f2280-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2280-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f2280-113">Requirements</span></span>



| <span data-ttu-id="f2280-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f2280-114">Requirement</span></span> | <span data-ttu-id="f2280-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f2280-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f2280-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2280-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f2280-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f2280-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f2280-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2280-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f2280-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f2280-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f2280-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f2280-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2280-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2280-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2280-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2280-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2280-123">**мЦивнджетсаурце**</span><span class="sxs-lookup"><span data-stu-id="f2280-123">**MCIWndGetSource**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)
</dt> </dl>

 

