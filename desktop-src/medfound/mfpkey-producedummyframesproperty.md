---
description: Указывает, создает ли кодировщик фиктивные записи кадра в битовом потоке для повторяющихся кадров.
ms.assetid: dc09cecb-98c0-40bb-9e5d-f4661bf98522
title: Свойство MFPKEY_PRODUCEDUMMYFRAMES (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b40bdaa54b3dc14a2b4ef44235d7f87cab5b905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263980"
---
# <a name="mfpkey_producedummyframes-property"></a><span data-ttu-id="34696-103">МФПКЭЙ \_ продуцедуммифрамес, свойство</span><span class="sxs-lookup"><span data-stu-id="34696-103">MFPKEY\_PRODUCEDUMMYFRAMES Property</span></span>

<span data-ttu-id="34696-104">Указывает, создает ли кодировщик фиктивные записи кадра в битовом потоке для повторяющихся кадров.</span><span class="sxs-lookup"><span data-stu-id="34696-104">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="34696-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="34696-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="34696-106">g \_ всзвмвкпродуцедуммифрамес</span><span class="sxs-lookup"><span data-stu-id="34696-106">g\_wszWMVCProduceDummyFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="34696-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="34696-107">Data Type</span></span>

<span data-ttu-id="34696-108">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="34696-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="34696-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="34696-109">Default Value</span></span>

<span data-ttu-id="34696-110">ВАРИАНТ \_ false</span><span class="sxs-lookup"><span data-stu-id="34696-110">VARIANT\_FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="34696-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34696-111">Remarks</span></span>

<span data-ttu-id="34696-112">Если это значение является ВАРИАНТным \_ false, кодек не будет поместит данные в поток битов для повторяющихся кадров.</span><span class="sxs-lookup"><span data-stu-id="34696-112">If this value is VARIANT\_FALSE, the codec will not put any data in the bit stream for duplicate frames.</span></span>

<span data-ttu-id="34696-113">Фиктивные кадры могут быть важны в приложениях, где сохраняются номера кадров.</span><span class="sxs-lookup"><span data-stu-id="34696-113">Dummy frames can be important in applications where frame numbers are persisted.</span></span> <span data-ttu-id="34696-114">Распространенным примером является то, что коды времени SMPTE поддерживаются для кодированного содержимого.</span><span class="sxs-lookup"><span data-stu-id="34696-114">A common example is when SMPTE time codes are maintained for encoded content.</span></span>

## <a name="requirements"></a><span data-ttu-id="34696-115">Требования</span><span class="sxs-lookup"><span data-stu-id="34696-115">Requirements</span></span>



| <span data-ttu-id="34696-116">Требование</span><span class="sxs-lookup"><span data-stu-id="34696-116">Requirement</span></span> | <span data-ttu-id="34696-117">Значение</span><span class="sxs-lookup"><span data-stu-id="34696-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34696-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34696-118">Minimum supported client</span></span><br/> | <span data-ttu-id="34696-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="34696-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="34696-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34696-120">Minimum supported server</span></span><br/> | <span data-ttu-id="34696-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="34696-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="34696-122">Header</span><span class="sxs-lookup"><span data-stu-id="34696-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="34696-123"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="34696-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34696-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34696-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34696-125">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="34696-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




