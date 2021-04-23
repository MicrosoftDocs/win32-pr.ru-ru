---
description: Метод Сенднмевент отправляет события в инструментарий управления Windows (WMI) (WMI).
ms.assetid: 85c33a71-72aa-4b0a-8e8b-3a220a080bb2
title: 'Метод Имониторевентер:: Сенднмевент (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.SendNMEvent
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 3286fca4d5b852d4562c13446699c1a6b40f3efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673424"
---
# <a name="imonitoreventersendnmevent-method"></a><span data-ttu-id="00184-103">Метод Имониторевентер:: Сенднмевент</span><span class="sxs-lookup"><span data-stu-id="00184-103">IMonitorEventer::SendNMEvent method</span></span>

<span data-ttu-id="00184-104">Метод **сенднмевент** отправляет события в инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="00184-104">The **SendNMEvent** method submits events to Windows Management Instrumentation (WMI).</span></span>

## <a name="syntax"></a><span data-ttu-id="00184-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00184-105">Syntax</span></span>


```C++
HRESULT SendNMEvent(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="00184-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="00184-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00184-107">*пнмевентдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="00184-107">*pNMEventData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00184-108">Указатель на событие, переданное в WMI.</span><span class="sxs-lookup"><span data-stu-id="00184-108">Pointer to the event submitted to WMI.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00184-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00184-109">Return value</span></span>

<span data-ttu-id="00184-110">Если метод выполнен успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="00184-110">If the method is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="00184-111">Если метод завершился неудачно, возвращаемое значение НМЕРР не \_ хватает \_ \_ памяти.</span><span class="sxs-lookup"><span data-stu-id="00184-111">If the method is unsuccessful, the return value is NMERR\_OUT\_OF\_MEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="00184-112">Требования</span><span class="sxs-lookup"><span data-stu-id="00184-112">Requirements</span></span>



| <span data-ttu-id="00184-113">Требование</span><span class="sxs-lookup"><span data-stu-id="00184-113">Requirement</span></span> | <span data-ttu-id="00184-114">Значение</span><span class="sxs-lookup"><span data-stu-id="00184-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="00184-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00184-115">Minimum supported client</span></span><br/> | <span data-ttu-id="00184-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="00184-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="00184-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00184-117">Minimum supported server</span></span><br/> | <span data-ttu-id="00184-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="00184-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="00184-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="00184-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="00184-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="00184-120"><dt>Netmon.h</dt></span></span> </dl> |



 

 




