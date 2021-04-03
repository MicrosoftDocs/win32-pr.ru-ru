---
description: Метод onframes должен быть реализован монитором. МКСВК вызывает этот метод, когда буфер записи полон или время обновления прошло.
ms.assetid: 243bd35b-2527-463e-b3d2-4bd840fe9c3f
title: 'Метод Имонитор:: onframes (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnFrames
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c5b6ff3e9d5b97a228e6e1d865fe4d8f1b5bfc9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809466"
---
# <a name="imonitoronframes-method"></a><span data-ttu-id="3920e-104">Метод Имонитор:: onframe</span><span class="sxs-lookup"><span data-stu-id="3920e-104">IMonitor::OnFrames method</span></span>

<span data-ttu-id="3920e-105">Метод **Onframes** должен быть реализован монитором.</span><span class="sxs-lookup"><span data-stu-id="3920e-105">The **OnFrames** method must be implemented by the monitor.</span></span> <span data-ttu-id="3920e-106">МКСВК вызывает этот метод, когда буфер записи полон или время обновления прошло.</span><span class="sxs-lookup"><span data-stu-id="3920e-106">The MCSVC calls this method when either the capture buffer is full or the update time has passed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3920e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3920e-107">Syntax</span></span>


```C++
HRESULT OnFrames(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a><span data-ttu-id="3920e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3920e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3920e-109">*Событие* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3920e-109">*Event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3920e-110">[Обновление \_ Структура событий](update-event.md) , содержащая сведения о кадрах, используемые для обновления событий.</span><span class="sxs-lookup"><span data-stu-id="3920e-110">[UPDATE\_EVENT](update-event.md) structure that holds frame information used to update events.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3920e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3920e-111">Return value</span></span>

<span data-ttu-id="3920e-112">Если метод выполнен успешно, возвращается значение S \_ OK (то же самое, что и ошибка).</span><span class="sxs-lookup"><span data-stu-id="3920e-112">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span> <span data-ttu-id="3920e-113">МКСВК передает возвращаемое значение обратно в НПП для обработки.</span><span class="sxs-lookup"><span data-stu-id="3920e-113">The MCSVC passes the returned value back to the NPP for processing.</span></span>

<span data-ttu-id="3920e-114">Если метод завершается неудачно, возвращаемое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="3920e-114">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="3920e-115">МКСВК передает возвращаемое значение обратно в НПП для обработки.</span><span class="sxs-lookup"><span data-stu-id="3920e-115">The MCSVC passes the returned value back to the NPP for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="3920e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3920e-116">Requirements</span></span>



| <span data-ttu-id="3920e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3920e-117">Requirement</span></span> | <span data-ttu-id="3920e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3920e-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3920e-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3920e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3920e-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3920e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3920e-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3920e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3920e-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3920e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3920e-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3920e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3920e-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3920e-124"><dt>Netmon.h</dt></span></span> </dl> |



 

 




