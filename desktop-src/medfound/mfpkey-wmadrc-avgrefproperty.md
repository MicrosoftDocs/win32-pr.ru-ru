---
description: Указывает средний уровень громкости звукового содержимого.
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: Свойство MFPKEY_WMADRC_AVGREF (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf18c37b00f84cc3ae3fdf1f44b2fbefcc56d9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662687"
---
# <a name="mfpkey_wmadrc_avgref-property"></a><span data-ttu-id="7136e-103">МФПКЭЙ \_ вмадрк \_ Авгреф, свойство</span><span class="sxs-lookup"><span data-stu-id="7136e-103">MFPKEY\_WMADRC\_AVGREF Property</span></span>

<span data-ttu-id="7136e-104">Указывает средний уровень громкости звукового содержимого.</span><span class="sxs-lookup"><span data-stu-id="7136e-104">Specifies the average volume level of audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7136e-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="7136e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="7136e-106">g \_ всзвмадркаверажереференце</span><span class="sxs-lookup"><span data-stu-id="7136e-106">g\_wszWMADRCAverageReference</span></span>

## <a name="data-type"></a><span data-ttu-id="7136e-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7136e-107">Data Type</span></span>

<span data-ttu-id="7136e-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="7136e-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="7136e-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7136e-109">Remarks</span></span>

<span data-ttu-id="7136e-110">Это значение можно получить из кодировщика после обработки содержимого.</span><span class="sxs-lookup"><span data-stu-id="7136e-110">You can get this value from the encoder after the content is processed.</span></span> <span data-ttu-id="7136e-111">Это значение также может быть задано для декодера в целях динамического управления диапазоном, но оно будет действовать, только если задано свойство [мфпкэй \_ вмадек \_ дркмоде](mfpkey-wmadec-drcmodeproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="7136e-111">This value can also be set on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

<span data-ttu-id="7136e-112">Дополнительные сведения о динамическом контроле диапазонов см. в статье [функции кодека Windows Media Audio Professional](/previous-versions/ms867218(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="7136e-112">For more information on dynamic range control see the web article [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="7136e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7136e-113">Requirements</span></span>



| <span data-ttu-id="7136e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7136e-114">Requirement</span></span> | <span data-ttu-id="7136e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7136e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7136e-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7136e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7136e-117">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7136e-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7136e-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7136e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7136e-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7136e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7136e-120">Header</span><span class="sxs-lookup"><span data-stu-id="7136e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7136e-121"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7136e-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7136e-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7136e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7136e-123">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7136e-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
