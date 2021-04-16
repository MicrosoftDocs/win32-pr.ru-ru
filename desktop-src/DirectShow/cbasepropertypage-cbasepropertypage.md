---
description: Метод конструктора.
ms.assetid: 5d9863e7-fdd9-4df2-a603-34a240a2286c
title: Конструктор Кбасепропертипаже. Кбасепропертипаже (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 915bc42cfb7f152cc061dab76caede6c998edf8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665169"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a><span data-ttu-id="be622-103">Кбасепропертипаже. Кбасепропертипаже, конструктор</span><span class="sxs-lookup"><span data-stu-id="be622-103">CBasePropertyPage.CBasePropertyPage constructor</span></span>

<span data-ttu-id="be622-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="be622-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="be622-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be622-105">Syntax</span></span>


```C++
CBasePropertyPage(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   int       DialogId,
   int       TitleId
);
```



## <a name="parameters"></a><span data-ttu-id="be622-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="be622-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be622-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="be622-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="be622-108">Строка, содержащая имя объекта для целей отладки.</span><span class="sxs-lookup"><span data-stu-id="be622-108">String that contains the name of the object, for debugging purposes.</span></span> <span data-ttu-id="be622-109">Дополнительные сведения см. в разделе [**кбасеобжект:: кбасеобжект**](cbaseobject-cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="be622-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="be622-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="be622-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="be622-111">Указатель на агрегированный интерфейс **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="be622-111">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="be622-112">*диалогид*</span><span class="sxs-lookup"><span data-stu-id="be622-112">*DialogId*</span></span> 
</dt> <dd>

<span data-ttu-id="be622-113">Идентификатор ресурса для этого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="be622-113">Resource ID for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="be622-114">*титлеид*</span><span class="sxs-lookup"><span data-stu-id="be622-114">*TitleId*</span></span> 
</dt> <dd>

<span data-ttu-id="be622-115">Идентификатор ресурса для строки, содержащей заголовок диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="be622-115">Resource ID for the string that contains the dialog box title.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="be622-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="be622-116">Examples</span></span>


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a><span data-ttu-id="be622-117">Требования</span><span class="sxs-lookup"><span data-stu-id="be622-117">Requirements</span></span>



| <span data-ttu-id="be622-118">Требование</span><span class="sxs-lookup"><span data-stu-id="be622-118">Requirement</span></span> | <span data-ttu-id="be622-119">Значение</span><span class="sxs-lookup"><span data-stu-id="be622-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be622-120">Header</span><span class="sxs-lookup"><span data-stu-id="be622-120">Header</span></span><br/>  | <dl> <span data-ttu-id="be622-121"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be622-121"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="be622-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="be622-122">Library</span></span><br/> | <dl> <span data-ttu-id="be622-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="be622-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be622-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be622-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be622-125">**Класс Кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="be622-125">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




