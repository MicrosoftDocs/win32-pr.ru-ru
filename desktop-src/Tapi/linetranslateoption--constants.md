---
description: '\_Константа битового флага линетранслатеоптион описывает параметр, используемый при преобразовании адресов.'
ms.assetid: 3f5e9952-945e-42b8-8536-b52a0c833282
title: Константы LINETRANSLATEOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e103f2a93d30be5260b27c7bf5c0e97f3ce7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685445"
---
# <a name="linetranslateoption_-constants"></a><span data-ttu-id="e08fd-103">\_Константы линетранслатеоптион</span><span class="sxs-lookup"><span data-stu-id="e08fd-103">LINETRANSLATEOPTION\_ Constants</span></span>

<span data-ttu-id="e08fd-104">Константа битового флага **линетранслатеоптион \_** описывает параметр, используемый при преобразовании адресов.</span><span class="sxs-lookup"><span data-stu-id="e08fd-104">The **LINETRANSLATEOPTION\_** bit-flag constant describes an option used by address translation.</span></span>

<dl> <dt>

<span data-ttu-id="e08fd-105"><span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**ЛИНЕТРАНСЛАТЕОПТИОН \_ канцелкаллваитинг**</span><span class="sxs-lookup"><span data-stu-id="e08fd-105"><span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**LINETRANSLATEOPTION\_CANCELCALLWAITING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e08fd-106">Если для расположения определена ожидающая строка вызова Cancel, установка этого бита приведет к вставке строки в начало строки с набором.</span><span class="sxs-lookup"><span data-stu-id="e08fd-106">If a Cancel Call Waiting string is defined for the location, setting this bit will cause that string to be inserted at the beginning of the dialable string.</span></span> <span data-ttu-id="e08fd-107">Обычно это используется приложениями для работы с данными и модемами, чтобы предотвратить прерывание вызовов с помощью сигналов, ожидающих звонка.</span><span class="sxs-lookup"><span data-stu-id="e08fd-107">This is commonly used by data modem and fax applications to prevent interruption of calls by call waiting beeps.</span></span> <span data-ttu-id="e08fd-108">Если для расположения не определена ожидающая строка вызова Cancel, этот бит не влияет на.</span><span class="sxs-lookup"><span data-stu-id="e08fd-108">If no Cancel Call Waiting string is defined for the location, this bit has no affect.</span></span> <span data-ttu-id="e08fd-109">Обратите внимание, что в приложениях, использующих этот бит, рекомендуется также установить \_ Безопасный бит линекаллпарамфлагс в члене **Двкаллпарамфлагс** структуры [**линекаллпарамс**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) , передаваемой в [**линемакекалл**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) с помощью параметра *лпкаллпарамс* . Таким образом, если линейное устройство использует механизм, отличный от цифр, доступных для набора, для подавления прерываний вызова этот механизм будет вызван.</span><span class="sxs-lookup"><span data-stu-id="e08fd-109">Note that applications using this bit are advised to also set the LINECALLPARAMFLAGS\_SECURE bit in the **dwCallParamFlags** member of the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure passed in to [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) through the *lpCallParams* parameter, so that if the line device uses a mechanism other than dialable digits to suppress call interrupts then that mechanism will be invoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e08fd-110"><span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**ЛИНЕТРАНСЛАТЕОПТИОН \_ кардоверриде**</span><span class="sxs-lookup"><span data-stu-id="e08fd-110"><span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**LINETRANSLATEOPTION\_CARDOVERRIDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e08fd-111">Вызывающая карточка по умолчанию должна быть переопределена указанной.</span><span class="sxs-lookup"><span data-stu-id="e08fd-111">The default calling card is to be overridden with a specified one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e08fd-112"><span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**ЛИНЕТРАНСЛАТЕОПТИОН \_ форцелд**</span><span class="sxs-lookup"><span data-stu-id="e08fd-112"><span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**LINETRANSLATEOPTION\_FORCELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e08fd-113">Этот параметр приводит к тому, что адрес (номер) будет преобразован на длинное расстояние.</span><span class="sxs-lookup"><span data-stu-id="e08fd-113">This option forces the address (number) to be translated as long distance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e08fd-114"><span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**ЛИНЕТРАНСЛАТЕОПТИОН \_ форцелокал**</span><span class="sxs-lookup"><span data-stu-id="e08fd-114"><span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**LINETRANSLATEOPTION\_FORCELOCAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e08fd-115">Этот параметр задает принудительное преобразование числа (адреса) в локальную.</span><span class="sxs-lookup"><span data-stu-id="e08fd-115">This option forces the number (address) to be translated as local.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e08fd-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e08fd-116">Remarks</span></span>

<span data-ttu-id="e08fd-117">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="e08fd-117">No extensibility.</span></span> <span data-ttu-id="e08fd-118">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="e08fd-118">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="e08fd-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e08fd-119">Requirements</span></span>



| <span data-ttu-id="e08fd-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e08fd-120">Requirement</span></span> | <span data-ttu-id="e08fd-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e08fd-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e08fd-122">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="e08fd-122">TAPI version</span></span><br/> | <span data-ttu-id="e08fd-123">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e08fd-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e08fd-124">Header</span><span class="sxs-lookup"><span data-stu-id="e08fd-124">Header</span></span><br/>       | <dl> <span data-ttu-id="e08fd-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e08fd-125"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e08fd-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e08fd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e08fd-127">**линекаллпарамс**</span><span class="sxs-lookup"><span data-stu-id="e08fd-127">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="e08fd-128">**линемакекалл**</span><span class="sxs-lookup"><span data-stu-id="e08fd-128">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="e08fd-129">**линетранслатеаутпут**</span><span class="sxs-lookup"><span data-stu-id="e08fd-129">**LINETRANSLATEOUTPUT**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslateoutput)
</dt> </dl>

 

 




