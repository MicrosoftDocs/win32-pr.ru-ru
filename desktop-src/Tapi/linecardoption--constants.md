---
description: '\_Константы линекардоптион определяют значения, используемые в элементе двоптионс структуры линекардентри, возвращаемой как часть структуры линетранслатекапс, возвращаемой линежеттранслатекапс.'
ms.assetid: 36c67fbf-e5ca-4ec4-a03a-0b828667abcc
title: Константы LINECARDOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd9948d4a8963e8a9c860f68f0067c601f602c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680049"
---
# <a name="linecardoption_-constants"></a><span data-ttu-id="71896-103">\_Константы линекардоптион</span><span class="sxs-lookup"><span data-stu-id="71896-103">LINECARDOPTION\_ Constants</span></span>

<span data-ttu-id="71896-104">**\_ Константы линекардоптион** определяют значения, используемые в элементе **двоптионс** структуры [**линекардентри**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) , возвращаемой как часть структуры [**линетранслатекапс**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) , возвращаемой [**линежеттранслатекапс**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span><span class="sxs-lookup"><span data-stu-id="71896-104">The **LINECARDOPTION\_constants** define values used in the **dwOptions** member of the [**LINECARDENTRY**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) structure returned as part of the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure returned by [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span></span> <span data-ttu-id="71896-105">**\_ Константы линекардоптион** t имеют следующие значения:</span><span class="sxs-lookup"><span data-stu-id="71896-105">The **LINECARDOPTION\_constants** t has the following values:</span></span>

<dl> <dt>

<span data-ttu-id="71896-106"><span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**ЛИНЕКАРДОПТИОН \_ скрыто**</span><span class="sxs-lookup"><span data-stu-id="71896-106"><span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**LINECARDOPTION\_HIDDEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71896-107">Эта телефонная карточка скрыта пользователем.</span><span class="sxs-lookup"><span data-stu-id="71896-107">This calling card has been hidden by the user.</span></span> <span data-ttu-id="71896-108">Он не отображается вспомогательным помощником в главном списке доступных телефонных карточек, но будет отображаться в списке карточек, из которого можно копировать правила набора.</span><span class="sxs-lookup"><span data-stu-id="71896-108">It is not shown by Dial Helper in the main listing of available calling cards, but will be shown in the list of cards from which dialing rules can be copied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71896-109"><span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**предопределенный ЛИНЕКАРДОПТИОН \_**</span><span class="sxs-lookup"><span data-stu-id="71896-109"><span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**LINECARDOPTION\_PREDEFINED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71896-110">Эта телефонная карточка представляет собой одно из стандартных определений телефонной карточки, включенных в телефонную связь корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="71896-110">This calling card is one of the predefined calling card definitions included with Telephony by Microsoft.</span></span> <span data-ttu-id="71896-111">Его нельзя удалить полностью с помощью вспомогательного метода вызова; Если пользователь попытается удалить его, он станет СКРЫТЫМ.</span><span class="sxs-lookup"><span data-stu-id="71896-111">It cannot be removed entirely using Dial Helper; if the user attempts to remove it, it will become HIDDEN.</span></span> <span data-ttu-id="71896-112">Поэтому он остается доступным для копирования правил набора номера.</span><span class="sxs-lookup"><span data-stu-id="71896-112">It thus continues to be accessible for copying of dialing rules.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71896-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71896-113">Remarks</span></span>

<span data-ttu-id="71896-114">Не расширяемый.</span><span class="sxs-lookup"><span data-stu-id="71896-114">Not extensible.</span></span> <span data-ttu-id="71896-115">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="71896-115">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="71896-116">Требования</span><span class="sxs-lookup"><span data-stu-id="71896-116">Requirements</span></span>



| <span data-ttu-id="71896-117">Требование</span><span class="sxs-lookup"><span data-stu-id="71896-117">Requirement</span></span> | <span data-ttu-id="71896-118">Значение</span><span class="sxs-lookup"><span data-stu-id="71896-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="71896-119">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="71896-119">TAPI version</span></span><br/> | <span data-ttu-id="71896-120">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="71896-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="71896-121">Header</span><span class="sxs-lookup"><span data-stu-id="71896-121">Header</span></span><br/>       | <dl> <span data-ttu-id="71896-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="71896-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




