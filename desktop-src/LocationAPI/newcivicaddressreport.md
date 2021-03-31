---
description: Происходит при создании отчета об использовании нового административного адреса.
ms.assetid: a8df870e-6744-4e8a-a103-56b446da135f
title: Событие НевЦивикаддрессрепорт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: fa786ecee4ce4223cdb7ec0c8400c5c11bf6e192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913508"
---
# <a name="newcivicaddressreport-event"></a><span data-ttu-id="e130e-103">Событие НевЦивикаддрессрепорт</span><span class="sxs-lookup"><span data-stu-id="e130e-103">NewCivicAddressReport event</span></span>

<span data-ttu-id="e130e-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="e130e-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e130e-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="e130e-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e130e-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e130e-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="e130e-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="e130e-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="e130e-108">Происходит при создании отчета об использовании нового административного адреса.</span><span class="sxs-lookup"><span data-stu-id="e130e-108">Occurs when a new civic address report is generated.</span></span>

## <a name="syntax"></a><span data-ttu-id="e130e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e130e-109">Syntax</span></span>


```JScript
.NewCivicAddressReport(
  newReport
)
```



## <a name="parameters"></a><span data-ttu-id="e130e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e130e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e130e-111">*неврепорт*</span><span class="sxs-lookup"><span data-stu-id="e130e-111">*newReport*</span></span> 
</dt> <dd>

<span data-ttu-id="e130e-112">Новый объект [**локатиондисп. диспЦивикаддрессрепорт**](locationdisp-dispcivicaddressreport.md) .</span><span class="sxs-lookup"><span data-stu-id="e130e-112">The new [**LocationDisp.DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e130e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e130e-113">Return value</span></span>

<span data-ttu-id="e130e-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e130e-114">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="e130e-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="e130e-115">Examples</span></span>

<span data-ttu-id="e130e-116">Пример использования этого события см. в разделе [прослушивание событий административного адреса](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="e130e-116">For an example of how to use this event, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="e130e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e130e-117">Requirements</span></span>



| <span data-ttu-id="e130e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e130e-118">Requirement</span></span> | <span data-ttu-id="e130e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e130e-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="e130e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e130e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e130e-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e130e-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e130e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e130e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e130e-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e130e-123">None supported</span></span><br/>                  |



 

