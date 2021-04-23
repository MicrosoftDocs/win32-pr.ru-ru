---
description: Преобразует местное время компьютера в формат UTC (время по Гринвичу).
ms.assetid: ff5d40ba-7d94-4f11-9c18-e41752d1d7b9
title: Метод Utilities. Локалтиметаутктиме
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.LocalTimeToUTCTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2691e3306a84ce4eff3d73df4b070ba4b65671f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685024"
---
# <a name="utilitieslocaltimetoutctime-method"></a><span data-ttu-id="50757-103">Метод Utilities. Локалтиметаутктиме</span><span class="sxs-lookup"><span data-stu-id="50757-103">Utilities.LocalTimeToUTCTime method</span></span>

<span data-ttu-id="50757-104">\[Метод **локалтиметаутктиме** доступен для использования в операционных системах, указанных в разделе требования.\]</span><span class="sxs-lookup"><span data-stu-id="50757-104">\[The **LocalTimeToUTCTime** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="50757-105">Метод **локалтиметаутктиме** Преобразует местное время компьютера в формат UTC (время по Гринвичу).</span><span class="sxs-lookup"><span data-stu-id="50757-105">The **LocalTimeToUTCTime** method converts the computer's local time to Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="syntax"></a><span data-ttu-id="50757-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50757-106">Syntax</span></span>


```VB
Utilities.LocalTimeToUTCTime( _
  ByVal LocalTime _
)
```



## <a name="parameters"></a><span data-ttu-id="50757-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="50757-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50757-108">*Localtime* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50757-108">*LocalTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50757-109">Местное время для преобразования в время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="50757-109">The local time to be converted to Coordinated Universal Time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50757-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50757-110">Return value</span></span>

<span data-ttu-id="50757-111">Время в формате UTC, соответствующее указанному местному времени.</span><span class="sxs-lookup"><span data-stu-id="50757-111">The Coordinated Universal Time that corresponds to the specified local time.</span></span>

## <a name="remarks"></a><span data-ttu-id="50757-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50757-112">Remarks</span></span>

<span data-ttu-id="50757-113">Несмотря на то, что система использует координированное всемирное время, приложения обычно отображают местное время, которое представляет собой дату и время суток для местного часового пояса компьютера.</span><span class="sxs-lookup"><span data-stu-id="50757-113">While the system uses Coordinated Universal Time internally, applications generally display the local time, which is the date and time of day for the computer's local time zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="50757-114">Требования</span><span class="sxs-lookup"><span data-stu-id="50757-114">Requirements</span></span>



| <span data-ttu-id="50757-115">Требование</span><span class="sxs-lookup"><span data-stu-id="50757-115">Requirement</span></span> | <span data-ttu-id="50757-116">Значение</span><span class="sxs-lookup"><span data-stu-id="50757-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50757-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="50757-117">Redistributable</span></span><br/> | <span data-ttu-id="50757-118">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="50757-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="50757-119">DLL</span><span class="sxs-lookup"><span data-stu-id="50757-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="50757-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50757-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50757-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50757-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50757-122">**Служебные программы**</span><span class="sxs-lookup"><span data-stu-id="50757-122">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




