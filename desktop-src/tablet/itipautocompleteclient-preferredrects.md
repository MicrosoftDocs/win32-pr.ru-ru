---
description: Позволяет клиенту предлагать место расположения списка автозавершения, чтобы избежать перекрытия панели ввода.
ms.assetid: c82ffecb-f3e6-4c50-80bb-8393b39d3b2a
title: 'Итипаутокомплетеклиент: метод:P Реферредректс (Типаутокомплете. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.PreferredRects
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 04e935c668e858ae3d22936e8a63f9116ebd6ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712493"
---
# <a name="itipautocompleteclientpreferredrects-method"></a><span data-ttu-id="f8b00-103">Итипаутокомплетеклиент: метод:P Реферредректс</span><span class="sxs-lookup"><span data-stu-id="f8b00-103">ITipAutocompleteClient::PreferredRects method</span></span>

<span data-ttu-id="f8b00-104">Позволяет клиенту предлагать место расположения списка автозавершения, чтобы избежать перекрытия панели ввода.</span><span class="sxs-lookup"><span data-stu-id="f8b00-104">Allows the client to suggest where to position the auto complete list to avoid overlapping the Input Panel.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8b00-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8b00-105">Syntax</span></span>


```C++
HRESULT PreferredRects(
  [in]      RECT *prcACList,
  [in]      RECT *prcField,
  [out]     RECT *prcModified,
  [in, out] BOOL *pfShownAboveTip
);
```



## <a name="parameters"></a><span data-ttu-id="f8b00-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8b00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8b00-107">*пркаклист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8b00-107">*prcACList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8b00-108">Прямоугольник в экранных координатах, указывающий предпочтительное расположение поставщика и размер пользовательского интерфейса списка автозавершения.</span><span class="sxs-lookup"><span data-stu-id="f8b00-108">A rectangle, in screen coordinates, indicating the provider's preferred location and the size of the auto complete list user interface.</span></span>

</dd> <dt>

<span data-ttu-id="f8b00-109">*пркфиелд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8b00-109">*prcField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8b00-110">Прямоугольник в экранных координатах, указывающий расположение и размер поля с сортировкой.</span><span class="sxs-lookup"><span data-stu-id="f8b00-110">A rectangle, in screen coordinates, indicating the location and the size of the focused field.</span></span>

</dd> <dt>

<span data-ttu-id="f8b00-111">*пркмодифиед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f8b00-111">*prcModified* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8b00-112">Прямоугольник, основанный на текущем состоянии Совета и расположении предпочтительного списка автозавершения и размера, заданного параметром *пркаклист*.</span><span class="sxs-lookup"><span data-stu-id="f8b00-112">A rectangle based on the current state of the TIP and the preferred auto complete list location and size specified by *prcACList*.</span></span>

</dd> <dt>

<span data-ttu-id="f8b00-113">*пфшовнабоветип* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="f8b00-113">*pfShownAboveTip* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8b00-114">**Значение true** , если измененный прямоугольник должен отображаться над целевой областью панели ввода текста; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f8b00-114">**TRUE** if the modified rectangle is to be shown above the Text Input Panel's target area; otherwise, **FALSE**.</span></span> <span data-ttu-id="f8b00-115">Перед вызовом метода это значение должно быть инициализировано до предпочтительной ориентации поставщика.</span><span class="sxs-lookup"><span data-stu-id="f8b00-115">This value must be initialized to the provider's preferred orientation before the method is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8b00-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8b00-116">Return value</span></span>

<span data-ttu-id="f8b00-117">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="f8b00-117">This method can return one of these values.</span></span>



| <span data-ttu-id="f8b00-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f8b00-118">Return code</span></span>                                                                                  | <span data-ttu-id="f8b00-119">Описание</span><span class="sxs-lookup"><span data-stu-id="f8b00-119">Description</span></span>                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8b00-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f8b00-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f8b00-121">Успешно.</span><span class="sxs-lookup"><span data-stu-id="f8b00-121">Success.</span></span><br/>                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="f8b00-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f8b00-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f8b00-123">Вызовите [**метод итипаутокомплетеклиент:: рекуестшовуи**](itipautocompleteclient-requestshowui.md) , чтобы задать окно списка автозаполнения всплывающего окна перед вызовом [**метода Итипаутокомплетеклиент::P реферредректс**](itipautocompleteclient-preferredrects.md).</span><span class="sxs-lookup"><span data-stu-id="f8b00-123">Call the [**ITipAutocompleteClient::RequestShowUI Method**](itipautocompleteclient-requestshowui.md) to set the popup auto complete list window before calling the [**ITipAutocompleteClient::PreferredRects Method**](itipautocompleteclient-preferredrects.md).</span></span><br/> |
| <dl> <span data-ttu-id="f8b00-124"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="f8b00-124"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="f8b00-125">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f8b00-125">An unspecified error occurred.</span></span><br/>                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="f8b00-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8b00-126">Remarks</span></span>

<span data-ttu-id="f8b00-127">Это метод, который вызывается поставщиком автоматического завершения, когда он собирается отобразить пользовательский интерфейс автоматического завершения.</span><span class="sxs-lookup"><span data-stu-id="f8b00-127">This is the method that the auto complete provider calls when it is about to show the auto complete user interface.</span></span> <span data-ttu-id="f8b00-128">Клиент изменяет предпочтительный прямоугольник поставщика, указанный параметром *пркаклист* , с помощью аргумента *пркмодифиед* .</span><span class="sxs-lookup"><span data-stu-id="f8b00-128">The client modifies the provider's preferred rectangle specified by *prcACList* through *prcModified* argument.</span></span>

<span data-ttu-id="f8b00-129">Вызовите [**метод итипаутокомплетеклиент:: рекуестшовуи**](itipautocompleteclient-requestshowui.md) , чтобы задать окно списка автозаполнения всплывающего окна перед вызовом **преферредректс**.</span><span class="sxs-lookup"><span data-stu-id="f8b00-129">Call the [**ITipAutocompleteClient::RequestShowUI Method**](itipautocompleteclient-requestshowui.md) to set the popup auto complete list window handle before you call **PreferredRects**.</span></span> <span data-ttu-id="f8b00-130">Несоблюдение этого действия приведет к ошибке **E \_ INVALIDARG** при вызове **преферредректс**.</span><span class="sxs-lookup"><span data-stu-id="f8b00-130">Failure to do so will cause an **E\_INVALIDARG** error when calling **PreferredRects**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8b00-131">Требования</span><span class="sxs-lookup"><span data-stu-id="f8b00-131">Requirements</span></span>



| <span data-ttu-id="f8b00-132">Требование</span><span class="sxs-lookup"><span data-stu-id="f8b00-132">Requirement</span></span> | <span data-ttu-id="f8b00-133">Значение</span><span class="sxs-lookup"><span data-stu-id="f8b00-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b00-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8b00-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f8b00-135">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f8b00-135">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="f8b00-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8b00-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f8b00-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f8b00-137">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="f8b00-138">Header</span><span class="sxs-lookup"><span data-stu-id="f8b00-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8b00-139"><dt>Типаутокомплете. h (также требуется Пенинпутпанел \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f8b00-139"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f8b00-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f8b00-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8b00-141"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8b00-141"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="f8b00-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8b00-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8b00-143">**Интерфейс Итипаутокомплетеклиент**</span><span class="sxs-lookup"><span data-stu-id="f8b00-143">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="f8b00-144">**Метод Итипаутокомплетеклиент:: Рекуестшовуи**</span><span class="sxs-lookup"><span data-stu-id="f8b00-144">**ITipAutocompleteClient::RequestShowUI Method**</span></span>](itipautocompleteclient-requestshowui.md)
</dt> <dt>

[<span data-ttu-id="f8b00-145">Справочник по панели ввода текста</span><span class="sxs-lookup"><span data-stu-id="f8b00-145">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




