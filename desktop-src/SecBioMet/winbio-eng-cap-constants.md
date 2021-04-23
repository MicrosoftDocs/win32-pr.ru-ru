---
title: Константы WINBIO_ENG_CAP (Винбио \_ types. h)
description: Укажите универсальные возможности подсистемы.
ms.assetid: 31C4E8AF-6EF8-43FF-A944-D7363A26BB1A
topic_type:
- apiref
api_name:
- WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT
- WINBIO_ENG_CAP_SPOOF_DETECTION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d69db9f0e15ca0d50aa5ca134fdc74904dec85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803905"
---
# <a name="winbio_eng_cap-constants"></a><span data-ttu-id="ec595-103">\_ \_ Константы винбио ENG</span><span class="sxs-lookup"><span data-stu-id="ec595-103">WINBIO\_ENG\_CAP Constants</span></span>

<span data-ttu-id="ec595-104">Следующие константы — это значения **\_ возможностей винбио** , которые можно использовать для указания универсальных возможностей компонента ядра, подключенного к определенной биометрической единице.</span><span class="sxs-lookup"><span data-stu-id="ec595-104">The following constants are **WINBIO\_CAPABILITIES** values that can be used to specify generic capabilities of the engine component that is connected to a specific biometric unit.</span></span> <span data-ttu-id="ec595-105">Эти возможности задаются в **женериценгинекапабилитиес** члене [**структуры \_ \_ \_ сведений о расширенном подсистеме винбио**](winbio-extended-engine-info.md) .</span><span class="sxs-lookup"><span data-stu-id="ec595-105">You specify these capabilities in **GenericEngineCapabilities** member of the [**WINBIO\_EXTENDED\_ENGINE\_INFO**](winbio-extended-engine-info.md) structure.</span></span>



| <span data-ttu-id="ec595-106">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="ec595-106">Constant/value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="ec595-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ec595-107">Description</span></span>                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span id="WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT"></span><span id="winbio_eng_cap_iterative_improvement"></span><dl> <span data-ttu-id="ec595-108"><dt>**Винбио \_ \_ \_ Итеративное \_ улучшение ENG Cap**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="ec595-108"><dt>**WINBIO\_ENG\_CAP\_ITERATIVE\_IMPROVEMENT**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="ec595-109">Компонент биометрического ядра СУБД может выполнять итеративное улучшение.</span><span class="sxs-lookup"><span data-stu-id="ec595-109">The biometric engine component can perform iterative improvement.</span></span><br/> |
| <span id="WINBIO_ENG_CAP_SPOOF_DETECTION"></span><span id="winbio_eng_cap_spoof_detection"></span><dl> <span data-ttu-id="ec595-110"><dt>**Винбио \_ \_ \_ \_ Обнаружение подделки ENG с ограничением авторизации**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="ec595-110"><dt>**WINBIO\_ENG\_CAP\_SPOOF\_DETECTION**</dt> <dt>0x00000002</dt></span></span> </dl>                   | <span data-ttu-id="ec595-111">Компонент биометрического ядра может выполнять обнаружение подделки.</span><span class="sxs-lookup"><span data-stu-id="ec595-111">The biometric engine component can perform spoof detection.</span></span><br/>       |



## <a name="requirements"></a><span data-ttu-id="ec595-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ec595-112">Requirements</span></span>



| <span data-ttu-id="ec595-113">Требование</span><span class="sxs-lookup"><span data-stu-id="ec595-113">Requirement</span></span> | <span data-ttu-id="ec595-114">Значение</span><span class="sxs-lookup"><span data-stu-id="ec595-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec595-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec595-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ec595-116">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ec595-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="ec595-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec595-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ec595-118">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="ec595-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ec595-119">Header</span><span class="sxs-lookup"><span data-stu-id="ec595-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec595-120"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec595-120"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





