---
title: команда обновления
description: Команда Update перерисовывает текущий кадр в указанный контекст устройства (DC). Устройство Digital-Video распознает эту команду.
ms.assetid: 51a83262-91d5-4852-ad17-bd62c14417b1
keywords:
- команда обновления Windows мультимедиа
topic_type:
- apiref
api_name:
- update
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb0fc96d404efd8e2f657985ffa5a8861d3b4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535348"
---
# <a name="update-command"></a><span data-ttu-id="86b83-105">команда обновления</span><span class="sxs-lookup"><span data-stu-id="86b83-105">update command</span></span>

<span data-ttu-id="86b83-106">Команда Update перерисовывает текущий кадр в указанный контекст устройства (DC).</span><span class="sxs-lookup"><span data-stu-id="86b83-106">The update command repaints the current frame into the specified device context (DC).</span></span> <span data-ttu-id="86b83-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="86b83-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="86b83-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="86b83-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("update %s %s %s"), 
  lpszDeviceID, 
  lpszHDC, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="86b83-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="86b83-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86b83-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="86b83-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="86b83-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="86b83-111">Identifier of an MCI device.</span></span> <span data-ttu-id="86b83-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="86b83-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="86b83-113"><span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*лпсздк*</span><span class="sxs-lookup"><span data-stu-id="86b83-113"><span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszHDC*</span></span>
</dt> <dd>

<span data-ttu-id="86b83-114">Маркер контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="86b83-114">Handle of a DC.</span></span> <span data-ttu-id="86b83-115">В следующей таблице перечислены типы устройств, которые распознают команду **Update** , и флаги, используемые каждым типом.</span><span class="sxs-lookup"><span data-stu-id="86b83-115">The following table lists device types that recognize the **update** command and the flags used by each type.</span></span>



| <span data-ttu-id="86b83-116">Значение</span><span class="sxs-lookup"><span data-stu-id="86b83-116">Value</span></span>        | <span data-ttu-id="86b83-117">Значение</span><span class="sxs-lookup"><span data-stu-id="86b83-117">Meaning</span></span>                       | <span data-ttu-id="86b83-118">Значение</span><span class="sxs-lookup"><span data-stu-id="86b83-118">Meaning</span></span>         |
|--------------|-------------------------------|-----------------|
| <span data-ttu-id="86b83-119">дигиталвидео</span><span class="sxs-lookup"><span data-stu-id="86b83-119">digitalvideo</span></span> | <span data-ttu-id="86b83-120">HDC *HDC* HDC *HDC* в *Rect*</span><span class="sxs-lookup"><span data-stu-id="86b83-120">hdc *hdc* hdc *hdc* at *rect*</span></span> | <span data-ttu-id="86b83-121">Paint HDC *HDC*</span><span class="sxs-lookup"><span data-stu-id="86b83-121">paint hdc *hdc*</span></span> |



 

<span data-ttu-id="86b83-122">В следующей таблице перечислены флаги, которые могут быть указаны в параметре **лпсздк** , и их значения.</span><span class="sxs-lookup"><span data-stu-id="86b83-122">The following table lists the flags that can be specified in the **lpszHDC** parameter and their meanings.</span></span>



| <span data-ttu-id="86b83-123">Значение</span><span class="sxs-lookup"><span data-stu-id="86b83-123">Value</span></span>               | <span data-ttu-id="86b83-124">Значение</span><span class="sxs-lookup"><span data-stu-id="86b83-124">Meaning</span></span>                                                                                                |
|---------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86b83-125">HDC *HDC*</span><span class="sxs-lookup"><span data-stu-id="86b83-125">hdc *hdc*</span></span>           | <span data-ttu-id="86b83-126">Задает маркер контроллера домена для рисования.</span><span class="sxs-lookup"><span data-stu-id="86b83-126">Specifies the handle of the DC to paint.</span></span>                                                               |
| <span data-ttu-id="86b83-127">HDC *HDC* в *Rect*</span><span class="sxs-lookup"><span data-stu-id="86b83-127">hdc *hdc* at *rect*</span></span> | <span data-ttu-id="86b83-128">Задает прямоугольник обрезки относительно прямоугольника клиента.</span><span class="sxs-lookup"><span data-stu-id="86b83-128">Specifies the clipping rectangle relative to the client rectangle.</span></span>                                     |
| <span data-ttu-id="86b83-129">Paint HDC *HDC*</span><span class="sxs-lookup"><span data-stu-id="86b83-129">paint hdc *hdc*</span></span>     | <span data-ttu-id="86b83-130">Закрашивает контроллер домена, когда приложение получает сообщение [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , ПРЕДНАЗНАЧЕННОЕ для контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="86b83-130">Paints the DC when the application receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message intended for a DC.</span></span> |



 

<span data-ttu-id="86b83-131">Чтобы указать маркер контроллера домена, используйте строку "HDC", за которой следует представление ASCII маркера.</span><span class="sxs-lookup"><span data-stu-id="86b83-131">To specify the handle of the DC, use the string "hdc" followed by an ASCII representation of the handle.</span></span> <span data-ttu-id="86b83-132">Прямоугольник задается как **x1 Y1 x2 Y2**.</span><span class="sxs-lookup"><span data-stu-id="86b83-132">The rectangle is specified as **X1 Y1 X2 Y2**.</span></span> <span data-ttu-id="86b83-133">Координаты **x1 Y1** определяют левый верхний угол прямоугольника, а координаты **x2 Y2** определяют ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="86b83-133">The coordinates **X1 Y1** specify the upper left corner of the rectangle, and the coordinates **X2 Y2** specify the width and height.</span></span>

</dd> <dt>

<span data-ttu-id="86b83-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="86b83-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="86b83-135">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="86b83-135">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="86b83-136">Для устройств Digital-Video также можно указать "Test".</span><span class="sxs-lookup"><span data-stu-id="86b83-136">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="86b83-137">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="86b83-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86b83-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86b83-138">Return Value</span></span>

<span data-ttu-id="86b83-139">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="86b83-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="86b83-140">Примеры</span><span class="sxs-lookup"><span data-stu-id="86b83-140">Examples</span></span>

<span data-ttu-id="86b83-141">Следующая команда обновляет все окно просмотра, используемое устройством "Movie".</span><span class="sxs-lookup"><span data-stu-id="86b83-141">The following command updates the entire display window used by the "movie" device.</span></span> <span data-ttu-id="86b83-142">Число 203 является обработчиком контроллера домена, полученного из функции [**бегинпаинт**](/windows/desktop/api/winuser/nf-winuser-beginpaint) .</span><span class="sxs-lookup"><span data-stu-id="86b83-142">The number 203 is a handle to a DC obtained from the [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) function.</span></span>

``` syntax
update movie hdc 203
```

## <a name="requirements"></a><span data-ttu-id="86b83-143">Требования</span><span class="sxs-lookup"><span data-stu-id="86b83-143">Requirements</span></span>



| <span data-ttu-id="86b83-144">Требование</span><span class="sxs-lookup"><span data-stu-id="86b83-144">Requirement</span></span> | <span data-ttu-id="86b83-145">Значение</span><span class="sxs-lookup"><span data-stu-id="86b83-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="86b83-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86b83-146">Minimum supported client</span></span><br/> | <span data-ttu-id="86b83-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="86b83-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="86b83-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86b83-148">Minimum supported server</span></span><br/> | <span data-ttu-id="86b83-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="86b83-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="86b83-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86b83-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86b83-151">MCI</span><span class="sxs-lookup"><span data-stu-id="86b83-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="86b83-152">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="86b83-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

