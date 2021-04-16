---
description: '\_Константы линелокатионоптион определяют значения, используемые в элементе двоптионс структуры линелокатионентри, возвращаемой как часть структуры линетранслатекапс, возвращаемой линежеттранслатекапс.'
ms.assetid: 3b185c16-2535-4a90-855b-29e52828ea4c
title: Константы LINELOCATIONOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f60398953d2f809e29a78323e3b1dedfcac7a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679587"
---
# <a name="linelocationoption_-constants"></a><span data-ttu-id="7fbe9-103">\_Константы линелокатионоптион</span><span class="sxs-lookup"><span data-stu-id="7fbe9-103">LINELOCATIONOPTION\_ Constants</span></span>

<span data-ttu-id="7fbe9-104">Константы **\_ линелокатионоптион** определяют значения, используемые в элементе **двоптионс** структуры [**линелокатионентри**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) , возвращаемой как часть структуры [**линетранслатекапс**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) , возвращаемой [**линежеттранслатекапс**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span><span class="sxs-lookup"><span data-stu-id="7fbe9-104">The **LINELOCATIONOPTION\_** constants define values used in the **dwOptions** member of the [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) structure returned as part of the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure returned by [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span></span>

<dl> <dt>

<span data-ttu-id="7fbe9-105"><span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**ЛИНЕЛОКАТИОНОПТИОН \_ пулседиал**</span><span class="sxs-lookup"><span data-stu-id="7fbe9-105"><span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION\_PULSEDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7fbe9-106">По умолчанию в этом расположении используется импульсный набор номеров.</span><span class="sxs-lookup"><span data-stu-id="7fbe9-106">The default dialing mode at this location is pulse dialing.</span></span> <span data-ttu-id="7fbe9-107">Если этот бит задан, [**линетранслатеаддресс**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) вставит в начало строки с набором номера "P" модификатор набора, возвращаемый при выборе этого расположения.</span><span class="sxs-lookup"><span data-stu-id="7fbe9-107">If this bit is set, [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) will insert a "P" dial modifier at the beginning of the dialable string returned when this location is selected.</span></span> <span data-ttu-id="7fbe9-108">Если этот бит не задан, **линетранслатеаддресс** вставит в начало строки "T" модификатор вызова.</span><span class="sxs-lookup"><span data-stu-id="7fbe9-108">If this bit is not set, **lineTranslateAddress** will insert a "T" dial modifier at the beginning of the dialable string.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7fbe9-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7fbe9-109">Remarks</span></span>

<span data-ttu-id="7fbe9-110">Не расширяемый.</span><span class="sxs-lookup"><span data-stu-id="7fbe9-110">Not extensible.</span></span> <span data-ttu-id="7fbe9-111">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="7fbe9-111">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fbe9-112">Требования</span><span class="sxs-lookup"><span data-stu-id="7fbe9-112">Requirements</span></span>



| <span data-ttu-id="7fbe9-113">Требование</span><span class="sxs-lookup"><span data-stu-id="7fbe9-113">Requirement</span></span> | <span data-ttu-id="7fbe9-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7fbe9-114">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7fbe9-115">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="7fbe9-115">TAPI version</span></span><br/> | <span data-ttu-id="7fbe9-116">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7fbe9-116">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7fbe9-117">Header</span><span class="sxs-lookup"><span data-stu-id="7fbe9-117">Header</span></span><br/>       | <dl> <span data-ttu-id="7fbe9-118"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fbe9-118"><dt>Tapi.h</dt></span></span> </dl> |



 

 




