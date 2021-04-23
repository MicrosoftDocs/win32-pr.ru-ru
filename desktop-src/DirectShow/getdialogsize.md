---
description: Функция Жетдиалогсизе Извлекает размер диалогового окна ресурса.
ms.assetid: b6c42f96-0381-493a-9503-f3bd4c6a8e1e
title: Функция Жетдиалогсизе (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDialogSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34eff1882306c85446f7cc7708efea3b17fcf7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652111"
---
# <a name="getdialogsize-function"></a><span data-ttu-id="7fbcf-103">Функция Жетдиалогсизе</span><span class="sxs-lookup"><span data-stu-id="7fbcf-103">GetDialogSize function</span></span>

<span data-ttu-id="7fbcf-104">Функция **жетдиалогсизе** Извлекает размер диалогового окна ресурса.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-104">The **GetDialogSize** function retrieves the size of a resource dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fbcf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7fbcf-105">Syntax</span></span>


```C++
BOOL WINAPI GetDialogSize(
   int     iResourceID,
   DLGPROC pDlgProc,
   LPARAM  lParam,
   SIZE    *pResult
);
```



## <a name="parameters"></a><span data-ttu-id="7fbcf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7fbcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fbcf-107">*иресаурцеид*</span><span class="sxs-lookup"><span data-stu-id="7fbcf-107">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbcf-108">Идентификатор ресурса диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-108">Dialog box resource identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7fbcf-109">*пдлгпрок*</span><span class="sxs-lookup"><span data-stu-id="7fbcf-109">*pDlgProc*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbcf-110">Указатель на процедуру диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-110">Pointer to the dialog box procedure.</span></span>

</dd> <dt>

<span data-ttu-id="7fbcf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7fbcf-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbcf-112">Значение, передаваемое в \_ сообщение ИНИТДИАЛОГ WM, отправленное во временное диалоговое окно сразу после создания.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-112">Value passed in the WM\_INITDIALOG message sent to the temporary dialog box just after it is created.</span></span>

</dd> <dt>

<span data-ttu-id="7fbcf-113">*пресулт*</span><span class="sxs-lookup"><span data-stu-id="7fbcf-113">*pResult*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbcf-114">Указатель на структуру **размера** , которая получает размеры диалогового окна в пикселях экрана.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-114">Pointer to a **SIZE** structure that receives the dimensions of the dialog box, in screen pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fbcf-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7fbcf-115">Return value</span></span>

<span data-ttu-id="7fbcf-116">Возвращает **значение true** , если ресурс диалогового окна был найден, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-116">Returns **TRUE** if the dialog box resource was found, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fbcf-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7fbcf-117">Remarks</span></span>

<span data-ttu-id="7fbcf-118">Страницы свойств могут использовать эту функцию для возврата фактического требуемого размера отображения.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-118">Property pages can use this function to return the actual display size they require.</span></span> <span data-ttu-id="7fbcf-119">Большинство страниц свойств — это диалоговые окна, которые имеют шаблоны диалоговых окон, хранящиеся в файлах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-119">Most property pages are dialog boxes and, as such, have dialog box templates stored in resource files.</span></span> <span data-ttu-id="7fbcf-120">Шаблоны используют единицы диалогового окна, которые не отображаются непосредственно на экранных точках.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-120">Templates use dialog box units that do not map directly onto screen pixels.</span></span> <span data-ttu-id="7fbcf-121">Однако функция [**жетпажеинфо**](cbasepropertypage-getpageinfo.md) страницы свойств должна возвращать реальный отображаемый размер в пикселях.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-121">However, a property page's [**GetPageInfo**](cbasepropertypage-getpageinfo.md) function must return the actual display size in pixels.</span></span> <span data-ttu-id="7fbcf-122">Страница свойств может вызывать `GetDialogSize` для вычисления размера отображаемого значения.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-122">The property page can call `GetDialogSize` to calculate the display size.</span></span>

<span data-ttu-id="7fbcf-123">Эта функция создает временный экземпляр диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-123">This function creates a temporary instance of the dialog box.</span></span> <span data-ttu-id="7fbcf-124">Чтобы не отображать диалоговое окно на экране, шаблон диалогового окна в файле ресурсов не должен иметь \_ свойство WS Visible.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-124">To avoid having the dialog box appear on the screen, the dialog box template in the resource file should not have a WS\_VISIBLE property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fbcf-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7fbcf-125">Requirements</span></span>



| <span data-ttu-id="7fbcf-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7fbcf-126">Requirement</span></span> | <span data-ttu-id="7fbcf-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7fbcf-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fbcf-128">Header</span><span class="sxs-lookup"><span data-stu-id="7fbcf-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7fbcf-129"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7fbcf-129"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7fbcf-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7fbcf-130">Library</span></span><br/> | <dl> <span data-ttu-id="7fbcf-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7fbcf-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fbcf-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7fbcf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fbcf-133">Вспомогательные функции страницы свойств</span><span class="sxs-lookup"><span data-stu-id="7fbcf-133">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




