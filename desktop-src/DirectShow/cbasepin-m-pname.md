---
description: Имя ПИН-кода.
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: 'Элемент Кбасепин:: m_pName (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pName
api_type:
- HeaderDef
api_location:
- Amfilter.h
ms.openlocfilehash: f2580b9aba379362c39e3d792504434fa18fe076
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657789"
---
# <a name="cbasepinm_pname-member"></a><span data-ttu-id="245b3-103">Элемент Кбасепин:: m \_ pName</span><span class="sxs-lookup"><span data-stu-id="245b3-103">CBasePin::m\_pName member</span></span>

<span data-ttu-id="245b3-104">Имя ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="245b3-104">Pin name.</span></span>

## <a name="syntax"></a><span data-ttu-id="245b3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="245b3-105">Syntax</span></span>


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a><span data-ttu-id="245b3-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="245b3-106">Remarks</span></span>

<span data-ttu-id="245b3-107">Метод [**кбасепин:: куерипининфо**](cbasepin-querypininfo.md) возвращает эту строку в качестве имени ПИН-кода, а метод [**Кбасепин:: QueryId**](cbasepin-queryid.md) возвращает его в качестве идентификатора ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="245b3-107">The [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md) method returns this string as the pin name, and the [**CBasePin::QueryId**](cbasepin-queryid.md) method returns it as the pin identifier.</span></span> <span data-ttu-id="245b3-108">Однако в общем случае имя и идентификатор ПИН-кода не должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="245b3-108">In general, however, the pin name and the pin identifier are not required to be the same.</span></span> <span data-ttu-id="245b3-109">Идентификатор ПИН-кода используется для сохраняемости графа.</span><span class="sxs-lookup"><span data-stu-id="245b3-109">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="245b3-110">Дополнительные сведения см. в разделе [**ибасефилтер:: финдпин**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).</span><span class="sxs-lookup"><span data-stu-id="245b3-110">For more information, see [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).</span></span>

## <a name="requirements"></a><span data-ttu-id="245b3-111">Требования</span><span class="sxs-lookup"><span data-stu-id="245b3-111">Requirements</span></span>



| <span data-ttu-id="245b3-112">Требование</span><span class="sxs-lookup"><span data-stu-id="245b3-112">Requirement</span></span> | <span data-ttu-id="245b3-113">Значение</span><span class="sxs-lookup"><span data-stu-id="245b3-113">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="245b3-114">Header</span><span class="sxs-lookup"><span data-stu-id="245b3-114">Header</span></span><br/> | <dl> <span data-ttu-id="245b3-115"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="245b3-115"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="245b3-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="245b3-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="245b3-117">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="245b3-117">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




