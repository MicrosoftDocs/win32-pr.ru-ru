---
description: Происходит при формировании нового отчета широты/долготы.
ms.assetid: 2b1a25a1-ccd6-43f8-979b-c2d414d666a2
title: Событие Невлатлонгрепорт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: ea305d17169b71d183a8d453e9885d8de878b026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674507"
---
# <a name="newlatlongreport-event"></a><span data-ttu-id="8823d-103">Событие Невлатлонгрепорт</span><span class="sxs-lookup"><span data-stu-id="8823d-103">NewLatLongReport event</span></span>

<span data-ttu-id="8823d-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="8823d-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8823d-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="8823d-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="8823d-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8823d-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="8823d-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="8823d-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="8823d-108">Происходит при формировании нового отчета широты/долготы.</span><span class="sxs-lookup"><span data-stu-id="8823d-108">Occurs when a new latitude/longitude report is generated.</span></span>

## <a name="syntax"></a><span data-ttu-id="8823d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8823d-109">Syntax</span></span>


```JScript
.NewLatLongReport(
  newReport
)
```



## <a name="parameters"></a><span data-ttu-id="8823d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="8823d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8823d-111">*неврепорт*</span><span class="sxs-lookup"><span data-stu-id="8823d-111">*newReport*</span></span> 
</dt> <dd>

<span data-ttu-id="8823d-112">Новый объект [**локатиондисп. дисплатлонгрепорт**](locationdisp-displatlongreport.md) .</span><span class="sxs-lookup"><span data-stu-id="8823d-112">The new [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8823d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8823d-113">Return value</span></span>

<span data-ttu-id="8823d-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8823d-114">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="8823d-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="8823d-115">Examples</span></span>

<span data-ttu-id="8823d-116">Пример использования этого события см. в разделе [Listening for LatLong Reports Events](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="8823d-116">For an example of how to use this event, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="8823d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8823d-117">Requirements</span></span>



| <span data-ttu-id="8823d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8823d-118">Requirement</span></span> | <span data-ttu-id="8823d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8823d-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="8823d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8823d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8823d-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8823d-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8823d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8823d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8823d-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8823d-123">None supported</span></span><br/>                  |



 

