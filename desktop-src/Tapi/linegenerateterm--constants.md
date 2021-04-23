---
description: '\_Константы побитового флага линеженератетерм описывают условия, при которых заканчивается создание цифр или тона.'
ms.assetid: 5cdc43c0-2349-4ffc-9bf7-3b498b35db95
title: Константы LINEGENERATETERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6804b09879471a77780a95ca4ed35b7aaa5b6e1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689469"
---
# <a name="linegenerateterm_-constants"></a><span data-ttu-id="6c3f5-103">\_Константы линеженератетерм</span><span class="sxs-lookup"><span data-stu-id="6c3f5-103">LINEGENERATETERM\_ Constants</span></span>

<span data-ttu-id="6c3f5-104">Константы побитового флага **линеженератетерм \_** описывают условия, при которых заканчивается создание цифр или тона.</span><span class="sxs-lookup"><span data-stu-id="6c3f5-104">The **LINEGENERATETERM\_** bit-flag constants describe the conditions under which digit or tone generation is terminated.</span></span>

<dl> <dt>

<span data-ttu-id="6c3f5-105"><span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**ЛИНЕЖЕНЕРАТЕТЕРМ \_ Отмена**</span><span class="sxs-lookup"><span data-stu-id="6c3f5-105"><span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**LINEGENERATETERM\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6c3f5-106">Запрос на формирование цифр или тонов был отменен этим приложением, другим приложением или из-за прекращения вызова.</span><span class="sxs-lookup"><span data-stu-id="6c3f5-106">The digit or tone generation request was canceled by this application, by another application, or because the call terminated.</span></span> <span data-ttu-id="6c3f5-107">Это значение также может быть возвращено, если не удается завершить создание цифр или тона из-за внутренней ошибки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="6c3f5-107">This value can also be returned when digit or tone generation cannot be completed due to internal failure of the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c3f5-108"><span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**ЛИНЕЖЕНЕРАТЕТЕРМ \_ Готово**</span><span class="sxs-lookup"><span data-stu-id="6c3f5-108"><span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM\_DONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6c3f5-109">Запрошенное количество цифр или запрошенных тонов было создано в течение запрошенного времени.</span><span class="sxs-lookup"><span data-stu-id="6c3f5-109">The requested number of digits or requested tones have been generated for the requested duration.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c3f5-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c3f5-110">Remarks</span></span>

<span data-ttu-id="6c3f5-111">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="6c3f5-111">No extensibility.</span></span> <span data-ttu-id="6c3f5-112">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="6c3f5-112">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c3f5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6c3f5-113">Requirements</span></span>



| <span data-ttu-id="6c3f5-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6c3f5-114">Requirement</span></span> | <span data-ttu-id="6c3f5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6c3f5-115">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6c3f5-116">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="6c3f5-116">TAPI version</span></span><br/> | <span data-ttu-id="6c3f5-117">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6c3f5-117">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6c3f5-118">Header</span><span class="sxs-lookup"><span data-stu-id="6c3f5-118">Header</span></span><br/>       | <dl> <span data-ttu-id="6c3f5-119"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c3f5-119"><dt>Tapi.h</dt></span></span> </dl> |



 

 




