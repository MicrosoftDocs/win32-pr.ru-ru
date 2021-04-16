---
description: Метод OnActivate вызывается при активации страницы свойств.
ms.assetid: aff843d4-cfb2-4255-a59c-0579f1cd24bd
title: Метод Кбасепропертипаже. OnActivate (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnActivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5093cb2ac71e8010bc689e4517b3d8bb758c8436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657486"
---
# <a name="cbasepropertypageonactivate-method"></a><span data-ttu-id="00599-103">Кбасепропертипаже. OnActivate, метод</span><span class="sxs-lookup"><span data-stu-id="00599-103">CBasePropertyPage.OnActivate method</span></span>

<span data-ttu-id="00599-104">`OnActivate`Метод вызывается при активации страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="00599-104">The `OnActivate` method is called when the property page is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="00599-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00599-105">Syntax</span></span>


```C++
virtual HRESULT OnActivate();
```



## <a name="parameters"></a><span data-ttu-id="00599-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="00599-106">Parameters</span></span>

<span data-ttu-id="00599-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="00599-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="00599-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00599-108">Return value</span></span>

<span data-ttu-id="00599-109">Реализация базового класса возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="00599-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="00599-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00599-110">Remarks</span></span>

<span data-ttu-id="00599-111">Метод [**кбасепропертипаже:: Activate**](cbasepropertypage-activate.md) вызывает `OnActivate` метод.</span><span class="sxs-lookup"><span data-stu-id="00599-111">The [**CBasePropertyPage::Activate**](cbasepropertypage-activate.md) method calls the `OnActivate` method.</span></span> <span data-ttu-id="00599-112">В производном классе Переопределите, `OnActivate` чтобы инициализировать диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="00599-112">In your derived class, override `OnActivate` to initialize the dialog box.</span></span>

## <a name="examples"></a><span data-ttu-id="00599-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="00599-113">Examples</span></span>

<span data-ttu-id="00599-114">В следующем примере инициализируется элемент управления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="00599-114">The following example initializes a trackbar control.</span></span> <span data-ttu-id="00599-115">В этом примере предполагается, что **m \_ повнингфилтер** является указателем на пользовательский интерфейс в фильтре, связанном со страницей свойств.</span><span class="sxs-lookup"><span data-stu-id="00599-115">This example assumes that **m\_pOwningFilter** is a pointer to a custom interface on the filter associated with the property page.</span></span> <span data-ttu-id="00599-116">(Для инициализации таких указателей используйте метод [**кбасепропертипаже:: OnConnect**](cbasepropertypage-onconnect.md) .)</span><span class="sxs-lookup"><span data-stu-id="00599-116">(Use the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to initialize such pointers.)</span></span>


```C++
HRESULT CMyProp::OnActivate(void)
{
    ASSERT(m_pOwningFilter != NULL);
    m_pOwningFilter->GetSomeProperty(&m_lOldVal);
    
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0, MAKELONG(0, 100));
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 10, 0);
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lOldVal);
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="00599-117">Требования</span><span class="sxs-lookup"><span data-stu-id="00599-117">Requirements</span></span>



| <span data-ttu-id="00599-118">Требование</span><span class="sxs-lookup"><span data-stu-id="00599-118">Requirement</span></span> | <span data-ttu-id="00599-119">Значение</span><span class="sxs-lookup"><span data-stu-id="00599-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00599-120">Header</span><span class="sxs-lookup"><span data-stu-id="00599-120">Header</span></span><br/>  | <dl> <span data-ttu-id="00599-121"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00599-121"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="00599-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="00599-122">Library</span></span><br/> | <dl> <span data-ttu-id="00599-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="00599-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00599-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00599-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00599-125">**Класс Кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="00599-125">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




