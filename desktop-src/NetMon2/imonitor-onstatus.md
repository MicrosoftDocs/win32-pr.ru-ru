---
description: Метод МКСВК вызывает метод OnStatus для уведомления монитора о существовании события состояния НПП. Этот метод должен быть реализован монитором.
ms.assetid: 771852b1-77d8-4d7d-b3fb-03eb3ea593b8
title: 'Метод Имонитор:: OnStatus (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStatus
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: fc2716a10673cc1178591b14a335b1d8559aa35a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155107"
---
# <a name="imonitoronstatus-method"></a><span data-ttu-id="16509-104">Метод Имонитор:: OnStatus</span><span class="sxs-lookup"><span data-stu-id="16509-104">IMonitor::OnStatus method</span></span>

<span data-ttu-id="16509-105">Метод МКСВК вызывает метод **OnStatus** для уведомления монитора о существовании события состояния НПП.</span><span class="sxs-lookup"><span data-stu-id="16509-105">The MCSVC method calls the **OnStatus** method to notify the monitor that an NPP status event exists.</span></span> <span data-ttu-id="16509-106">Этот метод должен быть реализован монитором.</span><span class="sxs-lookup"><span data-stu-id="16509-106">This method must be implemented by the monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="16509-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16509-107">Syntax</span></span>


```C++
HRESULT OnStatus(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a><span data-ttu-id="16509-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="16509-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16509-109">*Событие* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="16509-109">*Event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16509-110">Структура [ \_ событий Update](update-event.md) .</span><span class="sxs-lookup"><span data-stu-id="16509-110">An [UPDATE\_EVENT](update-event.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16509-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16509-111">Return value</span></span>

<span data-ttu-id="16509-112">Если метод выполнен успешно, возвращается значение S \_ (то же, что и параметр noreturn), а мксвк передает возвращаемое значение обратно в НПП для обработки.</span><span class="sxs-lookup"><span data-stu-id="16509-112">If the method is successful, the return value is S\_OK (which is the same as NOERROR), and the MCSVC passes the returned value back to the NPP for processing.</span></span>

<span data-ttu-id="16509-113">Если метод завершается неудачно, возвращается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="16509-113">If the method is unsuccessful, return an error code.</span></span> <span data-ttu-id="16509-114">При возникновении ошибки МКСВК передает возвращенное значение обратно в НПП для обработки.</span><span class="sxs-lookup"><span data-stu-id="16509-114">On error, the MCSVC passes the returned value back to the NPP for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="16509-115">Требования</span><span class="sxs-lookup"><span data-stu-id="16509-115">Requirements</span></span>



| <span data-ttu-id="16509-116">Требование</span><span class="sxs-lookup"><span data-stu-id="16509-116">Requirement</span></span> | <span data-ttu-id="16509-117">Значение</span><span class="sxs-lookup"><span data-stu-id="16509-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="16509-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="16509-118">Minimum supported client</span></span><br/> | <span data-ttu-id="16509-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="16509-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="16509-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="16509-120">Minimum supported server</span></span><br/> | <span data-ttu-id="16509-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="16509-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="16509-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="16509-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="16509-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="16509-123"><dt>Netmon.h</dt></span></span> </dl> |



 

 




