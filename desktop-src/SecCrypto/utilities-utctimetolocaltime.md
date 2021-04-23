---
description: Преобразует время в формате UTC (время по Гринвичу) в местное время компьютера.
ms.assetid: 4085d7cb-d346-477d-a043-e96fb951c35a
title: Метод Utilities. Утктиметолокалтиме
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.UTCTimeToLocalTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fe41cf8d9ec92c0c71be5130aded0b7db539b9b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685023"
---
# <a name="utilitiesutctimetolocaltime-method"></a><span data-ttu-id="1b63c-103">Метод Utilities. Утктиметолокалтиме</span><span class="sxs-lookup"><span data-stu-id="1b63c-103">Utilities.UTCTimeToLocalTime method</span></span>

<span data-ttu-id="1b63c-104">\[Метод **утктиметолокалтиме** доступен для использования в операционных системах, указанных в разделе требования.\]</span><span class="sxs-lookup"><span data-stu-id="1b63c-104">\[The **UTCTimeToLocalTime** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="1b63c-105">Метод **утктиметолокалтиме** преобразует всеобщее скоординированное время (время по Гринвичу) в местное время компьютера.</span><span class="sxs-lookup"><span data-stu-id="1b63c-105">The **UTCTimeToLocalTime** method converts Coordinated Universal Time (Greenwich Mean Time) to the computer's local time.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b63c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b63c-106">Syntax</span></span>


```VB
Utilities.UTCTimeToLocalTime( _
  ByVal UTCTime _
)
```



## <a name="parameters"></a><span data-ttu-id="1b63c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b63c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b63c-108">*Утктиме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b63c-108">*UTCTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b63c-109">Время в формате UTC, которое необходимо преобразовать в местное время компьютера.</span><span class="sxs-lookup"><span data-stu-id="1b63c-109">The Coordinated Universal Time to be converted to the computer's local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b63c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b63c-110">Return value</span></span>

<span data-ttu-id="1b63c-111">Местное время, соответствующее заданному всеобщему скоординированному времени.</span><span class="sxs-lookup"><span data-stu-id="1b63c-111">The local time that corresponds to the specified Coordinated Universal Time.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b63c-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b63c-112">Remarks</span></span>

<span data-ttu-id="1b63c-113">Несмотря на то, что система использует координированное всемирное время, приложения обычно отображают местное время, которое представляет собой дату и время суток для местного часового пояса компьютера.</span><span class="sxs-lookup"><span data-stu-id="1b63c-113">While the system uses Coordinated Universal Time internally, applications generally display the local time, which is the date and time of day for the computer's local time zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b63c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1b63c-114">Requirements</span></span>



| <span data-ttu-id="1b63c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1b63c-115">Requirement</span></span> | <span data-ttu-id="1b63c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1b63c-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b63c-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="1b63c-117">Redistributable</span></span><br/> | <span data-ttu-id="1b63c-118">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="1b63c-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1b63c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="1b63c-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="1b63c-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b63c-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b63c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b63c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b63c-122">**Служебные программы**</span><span class="sxs-lookup"><span data-stu-id="1b63c-122">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




