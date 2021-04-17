---
title: Сообщение MCIWNDM_GETSTYLES (VFW. h)
description: Сообщение МЦИВНДМ- \_ styles Получает флаги, указывающие текущие стили окна мЦивнд, используемые окном. Это сообщение можно отправить явно или с помощью макроса МЦивнджетстилес.
ms.assetid: cd34ba05-47cb-488e-a6c6-4ec1c0d25de8
keywords:
- MCIWNDM_GETSTYLES сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 983e37291977edf2473c2b603cd5b40792fb7989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672855"
---
# <a name="mciwndm_getstyles-message"></a><span data-ttu-id="03b78-105">Сообщение МЦИВНДМных \_ стилей</span><span class="sxs-lookup"><span data-stu-id="03b78-105">MCIWNDM\_GETSTYLES message</span></span>

<span data-ttu-id="03b78-106">Сообщение **мЦивндм- \_ styles** Получает флаги, указывающие текущие стили окна мЦивнд, используемые окном.</span><span class="sxs-lookup"><span data-stu-id="03b78-106">The **MCIWNDM\_GETSTYLES** message retrieves the flags specifying the current MCIWnd window styles used by a window.</span></span> <span data-ttu-id="03b78-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетстилес**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .</span><span class="sxs-lookup"><span data-stu-id="03b78-107">You can send this message explicitly or by using the [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) macro.</span></span>


```C++
MCIWNDM_GETSTYLES 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="03b78-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03b78-108">Return Value</span></span>

<span data-ttu-id="03b78-109">Возвращает значение, представляющее текущие стили окна МЦивнд.</span><span class="sxs-lookup"><span data-stu-id="03b78-109">Returns a value representing the current styles of the MCIWnd window.</span></span> <span data-ttu-id="03b78-110">Возвращаемое значение является побитовым оператором или в стилях окна МЦивнд (флаги МЦИВНДФ).</span><span class="sxs-lookup"><span data-stu-id="03b78-110">The return value is the bitwise OR operator of the MCIWnd window styles (MCIWNDF flags).</span></span>

## <a name="requirements"></a><span data-ttu-id="03b78-111">Требования</span><span class="sxs-lookup"><span data-stu-id="03b78-111">Requirements</span></span>



| <span data-ttu-id="03b78-112">Требование</span><span class="sxs-lookup"><span data-stu-id="03b78-112">Requirement</span></span> | <span data-ttu-id="03b78-113">Значение</span><span class="sxs-lookup"><span data-stu-id="03b78-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="03b78-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="03b78-114">Minimum supported client</span></span><br/> | <span data-ttu-id="03b78-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="03b78-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="03b78-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="03b78-116">Minimum supported server</span></span><br/> | <span data-ttu-id="03b78-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="03b78-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="03b78-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="03b78-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="03b78-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="03b78-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03b78-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03b78-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03b78-121">**мЦивнджетстилес**</span><span class="sxs-lookup"><span data-stu-id="03b78-121">**MCIWndGetStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
</dt> </dl>

 

 





