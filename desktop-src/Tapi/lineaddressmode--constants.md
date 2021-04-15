---
description: '\_Константы побитового флага линеаддрессмоде описывают различные способы идентификации адреса на устройстве линии.'
ms.assetid: f0f132a0-2e8e-478f-909b-c100aa360daa
title: Константы LINEADDRESSMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5e926772c82a36865c7f3b95c1ca1321db5682
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688876"
---
# <a name="lineaddressmode_-constants"></a><span data-ttu-id="85a36-103">\_Константы линеаддрессмоде</span><span class="sxs-lookup"><span data-stu-id="85a36-103">LINEADDRESSMODE\_ Constants</span></span>

<span data-ttu-id="85a36-104">Константы побитового флага **линеаддрессмоде \_** описывают различные способы идентификации адреса на устройстве линии.</span><span class="sxs-lookup"><span data-stu-id="85a36-104">The **LINEADDRESSMODE\_** bit-flag constants describe various ways of identifying an address on a line device.</span></span>

<dl> <dt>

<span data-ttu-id="85a36-105"><span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**ЛИНЕАДДРЕССМОДЕ \_ ADDRESSID**</span><span class="sxs-lookup"><span data-stu-id="85a36-105"><span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE\_ADDRESSID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="85a36-106">Адрес указывается с небольшим целым числом в диапазоне от 0 до *двнумаддрессес* минус один, где *двнумаддрессес* — это значение в возможностях устройства линии.</span><span class="sxs-lookup"><span data-stu-id="85a36-106">The address is specified with a small integer in the range 0 to *dwNumAddresses* minus one, where *dwNumAddresses* is the value in the line's device capabilities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="85a36-107"><span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**ЛИНЕАДДРЕССМОДЕ \_ диалаблеаддр**</span><span class="sxs-lookup"><span data-stu-id="85a36-107"><span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE\_DIALABLEADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="85a36-108">Адрес указывается по номеру телефона.</span><span class="sxs-lookup"><span data-stu-id="85a36-108">The address is specified through its phone number.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85a36-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85a36-109">Remarks</span></span>

<span data-ttu-id="85a36-110">Старшие 16 бит можно назначить для расширений для конкретных устройств.</span><span class="sxs-lookup"><span data-stu-id="85a36-110">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="85a36-111">16 младших разрядов зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="85a36-111">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="85a36-112">Эта константа используется для выбора адреса в строке, в которой происходит вызов.</span><span class="sxs-lookup"><span data-stu-id="85a36-112">This constant is used to select an address on a line on which to originate a call.</span></span> <span data-ttu-id="85a36-113">В обычной модели адрес выбирается посредством идентификатора адреса.</span><span class="sxs-lookup"><span data-stu-id="85a36-113">The usual model would select the address by means of its address identifier.</span></span> <span data-ttu-id="85a36-114">Идентификаторы адресов — это механизм, используемый для идентификации адресов по всему интерфейсу TAPI.</span><span class="sxs-lookup"><span data-stu-id="85a36-114">Address identifiers are the mechanism used to identify addresses throughout TAPI.</span></span> <span data-ttu-id="85a36-115">Однако в некоторых средах, при совершении вызова, часто бывает более практично указывать исходящий адрес вызова по номеру телефона, а не по идентификатору адреса.</span><span class="sxs-lookup"><span data-stu-id="85a36-115">However, in some environments, when making a call, it is often more practical to identify a call's originating address by phone number rather than by address identifier.</span></span> <span data-ttu-id="85a36-116">Одним из примеров является возможность моделирования большого количества станций (третьих сторон) на коммутаторе с помощью одного линейного устройства с множеством адресов.</span><span class="sxs-lookup"><span data-stu-id="85a36-116">One example is in the possible modeling of large numbers of stations (third party) on the switch by means of one line device with many addresses.</span></span> <span data-ttu-id="85a36-117">Линия представляет набор всех станций, каждая из которых сопоставляется с адресом с собственным основным номером телефона и идентификатором адреса.</span><span class="sxs-lookup"><span data-stu-id="85a36-117">The line represents the set of all stations, and each station is mapped to an address with its own primary phone number and address identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="85a36-118">Требования</span><span class="sxs-lookup"><span data-stu-id="85a36-118">Requirements</span></span>



| <span data-ttu-id="85a36-119">Требование</span><span class="sxs-lookup"><span data-stu-id="85a36-119">Requirement</span></span> | <span data-ttu-id="85a36-120">Значение</span><span class="sxs-lookup"><span data-stu-id="85a36-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="85a36-121">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="85a36-121">TAPI version</span></span><br/> | <span data-ttu-id="85a36-122">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="85a36-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="85a36-123">Header</span><span class="sxs-lookup"><span data-stu-id="85a36-123">Header</span></span><br/>       | <dl> <span data-ttu-id="85a36-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="85a36-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




