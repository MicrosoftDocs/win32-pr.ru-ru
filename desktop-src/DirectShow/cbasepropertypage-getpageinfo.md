---
description: 'Метод Жетпажеинфо извлекает сведения о странице свойств. Этот метод реализует метод Ипропертипаже:: Жетпажеинфо.'
ms.assetid: f2e04652-7c71-48b2-b964-4e07ac98d367
title: Кбасепропертипаже. Жетпажеинфо, метод (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.GetPageInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27faecf50381b098dfcbee34d1494e37c77a36ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668993"
---
# <a name="cbasepropertypagegetpageinfo-method"></a><span data-ttu-id="064b8-104">Кбасепропертипаже. Жетпажеинфо, метод</span><span class="sxs-lookup"><span data-stu-id="064b8-104">CBasePropertyPage.GetPageInfo method</span></span>

<span data-ttu-id="064b8-105">`GetPageInfo`Метод получает сведения о странице свойств.</span><span class="sxs-lookup"><span data-stu-id="064b8-105">The `GetPageInfo` method retrieves information about the property page.</span></span> <span data-ttu-id="064b8-106">Этот метод реализует метод **ипропертипаже:: жетпажеинфо** .</span><span class="sxs-lookup"><span data-stu-id="064b8-106">This method implements the **IPropertyPage::GetPageInfo** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="064b8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="064b8-107">Syntax</span></span>


```C++
HRESULT GetPageInfo(
   LPPROPPAGEINFO pPageInfo
);
```



## <a name="parameters"></a><span data-ttu-id="064b8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="064b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="064b8-109">*pPageInfo*</span><span class="sxs-lookup"><span data-stu-id="064b8-109">*pPageInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="064b8-110">Указатель на структуру **проппажеинфо** , выделенную вызывающей стороной.</span><span class="sxs-lookup"><span data-stu-id="064b8-110">Pointer to a caller-allocated **PROPPAGEINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="064b8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="064b8-111">Return value</span></span>

<span data-ttu-id="064b8-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="064b8-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="064b8-113">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="064b8-113">Possible values include the following.</span></span>



| <span data-ttu-id="064b8-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="064b8-114">Return code</span></span>                                                                                   | <span data-ttu-id="064b8-115">Описание</span><span class="sxs-lookup"><span data-stu-id="064b8-115">Description</span></span>                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="064b8-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="064b8-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="064b8-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="064b8-117">Success.</span></span><br/>             |
| <dl> <span data-ttu-id="064b8-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="064b8-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="064b8-119">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="064b8-119">Insufficient memory.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="064b8-120">Требования</span><span class="sxs-lookup"><span data-stu-id="064b8-120">Requirements</span></span>



| <span data-ttu-id="064b8-121">Требование</span><span class="sxs-lookup"><span data-stu-id="064b8-121">Requirement</span></span> | <span data-ttu-id="064b8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="064b8-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="064b8-123">Header</span><span class="sxs-lookup"><span data-stu-id="064b8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="064b8-124"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="064b8-124"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="064b8-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="064b8-125">Library</span></span><br/> | <dl> <span data-ttu-id="064b8-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="064b8-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="064b8-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="064b8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="064b8-128">**Класс Кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="064b8-128">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




