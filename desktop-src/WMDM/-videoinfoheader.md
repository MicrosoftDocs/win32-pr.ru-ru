---
title: Структура _VIDEOINFOHEADER
description: '\_Структура видеоинфохеадер содержит сведения о видеопотоке и включает \_ структуру битмапинфохеадер, определяющую формат отдельного кадра.'
ms.assetid: 5a39d66e-8dbc-4572-8370-14f722b6c906
keywords:
- _VIDEOINFOHEADER структура диспетчер устройств Windows Media
topic_type:
- apiref
api_name:
- _VIDEOINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5b389c5c82296e95ecfb3900518af4a2c7ddd7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694439"
---
# <a name="_videoinfoheader-structure"></a><span data-ttu-id="c6e03-104">\_Структура ВИДЕОИНФОХЕАДЕР</span><span class="sxs-lookup"><span data-stu-id="c6e03-104">\_VIDEOINFOHEADER structure</span></span>

<span data-ttu-id="c6e03-105">Структура **\_ видеоинфохеадер** содержит сведения о видеопотоке и включает структуру **\_ битмапинфохеадер** , определяющую формат отдельного кадра.</span><span class="sxs-lookup"><span data-stu-id="c6e03-105">The **\_VIDEOINFOHEADER** structure contains information about a video stream and includes a **\_BITMAPINFOHEADER** structure that defines the format of an individual frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6e03-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6e03-106">Syntax</span></span>


```C++
typedef struct _tagVIDEOINFOHEADER {
  RECT             rcSource;
  RECT             rcTarget;
  DWORD            dwBitRate;
  DWORD            dwBitErrorRate;
  REFERENCE_TIME   AvgTimePerFrame;
  BITMAPINFOHEADER bmiHeader;
} _VIDEOINFOHEADER;
```



## <a name="members"></a><span data-ttu-id="c6e03-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c6e03-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c6e03-108">**рксаурце**</span><span class="sxs-lookup"><span data-stu-id="c6e03-108">**rcSource**</span></span>
</dt> <dd>

<span data-ttu-id="c6e03-109">Структура **Rect** , указывающая исходное видеоокно.</span><span class="sxs-lookup"><span data-stu-id="c6e03-109">**RECT** structure that specifies the source video window.</span></span>

</dd> <dt>

<span data-ttu-id="c6e03-110">**рктаржет**</span><span class="sxs-lookup"><span data-stu-id="c6e03-110">**rcTarget**</span></span>
</dt> <dd>

<span data-ttu-id="c6e03-111">Структура **Rect** , указывающая целевое окно видео.</span><span class="sxs-lookup"><span data-stu-id="c6e03-111">**RECT** structure that specifies the destination video window.</span></span>

</dd> <dt>

<span data-ttu-id="c6e03-112">**двбитрате**</span><span class="sxs-lookup"><span data-stu-id="c6e03-112">**dwBitRate**</span></span>
</dt> <dd>

<span data-ttu-id="c6e03-113">Значение **типа DWORD** , указывающее приблизительную скорость передачи данных видеопотока в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="c6e03-113">**DWORD** value that specifies the video stream's approximate data rate, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="c6e03-114">**двбитерроррате**</span><span class="sxs-lookup"><span data-stu-id="c6e03-114">**dwBitErrorRate**</span></span>
</dt> <dd>

<span data-ttu-id="c6e03-115">Значение **типа DWORD** , указывающее частоту ошибок данных потока видео в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="c6e03-115">**DWORD** value that specifies the video stream's data error rate, in bit errors per second.</span></span>

</dd> <dt>

<span data-ttu-id="c6e03-116">**авгтимеперфраме**</span><span class="sxs-lookup"><span data-stu-id="c6e03-116">**AvgTimePerFrame**</span></span>
</dt> <dd>

<span data-ttu-id="c6e03-117">**Справочные материалы \_ Значение времени** , указывающее среднее время показа видеокадра (в 100-наносекундных единицах).</span><span class="sxs-lookup"><span data-stu-id="c6e03-117">**REFERENCE\_TIME** value that specifies the video frame's average display time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="c6e03-118">**бмихеадер**</span><span class="sxs-lookup"><span data-stu-id="c6e03-118">**bmiHeader**</span></span>
</dt> <dd>

<span data-ttu-id="c6e03-119">Структура Win32 **\_ битмапинфохеадер** , которая содержит сведения о цвете и измерении для растрового изображения видео.</span><span class="sxs-lookup"><span data-stu-id="c6e03-119">Win32 **\_BITMAPINFOHEADER** structure that contains color and dimension information for the video image bitmap.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6e03-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c6e03-120">Requirements</span></span>



| <span data-ttu-id="c6e03-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c6e03-121">Requirement</span></span> | <span data-ttu-id="c6e03-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c6e03-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c6e03-123">Header</span><span class="sxs-lookup"><span data-stu-id="c6e03-123">Header</span></span><br/> | <dl> <span data-ttu-id="c6e03-124"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c6e03-124"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6e03-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6e03-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6e03-126">**\_битмапинфохеадер**</span><span class="sxs-lookup"><span data-stu-id="c6e03-126">**\_BITMAPINFOHEADER**</span></span>](-bitmapinfoheader.md)
</dt> <dt>

[<span data-ttu-id="c6e03-127">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="c6e03-127">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





