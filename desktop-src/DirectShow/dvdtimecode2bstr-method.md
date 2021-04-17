---
description: Метод DVDTimeCode2bstr извлекает строку, указывающую текущее время на диске.
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: Метод DVDTimeCode2bstr
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042c6889fd2d5ee76aa42fc4e92f1c2754a5c95d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673033"
---
# <a name="dvdtimecode2bstr-method"></a><span data-ttu-id="b24a4-103">Метод DVDTimeCode2bstr</span><span class="sxs-lookup"><span data-stu-id="b24a4-103">DVDTimeCode2bstr Method</span></span>

> [!Note]  
> <span data-ttu-id="b24a4-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b24a4-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b24a4-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="b24a4-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b24a4-106">`DVDTimeCode2bstr`Метод получает строку, указывающую текущее время на диске.</span><span class="sxs-lookup"><span data-stu-id="b24a4-106">The `DVDTimeCode2bstr` method retrieves a string indicating the current time on the disc.</span></span>

``` syntax
[ sTimeCode = ] MSWebDVD.DVDTimeCode2bstr(nTimeCode)
```

## <a name="parameters"></a><span data-ttu-id="b24a4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b24a4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b24a4-108"><span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*стимекоде*</span><span class="sxs-lookup"><span data-stu-id="b24a4-108"><span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*</span></span>
</dt> <dd>

<span data-ttu-id="b24a4-109">Указывает текущее время на диске относительно начала заголовка в виде числа, полученного с помощью события [**\_ \_ хмсф Current в текущем \_ \_ времени**](ec-dvd-current-hmsf-time.md) в формате "DVD".</span><span class="sxs-lookup"><span data-stu-id="b24a4-109">Specifies the current time on the disc relative to the start of the title as a Number obtained through the [**EC\_DVD\_CURRENT\_HMSF\_TIME**](ec-dvd-current-hmsf-time.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b24a4-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b24a4-110">Return Value</span></span>

<span data-ttu-id="b24a4-111">Возвращает строку из 11 символов в формате "чч: мм: СС: FF", представляющей часы, минуты, секунды и кадры, определяющие текущее время.</span><span class="sxs-lookup"><span data-stu-id="b24a4-111">Returns an 11-character String in the format "hh:mm:ss:ff" representing the hours, minutes, seconds and frames that define the current time.</span></span>

## <a name="remarks"></a><span data-ttu-id="b24a4-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b24a4-112">Remarks</span></span>

<span data-ttu-id="b24a4-113">Этот метод доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b24a4-113">This method is read only.</span></span>

## <a name="see-also"></a><span data-ttu-id="b24a4-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b24a4-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b24a4-115">Обработка уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="b24a4-115">Handling DVD Event Notifications</span></span>](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



