---
description: Эти функции обеспечивают поддержку реализации интерфейса IUnknown в DirectShow.
ms.assetid: 991e4c69-7d30-4ecf-9ccf-4920452c21d6
title: Вспомогательные функции COM (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COM
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9522469ee1aa4f4efa63b4cff6ad73204973a622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680003"
---
# <a name="com-helper-functions"></a><span data-ttu-id="68087-103">Вспомогательные функции COM</span><span class="sxs-lookup"><span data-stu-id="68087-103">COM Helper Functions</span></span>

<span data-ttu-id="68087-104">Эти функции обеспечивают поддержку реализации интерфейса **IUnknown** в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="68087-104">These functions provide support for implementing the **IUnknown** interface in DirectShow.</span></span>



| <span data-ttu-id="68087-105">Функция</span><span class="sxs-lookup"><span data-stu-id="68087-105">Function</span></span>                                               | <span data-ttu-id="68087-106">Описание</span><span class="sxs-lookup"><span data-stu-id="68087-106">Description</span></span>                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="68087-107">**ОБЪЯВЛЕНИЕ \_ IUnknown**</span><span class="sxs-lookup"><span data-stu-id="68087-107">**DECLARE\_IUNKNOWN**</span></span>](declare-iunknown.md)          | <span data-ttu-id="68087-108">Объявляет три метода базового интерфейса для нового интерфейса.</span><span class="sxs-lookup"><span data-stu-id="68087-108">Declares the three methods of the base interface for a new interface.</span></span> |
| [<span data-ttu-id="68087-109">**GetInterface**</span><span class="sxs-lookup"><span data-stu-id="68087-109">**GetInterface**</span></span>](getinterface.md)                   | <span data-ttu-id="68087-110">Извлекает указатель интерфейса на запрошенный клиент.</span><span class="sxs-lookup"><span data-stu-id="68087-110">Retrieves an interface pointer to the requested client.</span></span>               |
| [<span data-ttu-id="68087-111">**инонделегатингункновн**</span><span class="sxs-lookup"><span data-stu-id="68087-111">**INonDelegatingUnknown**</span></span>](inondelegatingunknown.md) | <span data-ttu-id="68087-112">Неделегированная версия интерфейса **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="68087-112">Nondelegating version of the **IUnknown** interface.</span></span>                  |
| [<span data-ttu-id="68087-113">**LoadOLEAut32**</span><span class="sxs-lookup"><span data-stu-id="68087-113">**LoadOLEAut32**</span></span>](loadoleaut32.md)                   | <span data-ttu-id="68087-114">Загружает библиотеку DLL службы автоматизации (OleAut32.dll).</span><span class="sxs-lookup"><span data-stu-id="68087-114">Loads the Automation DLL (OleAut32.dll).</span></span>                              |



 

## <a name="requirements"></a><span data-ttu-id="68087-115">Требования</span><span class="sxs-lookup"><span data-stu-id="68087-115">Requirements</span></span>



| <span data-ttu-id="68087-116">Требование</span><span class="sxs-lookup"><span data-stu-id="68087-116">Requirement</span></span> | <span data-ttu-id="68087-117">Значение</span><span class="sxs-lookup"><span data-stu-id="68087-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68087-118">Header</span><span class="sxs-lookup"><span data-stu-id="68087-118">Header</span></span><br/>  | <dl> <span data-ttu-id="68087-119"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="68087-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="68087-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="68087-120">Library</span></span><br/> | <dl> <span data-ttu-id="68087-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="68087-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68087-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68087-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68087-123">Служебные функции</span><span class="sxs-lookup"><span data-stu-id="68087-123">Utility Functions</span></span>](utility-functions.md)
</dt> </dl>

 

 




