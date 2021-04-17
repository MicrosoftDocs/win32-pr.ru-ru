---
description: Перечисление, используемое для отправки ответов от подсистемы захвата к диагностика графики.
MS-HAID: vspixengine.PixPipeResponse
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Перечисление Пикспипереспонсе
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5BFEE25D-3E03-493E-AFEF-DD8C70C53FC5
api_name:
- PixPipeResponse
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09ab253be5e02cc7329195016a406758b7a82e2b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701115"
---
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span data-ttu-id="cb5e9-103"><span id="vspixengine.pixpiperesponse"></span>Перечисление Пикспипереспонсе</span><span class="sxs-lookup"><span data-stu-id="cb5e9-103"><span id="vspixengine.pixpiperesponse"></span>PixPipeResponse enumeration</span></span>

<span data-ttu-id="cb5e9-104">Перечисление, используемое для отправки ответов от подсистемы захвата к диагностика графики.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-104">An enum used to send responses from the capture engine to Graphics Diagnostics.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb5e9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb5e9-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="cb5e9-106">Константы</span><span class="sxs-lookup"><span data-stu-id="cb5e9-106">Constants</span></span>

<span data-ttu-id="cb5e9-107"><span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**\_доступны новые данные \_**</span><span class="sxs-lookup"><span data-stu-id="cb5e9-107"><span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NEW\_DATA\_AVAILABLE**</span></span>  
<span data-ttu-id="cb5e9-108">Ответ, указывающий, что новые данные были записаны в журнал графики и готовы к чтению.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-108">A response which indicates that new data has been written to the graphics log and is ready to be read.</span></span>

<span data-ttu-id="cb5e9-109"><span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**данные ЭКСПЕРИМЕНТа \_**</span><span class="sxs-lookup"><span data-stu-id="cb5e9-109"><span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**EXPERIMENT\_DATA**</span></span>  
<span data-ttu-id="cb5e9-110">Ответ, который указывает сведения о конфигурации сеанса записи.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-110">A response which indicates configuration information about the capture session.</span></span>

<span data-ttu-id="cb5e9-111"><span id="ERRORCODE"></span><span id="errorcode"></span>**КОД ошибки**</span><span class="sxs-lookup"><span data-stu-id="cb5e9-111"><span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**</span></span>  
<span data-ttu-id="cb5e9-112">Ответ, указывающий, что в подсистеме записи обнаружена ошибка.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-112">A response which indicates that the capture engine has encountered an error.</span></span>

<span data-ttu-id="cb5e9-113"><span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**аппликатионкаптуреинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="cb5e9-113"><span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**</span></span>  
<span data-ttu-id="cb5e9-114">Ответ, указывающий, что подсистема отслеживания начала запись графических данных.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-114">A response which indicates that the capture engine has started capturing graphics information.</span></span> <span data-ttu-id="cb5e9-115">Это не означает, что данные будут доступны для анализа.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-115">This does not indicate that data is available to be examined yet.</span></span>

<span data-ttu-id="cb5e9-116"><span id="PARTIAL_DATA"></span><span id="partial_data"></span>**ЧАСТИЧные \_ данные**</span><span class="sxs-lookup"><span data-stu-id="cb5e9-116"><span id="PARTIAL_DATA"></span><span id="partial_data"></span>**PARTIAL\_DATA**</span></span>  
<span data-ttu-id="cb5e9-117">Ответ, указывающий, что в журнал графики записаны частичные данные.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-117">A response which indicates that partial data has been written to the graphics log.</span></span>

<span data-ttu-id="cb5e9-118"><span id="READY"></span><span id="ready"></span>**ВСЁ**</span><span class="sxs-lookup"><span data-stu-id="cb5e9-118"><span id="READY"></span><span id="ready"></span>**READY**</span></span>  
<span data-ttu-id="cb5e9-119">Ответ, указывающий, что подсистема отслеживания готова начать запись графических данных.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-119">A response which indicates that the capture engine is ready to start capturing graphics information.</span></span>

<span data-ttu-id="cb5e9-120"><span id="DONE"></span><span id="done"></span>**Договорились**</span><span class="sxs-lookup"><span data-stu-id="cb5e9-120"><span id="DONE"></span><span id="done"></span>**DONE**</span></span>  
<span data-ttu-id="cb5e9-121">Внутренние</span><span class="sxs-lookup"><span data-stu-id="cb5e9-121">Internal</span></span>

<span data-ttu-id="cb5e9-122"><span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**каптурестартед**</span><span class="sxs-lookup"><span data-stu-id="cb5e9-122"><span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**</span></span>  
<span data-ttu-id="cb5e9-123">Ответ, указывающий на начало записи кадров.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-123">A response which indicates that a frame capture has started.</span></span>

<span data-ttu-id="cb5e9-124"><span id="STATUS"></span><span id="status"></span>**СОСТОЯНИЕ**</span><span class="sxs-lookup"><span data-stu-id="cb5e9-124"><span id="STATUS"></span><span id="status"></span>**STATUS**</span></span>  
<span data-ttu-id="cb5e9-125">Ответ, который указывает сведения о состоянии собираемого приложения; Например, частота кадров.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-125">A response which indicates status information about the app being captured; for example, framerate.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb5e9-126">Требования</span><span class="sxs-lookup"><span data-stu-id="cb5e9-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="cb5e9-127">Header</span><span class="sxs-lookup"><span data-stu-id="cb5e9-127">Header</span></span></p></td><td><span data-ttu-id="cb5e9-128">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="cb5e9-128">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



