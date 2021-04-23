---
description: '\_Константы побитового флага фонехуксвитчдев описывают различные устройства ввода-вывода с собственной хуксвитч, управляемой с компьютера.'
ms.assetid: b3272a75-87b0-4afc-b2e2-2d65e4b49300
title: Константы PHONEHOOKSWITCHDEV_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a6727bf8103c35402bebc048de4ed9286650be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680105"
---
# <a name="phonehookswitchdev_-constants"></a><span data-ttu-id="b890b-103">\_Константы фонехуксвитчдев</span><span class="sxs-lookup"><span data-stu-id="b890b-103">PHONEHOOKSWITCHDEV\_ Constants</span></span>

<span data-ttu-id="b890b-104">Константы побитового флага **фонехуксвитчдев \_** описывают различные устройства ввода-вывода с собственной хуксвитч, управляемой с компьютера.</span><span class="sxs-lookup"><span data-stu-id="b890b-104">The **PHONEHOOKSWITCHDEV\_** bit-flag constants describe various audio I/O devices each with its own hookswitch controllable from the computer.</span></span>

<dl> <dt>

<span data-ttu-id="b890b-105"><span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**ФОНЕХУКСВИТЧДЕВная \_ трубка**</span><span class="sxs-lookup"><span data-stu-id="b890b-105"><span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**PHONEHOOKSWITCHDEV\_HANDSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b890b-106">Это Стандартный и мауспиеценый телефон.</span><span class="sxs-lookup"><span data-stu-id="b890b-106">This is a standard ear- and mouthpiece phone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b890b-107"><span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**ФОНЕХУКСВИТЧДЕВ \_ гарнитура**</span><span class="sxs-lookup"><span data-stu-id="b890b-107"><span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**PHONEHOOKSWITCHDEV\_HEADSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b890b-108">Это гарнитура, подключенная к набору телефонов.</span><span class="sxs-lookup"><span data-stu-id="b890b-108">This is a headset connected to the phone set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b890b-109"><span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**ФОНЕХУКСВИТЧДЕВ \_ докладчик**</span><span class="sxs-lookup"><span data-stu-id="b890b-109"><span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**PHONEHOOKSWITCHDEV\_SPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b890b-110">Это встроенная громкоговоритель и микрофон.</span><span class="sxs-lookup"><span data-stu-id="b890b-110">This is a built-in loudspeaker and microphone.</span></span> <span data-ttu-id="b890b-111">Это может быть также внешний подключенный к дополнения динамик с внешним подключением к телефонному набору.</span><span class="sxs-lookup"><span data-stu-id="b890b-111">This could also be an externally connected adjunct speaker to the telephone set.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b890b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b890b-112">Remarks</span></span>

<span data-ttu-id="b890b-113">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="b890b-113">No extensibility.</span></span> <span data-ttu-id="b890b-114">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="b890b-114">All 32 bits are reserved.</span></span>

<span data-ttu-id="b890b-115">Эти константы используются в структуре данных [**фонекапс**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) для указания возможностей устройства хуксвитч телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="b890b-115">These constants are used in the [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) data structure to indicate the hookswitch device capabilities of a phone device.</span></span> <span data-ttu-id="b890b-116">Структура [**фонестатус**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) сообщает о состоянии устройств хуксвитч телефона.</span><span class="sxs-lookup"><span data-stu-id="b890b-116">The [**PHONESTATUS**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) structure reports the state of the phone's hookswitch devices.</span></span> <span data-ttu-id="b890b-117">Функция [**фонесесуксвитч**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) и [**фонежесуксвитч**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) используют ее в качестве параметра для выбора устройства ввода-вывода телефона.</span><span class="sxs-lookup"><span data-stu-id="b890b-117">The function [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) and [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) use it as a parameter to select the phone's I/O device.</span></span>

## <a name="requirements"></a><span data-ttu-id="b890b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b890b-118">Requirements</span></span>



| <span data-ttu-id="b890b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b890b-119">Requirement</span></span> | <span data-ttu-id="b890b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b890b-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b890b-121">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="b890b-121">TAPI version</span></span><br/> | <span data-ttu-id="b890b-122">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b890b-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b890b-123">Header</span><span class="sxs-lookup"><span data-stu-id="b890b-123">Header</span></span><br/>       | <dl> <span data-ttu-id="b890b-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b890b-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




